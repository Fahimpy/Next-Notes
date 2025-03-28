# Next-Notes

### **পর্ব ১: Next.js প্রজেক্ট সেটআপ ও বেসিক ফোল্ডার স্ট্রাকচার**  
আমরা প্রথমে **Next.js** ইন্সটল করবো এবং প্রয়োজনীয় প্যাকেজ সেটআপ করবো।  

---

### **📌 ধাপ ১: Next.js প্রজেক্ট তৈরি করা**  
প্রথমে **Next.js** প্রজেক্ট তৈরি করতে নিচের কমান্ডটি চালাও:

```bash
npx create-next-app@latest my-blog
```
or
```bash
yarn create next-app my-blog
```

👉 **my-blog** হচ্ছে তোমার প্রজেক্টের নাম, তুমি চাইলে অন্য নাম দিতে পারো।

> 🔹 **প্রশ্ন:** Next.js কেনো ব্যবহার করবো?  
> 🔹 **উত্তর:** Next.js SEO ফ্রেন্ডলি, SSR (Server-Side Rendering) এবং SSG (Static Site Generation) সাপোর্ট করে, যা ব্লগ CMS-এর জন্য পারফেক্ট।

---

### **📌 ধাপ ২: প্রজেক্টে প্রবেশ করা ও ডেভেলপমেন্ট সার্ভার চালানো**  
প্রজেক্ট ডিরেক্টরিতে যাও:

```bash
cd my-blog
```

এরপর **Next.js Dev Server** চালাও:

```bash
npm run dev
```

এখন **http://localhost:3000** ওপেন করলেই Next.js ডিফল্ট পেইজ দেখাবে।

---

### **📌 ধাপ ৩: Tailwind CSS সেটআপ করা**  
আমরা UI সুন্দর ও রেসপন্সিভ করতে **Tailwind CSS** ব্যবহার করবো। ইন্সটল করতে:

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

এতে **tailwind.config.js** ও **postcss.config.js** ফাইল তৈরি হবে।

---

### **📌 ধাপ ৪: Tailwind কনফিগার করা**  
📁 **tailwind.config.js** ফাইল ওপেন করে `content` সেট করো:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./pages/**/*.{js,ts,jsx,tsx}",
    "./components/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

