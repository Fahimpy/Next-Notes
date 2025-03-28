🔥 চলো শুরু করি **Step 6: Category Management UI (Add/Edit/Delete)** — যাতে প্রোডাক্ট এড/এডিট করতে পারো dropdown থেকে category select করে। 

এই ধাপে করবো:

---

## ✅ Step 6 Goals:

1. Admin Dashboard এর Category List Page  
2. Category Add Form  
3. Edit/Delete Functionality  
4. Product Add/Edit ফর্মে Category Dropdown  

---

## 📄 1. Category List Page + Add Form

📁 **app/admin/categories/page.tsx**
```tsx
'use client'

import { useEffect, useState } from 'react'

type Category = {
  id: string
  name: string
  slug: string
}

export default function CategoryPage() {
  const [categories, setCategories] = useState<Category[]>([])
  const [name, setName] = useState('')
  const [slug, setSlug] = useState('')

  useEffect(() => {
    fetch('/api/categories')
      .then(res => res.json())
      .then(data => setCategories(data.categories))
  }, [])

  const addCategory = async () => {
    const res = await fetch('/api/categories', {
      method: 'POST',
      body: JSON.stringify({ name, slug })
    })
    if (res.ok) {
      const { category } = await res.json()
      setCategories([category, ...categories])
      setName('')
      setSlug('')
    }
  }

  const deleteCategory = async (id: string) => {
    if (!confirm('Delete this category?')) return
    await fetch(`/api/categories/${id}`, { method: 'DELETE' })
    setCategories(categories.filter(c => c.id !== id))
  }

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Manage Categories</h1>

      <div className="space-x-2 mb-6">
        <input
          placeholder="Category Name"
          className="p-2 border rounded"
          value={name}
          onChange={(e) => setName(e.target.value)}
        />
        <input
          placeholder="Slug"
          className="p-2 border rounded"
          value={slug}
          onChange={(e) => setSlug(e.target.value)}
        />
        <button onClick={addCategory} className="bg-green-600 text-white px-4 py-2 rounded">Add</button>
      </div>

      <ul className="space-y-2">
        {categories.map(cat => (
          <li key={cat.id} className="flex justify-between bg-white p-2 border rounded">
            <span>{cat.name} ({cat.slug})</span>
            <button onClick={() => deleteCategory(cat.id)} className="text-red-600 hover:underline">Delete</button>
          </li>
        ))}
      </ul>
    </div>
  )
}
```

---

## ⚙️ 2. API Routes for Category

📁 **app/api/categories/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET() {
  const categories = await prisma.category.findMany({ orderBy: { createdAt: 'desc' } })
  return NextResponse.json({ categories })
}

export async function POST(req: Request) {
  const body = await req.json()
  const category = await prisma.category.create({
    data: {
      name: body.name,
      slug: body.slug
    }
  })
  return NextResponse.json({ category })
}
```

📁 **app/api/categories/[id]/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function DELETE(_: Request, { params }: { params: { id: string } }) {
  await prisma.category.delete({ where: { id: params.id } })
  return NextResponse.json({ success: true })
}
```

---

## 🔄 3. Update Product Add/Edit Forms: Category Dropdown

### ✏️ Replace this:
```tsx
<input {...register('categoryId')} placeholder="Category ID" className="w-full p-2 border rounded" />
```

### ✅ With this:
```tsx
const [categories, setCategories] = useState<{ id: string, name: string }[]>([])

useEffect(() => {
  fetch('/api/categories')
    .then(res => res.json())
    .then(data => setCategories(data.categories))
}, [])

<select {...register('categoryId')} className="w-full p-2 border rounded">
  <option value="">-- Select Category --</option>
  {categories.map(cat => (
    <option key={cat.id} value={cat.id}>{cat.name}</option>
  ))}
</select>
{errors.categoryId && <p className="text-red-500 text-sm">{errors.categoryId.message}</p>}
```

---

## ✅ Final Output of Step 6:

- Category Add/Delete করা যাচ্ছে  
- প্রোডাক্ট ফর্মে category dropdown ব্যবহার করা যাচ্ছে  
- রিয়েল ডেটা category table থেকে আসছে  

---

## ⏭️ Next Step

আমরা এখন পারি করতে:
➡️ **Step 7: Order System (Add to Cart, Checkout, Save Order)**

> বলো "Step 7 শুরু কর" — আমি করব:
- Guest Cart (LocalStorage)
- Checkout Page UI
- Order DB Save System

Ready? 😊
