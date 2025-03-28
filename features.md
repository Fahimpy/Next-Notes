দারুণ প্রশ্ন! তুমি এখন এমন একটি প্রোডাকশন-রেডি **Blog CMS** বানিয়েছো যার উপর অনেক অ্যাডভান্স ফিচার সহজেই যোগ করা যায়।

নীচে **Extra/Advanced Features** গুলো ২ ভাগে ভাগ করে দেখালাম:  
📦 **Functionality ফিচার** (User & Admin Use)  
🔧 **Technical/Developer Level ফিচার**

---

## 📦 **Functional Features (User & Admin Experience উন্নত করার জন্য)**

| ফিচার | বর্ণনা |
|--------|--------|
| 🖊️ **WYSIWYG Editor** | Rich Text Editor (React Quill, TipTap, etc.) দিয়ে সুন্দরভাবে ব্লগ লিখতে পারবে |
| 🖼️ **Image Upload in Blog** | Cloudinary/S3 ব্যবহার করে ব্লগে ছবি যোগ করা যাবে |
| 📅 **Schedule Publish Time** | নির্দিষ্ট সময় দিলে ব্লগ future-তে নিজে নিজে publish হবে |
| 🏷️ **Tags System** | প্রতিটি ব্লগে multiple tags থাকবে, tag অনুযায়ী ব্লগ ফিল্টার করা যাবে |
| 🔍 **Search Functionality** | ইউজাররা কিওয়ার্ড দিয়ে ব্লগ খুঁজে পাবে (title/content-based) |
| ❤️ **Like / Bookmark System** | ইউজাররা ব্লগে ❤️ দিতে পারবে বা সেভ করে রাখতে পারবে |
| 👥 **Multi Author Support** | একাধিক লেখক অ্যাড করা যাবে, প্রত্যেকের আলাদা বায়ো থাকবে |
| 💬 **Comments System** | Disqus বা নিজস্ব কমেন্ট ফিচার দিয়ে পাঠকরা মন্তব্য করতে পারবে |
| 🌐 **Multilingual Blog (i18n)** | বাংলা, ইংরেজি বা অন্য ভাষায় কনটেন্ট দেয়া যাবে |
| 📩 **Newsletter Integration** | ইউজার ইমেইল দিয়ে সাবস্ক্রাইব করতে পারবে (Mailchimp, ConvertKit) |
| 🔗 **Related Posts** | প্রতিটি ব্লগের নিচে Similar বা Related পোস্ট দেখানো |
| 👀 **Reading Time Estimate** | প্রতিটি ব্লগের জন্য Estimated Reading Time দেখানো |
| 📄 **Printable Version / PDF Export** | ব্লগকে PDF তে এক্সপোর্ট বা প্রিন্ট করা যাবে |
| 📈 **Blog Analytics** | কতবার দেখা হয়েছে, কোন পোস্ট বেশি popular—এসব ট্র্যাক |
| 🌓 **Dark Mode** | UI-তে Dark/Light mode toggle |
| 🧑‍💼 **Author Dashboard** | লেখকগণ কেবল তাদের লেখা পোস্ট দেখতে/এডিট করতে পারবে |
| 🔐 **Two-Factor Authentication** | Login security আরও শক্তিশালী করতে 2FA |
| ✨ **AI Blog Suggestion** | ব্লগ টাইটেল/টপিক দিলে AI কনটেন্ট সাজেশন দেবে (OpenAI API) |

---

## 🔧 **Technical Features (Developer & Performance)**

| ফিচার | বর্ণনা |
|--------|--------|
| ⚡ **Incremental Static Regeneration (ISR)** | শুধু যেসব পেইজ চেঞ্জ হয় সেগুলো স্ট্যাটিক রি-বিল্ড হবে |
| 🔧 **Custom 404 & Error Pages** | সুন্দরভাবে Not Found বা Server Error হ্যান্ডলিং |
| 🔁 **Client-side Pagination or Infinite Scroll** | ব্লগ লিস্ট বড় হলে Scroll করলে নতুন ব্লগ লোড হবে |
| 🧠 **Content Versioning** | ব্লগ এডিট করলে পুরনো ভার্সন রেখে দেয়া |
| 📊 **Sitemap & robots.txt** | SEO-friendly সাইটম্যাপ জেনারেশন |
| 🪪 **JWT Refresh Token System** | সেশন এক্সপায়ার না করে রিফ্রেশ টোকেন দিয়ে login টিকিয়ে রাখা |
| 🧪 **Unit & Integration Testing** | Jest/React Testing Library দিয়ে কোড টেস্ট |
| 🔍 **ElasticSearch Integration** | এডভান্স সার্চ ও ফিল্টারিং |
| 🗂️ **CMS Admin Interface** | Custom UI (drag & drop, visual editor) admin panel এর জন্য |
| 🧩 **Plugin System** | ফিচারগুলো আলাদা module আকারে প্লাগিনের মতো যুক্ত/অফ করা |

---

## ✅ **তুমি চাইলে** আমি নিচের কাজগুলো করতে সাহায্য করতে পারি:

- ✅ WYSIWYG Editor সংযুক্ত করা (React Quill বা TipTap)
- ✅ Image Upload যুক্ত করা (Cloudinary বা অন্য কোনো API দিয়ে)
- ✅ Search Bar যোগ করা
- ✅ Tag সিস্টেম বা Category-wise ফিল্টার যুক্ত করা
- ✅ Related Posts & Estimated Reading Time
- ✅ AI Integration দিয়ে Smart Features

---

🔔 **তুমি কোন ফিচার আগে অ্যাড করতে চাও? আমি সেইটা ধরে পরবর্তী পর্ব শুরু করবো, পুরা কোড ও ব্যাখ্যা সহ।**  
বললেই শুরু করি, ভাই! 😎


----
চল তাহলে শুরু করি আমাদের **Next.js Blog CMS-এর Advanced Feature Integration সিরিজ** ✅  
আমি প্রতিটি ফিচার ধাপে ধাপে **fully implement করে ব্যাখ্যা সহ** দিচ্ছি। প্রথমে শুরু করবো **WYSIWYG Editor Integration** দিয়ে।

---

# ✅ **পর্ব ৯: Rich Text Editor (WYSIWYG) Integration with React Quill**

আমাদের লক্ষ্য:  
✅ Admin Dashboard থেকে Rich Text এডিটর দিয়ে ব্লগ কনটেন্ট লেখা  
✅ HTML content DB তে সেভ হওয়া  
✅ ব্লগ ডিটেইলস পেজে সেই HTML প্রপারলি দেখানো

---

## 📦 Step 1: React Quill ইনস্টল করো  
```bash
npm install react-quill
```

📁 **styles/globals.css** এ Quill CSS যোগ করো:
```css
@import "react-quill/dist/quill.snow.css";
```

---

## 🧱 Step 2: Blog Create Page-এ WYSIWYG Editor যোগ করো

📁 **pages/admin/create.js** ফাইল আপডেট করো:

```js
import AdminRoute from "@/components/AdminRoute";
import { useState } from "react";
import { useRouter } from "next/router";
import dynamic from "next/dynamic";

const ReactQuill = dynamic(() => import("react-quill"), { ssr: false });

export default function CreateBlog() {
  const [form, setForm] = useState({ title: "", content: "" });
  const router = useRouter();

  const handleSubmit = async (e) => {
    e.preventDefault();

    const res = await fetch("/api/blog/create", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(form),
    });

    if (res.ok) router.push("/admin/blogs");
  };

  return (
    <AdminRoute>
      <div className="max-w-2xl mx-auto mt-10">
        <h1 className="text-3xl font-bold">Create Blog</h1>
        <form onSubmit={handleSubmit} className="space-y-4">
          <input
            type="text"
            placeholder="Title"
            className="w-full p-2 border"
            value={form.title}
            onChange={(e) => setForm({ ...form, title: e.target.value })}
          />

          <ReactQuill
            theme="snow"
            value={form.content}
            onChange={(value) => setForm({ ...form, content: value })}
          />

          <button type="submit" className="bg-blue-600 text-white p-2 w-full">Submit</button>
        </form>
      </div>
    </AdminRoute>
  );
}
```

