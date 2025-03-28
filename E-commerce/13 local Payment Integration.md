🔥 চলো শুরু করি **STEP 3: SSLCommerz / bKash Payment Integration** — যাতে তোমার কাস্টমাররা বাংলাদেশি payment gateway দিয়ে অর্ডার করতে পারে!

---

## ✅ তুমি যেটা বলেছিলে:

- ✅ **bKash** বা **SSLCommerz** চাই  
- 🎯 আমরা এখন শুরু করছি **SSLCommerz Integration** (easiest + widely used)  
- Future এ bKash API or hosted flow-ও অ্যাড করা যাবে।

---

## 🧩 Step-by-Step Integration Plan:

1. 🛠️ SSLCommerz Sandbox credentials নিয়ে `.env` ফাইলে রাখা  
2. 🔐 Checkout API route → Redirects to SSLCommerz  
3. ✅ Success/Fail Callback routes handle করে DB update  
4. 🧾 Order status update → "Paid"  
5. 🧪 Test with sandbox environment

---

## 🔐 1. Sandbox Credentials (You need to create sandbox account)

- Go to: https://developer.sslcommerz.com
- Create account → Get:
  - `store_id`
  - `store_passwd`

📁 **.env**
```env
SSLCZ_STORE_ID=your_store_id
SSLCZ_STORE_PASSWD=your_password
NEXT_PUBLIC_SITE_URL=http://localhost:3000
```

---

## 🔧 2. Payment Initialization API

📁 **app/api/pay/route.ts**
```ts
import { NextResponse } from 'next/server'

export async function POST(req: Request) {
  const body = await req.json()
  const orderId = body.orderId
  const amount = body.amount

  const data = {
    store_id: process.env.SSLCZ_STORE_ID!,
    store_passwd: process.env.SSLCZ_STORE_PASSWD!,
    total_amount: amount,
    currency: 'BDT',
    tran_id: orderId,
    success_url: `${process.env.NEXT_PUBLIC_SITE_URL}/api/pay/success?orderId=${orderId}`,
    fail_url: `${process.env.NEXT_PUBLIC_SITE_URL}/api/pay/fail`,
    cancel_url: `${process.env.NEXT_PUBLIC_SITE_URL}/api/pay/cancel`,
    emi_option: 0,
    cus_name: body.name,
    cus_email: body.email,
    cus_phone: body.phone,
    cus_add1: body.address,
    cus_city: body.city,
    shipping_method: 'Courier',
    product_name: 'Ecommerce Order',
    product_category: 'General',
    product_profile: 'general',
  }

  const res = await fetch('https://sandbox.sslcommerz.com/gwprocess/v4/api.php', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(data)
  })

  const responseData = await res.json()
  return NextResponse.json({ url: responseData.GatewayPageURL })
}
```

---

## 🟢 3. Checkout Page থেকে Call

📁 **app/checkout/page.tsx**
```tsx
const initiateSSLPayment = async (orderId: string, total: number) => {
  const res = await fetch('/api/pay', {
    method: 'POST',
    body: JSON.stringify({ orderId, amount: total, ...form })
  })
  const { url } = await res.json()
  window.location.href = url
}
```

Checkout Submit এ:
```tsx
const res = await fetch('/api/checkout', { method: 'POST', body: JSON.stringify({ ...form, items: cart, total }) })
const { orderId } = await res.json()
await initiateSSLPayment(orderId, total)
```

---

## 🟢 4. Success Callback Route

