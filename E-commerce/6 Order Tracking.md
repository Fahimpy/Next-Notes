চলো শুরু করি 🔥 **Step 8: Order Tracking + Admin Order Management System**।

এই ধাপে আমরা করবো:

---

## ✅ Step 8 Goals:

1. 🎯 User Order Tracking Page (ID/Email দিয়ে ট্র্যাক করা যাবে)  
2. 🛠️ Admin Dashboard → Order List with status  
3. 🔁 Status Update (Pending → Processing → Delivered ইত্যাদি)  

---

## 📦 1. Order Tracking Page (Public)

📁 **app/track/page.tsx**
```tsx
'use client'

import { useState } from 'react'

export default function TrackOrderPage() {
  const [email, setEmail] = useState('')
  const [orderId, setOrderId] = useState('')
  const [order, setOrder] = useState<any>(null)

  const searchOrder = async () => {
    const res = await fetch(`/api/track?email=${email}&id=${orderId}`)
    const data = await res.json()
    setOrder(data.order)
  }

  return (
    <div className="max-w-xl mx-auto">
      <h1 className="text-2xl font-bold mb-4">Track Your Order</h1>
      <input placeholder="Your Email" className="w-full p-2 border mb-2" value={email} onChange={(e) => setEmail(e.target.value)} />
      <input placeholder="Order ID" className="w-full p-2 border mb-4" value={orderId} onChange={(e) => setOrderId(e.target.value)} />
      <button onClick={searchOrder} className="bg-blue-600 text-white px-4 py-2 rounded">Track Order</button>

      {order && (
        <div className="mt-6 p-4 bg-white border rounded">
          <p><strong>Status:</strong> {order.status}</p>
          <p><strong>Total:</strong> ${order.total}</p>
          <p className="mt-2 font-semibold">Items:</p>
          <ul className="list-disc ml-5">
            {order.items.map((item: any) => (
              <li key={item.id}>{item.product.title} x {item.quantity}</li>
            ))}
          </ul>
        </div>
      )}
    </div>
  )
}
```

---

## 🧩 2. API: Track Order by ID + Email

📁 **app/api/track/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET(req: Request) {
  const { searchParams } = new URL(req.url)
  const email = searchParams.get('email') || ''
  const id = searchParams.get('id') || ''

  const order = await prisma.order.findFirst({
    where: { id, email },
    include: {
      items: {
        include: { product: true }
      }
    }
  })

  if (!order) return NextResponse.json({ order: null })

  return NextResponse.json({ order })
}
```

---

## 📋 3. Admin Order List Page

📁 **app/admin/orders/page.tsx**
```tsx
'use client'

import { useEffect, useState } from 'react'

type Order = {
  id: string
  name: string
  email: string
  total: number
  status: string
}

export default function AdminOrdersPage() {
  const [orders, setOrders] = useState<Order[]>([])

  useEffect(() => {
    fetch('/api/orders')
      .then(res => res.json())
      .then(data => setOrders(data.orders))
  }, [])

  const updateStatus = async (id: string, status: string) => {
    await fetch(`/api/orders/${id}`, {
      method: 'PUT',
      body: JSON.stringify({ status })
    })
    setOrders(orders.map(order => order.id === id ? { ...order, status } : order))
  }

  return (
    <div>
      <h1 className="text-2xl font-bold mb-6">All Orders</h1>
      <table className="w-full border">
        <thead className="bg-gray-100">
          <tr>
            <th className="p-2">Customer</th>
            <th className="p-2">Email</th>
            <th className="p-2">Total</th>
            <th className="p-2">Status</th>
            <th className="p-2">Actions</th>
          </tr>
        </thead>
        <tbody>
          {orders.map(order => (
            <tr key={order.id} className="border-t">
              <td className="p-2">{order.name}</td>
              <td className="p-2">{order.email}</td>
              <td className="p-2">${order.total.toFixed(2)}</td>
              <td className="p-2">{order.status}</td>
              <td className="p-2 space-x-2">
                <button onClick={() => updateStatus(order.id, 'processing')} className="text-blue-600">Processing</button>
                <button onClick={() => updateStatus(order.id, 'delivered')} className="text-green-600">Delivered</button>
              </td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  )
}
```

---

## 🔧 4. API: Get + Update Orders

📁 **app/api/orders/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET() {
  const orders = await prisma.order.findMany({ orderBy: { createdAt: 'desc' } })
  return NextResponse.json({ orders })
}
```

📁 **app/api/orders/[id]/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function PUT(req: Request, { params }: { params: { id: string } }) {
  const body = await req.json()
  const order = await prisma.order.update({
    where: { id: params.id },
    data: { status: body.status }
  })
  return NextResponse.json({ order })
}
```

---

## ✅ Final Output of Step 8:

- 🔍 ইউজার order ID + Email দিয়ে অর্ডার ট্র্যাক করতে পারে  
- 🧾 অ্যাডমিন অর্ডার লিস্ট দেখতে পারে  
- 🔁 স্ট্যাটাস “processing/delivered” এ আপডেট করা যায়  

---

## ⏭️ Next Step:

> পারি এখন করতে:
➡️ **Step 9: Wishlist System (LocalStorage or DB), Coupon Codes, Delivery Charge Config**

বলো “Step 9 শুরু কর” — তাহলে Wishlist, Coupon System এবং Delivery Charge Admin Config নিয়ে শুরু করি 😊