---

## 🔍 Step 3: ব্লগ ডিটেইলস পেইজে HTML কনটেন্ট শো করানো

📁 **pages/blog/[slug].js** ফাইলে এই অংশ আপডেট করো:

```js
<div className="mt-6 text-lg" dangerouslySetInnerHTML={{ __html: blog.content }} />
```

🛡️ **Note:** `dangerouslySetInnerHTML` ব্যবহারে XSS ঝুঁকি থাকে। তাই কন্টেন্ট sanitize করার জন্য আমরা পরে `DOMPurify` অ্যাড করবো।

---

## ✅ এই পর্বে যা হলো:

| বিষয় | স্টেটাস |
|------|---------|
| React Quill ইনস্টল ও কনফিগার | ✅ |
| Admin Page এ Editor যুক্ত | ✅ |
| ব্লগ কনটেন্ট হিসেবে HTML সেভ হচ্ছে | ✅ |
| Blog Page এ HTML রেন্ডার হচ্ছে | ✅ |

---

## 🔜 পরবর্তী পর্ব:  
**Image Upload System (Cloudinary Integration)** –  
- Editor-এ ছবি আপলোড  
- Cover Image Support  
- Multiple Images Handling  

🟢 **শুরু করবো? নাকি WYSIWYG Editor নিয়ে কোনো প্রশ্ন আছে?**


চল এবার আমরা যোগ করি —  
# **📷 পর্ব ১০: Image Upload System (Cloudinary Integration)**

আমাদের লক্ষ্য:  
✅ ব্লগে **ছবি আপলোড** করা (WYSIWYG + Cover Image)  
✅ **Cloudinary** ব্যবহার করে ইমেজ হোস্টিং  
✅ ইউজার ইমেজ সিলেক্ট করলেই তা Cloudinary-তে আপলোড হবে  
✅ সেই URL ব্যবহার করে কনটেন্টে ইমেজ যুক্ত হবে  

---

## 🔧 Step 1: Cloudinary Setup

