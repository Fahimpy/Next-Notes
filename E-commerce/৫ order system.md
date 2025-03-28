🔥 চলো শুরু করি **Step 7: Add to Cart + Checkout + Order Save System** — গেস্ট ইউজার হিসেবেও অর্ডার করা যাবে!

---

## ✅ Step 7 Goals:

1. 🛒 LocalStorage-based Cart System (Guest-friendly)  
2. ✅ Checkout Page with Customer Info  
3. 💾 Save Order + OrderItems to Database  
4. 🎉 Order Success Message  

---

## 🧱 1. Cart System (LocalStorage)

📁 **lib/cart.ts** (Utility functions for cart management)

```ts
export function getCart(): any[] {
  if (typeof window === 'undefined') return []
  const cart = localStorage.getItem('cart')
  return cart ? JSON.parse(cart) : []
}

export function addToCart(product: any) {
  const cart = getCart()
  const existing = cart.find((item: any) => item.id === product.id)
  if (existing) {
    existing.quantity += 1
  } else {
    cart.push({ ...product, quantity: 1 })
  }
  localStorage.setItem('cart', JSON.stringify(cart))
}

export function removeFromCart(id: string) {
  const cart = getCart().filter((item: any) => item.id !== id)
  localStorage.setItem('cart', JSON.stringify(cart))
}

export function clearCart() {
  localStorage.removeItem('cart')
}
```

---

## 🖱️ 2. Add to Cart Button

📁 **components/AddToCartButton.tsx**
```tsx
'use client'
import { addToCart } from '@/lib/cart'
import { useRouter } from 'next/navigation'

export default function AddToCartButton({ product }: { product: any }) {
  const router = useRouter()

  return (
    <button
      onClick={() => {
        addToCart(product)
        alert('Added to cart!')
        router.refresh()
      }}
      className="bg-blue-600 text-white px-4 py-2 rounded mt-2"
    >
      Add to Cart
    </button>
  )
}
```

---

## 🛒 3. Cart Page UI

📁 **app/cart/page.tsx**
```tsx
'use client'
import { getCart, removeFromCart } from '@/lib/cart'
import { useEffect, useState } from 'react'
import Link from 'next/link'

export default function CartPage() {
  const [cart, setCart] = useState<any[]>([])

  useEffect(() => {
    setCart(getCart())
  }, [])

  const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0)

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Your Cart</h1>
      {cart.length === 0 ? (
        <p>Your cart is empty.</p>
      ) : (
        <>
          <ul className="space-y-2 mb-4">
            {cart.map(item => (
              <li key={item.id} className="flex justify-between border-b p-2">
                <span>{item.title} x {item.quantity}</span>
                <span>${(item.price * item.quantity).toFixed(2)}</span>
                <button onClick={() => {
                  removeFromCart(item.id)
                  setCart(getCart())
                }} className="text-red-600 text-sm">Remove</button>
              </li>
            ))}
          </ul>
          <p className="text-lg font-semibold">Total: ${total.toFixed(2)}</p>
          <Link href="/checkout" className="inline-block mt-4 bg-green-600 text-white px-4 py-2 rounded">Checkout</Link>
        </>
      )}
    </div>
  )
}
```

---

## 🧾 4. Checkout Page UI

📁 **app/checkout/page.tsx**
```tsx
'use client'
import { getCart, clearCart } from '@/lib/cart'
import { useState } from 'react'
import { useRouter } from 'next/navigation'

export default function CheckoutPage() {
  const [form, setForm] = useState({ name: '', email: '', phone: '', address: '', city: '' })
  const [message, setMessage] = useState('')
  const router = useRouter()
  const cart = getCart()

  const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0)

  const handleSubmit = async (e: any) => {
    e.preventDefault()
    const res = await fetch('/api/checkout', {
      method: 'POST',
      body: JSON.stringify({ ...form, items: cart, total }),
    })
    if (res.ok) {
      clearCart()
      setMessage('Order placed successfully!')
      router.push('/')
    }
  }

  return (
    <div className="max-w-xl mx-auto">
      <h1 className="text-2xl font-bold mb-4">Checkout</h1>
      <form onSubmit={handleSubmit} className="space-y-4">
        <input required placeholder="Name" className="p-2 border w-full" value={form.name} onChange={e => setForm({ ...form, name: e.target.value })} />
        <input required placeholder="Email" className="p-2 border w-full" value={form.email} onChange={e => setForm({ ...form, email: e.target.value })} />
        <input required placeholder="Phone" className="p-2 border w-full" value={form.phone} onChange={e => setForm({ ...form, phone: e.target.value })} />
        <input required placeholder="Address" className="p-2 border w-full" value={form.address} onChange={e => setForm({ ...form, address: e.target.value })} />
        <input required placeholder="City" className="p-2 border w-full" value={form.city} onChange={e => setForm({ ...form, city: e.target.value })} />
        <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded">Place Order</button>
      </form>
      {message && <p className="mt-4 text-green-600">{message}</p>}
    </div>
  )
}
```

---

## 📦 5. Checkout API Route

📁 **app/api/checkout/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function POST(req: Request) {
  const body = await req.json()
  const { name, email, phone, address, city, items, total } = body

  const order = await prisma.order.create({
    data: {
      name, email, phone, address, city, total,
      items: {
        create: items.map((item: any) => ({
          productId: item.id,
          quantity: item.quantity,
          price: item.price
        }))
      }
    }
  })

  return NextResponse.json({ success: true, orderId: order.id })
}
```

---

## ✅ Final Output of Step 7:

- 🛒 Cart সিস্টেম লোকালস্টোরেজে চলে  
- ✅ গেস্ট ইউজার অর্ডার দিতে পারে  
- 📦 অর্ডার ডাটাবেজে সেভ হয়  
- 🎉 সফল অর্ডার মেসেজ / রিডাইরেক্ট হয়  

---

## ⏭️ Next Step:

> পারি এখন করতে:
➡️ **Step 8: Order Tracking + Admin Order View**

এতে থাকবে:
- অর্ডার ট্র্যাকিং পেইজ (অর্ডার আইডি/ইমেইল দিয়ে)
- Admin Dashboard এ Order List  
- Order Status Update system

বলো, "Step 8 শুরু কর" — আমি করে দিবো 😊
