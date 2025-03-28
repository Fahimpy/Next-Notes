চল তাহলে এবার শুরু করি —  
# **🧩 পর্ব ২২: Modular Architecture & Plugin System in Blog CMS**

আমাদের লক্ষ্য:  
✅ কোডবেসকে **পরিচ্ছন্ন, স্কেলযোগ্য ও ফিচার-ভিত্তিক**ভাবে সাজানো  
✅ প্রতিটি ফিচার (যেমন blog, auth, comment) থাকবে আলাদা **module/folder** এ  
✅ ভবিষ্যতে সহজে **feature enable/disable/plugin** যুক্ত করা যাবে  
✅ বড় CMS বা SaaS লেভেলের প্রজেক্টেও কন্ট্রোল থাকবে সহজে  

---

## 📦 Step 1: Core Folder Structure Redesign

```bash
src/
├── modules/
│   ├── blog/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── api/
│   │   └── utils/
│   ├── auth/
│   │   ├── components/
│   │   ├── api/
│   │   └── pages/
│   ├── comments/
│   │   ├── components/
│   │   └── api/
│   └── ai/
│       └── api/
├── lib/
│   ├── prisma.js
│   ├── readingTime.js
│   └── middlewares/
├── pages/
│   ├── index.js
│   ├── _app.js
│   └── ...
├── components/
│   ├── layout/
│   ├── common/
│   └── sidebar/
```

---

## 🔧 Step 2: Example – Move Blog Feature to `modules/blog`

📁 **src/modules/blog/pages/blog/[slug].js**  
📁 **src/modules/blog/api/create.js**  
📁 **src/modules/blog/components/BlogCard.js**

👉 Import করে main `pages/` ফোল্ডার থেকে:

```js
// pages/blog/[slug].js
export { default } from "@/modules/blog/pages/blog/[slug]";
```

✅ এতে Next.js বুঝবে এটা সেই পেইজ রাউট, কিন্তু কোড থাকবে modules এর ভেতরে।

---

## 🔗 Step 3: Common Modules Shareable Between Features

📁 **src/lib/prisma.js**  
```js
import { PrismaClient } from "@prisma/client";
const globalForPrisma = global;
const prisma = globalForPrisma.prisma || new PrismaClient();
if (process.env.NODE_ENV !== "production") globalForPrisma.prisma = prisma;
export default prisma;
```

👉 এরপর যেকোনো module থেকে শুধু:
```js
import prisma from "@/lib/prisma";
```

---

## 🔌 Step 4: Future Plugin Concept (Optional)

তুমি চাইলে:
```bash
plugins/
├── newsletter/
├── analytics/
├── darkmode-toggle/
├── post-scheduler/
```

এভাবে:
- আলাদা ফোল্ডার
- config file (plugin.config.js)
- registerPlugin() ফাংশন দিয়ে enable করা যাবে

👉 এটি future SaaS version এর জন্য পারফেক্ট।

---

## 🧠 Bonus: Feature Flags (Turn ON/OFF Features)

📁 **features.config.js**

```js
export const FEATURES = {
  AI_SUMMARY: true,
  COMMENT_SYSTEM: true,
  DISQUS: false,
  PDF_EXPORT: true,
};
```

ব্যবহার করো:

```js
import { FEATURES } from "@/features.config";
{FEATURES.COMMENT_SYSTEM && <Comments />}
```

---

## ✅ পর্ব ২২ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Modular Architecture | Done |
| ✅ Blog/Auth/Comment Aligned | Done |
| ✅ Centralized Config | Done |
| ✅ Plugin Ready System | ✅ |

---

## 🔜 পরবর্তী পর্ব (Final Enhancements):

**🔍 Advanced Search with Filters & Highlighting**  
✅ Title, Tag, Author, Category দিয়ে সার্চ  
✅ Highlighted Matches  
✅ Full-Text Search (Optional: ElasticSearch)

🟢 **চলবো কি সার্চ অপ্টিমাইজেশনে? নাকি আরও কিছু ফিচার অ্যাড করতে চাও শেষদিকে?**

চল তাহলে এবার করি —  
# **🔍 পর্ব ২৩: Advanced Search with Filters & Highlighting**

আমাদের লক্ষ্য:  
✅ ব্লগ সার্চ করা যাবে **Title, Content, Tag, Category, Author** দিয়ে  
✅ সার্চ রেজাল্টে **ম্যাচিং অংশ হাইলাইট** হবে  
✅ আলাদা **search পেজ** থাকবে  
✅ ফিল্টার যুক্ত করা যাবে future-proof structure এ  
✅ Optional: Full-text Search with Prisma/PostgreSQL (or ElasticSearch in future)