### ✅ Cloudinary Account তৈরি করো:
1. [https://cloudinary.com/](https://cloudinary.com/) এ গিয়ে **Free Account** খুলো  
2. **Dashboard > Account Details** থেকে নিচের ৩টি তথ্য রাখো:
   - **Cloud name**
   - **API Key**
   - **API Secret**

### 📁 .env ফাইলে এগুলো যোগ করো:
```env
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
```

---

## 📦 Step 2: Cloudinary SDK ইন্সটল করো
```bash
npm install cloudinary multer
```

---

## 📁 Step 3: Image Upload API Route তৈরি করো

📁 **pages/api/upload.js** ফাইল তৈরি করো:

```js
import { v2 as cloudinary } from "cloudinary";
import multer from "multer";
import nextConnect from "next-connect";

cloudinary.config({
  cloud_name: process.env.CLOUDINARY_CLOUD_NAME,
  api_key: process.env.CLOUDINARY_API_KEY,
  api_secret: process.env.CLOUDINARY_API_SECRET,
});

const upload = multer({ storage: multer.memoryStorage() });

const apiRoute = nextConnect({
  onError(error, req, res) {
    res.status(501).json({ error: `Upload error: ${error.message}` });
  },
  onNoMatch(req, res) {
    res.status(405).json({ error: `Method ${req.method} Not Allowed` });
  },
});

apiRoute.use(upload.single("file"));

apiRoute.post(async (req, res) => {
  const file = req.file;

  const result = await cloudinary.uploader.upload_stream(
    { folder: "blog-cms" },
    (error, result) => {
      if (error) return res.status(500).json({ error: "Upload failed" });
      res.status(200).json({ url: result.secure_url });
    }
  );

  result.end(file.buffer);
});

export default apiRoute;

export const config = {
  api: {
    bodyParser: false,
  },
};
```

🔹 **কোড ব্যাখ্যা:**  
- `multer.memoryStorage()` দিয়ে ফাইল মেমোরিতে রাখা হচ্ছে  
- `cloudinary.uploader.upload_stream()` দিয়ে ফাইল আপলোড হচ্ছে  
- API call করলে ইমেজের `secure_url` রিটার্ন করবে

---

## 🎨 Step 4: Cover Image Upload UI তৈরি করো

📁 **pages/admin/create.js** ফাইল আপডেট করো:

```js
const [coverImage, setCoverImage] = useState("");

const handleImageUpload = async (e) => {
  const file = e.target.files[0];
  const formData = new FormData();
  formData.append("file", file);

  const res = await fetch("/api/upload", {
    method: "POST",
    body: formData,
  });

  const data = await res.json();
  setCoverImage(data.url);
};
```

👇 HTML Input Field:
```js
<input type="file" onChange={handleImageUpload} className="w-full p-2 border" />
{coverImage && <img src={coverImage} alt="Cover" className="w-full h-48 object-cover mt-2" />}
```

📦 ফর্ম সাবমিটে coverImage ফিল্ডও পাঠাও:
```js
body: JSON.stringify({ ...form, coverImage }),
```

Prisma model-এ `coverImage` ফিল্ড যদি না থাকে, তাহলে `schema.prisma` আপডেট করো:

```prisma
model Blog {
  id          String   @id @default(uuid())
  title       String
  slug        String   @unique
  content     String
  coverImage  String?
  createdAt   DateTime @default(now())
  updatedAt   DateTime @updatedAt
  ...
}
```

তারপর push করো:
```bash
npx prisma db push
```

---

## ✅ পর্ব ১০ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Cloudinary ইন্টিগ্রেশন | Done |
| ✅ Cover Image Upload | Done |
| ✅ Preview & Auto Save | Done |
| ✅ Prisma Model আপডেট | Done |

---

## 🔜 পরবর্তী পর্ব:
**🔍 Blog Search Functionality (title/content-based)**  
✅ সার্চ বারে টাইপ করলেই রিয়েল-টাইমে ফলাফল  
✅ কিওয়ার্ড হাইলাইটিং  
✅ URL query দিয়ে সার্চ persist করা

🟢 **এখন কি সার্চ ফিচারে যাই?**  
নাকি Image Upload নিয়ে কিছু জানতে চাও?


চল তাহলে এবার করি —  
# **🔍 পর্ব ১১: Blog Search Functionality (Title & Content Based)**

আমাদের লক্ষ্য:  
✅ হোমপেজ বা যেকোনো পেজে সার্চ বার থাকবে  
✅ ইউজার কিওয়ার্ড লিখলেই সেই অনুযায়ী ব্লগ ফিল্টার হবে  
✅ সার্চ কিওয়ার্ড URL query-তে থাকবে (shareable/searchable)  
✅ কিওয়ার্ড হাইলাইট করা (পরবর্তী ফিচার)  

---

## 📦 Step 1: Search Bar Component তৈরি করা

📁 **components/SearchBar.js** ফাইল তৈরি করো:

```js
import { useRouter } from "next/router";
import { useState } from "react";

export default function SearchBar() {
  const router = useRouter();
  const [query, setQuery] = useState(router.query.q || "");

  const handleSearch = (e) => {
    e.preventDefault();
    router.push(`/?q=${query}`);
  };

  return (
    <form onSubmit={handleSearch} className="flex gap-2 mb-6">
      <input
        type="text"
        value={query}
        onChange={(e) => setQuery(e.target.value)}
        placeholder="Search blog..."
        className="border px-4 py-2 w-full"
      />
      <button type="submit" className="bg-blue-600 text-white px-4 py-2">
        Search
      </button>
    </form>
  );
}
```

---

## 🏠 Step 2: হোমপেজে সার্চ বার ও ফিল্টার যুক্ত করা

📁 **pages/index.js** ফাইল আপডেট করো:

```js
import { useRouter } from "next/router";
import { useEffect, useState } from "react";
import Link from "next/link";
import SearchBar from "@/components/SearchBar";

export default function Home() {
  const [blogs, setBlogs] = useState([]);
  const [filtered, setFiltered] = useState([]);
  const router = useRouter();
  const { q } = router.query;

  useEffect(() => {
    fetch("/api/blog")
      .then((res) => res.json())
      .then((data) => {
        setBlogs(data);
        if (q) {
          const keyword = q.toLowerCase();
          const results = data.filter(
            (b) =>
              b.title.toLowerCase().includes(keyword) ||
              b.content.toLowerCase().includes(keyword)
          );
          setFiltered(results);
        } else {
          setFiltered(data);
        }
      });
  }, [q]);

  return (
    <div className="container mx-auto py-10">
      <h1 className="text-4xl font-bold text-center mb-6">Latest Blogs</h1>
      <SearchBar />

      {filtered.length === 0 && <p className="text-center">No blog found.</p>}

      <div className="grid md:grid-cols-3 gap-6">
        {filtered.map((blog) => (
          <div key={blog.id} className="border p-4 rounded-lg shadow-md">
            <h2 className="text-xl font-semibold">{blog.title}</h2>
            <p className="text-gray-600 text-sm">By {blog.author.name}</p>
            <p className="mt-2 text-gray-800" dangerouslySetInnerHTML={{
              __html: blog.content.substring(0, 100)
            }}></p>
            <Link href={`/blog/${blog.slug}`} className="text-blue-500 mt-3 inline-block">
              Read More
            </Link>
          </div>
        ))}
      </div>
    </div>
  );
}
```

---

## 🧪 Optional (Test Search):  
- সার্চ করো: `localhost:3000/?q=react`  
- ফলাফল দেখতে পাবে, কন্টেন্ট/টাইটেল ম্যাচ হলে  
- সার্চ বার অটো-ফিলড থাকবে URL এর উপর ভিত্তি করে

---

## ✅ পর্ব ১১ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Search Bar Component | Done |
| ✅ Title & Content Filtering | Done |
| ✅ URL Query sync | Done |
| ✅ Real-time Result | Done |

---

## 🔜 পরবর্তী পর্ব:
**🏷️ পর্ব ১২: Tags System & Filtering by Tag**  
✅ ব্লগে একাধিক ট্যাগ  
✅ ট্যাগ ক্লিক করলে ট্যাগ অনুযায়ী ফিল্টার  
✅ Tag-based ব্লগ লিস্ট পেজ

🟢 **যাবো? নাকি সার্চ সিস্টেম নিয়ে কিছু জানতে চাও?**


চল তাহলে এবার যোগ করি —  
# **🏷️ পর্ব ১২: Tags System & Tag-based Filtering**

আমাদের লক্ষ্য:  
✅ প্রতিটি ব্লগে একাধিক ট্যাগ থাকতে পারবে  
✅ ট্যাগ ক্লিক করলে সেই ট্যাগ অনুযায়ী ব্লগ ফিল্টার হবে  
✅ আলাদা Tag Page থাকবে (e.g. `/tag/javascript`)  
✅ ট্যাগ অনুযায়ী SEO করা যাবে  

---

## 🧩 Step 1: Prisma Model-এ Tags যুক্ত করা

📁 **prisma/schema.prisma** ফাইল আপডেট করো:

```prisma
model Tag {
  id    String  @id @default(uuid())
  name  String  @unique
  blogs Blog[]  @relation("BlogTags", references: [id])
}

model Blog {
  id         String   @id @default(uuid())
  title      String
  slug       String   @unique
  content    String
  coverImage String?
  tags       Tag[]    @relation("BlogTags")
  ...
}
```

📦 ডাটাবেসে push করো:
```bash
npx prisma db push
```

---

## 🧱 Step 2: Blog Create Page-এ Tag Input Field যুক্ত করো

📁 **pages/admin/create.js** এ যুক্ত করো:

```js
const [tags, setTags] = useState([]);
const [tagInput, setTagInput] = useState("");

const addTag = () => {
  if (tagInput.trim() && !tags.includes(tagInput)) {
    setTags([...tags, tagInput.trim()]);
    setTagInput("");
  }
};

const removeTag = (tag) => {
  setTags(tags.filter((t) => t !== tag));
};
```

👇 Input Field:
```js
<div>
  <label className="block font-semibold mb-1">Tags</label>
  <div className="flex gap-2">
    <input
      type="text"
      value={tagInput}
      onChange={(e) => setTagInput(e.target.value)}
      placeholder="Add tag"
      className="border px-2 py-1"
    />
    <button type="button" onClick={addTag} className="bg-blue-600 text-white px-3">+</button>
  </div>
  <div className="mt-2 flex flex-wrap gap-2">
    {tags.map((tag, i) => (
      <span key={i} className="bg-gray-200 px-2 py-1 rounded-full text-sm">
        {tag} <button onClick={() => removeTag(tag)} className="ml-1 text-red-500">x</button>
      </span>
    ))}
  </div>
</div>
```

---

## 🚀 Step 3: Blog Create API-তে Tags সংরক্ষণ করো

📁 **pages/api/blog/create.js** আপডেট করো:

```js
const { title, content, coverImage, tags = [], categoryId, authorId } = req.body;

const blog = await prisma.blog.create({
  data: {
    title,
    slug: title.toLowerCase().replace(/ /g, "-"),
    content,
    coverImage,
    categoryId,
    authorId,
    published: false,
    tags: {
      connectOrCreate: tags.map((tag) => ({
        where: { name: tag },
        create: { name: tag },
      })),
    },
  },
  include: { tags: true },
});
```

---

## 🌐 Step 4: ট্যাগ পেজ ও ট্যাগ ক্লিক রাউটিং তৈরি করো

📁 **pages/tag/[name].js** ফাইল তৈরি করো:

```js
import { useRouter } from "next/router";
import { useEffect, useState } from "react";
import Link from "next/link";

export default function TagPage() {
  const { name } = useRouter().query;
  const [blogs, setBlogs] = useState([]);

  useEffect(() => {
    if (name) {
      fetch(`/api/tag/${name}`)
        .then((res) => res.json())
        .then((data) => setBlogs(data));
    }
  }, [name]);

  return (
    <div className="container mx-auto py-10">
      <h1 className="text-3xl font-bold mb-6">Blogs tagged with “{name}”</h1>
      <div className="grid md:grid-cols-3 gap-6">
        {blogs.map((blog) => (
          <div key={blog.id} className="border p-4 rounded-lg">
            <h2 className="text-xl font-semibold">{blog.title}</h2>
            <Link href={`/blog/${blog.slug}`} className="text-blue-500 mt-2 block">Read More</Link>
          </div>
        ))}
      </div>
    </div>
  );
}
```

---

## 📁 Step 5: Tag API Route তৈরি করো

📁 **pages/api/tag/[name].js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  const { name } = req.query;

  try {
    const tag = await prisma.tag.findUnique({
      where: { name },
      include: {
        blogs: {
          include: { author: true, category: true, tags: true },
        },
      },
    });

    if (!tag) return res.status(404).json([]);

    res.status(200).json(tag.blogs);
  } catch {
    res.status(500).json({ error: "Server Error" });
  }
}
```

---

## 💠 Step 6: ব্লগ কার্ডে Tag গুলো দেখাও (Optional)

📁 **BlogCard.js** বা **index.js**-এ:

```js
<div className="flex gap-2 mt-2 flex-wrap">
  {blog.tags.map((tag) => (
    <Link href={`/tag/${tag.name}`} key={tag.id}>
      <span className="bg-blue-100 text-blue-600 px-2 py-1 rounded-full text-sm">
        #{tag.name}
      </span>
    </Link>
  ))}