📁 **app/api/pay/success/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET(req: Request) {
  const { searchParams } = new URL(req.url)
  const orderId = searchParams.get('orderId') || ''

  await prisma.order.update({
    where: { id: orderId },
    data: { status: 'paid' }
  })

  return NextResponse.redirect(`${process.env.NEXT_PUBLIC_SITE_URL}/thank-you`)
}
```

---

## ✅ 5. Final Output:

- ✅ Payment goes to SSLCommerz Gateway  
- ✅ Success এ অর্ডার “paid” হিসেবে mark  
- ✅ Order redirect হয় Thank You page এ  
- 🧪 Tested with sandbox  

---

## 🧪 Test with Sandbox Card:

- Use sandbox card from: https://developer.sslcommerz.com/docs/test-credentials/

---

## ⏭️ Next Step:

> এখন পারি:
➡️ **STEP 4: User Login/Register System (with NextAuth)**

বলো “NextAuth শুরু করো” — আমি করব:

- Signup/Login Pages  
- User Session  
- Wishlist, Order History user-wise  
- Admin role support  

Ready? 😊

চল দেই! 🚀  
এখন করছি **bKash Payment Integration** – বাংলাদেশি কাস্টমারদের জন্য সবচেয়ে চাওয়া ফিচার ✅

---

## ✅ GOAL:

- 🔐 bKash Hosted Checkout (redirect flow)  
- 💳 ইউজার redirect হবে bKash পেমেন্ট গেটওয়েতে  
- 🎯 পেমেন্ট success হলে order “paid” হিসেবে mark হবে  
- 🧪 Sandbox এ কাজ করবে, Live করতে চাইলে শুধু credentials change

---

## 🧩 Step-by-Step bKash Integration (Hosted Checkout):

---

## 1️⃣ Get bKash Sandbox Credentials

Signup here → https://developer.bka.sh/

You'll get:
- `app_key`
- `app_secret`
- `username`
- `password`

📁 **.env**
```env
BKASH_USERNAME=sandbox@bkash.com
BKASH_PASSWORD=sandboxpass
BKASH_APP_KEY=sandbox_key
BKASH_APP_SECRET=sandbox_secret
BKASH_BASE_URL=https://tokenized.sandbox.bka.sh
```

---

## 2️⃣ Create API: `/api/bkash/token`

📁 **app/api/bkash/token/route.ts**
```ts
import { NextResponse } from 'next/server'

export async function GET() {
  const res = await fetch(`${process.env.BKASH_BASE_URL}/tokenized/checkout/token/grant`, {
    method: 'POST',
    headers: {
      username: process.env.BKASH_USERNAME!,
      password: process.env.BKASH_PASSWORD!,
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      app_key: process.env.BKASH_APP_KEY,
      app_secret: process.env.BKASH_APP_SECRET
    })
  })

  const data = await res.json()
  return NextResponse.json(data)
}
```

---

## 3️⃣ API: `/api/bkash/create-payment`

📁 **app/api/bkash/create-payment/route.ts**
```ts
import { NextResponse } from 'next/server'

export async function POST(req: Request) {
  const body = await req.json()
  const tokenRes = await fetch(`${process.env.NEXT_PUBLIC_SITE_URL}/api/bkash/token`)
  const tokenData = await tokenRes.json()

  const paymentRes = await fetch(`${process.env.BKASH_BASE_URL}/tokenized/checkout/create`, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      authorization: tokenData.id_token,
      'x-app-key': process.env.BKASH_APP_KEY!
    },
    body: JSON.stringify({
      mode: '0011',
      payerReference: body.email,
      callbackURL: `${process.env.NEXT_PUBLIC_SITE_URL}/api/bkash/success?orderId=${body.orderId}`,
      amount: body.amount,
      currency: 'BDT',
      intent: 'sale',
      merchantInvoiceNumber: body.orderId,
    })
  })

  const paymentData = await paymentRes.json()
  return NextResponse.json(paymentData)
}
```

---

## 4️⃣ Success Route: `/api/bkash/success`

📁 **app/api/bkash/success/route.ts**
```ts
import { prisma } from '@/lib/db'
import { NextResponse } from 'next/server'

export async function GET(req: Request) {
  const { searchParams } = new URL(req.url)
  const orderId = searchParams.get('orderId') || ''

  await prisma.order.update({
    where: { id: orderId },
    data: { status: 'paid' }
  })

  return NextResponse.redirect(`${process.env.NEXT_PUBLIC_SITE_URL}/thank-you`)
}
```

---

## ✅ Frontend Checkout Integration

📁 **app/checkout/page.tsx**
```tsx
const initiateBkash = async (orderId: string, amount: number) => {
  const res = await fetch('/api/bkash/create-payment', {
    method: 'POST',
    body: JSON.stringify({ orderId, amount, email: form.email }),
  })
  const data = await res.json()
  window.location.href = data.bkashURL
}
```

Form submit করার পর:
```tsx
const res = await fetch('/api/checkout', {
  method: 'POST',
  body: JSON.stringify({ ...form, items: cart, total })
})
const { orderId } = await res.json()
await initiateBkash(orderId, total)
```

---

## ✅ Final Output:

- 💳 ইউজাররা bKash Gateway-এ redirect হয়  
- 🟢 Success হলে DB-তে Order `paid` হয়  
- 🔄 Uses real bKash API flow  
- 🔐 Works with sandbox → Ready for live creds

---

## ⏭️ Next Step:

➡️ পারি এখন শুরু করতে:
**STEP 4: User Login / Signup with NextAuth**

> বলো "Login System বানাও" — আমি:

- ✅ Signup / Login ফর্ম
- ✅ User Session Cookie
- ✅ Admin/User role support
- ✅ Wishlist / Orders user-wise

প্রস্তুত তো? 😊

দারুণ! এখন চল করি **bKash Personal Payment Method Integration** —  
যেটা সবচেয়ে সহজ, **নির্ভরযোগ্য** এবং **ছোট ব্যবসার জন্য একদম পারফেক্ট** ✅

---

## ✅ bKash Personal Payment – কীভাবে কাজ করবে?

> এটা gateway-based না — user তোমার personal bKash number-এ টাকা পাঠাবে → তুমি ম্যানুয়ালি verify করবে।

---

## 🧠 Flow Plan:

1. 💳 Checkout পেজে "bKash Personal Payment" অপশন থাকবে  
2. 🧾 কাস্টমারকে দেখাবে তোমার personal bKash নম্বর  
3. 📸 কাস্টমার Payment screenshot বা ট্রানজেকশন ID ইনপুট করবে  
4. 🟡 Order will be marked as **“pending”**  
5. ✅ তুমি Admin Panel থেকে “confirmed” করতে পারবে

---

## 🛠️ 1. Checkout Page: Add Option

📁 **app/checkout/page.tsx**

```tsx
const [paymentMethod, setPaymentMethod] = useState('bkash')
const [trxId, setTrxId] = useState('')
```

🧾 Add to the form:
```tsx
<div className="mt-4">
  <h3 className="font-semibold">Select Payment Method</h3>
  <label className="block mt-2">
    <input type="radio" value="bkash" checked={paymentMethod === 'bkash'} onChange={(e) => setPaymentMethod(e.target.value)} />
    <span className="ml-2">bKash Personal Payment</span>
  </label>