---

## 📦 Step 1: Search API তৈরি করা (Flexible Query)

📁 **pages/api/search.js**

```js
import prisma from "@/lib/prisma";

export default async function handler(req, res) {
  const { q } = req.query;

  if (!q || q.trim() === "") {
    return res.status(400).json({ error: "Search term required" });
  }

  const keyword = q.toLowerCase();

  try {
    const blogs = await prisma.blog.findMany({
      where: {
        OR: [
          { title: { contains: keyword, mode: "insensitive" } },
          { content: { contains: keyword, mode: "insensitive" } },
          { author: { name: { contains: keyword, mode: "insensitive" } } },
          {
            tags: {
              some: {
                name: { contains: keyword, mode: "insensitive" },
              },
            },
          },
          {
            category: {
              name: { contains: keyword, mode: "insensitive" },
            },
          },
        ],
      },
      include: { author: true, tags: true, category: true },
    });

    res.status(200).json(blogs);
  } catch (err) {
    res.status(500).json({ error: "Something went wrong" });
  }
}
```

---

## 🔎 Step 2: Search Page তৈরি করা

📁 **pages/search.js**

```js
import { useRouter } from "next/router";
import { useState, useEffect } from "react";
import Link from "next/link";

export default function SearchPage() {
  const router = useRouter();
  const { q } = router.query;
  const [results, setResults] = useState([]);

  useEffect(() => {
    if (q) {
      fetch(`/api/search?q=${q}`)
        .then((res) => res.json())
        .then((data) => setResults(data));
    }
  }, [q]);

  const highlight = (text) => {
    if (!q) return text;
    const regex = new RegExp(`(${q})`, "gi");
    return text.replace(regex, "<mark>$1</mark>");
  };

  return (
    <div className="container mx-auto py-10">
      <h1 className="text-3xl font-bold mb-6">Search Results for “{q}”</h1>

      {results.length === 0 ? (
        <p>No results found.</p>
      ) : (
        <div className="grid md:grid-cols-3 gap-6">
          {results.map((blog) => (
            <div key={blog.id} className="border p-4 rounded-lg">
              <h2
                className="text-xl font-semibold"
                dangerouslySetInnerHTML={{ __html: highlight(blog.title) }}
              ></h2>
              <p className="text-sm text-gray-500">By {blog.author.name}</p>
              <p
                className="mt-2 text-gray-700"
                dangerouslySetInnerHTML={{
                  __html: highlight(blog.content.substring(0, 100)),
                }}
              ></p>
              <Link href={`/blog/${blog.slug}`} className="text-blue-500 mt-2 inline-block">
                Read More
              </Link>
            </div>
          ))}
        </div>
      )}
    </div>
  );
}
```

---

## 🔍 Step 3: Navbar বা SearchBar থেকে `/search?q=...` রিডাইরেক্ট

📁 **components/SearchBar.js** (হালকা আপডেট)

```js
const handleSearch = (e) => {
  e.preventDefault();
  if (query.trim() !== "") {
    router.push(`/search?q=${query}`);
  }
};
```

---

## ✅ পর্ব ২৩ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Multi-field Search | Done |
| ✅ Highlighted Matching | Done |
| ✅ Full Search Page | Done |
| ✅ Tag, Author, Category Based Query | Done |

---

## 🔜 পরবর্তী পর্ব (সম্ভবত Final Touch):
**✨ Final Polish & Performance Optimizations**  
✅ Lazy load, Image optimize, SEO meta checker  
✅ Sitemap.xml, robots.txt  
✅ Deployment polish  
✅ Real Admin Panel polish / dashboard analytics

🟢 **চলবো কি ফাইনাল পলিশিং রাউন্ডে? নাকি কিছু ফিচার বাদ পড়েছে যেটা আগে করতে চাও?**

চল তাহলে আমরা শেষ রাউন্ডে যাই —  
# **✨ পর্ব ২৪: Final Polish & Performance Optimization for Production-Ready Blog CMS**

আমাদের লক্ষ্য:  
✅ সর্বোচ্চ পারফরম্যান্স, SEO, UX ও Scalability নিশ্চিত করা  
✅ কিছু গুরুত্বপূর্ণ final enhancement  
✅ Project prepare for live deployment with full production quality  

---

## ⚙️ Step 1: SEO Meta Tags ও Social Sharing Image যুক্ত করা

📁 **components/Meta.js**