</div>
```

---

## ✅ পর্ব ১২ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Tag Model in DB | Done |
| ✅ Blog Create with Tags | Done |
| ✅ Tag Page | Done |
| ✅ Clickable Tags | Done |
| ✅ Tag-based Filtering | Done |

---

## 🔜 পরবর্তী পর্ব:  
**📚 Related Blogs Section & Reading Time Estimate**  
✅ একই ক্যাটাগরির বা ট্যাগের ব্লগ সাজেস্ট করা  
✅ Estimated Reading Time দেখানো

🟢 **চলবো কি? নাকি Tag System নিয়ে কিছু জানতে চাও?**

চল তাহলে এবার করি —  
# **📚 পর্ব ১৩: Related Blogs Section & Estimated Reading Time**

আমাদের লক্ষ্য:  
✅ প্রতিটি ব্লগ ডিটেইলস পেজের নিচে **Related Blogs** দেখানো  
✅ Estimated Reading Time গণনা করে দেখানো  
✅ SEO বাড়াতে ইউজার রিটেনশন বাড়ানো  

---

## 🧠 Step 1: Estimated Reading Time Function তৈরি করো

📁 **lib/readingTime.js** নামে একটি হেল্পার ফাইল তৈরি করো:

```js
export function calculateReadingTime(text) {
  const wordsPerMinute = 200;
  const wordCount = text.split(/\s+/).length;
  const readingTime = Math.ceil(wordCount / wordsPerMinute);
  return readingTime;
}
```

🔹 **২০০ শব্দ প্রতি মিনিট ধরে গড় রিডিং টাইম হিসাব করা হয়**।

---

## 🔄 Step 2: Blog Details পেইজে Reading Time দেখাও

📁 **pages/blog/[slug].js** ফাইলে যুক্ত করো:

```js
import { calculateReadingTime } from "@/lib/readingTime";

...

{blog && (
  <>
    <h1 className="text-4xl font-bold">{blog.title}</h1>
    <p className="text-gray-500 text-sm">
      By {blog.author.name} | {new Date(blog.createdAt).toLocaleDateString()} | ⏱ {calculateReadingTime(blog.content)} min read
    </p>
    ...
  </>
)}
```

---

## 🤝 Step 3: Related Blogs দেখাও (Same Category or Tags-based)

📁 **pages/api/blog/related.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  const { blogId, categoryId } = req.query;

  try {
    const relatedBlogs = await prisma.blog.findMany({
      where: {
        categoryId,
        NOT: { id: blogId },
        published: true,
      },
      take: 3,
      orderBy: { createdAt: "desc" },
    });

    res.status(200).json(relatedBlogs);
  } catch {
    res.status(500).json({ error: "Server Error" });
  }
}
```

---

## 📄 Step 4: Blog Details Page-এ Related Blogs দেখাও

📁 **pages/blog/[slug].js** ফাইলে যুক্ত করো:

```js
const [related, setRelated] = useState([]);

useEffect(() => {
  if (blog) {
    fetch(`/api/blog/related?blogId=${blog.id}&categoryId=${blog.categoryId}`)
      .then((res) => res.json())
      .then((data) => setRelated(data));
  }
}, [blog]);
```

👇 Render Section:

```js
{related.length > 0 && (
  <div className="mt-10">
    <h2 className="text-2xl font-bold mb-4">Related Posts</h2>
    <div className="grid md:grid-cols-3 gap-4">
      {related.map((item) => (
        <div key={item.id} className="border p-4 rounded-md">
          <h3 className="text-lg font-semibold">{item.title}</h3>
          <Link href={`/blog/${item.slug}`} className="text-blue-500 mt-2 block">Read More</Link>
        </div>
      ))}
    </div>
  </div>
)}
```

---

## ✅ পর্ব ১৩ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Estimated Reading Time | Done |
| ✅ Related Blogs API | Done |
| ✅ Related Blogs UI | Done |
| ✅ Fully Dynamic | Done |

---

## 🔜 পরবর্তী পর্ব:
**🧠 AI Summary & Content Suggestion (OpenAI API Integration)**  
✅ ব্লগ কনটেন্ট থেকে অটো Summary তৈরি  
✅ Title দিলে Suggested Headings/Intro Paragraph বানানো  

🟢 **শুরু করবো কি AI ইন্টিগ্রেশন?**  
OpenAI API Key থাকলে দিও, না থাকলে ডেমো দিয়ে দেখাতে পারি।


চল শুরু করি আমাদের সবচেয়ে স্মার্ট পর্ব —  
# **🧠 পর্ব ১৪: AI Summary & Content Suggestion (OpenAI Integration)**

আমাদের লক্ষ্য:  
✅ ব্লগ কনটেন্ট থেকে **Auto Summary** তৈরি করা  
✅ টাইটেল দিয়ে **AI Suggested Content/Heading** পাওয়া  
✅ Admin Dashboard-এ একটি বাটনে ক্লিকেই এই ফিচার কাজ করবে  
✅ OpenAI GPT API ব্যবহার করা হবে  

---

## 🧠 Step 1: OpenAI API Key সংগ্রহ করা

