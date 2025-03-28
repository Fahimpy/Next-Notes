চল দেই! 🚀  
এখন শুরু করছি **STEP 3: Email Invoice System via SendGrid**  
যাতে অর্ডার কনফার্ম হলে ইউজার **ইনভয়েস ইমেইল পায় PDF ছাড়াও একটি সুন্দর HTML ইনভয়েস** ✅

---

## ✅ GOAL:

- 📧 কাস্টমারকে অর্ডার কনফার্মেশনের পর Email যাবে  
- 🧾 Email-এ থাকবে: প্রোডাক্ট লিস্ট, total, অর্ডার আইডি  
- ✉️ Uses SendGrid API  
- 🛡️ নিরাপদ `.env` কনফিগারেশন  
- 💡 Future: Add optional PDF attachment

---

## 🛠️ Step-by-Step Setup

---

### 1️⃣ Get SendGrid API Key

👉 Sign up here: https://sendgrid.com/  
➡️ Go to **Settings > API Keys**  
➡️ Create Key (Full Access or Restricted to Mail Send)

📁 **.env**
```env
SENDGRID_API_KEY=SG.xxxxxxxx
SENDGRID_FROM_EMAIL=yourverified@email.com
```

⚠️ **Email must be verified in SendGrid (Sender Authentication)**

---

### 2️⃣ Install SendGrid Mail SDK

```bash
npm install @sendgrid/mail
```

---

### 3️⃣ Create Mail Utility Function

📁 **lib/mail.ts**
```ts
import sgMail from '@sendgrid/mail'

sgMail.setApiKey(process.env.SENDGRID_API_KEY!)

export async function sendOrderEmail({
  to,
  name,
  orderId,
  items,
  total
}: {
  to: string
  name: string
  orderId: string
  items: { title: string, price: number, quantity: number }[]
  total: number
}) {
  const html = `
    <h2>Hi ${name},</h2>
    <p>Thanks for your order. Here's your order summary:</p>
    <p><strong>Order ID:</strong> ${orderId}</p>
    <table style="width: 100%; border-collapse: collapse;" border="1">
      <tr><th>Product</th><th>Price</th><th>Qty</th></tr>
      ${items.map(i => `<tr><td>${i.title}</td><td>$${i.price}</td><td>${i.quantity}</td></tr>`).join('')}
    </table>
    <p><strong>Total:</strong> $${total}</p>
    <p>We’ll notify you once your order is shipped.</p>
    <p>— Your Shop Team</p>
  `

  await sgMail.send({
    to,
    from: process.env.SENDGRID_FROM_EMAIL!,
    subject: `Order Confirmation - ${orderId}`,
    html
  })
}
```

---

### 4️⃣ Call Email Function After Order

📁 **app/api/checkout/route.ts**
```ts
import { sendOrderEmail } from '@/lib/mail'

await sendOrderEmail({
  to: email,
  name,
  orderId: order.id,
  total,
  items
})
```

---

## 🧪 Test It

✔️ Place an order  
✔️ Check email inbox  
✔️ You’ll receive a well-formatted HTML invoice

---

## ✅ Optional Upgrade (Later)

| Feature | Status |
|--------|--------|
| 📎 PDF invoice (via PDFKit or Puppeteer) | Can be added later |
| 📦 Shipment email follow-up | Optional |
| 🧾 Invoice number with logic | Easy to add |
| 📤 Admin email on new order | Optional too |

---

## ✅ Step 3 Complete: Email Invoice via SendGrid – DONE!

- ✅ কাস্টমার ইমেইল পায় অর্ডারের পর  
- ✅ Includes full summary  
- ✅ Uses official SendGrid SDK  
- ✅ Easy to customize / scale  

---

## 🏁 You’ve Officially Built a Full Professional-Grade eCommerce System! 🎉

> চাইলে এখন আমি:

- 🗂️ Full Code Summary বানিয়ে দিতে পারি  
- 🧪 Test Coverage যুক্ত করে দিতে পারি  
- 🚀 এক ক্লিকে **Deploy করে Live করে দিতে পারি**

**বলো: “Deploy করো” বা “Code Summary দাও” — আমি সেটআপ করে ফেলি 🔥**
