চমৎকার! 🧠 এখন বানাই **Admin Dashboard Analytics Chart** — যাতে তুমি সহজে বুঝতে পারো:

- মোট বিক্রি হয়েছে কত 💰  
- কতগুলো অর্ডার হয়েছে 📦  
- কোন প্রোডাক্টগুলো বেস্টসেলিং 📊  
- দিন বা মাস অনুযায়ী গ্রাফ 📈

---

## ✅ Analytics Chart Features

1. 📆 Daily/Monthly Sales (Line Chart)  
2. 💰 Total Revenue  
3. 📦 Total Orders  
4. 🏆 Top Products by Quantity Sold  

---

## 📦 1. Backend API for Dashboard Data

📁 **app/api/admin/analytics/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'
import { startOfMonth } from 'date-fns'

export async function GET() {
  const now = new Date()
  const start = startOfMonth(now)

  const totalOrders = await prisma.order.count()
  const totalRevenue = await prisma.order.aggregate({
    _sum: { total: true }
  })

  const monthlySales = await prisma.order.findMany({
    where: { createdAt: { gte: start } },
    select: { createdAt: true, total: true }
  })

  const topProducts = await prisma.orderItem.groupBy({
    by: ['productId'],
    _sum: { quantity: true },
    orderBy: { _sum: { quantity: 'desc' } },
    take: 5
  })

  const productNames = await prisma.product.findMany({
    where: {
      id: { in: topProducts.map(p => p.productId) }
    }
  })

  return NextResponse.json({
    totalOrders,
    totalRevenue: totalRevenue._sum.total || 0,
    monthlySales,
    topProducts: topProducts.map(p => ({
      name: productNames.find(prod => prod.id === p.productId)?.title || 'Unknown',
      quantity: p._sum.quantity || 0
    }))
  })
}
```

---

## 📊 2. Frontend: Chart.js + Admin Dashboard UI

### 📦 Install Recharts (chart library)

```bash
npm install recharts
```

---

📁 **app/admin/page.tsx**
```tsx
'use client'
import { useEffect, useState } from 'react'
import {
  LineChart, Line, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer,
  BarChart, Bar
} from 'recharts'

export default function AdminDashboard() {
  const [data, setData] = useState<any>(null)

  useEffect(() => {
    fetch('/api/admin/analytics')
      .then(res => res.json())
      .then(setData)
  }, [])

  if (!data) return <p>Loading...</p>

  // Format for chart
  const chartData = data.monthlySales.map((d: any) => ({
    date: new Date(d.createdAt).toLocaleDateString(),
    total: d.total
  }))

  return (
    <div className="space-y-8">
      <h1 className="text-2xl font-bold mb-2">📊 Admin Dashboard</h1>

      <div className="grid grid-cols-1 sm:grid-cols-2 gap-6">
        <div className="bg-white p-4 shadow rounded">
          <h2 className="text-xl font-semibold">Total Revenue</h2>
          <p className="text-2xl mt-2 font-bold text-green-600">${data.totalRevenue.toFixed(2)}</p>
        </div>
        <div className="bg-white p-4 shadow rounded">
          <h2 className="text-xl font-semibold">Total Orders</h2>
          <p className="text-2xl mt-2 font-bold text-blue-600">{data.totalOrders}</p>
        </div>
      </div>

      <div className="bg-white p-4 shadow rounded">
        <h2 className="text-lg font-bold mb-2">📅 Monthly Sales</h2>
        <ResponsiveContainer width="100%" height={300}>
          <LineChart data={chartData}>
            <CartesianGrid strokeDasharray="3 3" />
            <XAxis dataKey="date" />
            <YAxis />
            <Tooltip />
            <Legend />
            <Line type="monotone" dataKey="total" stroke="#8884d8" />
          </LineChart>
        </ResponsiveContainer>
      </div>

      <div className="bg-white p-4 shadow rounded">
        <h2 className="text-lg font-bold mb-2">🏆 Top Products</h2>
        <ResponsiveContainer width="100%" height={300}>
          <BarChart data={data.topProducts}>
            <XAxis dataKey="name" />
            <YAxis />
            <Tooltip />
            <Bar dataKey="quantity" fill="#82ca9d" />
          </BarChart>
        </ResponsiveContainer>
      </div>
    </div>
  )
}
```

---

## ✅ Final Output:

- 💵 Total revenue ও order count মেট্রিক  
- 📈 লাইন গ্রাফে দেখাবে মাসভিত্তিক বিক্রি  
- 📊 বেস্ট সেলিং প্রোডাক্টগুলো বার গ্রাফে  
- 🔄 ডায়নামিক API দিয়ে সব কিছু অটো আপডেটেড  

---

## ⏭️ Next Options:

> এখন পারি শুরু করতে:

- 💅 Final UI polish (Admin light/dark mode, cards)
- 🌐 Deployment to Vercel
- 🧪 Unit + E2E Test
- 🌍 SaaS (multi-shop) extension

তুমি চাইলে এখন আমি Admin Dashboard polish করে দিতে পারি Tailwind UI cards/stats/styling সহ।

বলো: “Admin UI polish করো” বা “Deploy করো” — আমি শুরু করব 🔥
