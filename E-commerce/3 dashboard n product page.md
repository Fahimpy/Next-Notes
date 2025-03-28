চমৎকার! এখন আমরা 🎯 **Step 3: Admin Dashboard Interface + Product Add Page** শুরু করছি।

এই ধাপে আমরা করবো:

---

## ✅ Step 3 Goals:

1. Admin Dashboard Layout (Sidebar + Content)  
2. Product Add Page তৈরি (UI form + Tailwind)  
3. Form Validation (React Hook Form + Zod)  
4. API Route: Product DB তে সেভ করবো  
5. সফল সাবমিশন ফিডব্যাক  

---

## 🏗️ 1. Admin Layout তৈরি করা

📁 **app/admin/layout.tsx**
```tsx
export default function AdminLayout({ children }: { children: React.ReactNode }) {
  return (
    <div className="flex min-h-screen">
      <aside className="w-64 bg-gray-900 text-white p-6">
        <h2 className="text-2xl font-bold mb-6">Admin</h2>
        <ul className="space-y-3">
          <li><a href="/admin/products" className="hover:underline">Products</a></li>
          <li><a href="/admin/orders" className="hover:underline">Orders</a></li>
          <li><a href="/admin/settings" className="hover:underline">Settings</a></li>
        </ul>
      </aside>
      <main className="flex-1 p-10 bg-gray-50">{children}</main>
    </div>
  )
}
```

---

## 📄 2. Create Product Add Page UI

📁 **app/admin/products/page.tsx**
```tsx
'use client'
import { useForm } from 'react-hook-form'
import { z } from 'zod'
import { zodResolver } from '@hookform/resolvers/zod'
import { useState } from 'react'

const formSchema = z.object({
  title: z.string().min(2),
  description: z.string().min(10),
  price: z.coerce.number().min(1),
  stock: z.coerce.number().min(0),
  categoryId: z.string().min(1),
  metaTitle: z.string().optional(),
  metaDesc: z.string().optional(),
  indexable: z.boolean().optional()
})

type FormValues = z.infer<typeof formSchema>

export default function ProductPage() {
  const [message, setMessage] = useState('')
  const { register, handleSubmit, formState: { errors } } = useForm<FormValues>({
    resolver: zodResolver(formSchema)
  })

  const onSubmit = async (data: FormValues) => {
    const res = await fetch('/api/products', {
      method: 'POST',
      body: JSON.stringify(data)
    })
    const result = await res.json()
    setMessage(result.message || 'Submitted!')
  }

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Add Product</h1>
      <form onSubmit={handleSubmit(onSubmit)} className="space-y-4 max-w-xl">
        <input {...register('title')} placeholder="Product Title" className="w-full p-2 border rounded" />
        {errors.title && <p className="text-red-500 text-sm">{errors.title.message}</p>}

        <textarea {...register('description')} placeholder="Description" className="w-full p-2 border rounded" />
        {errors.description && <p className="text-red-500 text-sm">{errors.description.message}</p>}

        <input type="number" {...register('price')} placeholder="Price" className="w-full p-2 border rounded" />
        <input type="number" {...register('stock')} placeholder="Stock" className="w-full p-2 border rounded" />

        <input {...register('categoryId')} placeholder="Category ID" className="w-full p-2 border rounded" />

        <input {...register('metaTitle')} placeholder="Meta Title" className="w-full p-2 border rounded" />
        <textarea {...register('metaDesc')} placeholder="Meta Description" className="w-full p-2 border rounded" />

        <label className="flex items-center gap-2">
          <input type="checkbox" {...register('indexable')} />
          Indexable in SEO?
        </label>

        <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">Add Product</button>
      </form>

      {message && <p className="mt-4 text-green-600">{message}</p>}
    </div>
  )
}
```

---

## 🔧 3. API Route to Save Product

📁 **app/api/products/route.ts**
```ts
import { NextResponse } from 'next/server'
import { prisma } from '@/lib/db'

export async function POST(req: Request) {
  try {
    const body = await req.json()
    const product = await prisma.product.create({
      data: {
        title: body.title,
        description: body.description,
        price: body.price,
        stock: body.stock,
        categoryId: body.categoryId,
        metaTitle: body.metaTitle,
        metaDesc: body.metaDesc,
        indexable: body.indexable ?? true,
      }
    })
    return NextResponse.json({ success: true, message: 'Product Added!', product })
  } catch (error) {
    return NextResponse.json({ success: false, message: 'Error Adding Product', error })
  }
}
```

---

## 🧪 4. Test

1. `npx prisma studio` দিয়ে ক্যাটাগরি আইডি দেখে বসাও
2. `/admin/products` গিয়ে প্রোডাক্ট এড করো
3. DB তে ইনসার্ট হয়েছে কিনা চেক করো

---

## ✅ শেষ ফলাফল

তোমার এখন একটি **Fully Working Product Add Page** আছে—with:
- Tailwind UI
- React Hook Form + Zod Validation
- API route
- Prisma insert
- SEO fields + indexable checkbox

