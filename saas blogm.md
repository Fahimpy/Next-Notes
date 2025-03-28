চল তাহলে শুরু করি আমাদের চূড়ান্ত ও সবচেয়ে চ্যালেঞ্জিং পর্ব —  
# **🧠 পর্ব ২৮: SaaS Blog CMS Architecture (Multi-Tenant System)**

আমাদের লক্ষ্য:  
✅ **Multi-user SaaS Blog CMS** বানানো  
✅ প্রতিটি ইউজার নিজের আলাদা ব্লগ, ডিজাইন, পোস্ট ও সেটিংস রাখতে পারবে  
✅ ভবিষ্যতে subscription-based pricing চালু করা যাবে  
✅ সাবডোমেইন/স্লাগ অনুযায়ী ইউজার blog চালাতে পারবে:  
`yourcms.com/user1` বা `user1.yourcms.com`

---

## 🔧 Step 1: SaaS Architecture Overview (বোঝার জন্য)

### 🧱 Core Concepts:

| বিষয় | ব্যাখ্যা |
|------|---------|
| **Tenant/User** | প্রতিটি রেজিস্টার্ড ইউজার একটি ব্লগ চালায় |
| **Multi-tenancy** | এক ডাটাবেজেই অনেক ইউজারের আলাদা ব্লগ |
| **Isolated Content** | User A অন্য ইউজারের পোস্ট/কমেন্ট দেখতে পারবে না |
| **Custom Theme + Settings** | User-ভিত্তিক থিম, টেমপ্লেট, SEO সেটিংস |
| **Custom Domain/Site URL** | Optional: user1.yourcms.com |

---

## 📦 Step 2: Prisma Schema Design – Add Tenant Awareness

📁 **schema.prisma** (মেইন টেবিলগুলোর সাথে `userId` যোগ করো)

```prisma
model User {
  id        String   @id @default(uuid())
  name      String
  email     String   @unique
  blogs     Blog[]
  settings  UserSetting?
  ...
}

model Blog {
  id        String   @id @default(uuid())
  title     String
  content   String
  userId    String
  user      User     @relation(fields: [userId], references: [id])
  ...
}

model UserSetting {
  id         String   @id @default(uuid())
  userId     String   @unique
  theme      String   @default("minimal")
  subdomain  String?
  logo       String?
  user       User     @relation(fields: [userId], references: [id])
}
```

📦 Push করো:
```bash
npx prisma db push
```

---

## 🧠 Step 3: Tenant Context এড করো

📁 **lib/getTenant.js**

```js
import prisma from "./prisma";

export async function getTenantFromSlug(slug) {
  return await prisma.userSetting.findFirst({
    where: { subdomain: slug },
    include: { user: true },
  });
}
```

👉 Future-এ আমরা `domain/userSlug` বা `subdomain.yourcms.com` এভোইড করতে পারবো।

---

## 🧱 Step 4: Middleware – Access Restriction per Tenant

📁 **middleware/withTenantCheck.js**

```js
export function withTenantCheck(handler) {
  return async (req, res) => {
    const session = await getSession({ req });
    const blogUserId = req.body.userId || req.query.userId;

    if (session?.user?.id !== blogUserId) {
      return res.status(403).json({ error: "Forbidden" });
    }

    return handler(req, res);
  };
}
```

👉 সকল blog API route এ wrap করে ফিচার isolate করো।

---

## 👥 Step 5: Dashboard-এ Per-User Data দেখাও

```js
const { data: session } = useSession();

useEffect(() => {
  fetch(`/api/blog?userId=${session.user.id}`)
    .then(res => res.json())
    .then(setBlogs);
}, []);
```

---

## 🌐 Step 6: UserSlug / Subdomain Based Routing (Future Option)

- `/[user]/blog/[slug]` → dynamic route
- `/dashboard/[user]/settings` → personal settings panel

👉 Advanced routing আমরা সাবডোমেইন বা ক্লিন URL দিয়ে future এ যোগ করবো।

---

## ✅ পর্ব ২৮ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ SaaS Aware Schema | Done |
| ✅ Per-user Blog Ownership | Done |
| ✅ User-wise Theme + Settings | Done |
| ✅ API Access Restriction | Done |
| ✅ Multi-user Ready | ✅ |

---

## 🔚 তোমার Full Project এখন:

✅ Custom Blog CMS  
✅ SEO, Editor, Theme, Comments, AI, PDF  
✅ Admin Panel + Security + Testing  
✅ SaaS Enabled Multi-User Support

---

## 🔜 এরপর কি?

তুমি চাইলে এখন থেকে:
- 🎨 UI Polish + Marketplace Launch
- 💰 Stripe Subscription Integration
- 🔗 Custom Domain Mapping
- 🌍 Public SaaS Landing Page

🟢 **বল কী হবে পর্ব ২৯? SaaS Pricing System? Custom Domain? বা এখন তুমি কোড জিপ ফরম্যাটে নিতে চাও?**