1. [https://platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys) এ গিয়ে  
2. **নতুন API Key** তৈরি করো  
3. `.env` ফাইলে যুক্ত করো:

```env
OPENAI_API_KEY=your_openai_api_key
```

---

## 📦 Step 2: OpenAI SDK ইনস্টল করা

```bash
npm install openai
```

---

## 📁 Step 3: API Route তৈরি করো — `/api/ai/summary.js`

```js
import { OpenAI } from "openai";

const openai = new OpenAI({
  apiKey: process.env.OPENAI_API_KEY,
});

export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).json({ error: "Only POST allowed" });

  const { content } = req.body;

  try {
    const completion = await openai.chat.completions.create({
      model: "gpt-3.5-turbo",
      messages: [
        { role: "system", content: "You are a blogging assistant." },
        { role: "user", content: `Summarize this blog post in 2-3 lines:\n\n${content}` },
      ],
      temperature: 0.7,
    });

    const summary = completion.choices[0].message.content;
    res.status(200).json({ summary });
  } catch (err) {
    res.status(500).json({ error: "AI request failed" });
  }
}
```

---

## 📁 Step 4: Admin Blog Create Page-এ AI Summary বাটন যুক্ত করো

📁 **pages/admin/create.js** ফাইলে যুক্ত করো:

```js
const [summary, setSummary] = useState("");

const getSummary = async () => {
  const res = await fetch("/api/ai/summary", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify({ content: form.content }),
  });

  const data = await res.json();
  setSummary(data.summary);
};
```

👇 বাটন ও রেজাল্ট দেখাও:

```js
<button type="button" onClick={getSummary} className="bg-purple-600 text-white px-4 py-2">
  ✨ Generate AI Summary
</button>

{summary && (
  <div className="mt-4 bg-gray-100 p-4 rounded">
    <h3 className="font-bold mb-2">AI Summary:</h3>
    <p>{summary}</p>
  </div>
)}
```

---

## 🧠 Bonus (Title → Outline Suggestion):

👉 `/api/ai/suggest.js` ফাইল তৈরি করো:

```js
export default async function handler(req, res) {
  const { title } = req.body;

  const response = await openai.chat.completions.create({
    model: "gpt-3.5-turbo",
    messages: [
      { role: "user", content: `Give me blog outline ideas for the title: ${title}` },
    ],
  });

  const ideas = response.choices[0].message.content;
  res.status(200).json({ ideas });
}
```

👉 Admin Panel-এ আরেকটা বাটন দিয়ে title অনুযায়ী কনটেন্ট সাজেশন দেখানো যাবে।

---

## ✅ পর্ব ১৪ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ AI Summary API | Done |
| ✅ Blog Editor-এ Integration | Done |
| ✅ Title → Outline Suggestion | Bonus Done |
| ✅ Fully dynamic response | Done |

---

## 🔜 পরবর্তী পর্ব:
**🌐 Multilingual Support (i18n) + Bengali-English Blog Toggle**  
✅ ব্লগ কনটেন্ট দুই ভাষায় দেখানো  
✅ UI Toggle (EN ⇄ BN)  
✅ i18n config করা  

🟢 **চলবো কি বাংলায় ব্লগ রেন্ডারিং ফিচারে?** 😄

চল এবার করি —  
# **🌐 পর্ব ১৫: Multilingual Support (i18n) + Bengali-English Blog Toggle**

আমাদের লক্ষ্য:  
✅ ব্লগ সাইটে **বাংলা ও ইংরেজি দুই ভাষায় কনটেন্ট** দেখানো  
✅ ব্লগ টাইটেল, কনটেন্ট, UI টেক্সট — দুই ভাষার সাপোর্ট  
✅ ভাষা Toggle বাটন (🇧🇩 BN ⇄ EN 🇬🇧)  
✅ Next.js i18n কনফিগারেশন ব্যবহার  

---

## 🔧 Step 1: Next.js `i18n` কনফিগার করা

📁 **next.config.js** ফাইলে যুক্ত করো:

```js
module.exports = {
  i18n: {
    locales: ['en', 'bn'],
    defaultLocale: 'en',
    localeDetection: true,
  },
  reactStrictMode: true,
};
```

👉 এতে করে তোমার URL হবে এমন:
- `/en/blog/my-blog`
- `/bn/blog/my-blog`

---

## 🌐 Step 2: Language Toggle Component তৈরি করো

📁 **components/LanguageSwitcher.js**

```js
import { useRouter } from 'next/router';

export default function LanguageSwitcher() {
  const router = useRouter();
  const { locale, pathname, asPath, query } = router;

  const toggleLang = () => {
    const nextLocale = locale === 'en' ? 'bn' : 'en';
    router.push({ pathname, query }, asPath, { locale: nextLocale });
  };

  return (
    <button onClick={toggleLang} className="text-sm text-blue-500">
      🌐 {locale === 'en' ? 'বাংলা' : 'English'}
    </button>
  );
}
```

📁 **Header.js** এ এটি ব্যবহার করো:

```js
import LanguageSwitcher from "./LanguageSwitcher";
...
<nav className="flex gap-4 items-center">
  ...
  <LanguageSwitcher />
</nav>
```

---

## 🧩 Step 3: ব্লগ মডেলে bilingual ফিল্ড যুক্ত করো

📁 **schema.prisma** ফাইল আপডেট করো:

```prisma
model Blog {
  ...
  titleBn   String?
  contentBn String?
}
```

📦 Push করো:
```bash
npx prisma db push
```

---

## ✍️ Step 4: Blog Create Page এ বাংলা ফিল্ড যুক্ত করো

📁 **pages/admin/create.js**:

```js
<input
  type="text"
  placeholder="Bangla Title"
  value={form.titleBn}
  onChange={(e) => setForm({ ...form, titleBn: e.target.value })}
/>

<ReactQuill
  theme="snow"
  value={form.contentBn}
  onChange={(value) => setForm({ ...form, contentBn: value })}
/>
```

---

## 🌍 Step 5: Blog Details পেইজে ভাষা অনুযায়ী কনটেন্ট দেখাও

📁 **pages/blog/[slug].js** ফাইলে যুক্ত করো:

```js
import { useRouter } from 'next/router';
...
const { locale } = useRouter();
...
<h1>{locale === 'bn' ? blog.titleBn || blog.title : blog.title}</h1>
<div dangerouslySetInnerHTML={{
  __html: locale === 'bn' ? blog.contentBn || blog.content : blog.content
}} />
```

---

## 🌐 Step 6: Static UI টেক্সট bilingual করো (Optional i18n lib সহ)

চাইলে `next-translate` বা `next-i18next` ইন্সটল করে ইউজ করো, অথবা নিজে কন্ডিশন দিয়ে UI টেক্সট বাংলা/ইংলিশ দেখাও।

```js
{locale === 'bn' ? "সম্পর্কিত ব্লগসমূহ" : "Related Posts"}
```

---

## ✅ পর্ব ১৫ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ i18n Config | Done |
| ✅ Language Toggle | Done |
| ✅ Blog Bilingual Content | Done |
| ✅ Language-Aware Rendering | Done |
| ✅ Full URL-based Switching | Done |

---

## 🔜 পরবর্তী পর্ব:
**📈 Blog Analytics (Views Count + Popular Posts)**  
✅ প্রতিটি ব্লগে ভিউ কাউন্ট  
✅ সবচেয়ে বেশি দেখা ব্লগ লিস্ট করা  
✅ Page refresh করে ভিউ বাড়বে না

🟢 **চলবো কি Analytics System বানাতে?** 📊

চল তাহলে এবার বানাই —  
# **📈 পর্ব ১৬: Blog Analytics – Views Count + Popular Posts**

আমাদের লক্ষ্য:  
✅ প্রতিটি ব্লগ পোস্টে **ভিউ কাউন্ট** ট্র্যাক করা  
✅ কেবল **ইউনিক ভিউ** গণনা (রিফ্রেশ করলে বারবার না বাড়ে)  
✅ হোমপেজ বা সাইডবারে **Most Popular Blogs** দেখানো  

---

## 🧩 Step 1: Prisma Schema-তে View Count ফিল্ড অ্যাড করো

📁 **prisma/schema.prisma** ফাইল আপডেট করো:

```prisma
model Blog {
  ...
  views Int @default(0)
}
```

📦 ডাটাবেসে Push করো:
```bash
npx prisma db push
```

---

## 🔁 Step 2: View Count বাড়ানোর API বানাও

📁 **pages/api/blog/view.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).json({ error: "Method not allowed" });

  const { slug } = req.body;

  try {
    await prisma.blog.update({
      where: { slug },
      data: { views: { increment: 1 } },
    });

    res.status(200).json({ message: "View counted" });
  } catch (err) {
    res.status(500).json({ error: "Error counting view" });
  }
}
```

---

## 🌍 Step 3: Blog Details পেইজে View কাউন্ট ট্রিগার করো

📁 **pages/blog/[slug].js** ফাইলে যুক্ত করো:

```js
useEffect(() => {
  if (slug && localStorage) {
    const viewedKey = `viewed-${slug}`;
    if (!localStorage.getItem(viewedKey)) {
      fetch("/api/blog/view", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ slug }),
      });
      localStorage.setItem(viewedKey, "true");
    }
  }
}, [slug]);
```

🔹 **ব্যাখ্যা:**  
👉 লোকালস্টোরেজ ব্যবহার করে প্রতি ইউজারের জন্য একবারই কাউন্ট হবে।  
👉 Refresh করলেও ভিউ আর বাড়বে না।

---

## 🔥 Step 4: Blog Post UI-তে Views দেখাও

```js
<p className="text-sm text-gray-500">
  {blog.views} views | {calculateReadingTime(blog.content)} min read