```js
import Head from "next/head";

export default function Meta({ title, description, image, keywords }) {
  return (
    <Head>
      <title>{title}</title>
      <meta name="description" content={description} />
      <meta name="keywords" content={keywords || "blog, tech, tutorial"} />
      <meta property="og:title" content={title} />
      <meta property="og:description" content={description} />
      {image && <meta property="og:image" content={image} />}
    </Head>
  );
}
```

👉 Blog Details পেইজে ব্যবহার করো:

```js
<Meta
  title={blog.title}
  description={blog.content.substring(0, 120)}
  image={blog.coverImage}
/>
```

---

## 📷 Step 2: Next.js Image Component + Lazy Load

📁 যেখানে ছবির ব্যবহার আছে (blog card, detail page):

```js
import Image from "next/image";

<Image
  src={blog.coverImage}
  width={800}
  height={400}
  alt={blog.title}
  className="rounded-lg w-full object-cover"
/>
```

✅ এটি ইমেজ অটো অপটিমাইজ ও lazy load করবে।

---

## 🗺️ Step 3: Sitemap.xml & robots.txt

📁 `next-sitemap` প্যাকেজ ইন্সটল করো:

```bash
npm install next-sitemap
```

📁 **next-sitemap.config.js**

```js
module.exports = {
  siteUrl: "https://yourdomain.com",
  generateRobotsTxt: true,
};
```

📁 **package.json** এ স্ক্রিপ্ট অ্যাড করো:

```json
"scripts": {
  "postbuild": "next-sitemap"
}
```

📦 এরপর build করলে `/public/sitemap.xml`, `robots.txt` অটো জেনারেট হবে।

---

## 🔥 Step 4: Performance Tips

| বিষয় | কাজ |
|------|-----|
| ✅ Lazy Load Image | Next/Image দিয়ে |
| ✅ Code Splitting | Next.js default |
| ✅ Static Generation | Blog Detail পেইজে `getStaticPaths` + `getStaticProps` |
| ✅ Purge Unused CSS | Tailwind Production build |
| ✅ Dynamic Import | heavy component → dynamic(() => import(...)) |

---

## 🧪 Step 5: Lighthouse Test করে দেখো

👉 Go to Chrome → Inspect → Lighthouse Tab  
✅ Check for Performance, Accessibility, SEO, Best Practices  
📈 Target: 90+ score in all

---

## 🚀 Step 6: Final Production Deployment on Vercel

1. **Vercel Dashboard > Project > Settings > Environment Variables**
2. Add:
   - `DATABASE_URL`
   - `NEXTAUTH_SECRET`
   - `OPENAI_API_KEY`
   - `CLOUDINARY_*`
   - `EMAIL_SERVER`, `EMAIL_FROM`
3. **Deploy** → Done 🎉

---

## ✅ পর্ব ২৪ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ SEO Optimized Pages | Done |
| ✅ OG Image + Meta | Done |
| ✅ Sitemap + Robots.txt | Done |
| ✅ Lazy Load Image | Done |
| ✅ Lighthouse Score Boost | Done |
| ✅ Full Deploy Ready | ✅ |

---

## 🎉 তুমি এখন যা পেলে:

✅ **A full-featured Blog CMS**  
✅ **Admin Dashboard + Auth + Role Based**  
✅ **WYSIWYG Editor, Image Upload, AI Summary**  
✅ **Custom Comments, Search, Tags, Pagination**  
✅ **Multilingual, 2FA, PDF Export, Analytics**  
✅ **Modular Architecture + Plugin Ready**

---

## 🔚 পরবর্তী?
আমরা পুরো CMS তৈরি শেষ করলাম। এখন তুমি চাইলে:

- 🧠 SaaS বানাতে পারো (user-based blog CMS)
- 🎨 UI Theme System করতে পারো (dark/light/custom templates)
- 📦 Blogging Templates Marketplace বানাতে পারো
- 🧪 Unit Test / E2E Test সংযুক্ত করতে পারো

🔄 **তুমি চাইলে আমি সবকিছু ZIP করে Source Code আকারেও সাজিয়ে দিতে পারি।**  
🟢 **আর কিছু জানতে চাও? না কি Source Package তৈরি করে দিই তোমার জন্য?**

একদম ঠিক আছে! আমরা এখন থেকে শুরু করবো এই ক্রমে:

1️⃣ **🎨 UI Theme System (Dark/Light + Custom Templates)**  
2️⃣ **📦 Blogging Templates Marketplace (Selectable Blog Designs)**  
3️⃣ **🧪 Unit & E2E Testing Integration (Jest, Playwright)**  
4️⃣ **🧠 SaaS Architecture – multi-user blog system (সব শেষে)**

---