---

## ⏭️ Next Step

তোমার অনুমতি পেলে আমরা করবো:
➡️ **Step 4: Product List Page with Filter, Edit, Delete**

> বলো “Step 4 শুরু কর” — আমি তোমার জন্য Product list table, search/filter system, edit/delete UI করে দিবো।

Ready? 😊


চলো তাহলে শুরু করি 🎯 **Step 4: Product List Page with Filter, Edit, Delete**!

এই ধাপে আমরা করবো:

---

## ✅ Step 4 Goals:

1. Admin Dashboard এর Product List Page  
2. Search & Filter by title, category  
3. Edit & Delete Button  
4. Product Edit Page  
5. Delete API route

---

## 🧾 1. Product List Page UI (with Search)

📁 **app/admin/products/page.tsx** (Update করে নিচের কোড বসাও)

```tsx
'use client'

import { useEffect, useState } from 'react'
import Link from 'next/link'

type Product = {
  id: string
  title: string
  price: number
  stock: number
  categoryId: string
}

export default function ProductListPage() {
  const [products, setProducts] = useState<Product[]>([])
  const [search, setSearch] = useState('')

  useEffect(() => {
    fetch('/api/products')
      .then(res => res.json())
      .then(data => setProducts(data.products))
  }, [])

  const filtered = products.filter(p => p.title.toLowerCase().includes(search.toLowerCase()))

  return (
    <div>
      <div className="flex justify-between mb-6">
        <h1 className="text-2xl font-bold">Products</h1>
        <Link href="/admin/products/new" className="bg-green-600 text-white px-4 py-2 rounded">+ Add New</Link>
      </div>

      <input
        type="text"
        placeholder="Search products..."
        className="p-2 mb-4 border rounded w-full max-w-sm"
        value={search}
        onChange={(e) => setSearch(e.target.value)}
      />

      <table className="w-full border text-left">
        <thead className="bg-gray-100">
          <tr>
            <th className="p-2">Title</th>
            <th className="p-2">Price</th>
            <th className="p-2">Stock</th>
            <th className="p-2">Actions</th>
          </tr>
        </thead>
        <tbody>
          {filtered.map(product => (
            <tr key={product.id} className="border-t">
              <td className="p-2">{product.title}</td>
              <td className="p-2">${product.price.toFixed(2)}</td>
              <td className="p-2">{product.stock}</td>
              <td className="p-2 space-x-2">
                <Link href={`/admin/products/edit/${product.id}`} className="text-blue-600 hover:underline">Edit</Link>
                <button onClick={() => handleDelete(product.id)} className="text-red-600 hover:underline">Delete</button>
              </td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  )

  async function handleDelete(id: string) {
    if (!confirm('Are you sure to delete?')) return
    const res = await fetch(`/api/products/${id}`, { method: 'DELETE' })
    if (res.ok) {
      setProducts(products.filter(p => p.id !== id))
    }
  }
}
```

---

## 🔗 2. API Routes: GET + DELETE Products

📁 **app/api/products/route.ts** (Update করে নিচেরটা রাখো)

```ts
import { NextResponse } from 'next/server'
import { prisma } from '@/lib/db'

export async function GET() {
  const products = await prisma.product.findMany({
    orderBy: { createdAt: 'desc' }
  })
  return NextResponse.json({ products })
}

export async function POST(req: Request) {
  try {
    const body = await req.json()
    const product = await prisma.product.create({
      data: {
        title: body.title,
        description: body.description,
        price: body.price,
        stock: body.stock,
        categoryId: body.categoryId,
        metaTitle: body.metaTitle,
        metaDesc: body.metaDesc,
        indexable: body.indexable ?? true,
      }
    })
    return NextResponse.json({ success: true, message: 'Product Added!', product })
  } catch (error) {
    return NextResponse.json({ success: false, message: 'Error Adding Product', error })
  }
}
```

📁 **app/api/products/[id]/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function DELETE(
  req: Request,
  { params }: { params: { id: string } }
) {
  await prisma.product.delete({ where: { id: params.id } })
  return NextResponse.json({ success: true })
}
```

---

## 🛠️ 3. Edit Page Routing (placeholder)

📁 **app/admin/products/edit/[id]/page.tsx**
```tsx
export default function EditProductPage({ params }: { params: { id: string } }) {
  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Edit Product - {params.id}</h1>
      {/* Later: Load existing data + editable form */}
      <p>Edit form will come here.</p>
    </div>
  )
}
```

---

## ✅ Final Output in This Step:

- 🔍 Product list দেখানো
- ✅ Search কাজ করে
- 🗑️ Delete বাটনে ডেটা মুছে যায়
- ✍️ Edit রাউট আছে, এখনো কাজ করা বাকি

---

## ⏭️ Next Step

> বলো "Edit Page বানাও", তাহলেই আমি:
- প্রোডাক্ট লোড করে,
- ফর্ম ফিল্ড প্রি-ফিল করে,
- আপডেট করার কোড দিবো

Edit রেডি করবো কি? 😊

দারুণ! 🎯 এখন শুরু করছি **Step 5: Edit Product Page**।

এই ধাপে করবো:

---

## ✅ Step 5 Goals:

1. ডাটাবেজ থেকে প্রোডাক্ট লোড করা  
2. ফর্ম প্রি-ফিল করা  
3. সাবমিট করলে প্রোডাক্ট আপডেট হবে  
4. সফল মেসেজ দেখানো  

---

## 📄 1. Edit Page with Pre-filled Form

📁 **app/admin/products/edit/[id]/page.tsx**
```tsx
'use client'