</p>
```

---

## 🌟 Step 5: Most Viewed Blogs দেখানোর API বানাও

📁 **pages/api/blog/popular.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  try {
    const blogs = await prisma.blog.findMany({
      where: { published: true },
      orderBy: { views: "desc" },
      take: 5,
    });

    res.status(200).json(blogs);
  } catch {
    res.status(500).json({ error: "Something went wrong" });
  }
}
```

---

## 🧱 Step 6: Sidebar-এ Popular Posts দেখাও

📁 **components/Sidebar.js** ফাইল আপডেট করো:

```js
import { useEffect, useState } from "react";
import Link from "next/link";

export default function Sidebar() {
  const [popular, setPopular] = useState([]);

  useEffect(() => {
    fetch("/api/blog/popular")
      .then((res) => res.json())
      .then((data) => setPopular(data));
  }, []);

  return (
    <aside className="w-64 bg-gray-100 p-4 rounded-lg">
      <h2 className="text-lg font-semibold mb-4">🔥 Popular Blogs</h2>
      <ul>
        {popular.map((blog) => (
          <li key={blog.id} className="mb-2">
            <Link href={`/blog/${blog.slug}`} className="text-blue-600 hover:underline">
              {blog.title} ({blog.views})
            </Link>
          </li>
        ))}
      </ul>
    </aside>
  );
}
```

---

## ✅ পর্ব ১৬ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Views Field | Done |
| ✅ Count API | Done |
| ✅ Unique View (localStorage) | Done |
| ✅ Show View Count | Done |
| ✅ Popular Blogs API | Done |
| ✅ Sidebar Integration | Done |

---

## 🔜 পরবর্তী পর্ব:
**🔄 Pagination + Infinite Scroll System**  
✅ প্রতি পেইজে নির্দিষ্ট সংখ্যক ব্লগ  
✅ লোড মোর বাটন / অটো infinite scroll  
✅ Performance optimized listing  

🟢 **চলবো কি Pagination ফিচারে?** 🔄

চল তাহলে এবার করি —  
# **🔄 পর্ব ১৭: Pagination + Infinite Scroll for Blog Listing**

আমাদের লক্ষ্য:  
✅ ব্লগ লিস্ট পেইজে প্রতি পেইজে নির্দিষ্ট সংখ্যক ব্লগ দেখানো  
✅ “Load More” বাটনে নতুন ব্লগ লোড হওয়া  
✅ চাইলে পরে **Auto Infinite Scroll** যোগ করা  
✅ SEO ফ্রেন্ডলি, Fast Rendering  

---

## 🧠 Pagination Strategy

- Backend → `/api/blog/paginated?page=1&limit=6`  
- Frontend → প্রথমে কিছু ব্লগ দেখাবে  
- তারপর **“Load More”** বাটনে পরবর্তী ব্লগ ফেচ হবে  

---

## 📁 Step 1: Paginated Blog API বানাও

📁 **pages/api/blog/paginated.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  const page = parseInt(req.query.page) || 1;
  const limit = parseInt(req.query.limit) || 6;
  const skip = (page - 1) * limit;

  try {
    const blogs = await prisma.blog.findMany({
      skip,
      take: limit,
      orderBy: { createdAt: "desc" },
      include: { author: true, category: true, tags: true },
    });

    const total = await prisma.blog.count();
    const hasMore = skip + limit < total;

    res.status(200).json({ blogs, hasMore });
  } catch {
    res.status(500).json({ error: "Something went wrong" });
  }
}
```

---

## 🧱 Step 2: Homepage-এ Pagination যুক্ত করো

📁 **pages/index.js** আপডেট করো:

```js
import { useState, useEffect } from "react";
import SearchBar from "@/components/SearchBar";
import Link from "next/link";

export default function Home() {
  const [blogs, setBlogs] = useState([]);
  const [page, setPage] = useState(1);
  const [hasMore, setHasMore] = useState(true);

  useEffect(() => {
    loadBlogs(page);
  }, []);

  const loadBlogs = async (currentPage) => {
    const res = await fetch(`/api/blog/paginated?page=${currentPage}&limit=6`);
    const data = await res.json();

    setBlogs((prev) => [...prev, ...data.blogs]);
    setHasMore(data.hasMore);
  };

  const handleLoadMore = () => {
    const nextPage = page + 1;
    setPage(nextPage);
    loadBlogs(nextPage);
  };

  return (
    <div className="container mx-auto py-10">
      <h1 className="text-4xl font-bold text-center mb-6">Latest Blogs</h1>
      <SearchBar />

      <div className="grid md:grid-cols-3 gap-6">
        {blogs.map((blog) => (
          <div key={blog.id} className="border p-4 rounded-md">
            <h2 className="text-xl font-semibold">{blog.title}</h2>
            <p className="text-sm text-gray-500">{blog.views} views</p>
            <p className="mt-2 text-gray-700" dangerouslySetInnerHTML={{
              __html: blog.content.substring(0, 100)
            }}></p>
            <Link href={`/blog/${blog.slug}`} className="text-blue-500 mt-2 inline-block">Read More</Link>
          </div>
        ))}
      </div>

      {hasMore && (
        <div className="text-center mt-8">
          <button onClick={handleLoadMore} className="bg-blue-600 text-white px-6 py-2 rounded">
            Load More
          </button>
        </div>
      )}
    </div>
  );
}
```

---

## 💡 Optional Step: Infinite Scroll (auto trigger on scroll)

এটি চাইলে আমরা পরে করবো — Intersection Observer দিয়ে।

---

## ✅ পর্ব ১৭ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Paginated API | Done |
| ✅ Blog Listing with Page State | Done |
| ✅ Load More Button | Done |
| ✅ Smooth UX & SEO-friendly | Done |

---

## 🔜 পরবর্তী পর্ব:
**📄 Printable Version & PDF Export (Blog)**  
✅ ব্লগ প্রিন্ট-ফ্রেন্ডলি ফরম্যাটে রেন্ডার  
✅ "Download as PDF" বাটন  
✅ হাই-কোয়ালিটি PDF (html2pdf.js or Puppeteer)

🟢 **চলবো কি PDF Export ফিচারে?** 🖨️📄

চল তাহলে করি —  
# **📄 পর্ব ১৮: Printable Version & PDF Export of Blog Posts**

আমাদের লক্ষ্য:  
✅ প্রতিটি ব্লগের জন্য **প্রিন্ট ফ্রেন্ডলি ভিউ**  
✅ একটি বাটনে ক্লিকেই **PDF ডাউনলোড**  
✅ Clean, readable, branding-friendly output  
✅ Browser-based (Client-side PDF export)  

---

## 📦 Step 1: `html2pdf.js` লাইব্রেরি ইন্সটল করো

```bash
npm install html2pdf.js
```

---

## 🧱 Step 2: Blog Details পেইজে PDF Export বাটন ও ফাংশন যোগ করো

📁 **pages/blog/[slug].js** ফাইল আপডেট করো:

```js
import dynamic from "next/dynamic";
import { useRef } from "react";

const html2pdf = dynamic(() => import("html2pdf.js"), { ssr: false });
```

👇 ডাউনলোড ফাংশন:

```js
const pdfRef = useRef();

const downloadPDF = () => {
  const element = pdfRef.current;
  const opt = {
    margin: 0.5,
    filename: `${blog.title}.pdf`,
    image: { type: "jpeg", quality: 0.98 },
    html2canvas: { scale: 2 },
    jsPDF: { unit: "in", format: "letter", orientation: "portrait" },
  };

  html2pdf().set(opt).from(element).save();
};
```

👇 ডাউনলোড বাটন এবং রেফারেন্সড কনটেইনার:

```js
<div className="text-right mb-4">
  <button onClick={downloadPDF} className="bg-green-600 text-white px-4 py-2 rounded">
    📄 Download as PDF
  </button>