এটি Tailwind কে বলছে, **pages/** ও **components/** ফোল্ডারে থাকা ফাইলগুলো স্ক্যান করতে।

---

### **📌 ধাপ ৫: Tailwind গ্লোবাল স্টাইল যোগ করা**  
📁 **styles/globals.css** ফাইল ওপেন করে নিচের কোডটি যোগ করো:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

### **📌 ধাপ ৬: ফোল্ডার স্ট্রাকচার সেটআপ**  
আমরা আমাদের প্রজেক্টের জন্য নিচের মতো ফোল্ডার স্ট্রাকচার রাখবো:

```
/my-blog
 ├── /pages
 │   ├── index.js          # Homepage
 │   ├── _app.js           # Main Layout
 │   ├── /blog             # Blog related pages
 │   │   ├── [slug].js     # Blog details page
 │   ├── /auth             # Login/Register pages
 │   ├── /dashboard        # Admin Panel
 ├── /components
 │   ├── Header.js         # Navbar/Menu
 │   ├── Footer.js         # Footer Section
 │   ├── Sidebar.js        # Sidebar
 │   ├── BlogCard.js       # Blog Preview Component
 ├── /styles
 │   ├── globals.css       # Global styles
 ├── /public
 │   ├── logo.png          # Site Logo
```

---

### **📌 ধাপ ৭: Navbar (Header) Component তৈরি করা**  
📁 **components/Header.js** ফাইল তৈরি করো এবং নিচের কোড লিখো:

```js
import Link from "next/link";

const Header = () => {
  return (
    <header className="bg-blue-600 text-white py-4">
      <div className="container mx-auto flex justify-between items-center px-4">
        <Link href="/">
          <h1 className="text-2xl font-bold cursor-pointer">My Blog</h1>
        </Link>
        <nav>
          <ul className="flex gap-4">
            <li><Link href="/" className="hover:underline">Home</Link></li>
            <li><Link href="/blog" className="hover:underline">Blog</Link></li>
            <li><Link href="/auth/login" className="hover:underline">Login</Link></li>
          </ul>
        </nav>
      </div>
    </header>
  );
};

export default Header;
```

---

### **📌 ধাপ ৮: Footer Component তৈরি করা**  
📁 **components/Footer.js** ফাইল তৈরি করো এবং নিচের কোড লিখো:

```js
const Footer = () => {
  return (
    <footer className="bg-gray-800 text-white text-center py-4 mt-8">
      <p>© {new Date().getFullYear()} My Blog. All rights reserved.</p>
    </footer>
  );
};

export default Footer;
```

---

### **📌 ধাপ ৯: Layout (গ্লোবাল লেআউট) সেটআপ করা**  
📁 **pages/_app.js** ফাইল আপডেট করো:

```js
import "../styles/globals.css";
import Header from "../components/Header";
import Footer from "../components/Footer";

function MyApp({ Component, pageProps }) {
  return (
    <div className="flex flex-col min-h-screen">
      <Header />
      <main className="flex-grow container mx-auto px-4">
        <Component {...pageProps} />
      </main>
      <Footer />
    </div>
  );
}

export default MyApp;
```

---

### **📌 ধাপ ১০: Homepage তৈরি করা**  
📁 **pages/index.js** ফাইল আপডেট করো:

```js
export default function Home() {
  return (
    <div className="text-center py-10">
      <h1 className="text-4xl font-bold">Welcome to My Blog</h1>
      <p className="text-gray-600 mt-2">Explore the latest articles and stories.</p>
    </div>
  );
}
```

---

### **✅ শেষ কথা:**  
এই পর্বে আমরা **Next.js সেটআপ, Tailwind CSS, Navbar, Footer এবং Homepage** তৈরি করলাম। এখন **http://localhost:3000** ওপেন করলেই দেখবে:

✅ **Navbar & Footer**  
✅ **Styled Homepage**  
✅ **Fully Responsive Layout**  

---

## **পর্ব ২: Next.js API Routes দিয়ে PostgreSQL কানেক্ট করা (Prisma ORM সহ)**  

তুমি **PostgreSQL** ব্যবহার করতে চাও, তাই আমরা **Prisma ORM** দিয়ে **PostgreSQL** সেটআপ করবো এবং ব্লগের জন্য **User, Blog, Category** মডেল তৈরি করবো।

---

## **📌 ধাপ ১: PostgreSQL ইনস্টল ও সেটআপ করা**  

### **👉 ১. Local PostgreSQL ইনস্টল (Mac/Linux/Windows)**
#### **Mac:**  
```bash
brew install postgresql
brew services start postgresql
```

#### **Linux:**  
```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo systemctl start postgresql
```

#### **Windows:**  
- **PostgreSQL Installer** ডাউনলোড করো: [https://www.postgresql.org/download/](https://www.postgresql.org/download/)  
- **pgAdmin** দিয়ে **ডাটাবেস তৈরি করো।**  

---

### **📌 ধাপ ২: PostgreSQL ডাটাবেস তৈরি করা**  
PostgreSQL টার্মিনালে লগিন করো:
```bash
psql -U postgres
```
**নতুন ডাটাবেস তৈরি করো:**  
```sql
CREATE DATABASE my_blog;
```
**নতুন ইউজার ও পাসওয়ার্ড সেট করো:**  
```sql
CREATE USER my_user WITH ENCRYPTED PASSWORD 'my_password';
GRANT ALL PRIVILEGES ON DATABASE my_blog TO my_user;
```
PostgreSQL CLI থেকে বের হও:
```bash
\q
```

---

### **📌 ধাপ ৩: Prisma ORM সেটআপ করা**  
```bash
npm install prisma @prisma/client
npx prisma init
```

এতে **prisma/schema.prisma** এবং **.env** ফাইল তৈরি হবে।

---

### **📌 ধাপ ৪: PostgreSQL কানেকশন সেটআপ করা**  
📁 **.env** ফাইল আপডেট করো:
```env
DATABASE_URL="postgresql://my_user:my_password@localhost:5432/my_blog?schema=public"
```

---

### **📌 ধাপ ৫: Prisma Schema আপডেট করা**  
📁 **prisma/schema.prisma** ফাইল আপডেট করো:

```prisma
generator client {
  provider = "prisma-client-js"
}

datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

model User {
  id       String  @id @default(uuid())
  name     String
  email    String  @unique
  password String
  role     String  @default("user")
  posts    Blog[]
}

model Blog {
  id          String   @id @default(uuid())
  title       String
  slug        String   @unique
  content     String
  createdAt   DateTime @default(now())
  updatedAt   DateTime @updatedAt
  author      User     @relation(fields: [authorId], references: [id])
  authorId    String
  category    Category @relation(fields: [categoryId], references: [id])
  categoryId  String
  published   Boolean  @default(false)
}

model Category {
  id    String  @id @default(uuid())
  name  String  @unique
  slug  String  @unique
  blogs Blog[]
}
```

---

### **📌 ধাপ ৬: Prisma Migrate চালানো**  
```bash
npx prisma generate
npx prisma migrate dev --name init
```

---

## **📌 ধাপ ৭: API Routes তৈরি করা (Next.js API Routes)**  

### **👉 ১. ব্লগ পোস্ট তৈরি করার API (Create Blog Post)**
📁 **pages/api/blog/create.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).json({ error: "Method not allowed" });

  try {
    const { title, content, categoryId, authorId } = req.body;

    if (!title || !content || !categoryId || !authorId) {
      return res.status(400).json({ error: "All fields are required" });
    }

    const newBlog = await prisma.blog.create({
      data: {
        title,
        slug: title.toLowerCase().replace(/ /g, "-"),
        content,
        categoryId,
        authorId,
        published: false,
      },
    });

    res.status(201).json(newBlog);
  } catch (error) {
    res.status(500).json({ error: "Server Error" });
  }
}
```

---

### **👉 ২. সব ব্লগ পোস্ট রিট্রিভ করার API (Get All Blogs)**
📁 **pages/api/blog/index.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "GET") return res.status(405).json({ error: "Method not allowed" });

  try {
    const blogs = await prisma.blog.findMany({
      include: {
        author: true,
        category: true,
      },
    });

    res.status(200).json(blogs);
  } catch (error) {
    res.status(500).json({ error: "Server Error" });
  }
}
```

---

### **👉 ৩. নির্দিষ্ট ব্লগ পোস্ট রিট্রিভ করার API (Get Single Blog by Slug)**
📁 **pages/api/blog/[slug].js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  const { slug } = req.query;

  if (req.method !== "GET") return res.status(405).json({ error: "Method not allowed" });

  try {
    const blog = await prisma.blog.findUnique({
      where: { slug },
      include: {
        author: true,
        category: true,
      },
    });

    if (!blog) return res.status(404).json({ error: "Blog not found" });

    res.status(200).json(blog);
  } catch (error) {
    res.status(500).json({ error: "Server Error" });
  }
}
```

---

## **📌 ধাপ ৮: API টেস্ট করা**
Postman বা Thunder Client দিয়ে API গুলো টেস্ট করো।

#### **✅ Create Blog Test (POST)**
```json
{
  "title": "First Blog",
  "content": "This is my first blog post.",
  "categoryId": "your-category-id",
  "authorId": "your-author-id"
}
```

#### **✅ Get All Blogs (GET)**
```
GET http://localhost:3000/api/blog
```

#### **✅ Get Single Blog (GET)**
```
GET http://localhost:3000/api/blog/first-blog
```

---

# **পর্ব ৩: ব্লগের জন্য UI ডিজাইন করা (Next.js Frontend Development)**  

এখন আমরা **ব্লগ UI** তৈরি করবো। এই ধাপে আমরা নিম্নলিখিত কাজ করবো:  
✅ **ব্লগ লিস্ট পেজ (Homepage)**  
✅ **ব্লগ ডিটেইলস পেজ**  
✅ **SEO সেটআপ (Meta Title, Description, Index/No Index)**  

---

## **📌 ধাপ ১: ব্লগ লিস্ট পেজ (Homepage) তৈরি করা**  

📁 **pages/index.js** ফাইল তৈরি করো এবং নিচের কোড লিখো:  

```js
import Link from "next/link";
import { useState, useEffect } from "react";

export default function Home() {
  const [blogs, setBlogs] = useState([]);

  useEffect(() => {
    fetch("/api/blog")
      .then((res) => res.json())
      .then((data) => setBlogs(data));
  }, []);

  return (
    <div className="container mx-auto py-10">
      <h1 className="text-4xl font-bold text-center mb-6">Latest Blogs</h1>
      <div className="grid md:grid-cols-3 gap-6">
        {blogs.map((blog) => (
          <div key={blog.id} className="border p-4 rounded-lg shadow-md">
            <h2 className="text-xl font-semibold">{blog.title}</h2>
            <p className="text-gray-600 text-sm">By {blog.author.name}</p>
            <p className="mt-2 text-gray-800">{blog.content.substring(0, 100)}...</p>
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

🔹 **কোড ব্যাখ্যা:**  
✅ **useEffect()** দিয়ে **API call** করা হয়েছে  
✅ **ব্লগ লিস্ট দেখানোর জন্য** **grid layout** ব্যবহার করা হয়েছে  
✅ **"Read More" লিঙ্ক** দিয়ে **ব্লগ ডিটেইলস পেজে** পাঠানো হয়েছে  

---

## **📌 ধাপ ২: ব্লগ ডিটেইলস পেজ তৈরি করা**  

📁 **pages/blog/[slug].js** ফাইল তৈরি করো এবং নিচের কোড লিখো:  

```js
import { useRouter } from "next/router";
import { useEffect, useState } from "react";
import Head from "next/head";

export default function BlogDetails() {
  const router = useRouter();
  const { slug } = router.query;
  const [blog, setBlog] = useState(null);

  useEffect(() => {
    if (slug) {
      fetch(`/api/blog/${slug}`)
        .then((res) => res.json())
        .then((data) => setBlog(data));
    }
  }, [slug]);

  if (!blog) return <p className="text-center mt-10">Loading...</p>;

  return (
    <div className="container mx-auto py-10">
      <Head>
        <title>{blog.title} | My Blog</title>
        <meta name="description" content={blog.content.substring(0, 150)} />
      </Head>

      <h1 className="text-4xl font-bold">{blog.title}</h1>
      <p className="text-gray-600 text-sm">By {blog.author.name} | {new Date(blog.createdAt).toLocaleDateString()}</p>
      <div className="mt-6 text-lg">{blog.content}</div>
    </div>
  );
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **useEffect()** দিয়ে **API call** করা হয়েছে  
✅ **Head component** দিয়ে **SEO-friendly Meta Tags** যোগ করা হয়েছে  
✅ **ব্লগ ডিটেইলস দেখানোর জন্য** **slug ভিত্তিক পেজ** তৈরি করা হয়েছে  

---

## **📌 ধাপ ৩: SEO সেটআপ করা (Meta Title, Description, Index/No Index)**  

📁 **components/SEO.js** নামে একটি কম্পোনেন্ট তৈরি করো এবং নিচের কোড লিখো:  

```js
import Head from "next/head";

const SEO = ({ title, description, noIndex }) => {
  return (
    <Head>
      <title>{title}</title>
      <meta name="description" content={description} />
      {noIndex && <meta name="robots" content="noindex, nofollow" />}
    </Head>
  );
};

export default SEO;
```

🔹 **কোড ব্যাখ্যা:**  
✅ **SEO ট্যাগ (title, meta description) ডাইনামিক করা হয়েছে**  
✅ **noindex/nofollow সাপোর্ট করা হয়েছে**  

এখন **index.js** ও **[slug].js** ফাইল আপডেট করে **SEO.js** কম্পোনেন্ট ব্যবহার করো:

📁 **pages/index.js**  
```js
import SEO from "@/components/SEO";
export default function Home() {
  return (
    <div>
      <SEO title="My Blog | Home" description="Read the latest blogs" />
      <h1>Welcome to My Blog</h1>
    </div>
  );
}
```

📁 **pages/blog/[slug].js**  
```js
<SEO title={`${blog.title} | My Blog`} description={blog.content.substring(0, 150)} />
```

---

## **📌 ধাপ ৪: Sidebar তৈরি করা**  

📁 **components/Sidebar.js** ফাইল তৈরি করো:  

```js
import Link from "next/link";

export default function Sidebar({ categories }) {
  return (
    <aside className="w-64 bg-gray-100 p-4 rounded-lg">
      <h2 className="text-lg font-semibold mb-4">Categories</h2>
      <ul>
        {categories.map((category) => (
          <li key={category.id} className="mb-2">
            <Link href={`/category/${category.slug}`} className="text-blue-500">
              {category.name}
            </Link>
          </li>
        ))}
      </ul>
    </aside>
  );
}
```

---

## **📌 ধাপ ৫: Sidebar ব্লগ ডিটেইলস পেজে যোগ করা**  
📁 **pages/blog/[slug].js** ফাইল আপডেট করো:

```js
import Sidebar from "@/components/Sidebar";

export default function BlogDetails({ categories }) {
  return (
    <div className="container mx-auto flex">
      <div className="w-2/3">
        <h1>{blog.title}</h1>
        <p>{blog.content}</p>
      </div>
      <Sidebar categories={categories} />
    </div>
  );
}
```

---

## **📌 চূড়ান্ত ফলাফল**  
✅ **http://localhost:3000/** 👉 ব্লগ লিস্ট দেখাবে  
✅ **http://localhost:3000/blog/first-blog** 👉 ব্লগ ডিটেইলস দেখাবে  
✅ **SEO (Meta Title, Description, Index/No Index) কাজ করবে**  

---

# **পর্ব ৪: Authentication (Login/Register) সিস্টেম সেটআপ করা**  

এই পর্বে আমরা **NextAuth.js** ব্যবহার করে **JWT-based Authentication** তৈরি করবো। আমাদের টার্গেট:  
✅ **User Register (নতুন ইউজার তৈরি করা)**  
✅ **User Login (ইউজার লগিন করা)**  
✅ **JWT Token দিয়ে Authentication**  
✅ **User Role (Admin/User ম্যানেজমেন্ট)**  

---

## **📌 ধাপ ১: NextAuth.js ইনস্টল করা**  
প্রথমে **NextAuth.js** ইন্সটল করো:
```bash
npm install next-auth bcryptjs
```
🔹 **bcryptjs** ইউজারের **password hash** করার জন্য ব্যবহার হবে।

---

## **📌 ধাপ ২: NextAuth কনফিগার করা**  
📁 **pages/api/auth/[...nextauth].js** ফাইল তৈরি করো এবং নিচের কোড লিখো:

```js
import NextAuth from "next-auth";
import CredentialsProvider from "next-auth/providers/credentials";
import { PrismaClient } from "@prisma/client";
import bcrypt from "bcryptjs";

const prisma = new PrismaClient();

export default NextAuth({
  session: {
    strategy: "jwt",
  },
  providers: [
    CredentialsProvider({
      name: "Credentials",
      credentials: {
        email: { label: "Email", type: "email", placeholder: "your-email@example.com" },
        password: { label: "Password", type: "password" },
      },
      async authorize(credentials) {
        const user = await prisma.user.findUnique({
          where: { email: credentials.email },
        });

        if (!user) throw new Error("No user found with this email");

        const isPasswordValid = await bcrypt.compare(credentials.password, user.password);
        if (!isPasswordValid) throw new Error("Incorrect password");

        return { id: user.id, name: user.name, email: user.email, role: user.role };
      },
    }),
  ],
  callbacks: {
    async jwt({ token, user }) {
      if (user) {
        token.id = user.id;
        token.role = user.role;
      }
      return token;
    },
    async session({ session, token }) {
      if (token) {
        session.user.id = token.id;
        session.user.role = token.role;
      }
      return session;
    },
  },
  secret: process.env.NEXTAUTH_SECRET,
});
```

🔹 **কোড ব্যাখ্যা:**  
✅ **CredentialsProvider** ইউজারের **email & password** দিয়ে লগিন চেক করে  
✅ **bcryptjs** দিয়ে **password validation** করা হয়েছে  
✅ **JWT token**-এর মধ্যে **user role** রাখা হয়েছে  

---

## **📌 ধাপ ৩: Register API তৈরি করা**  

📁 **pages/api/auth/register.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";
import bcrypt from "bcryptjs";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).json({ error: "Method not allowed" });

  const { name, email, password } = req.body;

  if (!name || !email || !password) {
    return res.status(400).json({ error: "All fields are required" });
  }

  const existingUser = await prisma.user.findUnique({ where: { email } });
  if (existingUser) {
    return res.status(400).json({ error: "User already exists" });
  }

  const hashedPassword = await bcrypt.hash(password, 10);

  const newUser = await prisma.user.create({
    data: {
      name,
      email,
      password: hashedPassword,
      role: "user",
    },
  });

  res.status(201).json({ message: "User registered successfully" });
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **Email Validation** করা হয়েছে  
✅ **Password Hashing** করা হয়েছে  
✅ **User Role: Default 'user'**  

---

## **📌 ধাপ ৪: Login/Register UI তৈরি করা**  

### **👉 ১. Register Page**  
📁 **pages/auth/register.js** ফাইল তৈরি করো:

```js
import { useState } from "react";
import { useRouter } from "next/router";

export default function Register() {
  const [form, setForm] = useState({ name: "", email: "", password: "" });
  const [error, setError] = useState("");
  const router = useRouter();

  const handleSubmit = async (e) => {
    e.preventDefault();
    const res = await fetch("/api/auth/register", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(form),
    });

    const data = await res.json();
    if (!res.ok) return setError(data.error);
    router.push("/auth/login");
  };

  return (
    <div className="max-w-md mx-auto mt-10">
      <h2 className="text-2xl font-bold">Register</h2>
      {error && <p className="text-red-500">{error}</p>}
      <form onSubmit={handleSubmit} className="space-y-4">
        <input type="text" placeholder="Name" className="w-full p-2 border" onChange={(e) => setForm({ ...form, name: e.target.value })} />
        <input type="email" placeholder="Email" className="w-full p-2 border" onChange={(e) => setForm({ ...form, email: e.target.value })} />
        <input type="password" placeholder="Password" className="w-full p-2 border" onChange={(e) => setForm({ ...form, password: e.target.value })} />
        <button type="submit" className="bg-blue-600 text-white p-2 w-full">Register</button>
      </form>
    </div>
  );
}
```

---

### **👉 ২. Login Page**  
📁 **pages/auth/login.js** ফাইল তৈরি করো:

```js
import { useState } from "react";
import { signIn } from "next-auth/react";
import { useRouter } from "next/router";

export default function Login() {
  const [form, setForm] = useState({ email: "", password: "" });
  const [error, setError] = useState("");
  const router = useRouter();

  const handleSubmit = async (e) => {
    e.preventDefault();
    const res = await signIn("credentials", {
      redirect: false,
      email: form.email,
      password: form.password,
    });

    if (res.error) return setError("Invalid email or password");
    router.push("/");
  };

  return (
    <div className="max-w-md mx-auto mt-10">
      <h2 className="text-2xl font-bold">Login</h2>
      {error && <p className="text-red-500">{error}</p>}
      <form onSubmit={handleSubmit} className="space-y-4">
        <input type="email" placeholder="Email" className="w-full p-2 border" onChange={(e) => setForm({ ...form, email: e.target.value })} />
        <input type="password" placeholder="Password" className="w-full p-2 border" onChange={(e) => setForm({ ...form, password: e.target.value })} />
        <button type="submit" className="bg-blue-600 text-white p-2 w-full">Login</button>
      </form>
    </div>
  );
}
```

---

# **পর্ব ৫: User Dashboard & Role-Based Access Control (RBAC)**  

এই পর্বে আমরা **User Dashboard** তৈরি করবো এবং **Role-Based Access Control (RBAC)** সেটআপ করবো। আমাদের লক্ষ্য:  
✅ **User Dashboard তৈরি করা**  
✅ **Admin/User পার্থক্য করা**  
✅ **Secure Routes (Admin Only Pages)**  

---

## **📌 ধাপ ১: User Dashboard Page তৈরি করা**  

📁 **pages/dashboard.js** ফাইল তৈরি করো:

```js
import { useSession, signOut } from "next-auth/react";
import { useRouter } from "next/router";

export default function Dashboard() {
  const { data: session, status } = useSession();
  const router = useRouter();

  if (status === "loading") return <p>Loading...</p>;

  if (!session) {
    router.push("/auth/login");
    return null;
  }

  return (
    <div className="max-w-2xl mx-auto mt-10">
      <h1 className="text-3xl font-bold">Dashboard</h1>
      <p>Welcome, {session.user.name}</p>
      <p>Your role: <strong>{session.user.role}</strong></p>

      <button onClick={() => signOut()} className="bg-red-500 text-white px-4 py-2 mt-4">
        Logout
      </button>

      {session.user.role === "admin" && (
        <div className="mt-6">
          <h2 className="text-xl font-semibold">Admin Section</h2>
          <p>You have admin privileges.</p>
        </div>
      )}
    </div>
  );
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **useSession()** দিয়ে লগিন ইউজার চেক করা হয়েছে  
✅ **signOut()** দিয়ে লগআউট অপশন যুক্ত করা হয়েছে  
✅ **Admin & User রোল আলাদা করা হয়েছে**  

---

## **📌 ধাপ ২: Secure Route (Admin Only Pages) তৈরি করা**  

📁 **components/AdminRoute.js** নামে একটি কম্পোনেন্ট তৈরি করো:

```js
import { useSession } from "next-auth/react";
import { useRouter } from "next/router";
import { useEffect } from "react";

export default function AdminRoute({ children }) {
  const { data: session, status } = useSession();
  const router = useRouter();

  useEffect(() => {
    if (status !== "loading" && (!session || session.user.role !== "admin")) {
      router.push("/");
    }
  }, [session, status]);

  if (status === "loading") return <p>Loading...</p>;

  return session && session.user.role === "admin" ? children : null;
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **session চেক করে ইউজার অ্যাডমিন কিনা সেটা যাচাই করা হয়েছে**  
✅ **যদি অ্যাডমিন না হয় তাহলে হোমপেজে রিডাইরেক্ট করা হবে**  

---

## **📌 ধাপ ৩: Admin Panel (Secure Route) তৈরি করা**  

📁 **pages/admin/index.js** ফাইল তৈরি করো:

```js
import AdminRoute from "@/components/AdminRoute";

export default function AdminDashboard() {
  return (
    <AdminRoute>
      <div className="max-w-2xl mx-auto mt-10">
        <h1 className="text-3xl font-bold">Admin Dashboard</h1>
        <p>Only admin can access this page.</p>
      </div>
    </AdminRoute>
  );
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **AdminRoute ব্যবহার করা হয়েছে, তাই শুধু অ্যাডমিনরাই পেজটি দেখতে পারবে**  

---

## **📌 ধাপ ৪: Navbar-এ Dashboard Link যুক্ত করা**  

📁 **components/Header.js** ফাইল আপডেট করো:

```js
import Link from "next/link";
import { useSession } from "next-auth/react";

const Header = () => {
  const { data: session } = useSession();

  return (
    <header className="bg-blue-600 text-white py-4">
      <div className="container mx-auto flex justify-between items-center px-4">
        <Link href="/">
          <h1 className="text-2xl font-bold cursor-pointer">My Blog</h1>
        </Link>
        <nav>
          <ul className="flex gap-4">
            <li><Link href="/" className="hover:underline">Home</Link></li>
            <li><Link href="/blog" className="hover:underline">Blog</Link></li>
            {session && <li><Link href="/dashboard" className="hover:underline">Dashboard</Link></li>}
            {!session ? (
              <li><Link href="/auth/login" className="hover:underline">Login</Link></li>
            ) : (
              <li><button onClick={() => signOut()} className="hover:underline">Logout</button></li>
            )}
          </ul>
        </nav>
      </div>
    </header>
  );
};

export default Header;
```

🔹 **কোড ব্যাখ্যা:**  
✅ **যদি ইউজার লগিন করা থাকে, তাহলে "Dashboard" দেখাবে**  
✅ **যদি ইউজার লগিন করা না থাকে, তাহলে "Login" দেখাবে**  

---

## **📌 ধাপ ৫: API Route Middleware দিয়ে API Secure করা**  

📁 **pages/api/admin/protected.js** ফাইল তৈরি করো:

```js
import { getSession } from "next-auth/react";

export default async function handler(req, res) {
  const session = await getSession({ req });

  if (!session || session.user.role !== "admin") {
    return res.status(403).json({ error: "Access denied" });
  }

  res.status(200).json({ message: "Welcome, Admin!" });
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **getSession() দিয়ে API-তে ইউজার চেক করা হয়েছে**  
✅ **শুধু "admin" রোল থাকলে API এক্সেস পাবে**  

---

## **📌 চূড়ান্ত ফলাফল**  
✅ **http://localhost:3000/dashboard** 👉 লগিন ইউজার দেখবে  
✅ **http://localhost:3000/admin** 👉 কেবল অ্যাডমিন দেখবে  
✅ **Navbar-এ "Dashboard" লিংক থাকবে (লগিন করা থাকলে)**  
✅ **API Route Middleware দিয়ে API Secure করা হয়েছে**  

---

# **পর্ব ৬: Admin Panel (Post Management) তৈরি করা**  

এই পর্বে আমরা **Admin Panel** থেকে ব্লগ পোস্ট **Create, Update, Delete** করতে পারবো। আমাদের লক্ষ্য:  
✅ **Admin Dashboard-এ Blog List দেখানো**  
✅ **New Blog Create করা**  
✅ **Blog Edit & Delete করা**  
✅ **Published/Unpublished Status ম্যানেজ করা**  

---

## **📌 ধাপ ১: Admin Dashboard-এ Blog List দেখানো**  

📁 **pages/admin/blogs.js** ফাইল তৈরি করো:

```js
import AdminRoute from "@/components/AdminRoute";
import { useEffect, useState } from "react";

export default function ManageBlogs() {
  const [blogs, setBlogs] = useState([]);

  useEffect(() => {
    fetch("/api/blog")
      .then((res) => res.json())
      .then((data) => setBlogs(data));
  }, []);

  return (
    <AdminRoute>
      <div className="max-w-4xl mx-auto mt-10">
        <h1 className="text-3xl font-bold">Manage Blogs</h1>
        <table className="w-full mt-4 border-collapse border border-gray-300">
          <thead>
            <tr className="bg-gray-200">
              <th className="border p-2">Title</th>
              <th className="border p-2">Status</th>
              <th className="border p-2">Actions</th>
            </tr>
          </thead>
          <tbody>
            {blogs.map((blog) => (
              <tr key={blog.id} className="border">
                <td className="border p-2">{blog.title}</td>
                <td className="border p-2">
                  {blog.published ? "Published" : "Unpublished"}
                </td>
                <td className="border p-2">
                  <button className="text-blue-500 mr-2">Edit</button>
                  <button className="text-red-500">Delete</button>
                </td>
              </tr>
            ))}
          </tbody>
        </table>
      </div>
    </AdminRoute>
  );
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **Admin Dashboard থেকে Blog List দেখানো হয়েছে**  
✅ **Published/Unpublished Status দেখা যাবে**  
✅ **Edit & Delete অপশন যোগ করা হয়েছে**  

---

## **📌 ধাপ ২: Blog Create ফর্ম তৈরি করা**  

📁 **pages/admin/create.js** ফাইল তৈরি করো:

```js
import AdminRoute from "@/components/AdminRoute";
import { useState } from "react";
import { useRouter } from "next/router";

export default function CreateBlog() {
  const [form, setForm] = useState({ title: "", content: "", categoryId: "" });
  const [error, setError] = useState("");
  const router = useRouter();

  const handleSubmit = async (e) => {
    e.preventDefault();
    const res = await fetch("/api/blog/create", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(form),
    });

    const data = await res.json();
    if (!res.ok) return setError(data.error);
    router.push("/admin/blogs");
  };

  return (
    <AdminRoute>
      <div className="max-w-2xl mx-auto mt-10">
        <h1 className="text-3xl font-bold">Create New Blog</h1>
        {error && <p className="text-red-500">{error}</p>}
        <form onSubmit={handleSubmit} className="space-y-4">
          <input
            type="text"
            placeholder="Title"
            className="w-full p-2 border"
            onChange={(e) => setForm({ ...form, title: e.target.value })}
          />
          <textarea
            placeholder="Content"
            className="w-full p-2 border"
            onChange={(e) => setForm({ ...form, content: e.target.value })}
          />
          <button type="submit" className="bg-blue-600 text-white p-2 w-full">
            Create
          </button>
        </form>
      </div>
    </AdminRoute>
  );
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **Admin Only Route ব্যবহার করা হয়েছে**  
✅ **নতুন Blog Create করার জন্য ফর্ম যুক্ত করা হয়েছে**  
✅ **Submit করলে ব্লগ Admin Dashboard-এ দেখাবে**  

---

## **📌 ধাপ ৩: Blog Delete API তৈরি করা**  

📁 **pages/api/blog/delete.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "DELETE") return res.status(405).json({ error: "Method not allowed" });

  const { id } = req.body;

  try {
    await prisma.blog.delete({ where: { id } });
    res.status(200).json({ message: "Blog deleted successfully" });
  } catch (error) {
    res.status(500).json({ error: "Server Error" });
  }
}
```

🔹 **কোড ব্যাখ্যা:**  
✅ **Admin যদি কোনো Blog Delete করতে চায়, তাহলে এটি API-তে পাঠাবে**  
✅ **Prisma ORM দিয়ে ডাটাবেস থেকে Blog Delete করা হচ্ছে**  

---

## **📌 ধাপ ৪: Admin Panel থেকে Blog Delete করা**  

📁 **pages/admin/blogs.js** ফাইল আপডেট করো:

```js
const handleDelete = async (id) => {
  if (confirm("Are you sure you want to delete this blog?")) {
    await fetch("/api/blog/delete", {
      method: "DELETE",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ id }),
    });

    setBlogs(blogs.filter((blog) => blog.id !== id));
  }
};
```

🔹 **কোড ব্যাখ্যা:**  
✅ **Delete বাটনে ক্লিক করলে ব্লগ মুছে যাবে**  
✅ **confirm() দিয়ে ইউজারকে নিশ্চিত করা হচ্ছে**  

---

## **📌 ধাপ ৫: Blog Edit API তৈরি করা**  

📁 **pages/api/blog/update.js** ফাইল তৈরি করো:

```js
import { PrismaClient } from "@prisma/client";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  if (req.method !== "PUT") return res.status(405).json({ error: "Method not allowed" });

  const { id, title, content } = req.body;

  try {
    const updatedBlog = await prisma.blog.update({
      where: { id },
      data: { title, content },
    });

    res.status(200).json(updatedBlog);
  } catch (error) {
    res.status(500).json({ error: "Server Error" });
  }
}
```

---

## **📌 ধাপ ৬: Blog Edit ফর্ম তৈরি করা**  

📁 **pages/admin/edit/[id].js** ফাইল তৈরি করো:

```js
import { useState, useEffect } from "react";
import { useRouter } from "next/router";

export default function EditBlog() {
  const router = useRouter();
  const { id } = router.query;
  const [form, setForm] = useState({ title: "", content: "" });

  useEffect(() => {
    if (id) {
      fetch(`/api/blog/${id}`)
        .then((res) => res.json())
        .then((data) => setForm({ title: data.title, content: data.content }));
    }
  }, [id]);

  const handleSubmit = async (e) => {
    e.preventDefault();
    await fetch("/api/blog/update", {
      method: "PUT",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({ id, ...form }),
    });

    router.push("/admin/blogs");
  };

  return (
    <form onSubmit={handleSubmit}>
      <input type="text" value={form.title} onChange={(e) => setForm({ ...form, title: e.target.value })} />
      <textarea value={form.content} onChange={(e) => setForm({ ...form, content: e.target.value })} />
      <button type="submit">Update</button>
    </form>
  );
}
```

---

# **পর্ব ৭: Final Deployment & Performance Optimization**  

এই পর্বে আমরা **Next.js Blog CMS**-এর **Deployment ও Performance Optimization** করবো। আমাদের লক্ষ্য:  
✅ **Vercel-এ Next.js ব্লগ ডেপ্লয় করা**  
✅ **PostgreSQL ডাটাবেস হোস্টিং করা**  
✅ **Image Optimization করা**  
✅ **Caching ও Performance Boost করা**  

---

## **📌 ধাপ ১: Vercel-এ ডেপ্লয়মেন্ট সেটআপ করা**  

### **👉 ১. Vercel CLI ইন্সটল করা**  
```bash
npm install -g vercel
```

### **👉 ২. Vercel অ্যাকাউন্ট লগিন করা**  
```bash
vercel login
```

### **👉 ৩. প্রজেক্ট ডেপ্লয় করা**  
```bash
vercel
```
এটি কিছু প্রশ্ন করবে, সব **ডিফল্ট অপশন** রেখে **Enter** প্রেস করো।

---

## **📌 ধাপ ২: PostgreSQL হোস্টিং (Supabase / Railway)**  

### **👉 Supabase ব্যবহার করে PostgreSQL সেটআপ করা**  
1. [Supabase](https://supabase.com/) ওয়েবসাইটে গিয়ে **Sign Up** করো  
2. **New Project > Database Settings**-এ গিয়ে **PostgreSQL URL** কপি করো  
3. `.env` ফাইল আপডেট করো:  

```env
DATABASE_URL="postgresql://your_user:your_password@your_host:5432/your_database"
```

4. Prisma Schema push করো:
```bash
npx prisma db push
```

---

## **📌 ধাপ ৩: Image Optimization (Next.js Built-in Feature)**  

Next.js-এর **next/image** ব্যবহার করে **Lazy Loading ও Optimization** করবো।

📁 **pages/index.js** ফাইল আপডেট করো:

```js
import Image from "next/image";

export default function Home() {
  return (
    <div>
      <h1>My Blog</h1>
      <Image src="/blog-image.jpg" width={800} height={500} alt="Blog Image" />
    </div>
  );
}
```

✅ **Next.js নিজে থেকেই ছবিকে WebP ফরম্যাটে কনভার্ট করে পারফরম্যান্স বুস্ট করবে।**  

---

## **📌 ধাপ ৪: API Caching & Performance Boost**  

📁 **pages/api/blog/index.js** ফাইল আপডেট করো:

```js
import { PrismaClient } from "@prisma/client";

const prisma = new PrismaClient();

export default async function handler(req, res) {
  res.setHeader("Cache-Control", "s-maxage=60, stale-while-revalidate");

  try {
    const blogs = await prisma.blog.findMany({
      include: { author: true, category: true },
    });

    res.status(200).json(blogs);
  } catch (error) {
    res.status(500).json({ error: "Server Error" });
  }
}
```

✅ **এই কোডটি 60 সেকেন্ডের জন্য API ক্যাশ রাখবে এবং দ্রুত লোড হবে।**  

---

## **📌 ধাপ ৫: Vercel-এ Environment Variables সেট করা**  

1. **Vercel Dashboard**-এ গিয়ে প্রজেক্ট সিলেক্ট করো  
2. **Settings > Environment Variables**-এ গিয়ে `.env` ফাইলের ভ্যারিয়েবলগুলো যোগ করো  
3. **Redeploy করো:**  
```bash
vercel --prod
```

---

## **📌 পরবর্তী ধাপ: Continuous Deployment (CI/CD) & Final Review**  

✅ **Continuous Deployment (GitHub Auto Deploy)**  
✅ **Security & Final Testing**  

🚀 **আমরা কি ফাইনাল রিভিউ ও অটো ডেপ্লয়মেন্ট সেটআপে যাবো? নাকি কোনো প্রশ্ন আছে?**



# **পর্ব ৮: Continuous Deployment (CI/CD), Final Review & Security Best Practices**

এখন আমাদের ব্লগ CMS প্রায় প্রস্তুত। এই পর্বে আমরা করবো:  
✅ **GitHub রিপোজিটরি কানেক্ট করে Continuous Deployment (CI/CD)**  
✅ **Final Review – কি কি আছে, কি কি করা হয়েছে**  
✅ **Security Best Practices যোগ করা**  
✅ **Production Checklist ফলো করা**

---

## ✅ **ধাপ ১: GitHub Repo + Vercel Continuous Deployment (CI/CD)**

### 🔹 ১. GitHub Repo তৈরি করো
1. [GitHub](https://github.com/) এ গিয়ে একটি **new repository** তৈরি করো, যেমন `my-blog-cms`
2. টার্মিনালে প্রজেক্টে গিয়ে Git ইনিশিয়ালাইজ করো:
```bash
git init
git remote add origin https://github.com/yourusername/my-blog-cms.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

### 🔹 ২. Vercel-এ GitHub Repo কানেক্ট করো
1. **Vercel Dashboard > Add New Project**  
2. GitHub Repo সিলেক্ট করো  
3. **Environment Variables** যোগ করো (যেমন `DATABASE_URL`, `NEXTAUTH_SECRET`)  
4. **Deploy** বাটন প্রেস করো

👉 এরপর থেকে **যখনই GitHub-এ push করবে, Vercel অটো ডেপ্লয় করবে!** 🚀

---

## ✅ **ধাপ ২: Final Feature Checklist (Recap)**

| ফিচার | স্টেটাস |
|-------|---------|
| ✅ Blog Title, Slug, Content | Done |
| ✅ Meta Title, Description, Index/No Index | Done |
| ✅ Blog Category | Done |
| ✅ Blog Details Page | Done |
| ✅ Author Bio, Created At | Done |
| ✅ Blog Status (Published/Unpublished) | Done |
| ✅ Admin Panel | Done |
| ✅ Blog CRUD (Create, Edit, Delete) | Done |
| ✅ User Roles: Admin/User | Done |
| ✅ Login/Register with NextAuth | Done |
| ✅ Secure API Routes | Done |
| ✅ SEO & Performance Optimizations | Done |
| ✅ Image Optimization | Done |
| ✅ Responsive Layout (TailwindCSS) | Done |
| ✅ Deployment with Vercel | Done |

---

## ✅ **ধাপ ৩: Security Best Practices**

| নিরাপত্তা বিষয় | করণীয় |
|----------------|--------|
| 🔐 Password Hashing | bcryptjs ✅ |
| 🔐 Sensitive API Routes | Session + Role Check ✅ |
| 🔐 Environment Variables | .env & Vercel ENV ✅ |
| 🔐 XSS Protection | content validation (future) |
| 🔐 CSRF Protection | NextAuth handles (✅) |
| 🔐 Admin-Only Routes | AdminRoute.js ✅ |

---

## ✅ **ধাপ ৪: Production Checklist**

- [x] 🔹 `next.config.js` এ image domain allow করা (যদি external image use হয়)
- [x] 🔹 favicon.ico ও SEO meta image অ্যাড করা
- [x] 🔹 canonical URL ব্যবহার করা
- [x] 🔹 Lighthouse দিয়ে Performance, SEO টেস্ট করা
- [x] 🔹 User input validation যোগ করা (future step)
- [x] 🔹 404 & Custom Error Page বানানো (future step)
- [x] 🔹 Sentry / LogRocket দিয়ে Error Monitoring (optional)

---

## ✅ **Bonus: Future Add-ons Ideas**

- 🔄 **WYSIWYG Editor (e.g., TipTap, React Quill)**  
- 🏷️ **Tags System & Tag-based Filtering**  
- 🗃️ **Image Upload (Cloudinary/S3)**  
- 🌍 **Multilingual Support (i18n)**  
- 🔍 **Search Functionality**  
- 📨 **Newsletter Signup**  
- 🧠 **AI Summary for Blogs (OpenAI API)**

---

## ✅ **সবশেষে...**
🎉 **তুমি এখন নিজে নিজেই প্রোফেশনাল Next.js ব্লগ CMS বানাতে পারো!**  
🔥 এটি প্রোডাকশন-রেডি। শুধু কনটেন্ট, ক্যাটাগরি, এবং কিছু polishing করলে লাইভ হয়ে যাবে।

---

### 🚀 তুমি কি এখন এই প্রজেক্টের সোর্স কোড একসাথে চাই?  
নাকি চাই **search, image upload বা WYSIWYG editor** যুক্ত করে আরও অ্যাডভান্স বানাতে?  

বললেই পরবর্তী লেভেলে নিয়ে যাবো! 😎
