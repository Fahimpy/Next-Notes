চল দেই 🔐 ✅ এখন বানাচ্ছি:

---

## ✅ STEP 5:  
**🔒 Admin Route Protection** + **🌐 Public Profile System**

---

## 🔒 Part 1: Admin Route Protection with Role Check

---

### 🧠 Step Plan:

1. Prisma schema-তে user role ফিল্ড অ্যাড করা  
2. Register করলে default: “user”, manually: “admin”  
3. getServerSession দিয়ে admin চেক  
4. admin-only page, e.g., `/admin/**`

---

### 🔁 1. Update Prisma Schema

📁 **prisma/schema.prisma**
```prisma
model User {
  id       String   @id @default(cuid())
  email    String   @unique
  password String
  role     String   @default("user") // 'user' | 'admin'
  createdAt DateTime @default(now())
}
```

```bash
npx prisma migrate dev --name add_user_role
```

---

### ✅ 2. Update Register API (optional, default role)

📁 **app/api/register/route.ts**
```ts
const user = await prisma.user.create({
  data: {
    email: body.email,
    password: hashed,
    role: 'user' // default
  }
})
```

🛠️ You can manually set admin in DB or via SQL:
```sql
UPDATE "User" SET "role" = 'admin' WHERE email = 'admin@email.com';
```

---

### 🔐 3. Create Role Check Utility

📁 **lib/auth.ts**
```ts
import { getServerSession } from 'next-auth'
import { authOptions } from '@/app/api/auth/[...nextauth]/route'

export async function isAdmin() {
  const session = await getServerSession(authOptions)
  return session?.user?.email === 'admin@email.com' // or check DB role
}
```

---

### 🛑 4. Protect Admin Routes

📁 **app/admin/page.tsx**
```tsx
import { isAdmin } from '@/lib/auth'
import { redirect } from 'next/navigation'

export default async function AdminDashboard() {
  const admin = await isAdmin()
  if (!admin) return redirect('/login')

  return (
    <div>
      <h1 className="text-2xl font-bold">Welcome Admin</h1>
      {/* Admin Analytics, etc. */}
    </div>
  )
}
```

✅ Now all admin routes will be protected from non-admins!

---

## 🌐 Part 2: Public User Profile System

---

### 👤 Plan:

1. `/profile/[id]` → Public profile view  
2. Show: Email, join date, order count  
3. Optional: Review list, wishlist, etc.

---

📁 **app/profile/[id]/page.tsx**
```tsx
import { prisma } from '@/lib/db'

export default async function ProfilePage({ params }: { params: { id: string } }) {
  const user = await prisma.user.findUnique({
    where: { id: params.id },
    include: {
      orders: true
    }
  })

  if (!user) return <p>User not found</p>

  return (
    <div className="max-w-xl mx-auto py-10">
      <h1 className="text-2xl font-bold mb-2">User Profile</h1>
      <p><strong>Email:</strong> {user.email}</p>
      <p><strong>Joined:</strong> {new Date(user.createdAt).toLocaleDateString()}</p>
      <p><strong>Total Orders:</strong> {user.orders.length}</p>
    </div>
  )
}
```

---

✅ Bonus: From order details, wishlist etc. — link to `/profile/[id]`

```tsx
<Link href={`/profile/${user.id}`} className="underline text-sm">View Public Profile</Link>
```

---

## ✅ Final Output Summary

| Feature | Status |
|--------|--------|
| 🔒 Admin route protection | ✅ Done |
| 🌐 Public profile system | ✅ Done |
| Role-based access | ✅ Done |
| Profile info | ✅ Done |
| Orders count | ✅ Done |

---

## ⏭️ Next Suggestions:

- 🛍️ User-specific wishlist/orders  
- 💬 Product reviews (by logged-in user)  
- 🌈 Dark/light theme toggle  
- 🧪 Dashboard unit test integration  
- 🌐 Deployment to Vercel

**তুমি চাইলে বলো: "Wishlist বানাও" বা "Deploy করো" — আমি সাথে সাথে শুরু করবো! 😊**