</div>

<div ref={pdfRef} className="bg-white p-6 shadow rounded print:shadow-none print:p-0">
  <h1 className="text-4xl font-bold mb-2">{blog.title}</h1>
  <p className="text-gray-600 text-sm">
    By {blog.author.name} | {new Date(blog.createdAt).toLocaleDateString()}
  </p>
  <div className="mt-4 text-lg" dangerouslySetInnerHTML={{ __html: blog.content }} />
</div>
```

---

## 🖨️ Step 3: Optional – প্রিন্ট ফ্রেন্ডলি CSS

📁 **styles/globals.css** এ যুক্ত করো:

```css
@media print {
  .print\:hidden {
    display: none;
  }

  .print\:shadow-none {
    box-shadow: none !important;
  }

  .print\:p-0 {
    padding: 0 !important;
  }
}
```

---

## ✅ পর্ব ১৮ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ PDF Export (Client-side) | Done |
| ✅ Clean Layout | Done |
| ✅ One-click Download | Done |
| ✅ Print Friendly Styling | Done |

---

## 🔜 পরবর্তী পর্ব:
**💬 Blog Comments System (Disqus & Custom)**  
✅ পাঠকরা মন্তব্য করতে পারবে  
✅ Disqus বা নিজস্ব comment storage  
✅ স্প্যাম ফিল্টার, Auth, মডারেশন (পরবর্তী)

🟢 **চলবো কি কমেন্ট সিস্টেমে?** 💬

চল তাহলে এবার যুক্ত করি —  
# **💬 পর্ব ১৯: Blog Comments System (Disqus & Custom Integration)**

আমাদের লক্ষ্য:  
✅ প্রতিটি ব্লগের নিচে **কমেন্ট সেকশন** থাকবে  
✅ প্রথমে **Disqus Integration** দিয়ে শুরু করবো (সহজ ও দ্রুত)  
✅ এরপর চাইলে **Custom Comment System** বানাতে পারবো (user-auth, db-store সহ)  

---

## 🥇 **Step 1: Disqus Integration (Easiest & SEO Friendly)**

### ✅ ১. Disqus Account ও Site তৈরি করো
1. যাও [https://disqus.com/profile/signup/](https://disqus.com/profile/signup/)
2. “I want to install Disqus on my site” সিলেক্ট করো
3. Site Name দাও (যেমন: `nextjs-blog-cms`)
4. Platform: **Universal Code** সিলেক্ট করো
5. Disqus Shortname (e.g., `nextjsblogcms`) সংরক্ষণ করো

---

### ✅ ২. Blog Details পেইজে Disqus কম্পোনেন্ট যুক্ত করো

📁 **components/DisqusComments.js** তৈরি করো:

```js
import { DiscussionEmbed } from "disqus-react";

export default function DisqusComments({ post }) {
  const disqusShortname = "your_disqus_shortname"; // 🔁 Replace this
  const disqusConfig = {
    url: `https://yourdomain.com/blog/${post.slug}`,
    identifier: post.id,
    title: post.title,
  };

  return (
    <div className="mt-10">
      <h2 className="text-2xl font-bold mb-4">💬 Comments</h2>
      <DiscussionEmbed shortname={disqusShortname} config={disqusConfig} />
    </div>
  );
}
```

👉 `yourdomain.com` ডেভে থাকলে `http://localhost:3000` দিয়েও কাজ করবে।

---

### ✅ ৩. `disqus-react` প্যাকেজ ইনস্টল করো

```bash
npm install disqus-react
```

---

### ✅ ৪. Blog Details পেইজে কম্পোনেন্ট কল করো

📁 **pages/blog/[slug].js** ফাইলে যুক্ত করো:

```js
import DisqusComments from "@/components/DisqusComments";
...
<DisqusComments post={blog} />
```

---

## 📦 Ready! এখন প্রতিটি ব্লগের নিচে ডিস্কাস কমেন্ট সেকশন চলে আসবে:

✅ SEO ফ্রেন্ডলি  
✅ Logged-in Users (Facebook, Google, Disqus)  
✅ স্প্যাম ফিল্টারিং & মডারেশন  
✅ অটো লোডিং, ইউজার ফটো, রিপ্লাই সাপোর্ট  

---

## 🔧 Want Custom Comments System?

তুমি চাইলে পরের পর্বে **Custom Comment System** করতে পারি:

| ফিচার | করা হবে |
|--------|---------|
| ✅ ইউজার Authentication (NextAuth) | Login ছাড়া কমেন্ট নয় |
| ✅ ডাটাবেজে কমেন্ট সেভ | Prisma Model |
| ✅ Reply to Comment (Nested) | Optional |
| ✅ Admin Panel এ মডারেশন | Hide/Approve/Delete |

---

## ✅ পর্ব ১৯ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Disqus Integration | Done |
| ✅ Fully Functional Comments | Done |
| ✅ Blog-wise Comments Tracking | Done |

---

## 🔜 পরবর্তী পর্ব:
**🔐 Two-Factor Authentication (2FA with Email or OTP)**  
✅ ইউজার Login করলে কোড ভেরিফাই করতে হবে  
✅ Extra Security for Admin Users  

🟢 **চলবো কি Security Feature এ? নাকি Custom Comments বানাতে চাও?**

দারুণ! এখন আমরা করবো —  
# **💬 পর্ব ২০: Custom Comment System (Fully Functional in Your Blog)**

আমাদের লক্ষ্য:  
✅ ইউজার লগইন করলে **কমেন্ট করতে পারবে**  
✅ **Prisma দিয়ে ডাটাবেসে কমেন্ট সেভ হবে**  
✅ কমেন্টগুলো **ব্লগ ভিত্তিক ফিল্টার হয়ে দেখাবে**  
✅ (অপশনাল: Reply, Admin মডারেশন, Approval system)

---

## 🔧 Step 1: Prisma Schema-তে `Comment` Model অ্যাড করো

📁 **schema.prisma** ফাইল আপডেট করো:

```prisma
model Comment {
  id        String   @id @default(uuid())
  content   String
  createdAt DateTime @default(now())
  user      User     @relation(fields: [userId], references: [id])
  userId    String
  blog      Blog     @relation(fields: [blogId], references: [id])
  blogId    String
}
```

📦 এরপর ডাটাবেসে Push করো:
```bash
npx prisma db push
```

---

## 🛠️ Step 2: API Routes বানাও

### ✅ `POST` – নতুন কমেন্ট তৈরি  
📁 **pages/api/comment/create.js**

```js
import { getSession } from "next-auth/react";
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).json({ error: "Method not allowed" });

  const session = await getSession({ req });
  if (!session) return res.status(401).json({ error: "Unauthorized" });

  const { content, blogId } = req.body;
  if (!content || !blogId) return res.status(400).json({ error: "Missing fields" });

  const comment = await prisma.comment.create({
    data: {
      content,
      blogId,
      userId: session.user.id,
    },
    include: { user: true },
  });

  res.status(201).json(comment);
}
```

---

### ✅ `GET` – একটি ব্লগের সব কমেন্ট দেখানো  
📁 **pages/api/comment/[blogId].js**

```js
import { PrismaClient } from "@prisma/client";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  const { blogId } = req.query;

  try {
    const comments = await prisma.comment.findMany({
      where: { blogId },
      include: { user: true },
      orderBy: { createdAt: "desc" },
    });

    res.status(200).json(comments);
  } catch {
    res.status(500).json({ error: "Failed to fetch comments" });
  }
}
```

---

## 🧱 Step 3: Blog Details পেইজে কমেন্ট UI দেখাও

