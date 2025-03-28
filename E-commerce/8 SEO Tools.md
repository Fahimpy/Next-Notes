চমৎকার! এখন শুরু করছি **Step 10: SEO Features – Meta Tags, robots.txt, sitemap.xml** — যাতে তোমার ই-কমার্স সাইট Google সহ সব সার্চ ইঞ্জিনে সঠিকভাবে ইনডেক্স হয়।

---

## ✅ Step 10 Goals:

1. 📌 Product-wise Meta Title + Meta Description সাপোর্ট  
2. 🤖 Dynamic `robots.txt` with control over indexability  
3. 🗺️ Dynamic `sitemap.xml` (auto-update with new pages)

---

## 🧠 1. Dynamic Meta Title + Description per Product

Prisma schema-তে আমরা আগেই রেখেছি:
```prisma
metaTitle     String?
metaDesc      String?
indexable     Boolean    @default(true)
```

📁 **app/product/[slug]/page.tsx**
```tsx
import { prisma } from '@/lib/db'
import { notFound } from 'next/navigation'
import { Metadata } from 'next'

export async function generateMetadata({ params }: { params: { slug: string } }): Promise<Metadata> {
  const product = await prisma.product.findUnique({ where: { slug: params.slug } })
  if (!product) return {}

  return {
    title: product.metaTitle || product.title,
    description: product.metaDesc || product.description.slice(0, 150),
    robots: product.indexable ? 'index, follow' : 'noindex'
  }
}

export default async function ProductPage({ params }: { params: { slug: string } }) {
  const product = await prisma.product.findUnique({ where: { slug: params.slug } })
  if (!product) return notFound()

  return (
    <div className="p-6">
      <h1 className="text-2xl font-bold">{product.title}</h1>
      <p className="mt-2 text-gray-600">{product.description}</p>
    </div>
  )
}
```

✅ এতে প্রতিটি প্রোডাক্টের জন্য আলাদা meta title, description, এবং robots নির্দেশনা যাবে।

---

## 🤖 2. Dynamic robots.txt Setup

📁 **app/robots.txt/route.ts**
```ts
import { NextResponse } from 'next/server'

export async function GET() {
  const content = `
User-agent: *
Allow: /
Sitemap: ${process.env.NEXT_PUBLIC_SITE_URL || 'https://yoursite.com'}/sitemap.xml
`
  return new NextResponse(content, {
    headers: {
      'Content-Type': 'text/plain'
    }
  })
}
```

📁 **next.config.js**
```js
module.exports = {
  async rewrites() {
    return [
      { source: '/robots.txt', destination: '/robots.txt' }
    ]
  }
}
```

📌 URL: `/robots.txt` → স্বয়ংক্রিয় ভাবে serve হবে

---

## 🗺️ 3. Dynamic Sitemap.xml Generation

📁 **app/sitemap.xml/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET() {
  const baseUrl = process.env.NEXT_PUBLIC_SITE_URL || 'https://yoursite.com'
  const products = await prisma.product.findMany({ where: { indexable: true } })

  const productLinks = products.map(p => `
    <url>
      <loc>${baseUrl}/product/${p.slug}</loc>
      <lastmod>${p.createdAt.toISOString()}</lastmod>
    </url>
  `).join('\n')

  const xml = `
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>${baseUrl}</loc>
  </url>
  <url>
    <loc>${baseUrl}/products</loc>
  </url>
  ${productLinks}
</urlset>
  `.trim()

  return new NextResponse(xml, {
    headers: {
      'Content-Type': 'application/xml'
    }
  })
}
```

📌 URL: `/sitemap.xml` → Google, Bing এর জন্য SEO ফ্রেন্ডলি সাইটম্যাপ তৈরি

---

## ✅ Final Output of Step 10:

- ✅ প্রতিটা প্রোডাক্টের জন্য আলাদা meta title/description  
- ❌ Index না করার অপশন (noindex) যুক্ত  
- 🤖 Fully dynamic robots.txt  
- 🗺️ Fully dynamic sitemap.xml — সার্চ ইঞ্জিনে আপডেটেড পেজ পাঠানোর জন্য  

---

## ⏭️ Next Step (Last Phase of Core Features):

> পারি এখন করতে:
➡️ **Step 11: Final Polish – Responsive Layout, Breadcrumbs, Internal Search, Filters, Footer, Videos, Compare, Multi-Payment**

বলো “Step 11 শুরু কর” — তাহলেই আমরা শেষ polish & features phase শুরু করি 🎯😊