</div>

{paymentMethod === 'bkash' && (
  <div className="mt-4 bg-pink-50 p-4 rounded">
    <p className="text-sm font-semibold">Send ৳{total} to:</p>
    <p className="text-lg font-bold text-pink-700">📱 01XXXXXXXXX (bKash Personal)</p>

    <label className="block mt-4">
      <span className="text-sm">Enter bKash Transaction ID:</span>
      <input value={trxId} onChange={(e) => setTrxId(e.target.value)} placeholder="Ex: TX1234ABCD" className="p-2 border rounded w-full mt-1" required />
    </label>
  </div>
)}
```

---

## 🔁 2. Submit Order API Update

📁 **app/api/checkout/route.ts** → Add `trxId`, `paymentMethod` field

```ts
const { name, email, phone, address, city, items, total, trxId, paymentMethod } = body

const order = await prisma.order.create({
  data: {
    name, email, phone, address, city, total,
    status: paymentMethod === 'bkash' ? 'pending' : 'unpaid',
    paymentMethod,
    paymentProof: trxId,
    items: {
      create: items.map((item: any) => ({
        productId: item.id,
        quantity: item.quantity,
        price: item.price
      }))
    }
  }
})
```

---

## 🔧 3. Update Prisma Schema (Add `paymentMethod`, `paymentProof`)

📁 **prisma/schema.prisma**
```prisma
model Order {
  id            String   @id @default(cuid())
  name          String
  email         String
  phone         String
  address       String
  city          String
  total         Float
  status        String   @default("unpaid")
  paymentMethod String?  // e.g. 'bkash', 'cod', 'sslcommerz'
  paymentProof  String?  // trxId, file URL, etc.
  items         OrderItem[]
  createdAt     DateTime @default(now())
}
```

```bash
npx prisma migrate dev --name add_payment_fields
```

---

## 🧾 4. Admin Panel: Confirm Order Payment

📁 **app/admin/orders/page.tsx** (add button to update order)

```tsx
{order.status === 'pending' && (
  <button
    onClick={() => updateStatus(order.id, 'paid')}
    className="text-green-600 underline text-sm"
  >
    Confirm bKash Payment
  </button>
)}
```

✅ তুমি Admin Dashboard থেকে manually “paid” করে দিতে পারবে।

---

## ✅ Final Output:

- ✅ কাস্টমার দেখে তোমার bKash নাম্বার  
- ✅ ট্রানজেকশন ID দিয়ে সাবমিট করে  
- ✅ অর্ডার “pending” হিসেবে save হয়  
- ✅ তুমি Admin panel থেকে “paid” mark করে দাও  

---

## 📌 Extra Option (Future):

- 🔍 Payment proof image upload  
- 📤 Email automation for payment confirmation  
- 📱 SMS API integration for alert

---

## ⏭️ Next Step:

> এখন পারি শুরু করতে:
➡️ **STEP 4: User Login System with NextAuth**

বলো: “Login System বানাও” — তাহলে Email+Password login/signup + session-based wishlist/orders তৈরি করে দেই 😊
