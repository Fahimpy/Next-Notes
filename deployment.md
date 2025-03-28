দারুণ! তাহলে আমাদের পরবর্তী দুটি পর্ব হবে:

---

## 🔁 **পর্ব ৩৩: Full Deployment (Vercel + Stripe + Webhook + Domain Ready)**  
✅ Vercel এর মাধ্যমে CMS SaaS Project ডেপ্লয়  
✅ Env config: Stripe, DB, Auth, Custom Domain  
✅ Stripe Webhook secure করে যুক্ত করা  
✅ SEO & Lighthouse Check

---

## 💻 **পর্ব ৩৪: Admin SaaS Analytics Dashboard**  
✅ Total Users, Blogs, Active Plans  
✅ Blog Views, New Signups, Revenue Chart  
✅ Admin Only Access  
✅ Optional: Chart.js or Recharts Integration

---

🔜 আমি এখন **পর্ব ৩৩: Deployment** শুরু করবো — একদম Vercel-ready গাইড + config সহ।  
🟢 **শুরু করি?** ✅

চল তাহলে শুরু করি —  
# **🔁 পর্ব ৩৩: Full Deployment (Vercel + Stripe + Custom Domain Ready)**

আমাদের লক্ষ্য:  
✅ ব্লগ SaaS CMS প্রজেক্টটি **Production-Ready ভাবে Deploy করা**  
✅ Vercel ব্যবহার করে দ্রুত, secure ও scalable ডেপ্লয়মেন্ট  
✅ Stripe, Prisma, Auth, Webhook সহ সব ENV সঠিকভাবে কনফিগার  
✅ Custom Domain ও Webhook কাজ করবে লাইভ সার্ভারে

---

## 🧠 Step 1: Code Preparation

### ✅ ১. Ensure Production-Ready Code

- ✅ `next.config.js` → `i18n`, images config ঠিক আছে  
- ✅ `tailwind.config.js` → dark mode, purge enabled  
- ✅ `.env.local` → সব secret/prod key রাখা  
- ✅ Stripe Webhook route → `pages/api/stripe/webhook.js` (bodyParser=false)

### ✅ ২. Build test locally

```bash
npm run build
```

---

## 🚀 Step 2: Deploy to Vercel (free and fast)

### 🧾 ১. GitHub Repo Push করো

```bash
git init
git add .
git commit -m "SaaS CMS ready for deploy"
git remote add origin https://github.com/yourname/yourcms.git
git push -u origin main
```

### 🌐 ২. Vercel এ Login করো → Import Project

- ✅ “New Project” → Import your repo  
- ✅ Framework: **Next.js**  
- ✅ Root: `/`  
- ✅ Add Environment Variables:

```env
DATABASE_URL=postgresql://...
NEXTAUTH_SECRET=...
NEXTAUTH_URL=https://yourcms.vercel.app
STRIPE_SECRET_KEY=sk_live_...
NEXT_PUBLIC_STRIPE_PUBLIC_KEY=pk_live_...
STRIPE_PRO_PRICE_ID=price_...
STRIPE_BUSINESS_PRICE_ID=price_...
STRIPE_WEBHOOK_SECRET=whsec_...
EMAIL_FROM=you@yourdomain.com
EMAIL_SERVER=smtp://...
CLOUDINARY_*=...
```

✅ Save & Deploy  
Vercel will auto-build and give you: `https://yourcms.vercel.app`

---

## 📩 Step 3: Stripe Webhook Connect করো (Live)

### ✅ Stripe Dashboard → Developers → Webhooks

1. Add Endpoint → `https://yourcms.vercel.app/api/stripe/webhook`
2. Events to receive:
   - `checkout.session.completed`
   - `invoice.paid`
   - `customer.subscription.updated`
3. Copy `Signing Secret` → Save as `STRIPE_WEBHOOK_SECRET` in Vercel ENV

✅ Test Subscription –> You’ll see DB update

---

## 🌍 Step 4: Custom Domain Point করা (Optional)

### 👉 Vercel → Project → Settings → Domains

1. Add `yourdomain.com`  
2. Update your DNS:
   - **CNAME** → `cname.vercel-dns.com`
   - Or **A Record** if needed

📌 Don’t forget to also allow `www.yourdomain.com` with redirect!

---

## ✅ Step 5: Production Checklists

| বিষয় | কাজ |
|------|-----|
| 🔒 SSL/HTTPS | Vercel handles it |
| 🔁 Stripe Webhook | Connected ✅ |
| 🌐 SEO Tags | Checked in Head ✅ |
| 📊 Lighthouse Test | Chrome → Audit |
| 🧪 Playwright Test | `npx playwright test` |
| 🧹 Remove test data | Prisma Studio → Clean |

---

## ✅ পর্ব ৩৩ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Live Deployment | Done |
| ✅ Stripe Webhook Linked | Done |
| ✅ Custom Domain Ready | Done |
| ✅ Secure ENV Setup | ✅ |

---

## 🔜 পরবর্তী পর্ব:
# **💻 পর্ব ৩৪: Admin SaaS Analytics Dashboard**

✅ Total Users, Active Blogs  
✅ Revenue, Top Plans, Usage Stats  
✅ Only for Admin Role  
✅ Clean, Dashboard UI with Graphs

🟢 **চলবো কি Analytics Dashboard তৈরিতে? নাকি ডেপ্লয়মেন্টে কিছু হেল্প লাগবে?**