import { useEffect, useState } from 'react'
import { useForm } from 'react-hook-form'
import { zodResolver } from '@hookform/resolvers/zod'
import { z } from 'zod'
import { useRouter } from 'next/navigation'

const formSchema = z.object({
  title: z.string().min(2),
  description: z.string().min(10),
  price: z.coerce.number().min(1),
  stock: z.coerce.number().min(0),
  categoryId: z.string().min(1),
  metaTitle: z.string().optional(),
  metaDesc: z.string().optional(),
  indexable: z.boolean().optional()
})

type FormValues = z.infer<typeof formSchema>

export default function EditProductPage({ params }: { params: { id: string } }) {
  const [loading, setLoading] = useState(true)
  const [message, setMessage] = useState('')
  const { register, handleSubmit, reset, formState: { errors } } = useForm<FormValues>({
    resolver: zodResolver(formSchema)
  })

  const router = useRouter()

  useEffect(() => {
    fetch(`/api/products/${params.id}`)
      .then(res => res.json())
      .then(data => {
        reset(data.product)
        setLoading(false)
      })
  }, [params.id, reset])

  const onSubmit = async (data: FormValues) => {
    const res = await fetch(`/api/products/${params.id}`, {
      method: 'PUT',
      body: JSON.stringify(data)
    })
    const result = await res.json()
    setMessage(result.message || 'Updated!')
  }

  if (loading) return <p>Loading...</p>

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Edit Product</h1>
      <form onSubmit={handleSubmit(onSubmit)} className="space-y-4 max-w-xl">
        <input {...register('title')} placeholder="Title" className="w-full p-2 border rounded" />
        {errors.title && <p className="text-red-500 text-sm">{errors.title.message}</p>}

        <textarea {...register('description')} placeholder="Description" className="w-full p-2 border rounded" />
        <input type="number" {...register('price')} placeholder="Price" className="w-full p-2 border rounded" />
        <input type="number" {...register('stock')} placeholder="Stock" className="w-full p-2 border rounded" />
        <input {...register('categoryId')} placeholder="Category ID" className="w-full p-2 border rounded" />
        <input {...register('metaTitle')} placeholder="Meta Title" className="w-full p-2 border rounded" />
        <textarea {...register('metaDesc')} placeholder="Meta Description" className="w-full p-2 border rounded" />

        <label className="flex items-center gap-2">
          <input type="checkbox" {...register('indexable')} />
          Indexable in SEO?
        </label>

        <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">Update Product</button>
      </form>

      {message && <p className="mt-4 text-green-600">{message}</p>}
    </div>
  )
}
```

---

## 🔧 2. API Route: GET + PUT by ID

📁 **app/api/products/[id]/route.ts** (Update with GET + PUT)

```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET(_: Request, { params }: { params: { id: string } }) {
  const product = await prisma.product.findUnique({ where: { id: params.id } })
  return NextResponse.json({ product })
}

export async function PUT(req: Request, { params }: { params: { id: string } }) {
  const body = await req.json()
  const product = await prisma.product.update({
    where: { id: params.id },
    data: {
      title: body.title,
      description: body.description,
      price: body.price,
      stock: body.stock,
      categoryId: body.categoryId,
      metaTitle: body.metaTitle,
      metaDesc: body.metaDesc,
      indexable: body.indexable ?? true,
    }
  })
  return NextResponse.json({ success: true, message: 'Product Updated!', product })
}

export async function DELETE(_: Request, { params }: { params: { id: string } }) {
  await prisma.product.delete({ where: { id: params.id } })
  return NextResponse.json({ success: true })
}
```

---

## ✅ Output of Step 5:

- Product details auto-load হচ্ছে
- ফর্মে প্রি-ফিলড ডেটা দেখায়
- আপডেট করলে ডেটাবেইসে সেভ হয়
- সফল হলে ✅ মেসেজ দেখা যায়

---

## ⏭️ Next Step:

> এখন পারি আমরা শুরু করতে:
➡️ **Step 6: Category Management UI (Add/Edit/Delete)**

যাতে প্রোডাক্ট এড করার সময় category select করা যায় (dropdown + relation)।  
এই স্টেপ শেষ হলে full Product CRUD system complete!

বলো, "Step 6 শুরু কর" – তাহলেই আমি ক্যাটাগরি মডিউল বানানো শুরু করবো 😊
