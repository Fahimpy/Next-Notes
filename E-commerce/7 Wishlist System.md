চলো ✨ শুরু করি **Step 9: Wishlist + Coupon Codes + Delivery Charge Configuration** — ইউজার একটিভ ফিচারগুলোর একটা দারুণ কম্বো!

---

## ✅ Step 9 Goals:

1. 💖 Wishlist System (LocalStorage)  
2. 🎟️ Coupon Code System (Admin add + Apply on Checkout)  
3. 🚚 Delivery Charge Setup (Admin config + auto add on total)  

---

## 💖 1. Wishlist System (LocalStorage Based)

📁 **lib/wishlist.ts**
```ts
export function getWishlist(): any[] {
  if (typeof window === 'undefined') return []
  const list = localStorage.getItem('wishlist')
  return list ? JSON.parse(list) : []
}

export function toggleWishlist(product: any) {
  let list = getWishlist()
  const exists = list.find((item: any) => item.id === product.id)
  if (exists) {
    list = list.filter((item: any) => item.id !== product.id)
  } else {
    list.push(product)
  }
  localStorage.setItem('wishlist', JSON.stringify(list))
}

export function removeFromWishlist(id: string) {
  const list = getWishlist().filter((item: any) => item.id !== id)
  localStorage.setItem('wishlist', JSON.stringify(list))
}
```

📁 **components/WishlistButton.tsx**
```tsx
'use client'
import { toggleWishlist } from '@/lib/wishlist'
import { useRouter } from 'next/navigation'

export default function WishlistButton({ product }: { product: any }) {
  const router = useRouter()

  return (
    <button onClick={() => {
      toggleWishlist(product)
      alert('Wishlist updated!')
      router.refresh()
    }} className="text-pink-600 underline text-sm mt-2">
      ❤️ Add to Wishlist
    </button>
  )
}
```

📁 **app/wishlist/page.tsx**
```tsx
'use client'
import { getWishlist, removeFromWishlist } from '@/lib/wishlist'
import { useEffect, useState } from 'react'

export default function WishlistPage() {
  const [wishlist, setWishlist] = useState<any[]>([])

  useEffect(() => {
    setWishlist(getWishlist())
  }, [])

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Your Wishlist</h1>
      {wishlist.length === 0 ? <p>No items in wishlist.</p> : (
        <ul className="space-y-2">
          {wishlist.map(item => (
            <li key={item.id} className="flex justify-between border-b py-2">
              <span>{item.title}</span>
              <button onClick={() => {
                removeFromWishlist(item.id)
                setWishlist(getWishlist())
              }} className="text-red-600 text-sm">Remove</button>
            </li>
          ))}
        </ul>
      )}
    </div>
  )
}
```

---

## 🎟️ 2. Coupon Code System

📄 Prisma schema তে অ্যাড করো:

```prisma
model Coupon {
  id        String   @id @default(cuid())
  code      String   @unique
  discount  Float    // percentage e.g. 10 = 10%
  active    Boolean  @default(true)
  createdAt DateTime @default(now())
}
```

```bash
npx prisma migrate dev --name add_coupon
```

---

📁 **app/admin/coupons/page.tsx** – Admin coupon add/list

```tsx
'use client'
import { useEffect, useState } from 'react'

export default function CouponPage() {
  const [coupons, setCoupons] = useState<any[]>([])
  const [code, setCode] = useState('')
  const [discount, setDiscount] = useState(10)

  useEffect(() => {
    fetch('/api/coupons')
      .then(res => res.json())
      .then(data => setCoupons(data.coupons))
  }, [])

  const addCoupon = async () => {
    const res = await fetch('/api/coupons', {
      method: 'POST',
      body: JSON.stringify({ code, discount })
    })
    const { coupon } = await res.json()
    setCoupons([coupon, ...coupons])
    setCode('')
    setDiscount(10)
  }

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Manage Coupons</h1>
      <input value={code} onChange={e => setCode(e.target.value)} placeholder="Code" className="p-2 border" />
      <input type="number" value={discount} onChange={e => setDiscount(+e.target.value)} className="p-2 border" />
      <button onClick={addCoupon} className="bg-green-600 text-white px-4 py-2 rounded">Add</button>

      <ul className="mt-4 space-y-2">
        {coupons.map(c => (
          <li key={c.id} className="border p-2">{c.code} - {c.discount}%</li>
        ))}
      </ul>
    </div>
  )
}
```

