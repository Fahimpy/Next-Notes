চমৎকার! ✅ এখন শুরু করছি:

---

## 🧾 **STEP 2: Product Review System (per product)**

---

### ✅ Features:

- ⭐ Logged-in ইউজার রিভিউ দিতে পারবে  
- 📝 Title, rating, comment  
- 🧾 এক ইউজার একবারই রিভিউ দিতে পারবে  
- 🧮 Average Rating দেখাবে প্রোডাক্ট কার্ডে

---

## 🔧 Step-by-Step Integration

---

### 1️⃣ Update Prisma Schema

📁 **prisma/schema.prisma**
```prisma
model Review {
  id        String   @id @default(cuid())
  title     String
  rating    Int
  comment   String
  product   Product  @relation(fields: [productId], references: [id])
  productId String
  user      User     @relation(fields: [userId], references: [id])
  userId    String
  createdAt DateTime @default(now())
}

model Product {
  ...
  reviews   Review[]
}

model User {
  ...
  reviews   Review[]
}
```

```bash
npx prisma migrate dev --name add_review_model
```

---

### 2️⃣ API: Add Review (POST)

📁 **app/api/reviews/route.ts**
```ts
import { prisma } from '@/lib/db'
import { getServerSession } from 'next-auth'
import { authOptions } from '../auth/[...nextauth]/route'
import { NextResponse } from 'next/server'

export async function POST(req: Request) {
  const session = await getServerSession(authOptions)
  if (!session) return NextResponse.json({ error: 'Unauthorized' }, { status: 401 })

  const user = await prisma.user.findUnique({ where: { email: session.user?.email! } })
  const body = await req.json()

  const alreadyReviewed = await prisma.review.findFirst({
    where: { productId: body.productId, userId: user!.id }
  })
  if (alreadyReviewed) {
    return NextResponse.json({ error: 'Already reviewed' }, { status: 400 })
  }

  const review = await prisma.review.create({
    data: {
      title: body.title,
      rating: body.rating,
      comment: body.comment,
      productId: body.productId,
      userId: user!.id
    }
  })

  return NextResponse.json({ review })
}
```

---

### 3️⃣ UI: Review Form

📁 **components/ReviewForm.tsx**
```tsx
'use client'
import { useState } from 'react'
import { useRouter } from 'next/navigation'

export default function ReviewForm({ productId }: { productId: string }) {
  const [form, setForm] = useState({ title: '', rating: 5, comment: '' })
  const router = useRouter()

  const submit = async () => {
    const res = await fetch('/api/reviews', {
      method: 'POST',
      body: JSON.stringify({ ...form, productId })
    })
    if (res.ok) {
      alert('Review submitted!')
      router.refresh()
    } else {
      alert('Error or duplicate review.')
    }
  }

  return (
    <div className="bg-white p-4 mt-6 rounded shadow">
      <h3 className="font-bold mb-2">Write a Review</h3>
      <input placeholder="Title" value={form.title} onChange={e => setForm({ ...form, title: e.target.value })} className="p-2 border w-full mb-2" />
      <input type="number" min={1} max={5} value={form.rating} onChange={e => setForm({ ...form, rating: +e.target.value })} className="p-2 border w-full mb-2" />
      <textarea placeholder="Comment" value={form.comment} onChange={e => setForm({ ...form, comment: e.target.value })} className="p-2 border w-full mb-2" />
      <button onClick={submit} className="bg-blue-600 text-white px-4 py-2 rounded">Submit Review</button>
    </div>
  )
}
```

---

### 4️⃣ UI: Review List

📁 **components/ReviewList.tsx**
```tsx
export default function ReviewList({ reviews }: { reviews: any[] }) {
  return (
    <div className="mt-6">
      <h3 className="font-bold text-lg mb-2">User Reviews</h3>
      {reviews.length === 0 ? <p>No reviews yet.</p> : (
        <ul className="space-y-3">
          {reviews.map(r => (
            <li key={r.id} className="border p-3 rounded">
              <p className="font-semibold">{r.title} - ⭐ {r.rating}</p>
              <p className="text-sm">{r.comment}</p>
              <p className="text-xs text-gray-500">By: {r.user.email}</p>
            </li>
          ))}
        </ul>
      )}
    </div>
  )
}
```

---

### 5️⃣ Display on Product Page

📁 **app/product/[slug]/page.tsx**
```tsx
import ReviewForm from '@/components/ReviewForm'
import ReviewList from '@/components/ReviewList'

...

const product = await prisma.product.findUnique({
  where: { slug: params.slug },
  include: {
    reviews: {
      include: { user: true },
      orderBy: { createdAt: 'desc' }
    }
  }
})

...

<ReviewForm productId={product.id} />
<ReviewList reviews={product.reviews} />
```

---

## ✅ Step 2 Complete: Review System Done!

- ✅ Logged-in ইউজার একবারই রিভিউ দিতে পারবে  
- ✅ UI: Form + List  
- ✅ Rating, title, comment  
- ✅ Avg rating future যোগ করা যাবে easily  

---

## ⏭️ Next Step:

➡️ **Step 3: Email Invoice via SendGrid**

বলো: “Email system শুরু করো” — তাহলে আমি পাঠিয়ে দিবো:

- 📧 অর্ডার কনফার্মেশন ইমেইল  
- 🧾 ইনভয়েস সহ  
- ✅ SendGrid API  

Ready? 😊