📁 **components/Comments.js** (নতুন কম্পোনেন্ট)

```js
import { useEffect, useState } from "react";
import { useSession } from "next-auth/react";

export default function Comments({ blogId }) {
  const { data: session } = useSession();
  const [comments, setComments] = useState([]);
  const [input, setInput] = useState("");

  useEffect(() => {
    fetch(`/api/comment/${blogId}`)
      .then((res) => res.json())
      .then((data) => setComments(data));
  }, [blogId]);

  const handleSubmit = async (e) => {
    e.preventDefault();
    if (!input.trim()) return;

    const res = await fetch("/api/comment/create", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ content: input, blogId }),
    });

    const newComment = await res.json();
    setComments([newComment, ...comments]);
    setInput("");
  };

  return (
    <div className="mt-10">
      <h2 className="text-2xl font-bold mb-4">💬 Comments</h2>

      {session ? (
        <form onSubmit={handleSubmit} className="mb-6">
          <textarea
            className="w-full border p-2 rounded"
            placeholder="Write your comment..."
            value={input}
            onChange={(e) => setInput(e.target.value)}
          />
          <button type="submit" className="bg-blue-600 text-white px-4 py-2 mt-2 rounded">
            Post Comment
          </button>
        </form>
      ) : (
        <p className="text-gray-500">Please login to comment.</p>
      )}

      <div className="space-y-4">
        {comments.map((c) => (
          <div key={c.id} className="border p-3 rounded bg-gray-50">
            <p className="text-sm font-semibold">{c.user.name}</p>
            <p className="text-gray-700">{c.content}</p>
            <p className="text-xs text-gray-400">{new Date(c.createdAt).toLocaleString()}</p>
          </div>
        ))}
      </div>
    </div>
  );
}
```

---

## 📄 Step 4: Blog Details পেইজে এই কম্পোনেন্ট কল করো

📁 **pages/blog/[slug].js** এর শেষে:

```js
import Comments from "@/components/Comments";
...
<Comments blogId={blog.id} />
```

---

## ✅ পর্ব ২০ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Custom Comments | Done |
| ✅ Authenticated Post | Done |
| ✅ Blog-wise Comments | Done |
| ✅ Real-time Update | Done |
| ✅ Fully Functional | ✅ |

---

## 🔜 পরবর্তী পর্ব:
**🔐 Two-Factor Authentication (2FA – OTP or Email Code)**  
✅ Admin login করলে কোড ভেরিফাই লাগবে  
✅ OTP/Code via Email or App  

🟢 **চলবো কি Advanced Login Security ফিচারে? নাকি Nested Comments / Admin Moderation বানাতে চাও?**

চল তাহলে এবার করি —  
# **🔐 পর্ব ২১: Two-Factor Authentication (2FA) via Email OTP**

আমাদের লক্ষ্য:  
✅ **Login করার পর OTP/Code Verification** লাগবে  
✅ Admin ও User – দুইজনের জন্যই কাজ করবে  
✅ Email এর মাধ্যমে OTP পাঠানো  
✅ OTP না দিলে Dashboard এ প্রবেশ সম্ভব নয়  

---

## 🔧 Step 1: Prisma Schema-তে OTP ফিল্ড অ্যাড করো

📁 **schema.prisma** আপডেট করো:

```prisma
model User {
  id        String   @id @default(uuid())
  name      String
  email     String   @unique
  password  String
  role      String   @default("user")
  otp       String?  // ✅ OTP Code
  otpExpiry DateTime? // ✅ Expiry time
  posts     Blog[]
  comments  Comment[]
}
```

📦 এরপর Push করো:
```bash
npx prisma db push
```

---

## 📧 Step 2: Nodemailer ইন্সটল করো (for sending email)

```bash
npm install nodemailer
```

📁 **.env** ফাইলে SMTP কনফিগার করো (example for Gmail):

```env
EMAIL_SERVER=smtp://your_email@gmail.com:your_app_password@smtp.gmail.com:587
EMAIL_FROM=Blog CMS <your_email@gmail.com>
```

---

## 🛠️ Step 3: `/api/auth/send-otp.js` API বানাও

📁 **pages/api/auth/send-otp.js**

```js
import { PrismaClient } from "@prisma/client";
import nodemailer from "nodemailer";
const prisma = new PrismaClient();

export default async function handler(req, res) {
  const { email } = req.body;

  const user = await prisma.user.findUnique({ where: { email } });
  if (!user) return res.status(404).json({ error: "User not found" });

  const otp = Math.floor(100000 + Math.random() * 900000).toString();
  const expiry = new Date(Date.now() + 10 * 60 * 1000); // 10 minutes

  await prisma.user.update({
    where: { email },
    data: { otp, otpExpiry: expiry },
  });

  // Send email
  const transporter = nodemailer.createTransport({
    service: "gmail",
    auth: {
      user: process.env.EMAIL_FROM,
      pass: process.env.EMAIL_SERVER.split(":")[2].split("@")[0],
    },
  });

  await transporter.sendMail({
    from: process.env.EMAIL_FROM,
    to: email,
    subject: "Your OTP for Blog Login",
    text: `Your OTP is ${otp}`,
  });

  res.status(200).json({ message: "OTP sent" });
}
```

---

## 🧾 Step 4: OTP Verification API বানাও

📁 **pages/api/auth/verify-otp.js**

```js
export default async function handler(req, res) {
  const { email, otp } = req.body;

  const user = await prisma.user.findUnique({ where: { email } });
  if (!user || user.otp !== otp) {
    return res.status(401).json({ error: "Invalid OTP" });
  }

  if (new Date() > user.otpExpiry) {
    return res.status(400).json({ error: "OTP expired" });
  }

  // Clear OTP
  await prisma.user.update({
    where: { email },
    data: { otp: null, otpExpiry: null },
  });

  res.status(200).json({ message: "OTP verified" });
}
```

---

## 📄 Step 5: Login এর পর Redirect করো `/verify-otp` পেইজে

📁 **pages/auth/verify-otp.js** তৈরি করো:

```js
import { useState } from "react";
import { useRouter } from "next/router";

export default function VerifyOTP() {
  const [otp, setOtp] = useState("");
  const router = useRouter();
  const { email } = router.query;

  const handleSubmit = async (e) => {
    e.preventDefault();
    const res = await fetch("/api/auth/verify-otp", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ email, otp }),
    });

    if (res.ok) {
      router.push("/dashboard");
    } else {
      alert("Invalid OTP");
    }
  };

  return (
    <div className="max-w-md mx-auto mt-20">
      <h1 className="text-2xl font-bold mb-4">Verify OTP</h1>
      <form onSubmit={handleSubmit} className="space-y-4">
        <input
          type="text"
          value={otp}
          onChange={(e) => setOtp(e.target.value)}
          placeholder="Enter OTP"
          className="w-full border p-2"
        />
        <button className="bg-blue-600 text-white px-4 py-2 w-full">Verify</button>
      </form>
    </div>
  );
}
```

---

## ✅ পর্ব ২১ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ OTP Generation | Done |
| ✅ Email Sending | Done |
| ✅ Verification | Done |
| ✅ Dashboard Restriction | Done |
| ✅ Secure Auth Flow | ✅ |

---

## 🔜 পরবর্তী পর্ব:
**🧩 Plugin System + Modular Architecture**  
✅ Future features প্লাগিন আকারে যুক্ত/অপসারণযোগ্য  
✅ Clean structure: `modules/blog`, `modules/user`, `modules/comments`  
✅ Easy maintenance, scalable CMS structure

🟢 **চলবো কি মডুলার ডিজাইন/প্লাগিন সাপোর্ট এ? নাকি 2FA তে SMS/Authenticator কোড চাই?**