📁 **app/api/coupons/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET() {
  const coupons = await prisma.coupon.findMany({ where: { active: true } })
  return NextResponse.json({ coupons })
}

export async function POST(req: Request) {
  const body = await req.json()
  const coupon = await prisma.coupon.create({
    data: {
      code: body.code.toUpperCase(),
      discount: body.discount
    }
  })
  return NextResponse.json({ coupon })
}
```

📁 **app/api/coupons/check/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function POST(req: Request) {
  const { code } = await req.json()
  const coupon = await prisma.coupon.findFirst({
    where: { code: code.toUpperCase(), active: true }
  })

  if (!coupon) {
    return NextResponse.json({ success: false, message: 'Invalid coupon' })
  }

  return NextResponse.json({ success: true, coupon })
}
```

---

📄 **Checkout পেইজে Coupon Input যোগ করো:**

```tsx
const [couponCode, setCouponCode] = useState('')
const [discount, setDiscount] = useState(0)

const applyCoupon = async () => {
  const res = await fetch('/api/coupons/check', {
    method: 'POST',
    body: JSON.stringify({ code: couponCode })
  })
  const data = await res.json()
  if (data.success) {
    setDiscount(data.coupon.discount)
    alert('Coupon applied!')
  } else {
    alert(data.message)
  }
}
```

Total calculate এর সময়:
```tsx
const discounted = total * (1 - discount / 100)
```

---

## 🚚 3. Delivery Charge Setup

📄 Prisma schema এ অ্যাড করো:

```prisma
model Settings {
  id            String  @id @default("site-settings")
  deliveryCharge Float  @default(50)
}
```

```bash
npx prisma migrate dev --name add_delivery_charge
```

📁 **app/api/settings/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET() {
  const settings = await prisma.settings.findUnique({ where: { id: 'site-settings' } })
  return NextResponse.json({ settings })
}

export async function PUT(req: Request) {
  const { deliveryCharge } = await req.json()
  const settings = await prisma.settings.upsert({
    where: { id: 'site-settings' },
    update: { deliveryCharge },
    create: { id: 'site-settings', deliveryCharge }
  })
  return NextResponse.json({ settings })
}
```

📁 **app/admin/settings/page.tsx**
```tsx
'use client'
import { useEffect, useState } from 'react'

export default function SettingsPage() {
  const [deliveryCharge, setDeliveryCharge] = useState(50)

  useEffect(() => {
    fetch('/api/settings')
      .then(res => res.json())
      .then(data => setDeliveryCharge(data.settings.deliveryCharge))
  }, [])

  const update = async () => {
    await fetch('/api/settings', {
      method: 'PUT',
      body: JSON.stringify({ deliveryCharge })
    })
    alert('Updated!')
  }

  return (
    <div>
      <h1 className="text-2xl font-bold mb-4">Delivery Charge Settings</h1>
      <input type="number" value={deliveryCharge} onChange={e => setDeliveryCharge(+e.target.value)} className="p-2 border" />
      <button onClick={update} className="bg-blue-600 text-white px-4 py-2 rounded ml-2">Update</button>
    </div>
  )
}
```

---

## ✅ Final Output of Step 9:

- 💖 Wishlist সিস্টেম যোগ হলো  
- 🎟️ কুপন কোড যোগ করা যাচ্ছে, checkout এ ডিসকাউন্ট হচ্ছে  
- 🚚 Delivery charge admin থেকে কনফিগার করা যাচ্ছে এবং checkout এ যোগ হচ্ছে  

---

## ⏭️ Next Step:

> পারি এখন করতে:
➡️ **Step 10: SEO Tools (Meta Title/Desc Control, robots.txt, sitemap.xml)**

বলো “Step 10 শুরু কর” — তাহলেই SEO সেকশন শুরু করি 😊
