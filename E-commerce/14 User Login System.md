দারুণ! 💥 এখন শুরু করছি **STEP 4: User Login / Signup System** using **NextAuth.js** (Credentials-based authentication) ✅

---

## ✅ GOAL:

- 🔐 User registration + login (email + password)  
- 🍪 Secure session with cookies  
- 🛍️ Wishlist & Order History → user-wise  
- 🛠️ Admin/user role system (future upgrade possible)

---

## 🧱 Step-by-Step Plan

1. ⚙️ Install & setup NextAuth  
2. 🔑 Add Credentials Provider (email/password login)  
3. 🛢️ Save users in PostgreSQL via Prisma  
4. 🔒 Create `/login` and `/register` pages  
5. ✅ Protect routes using `getServerSession()`  
6. 🌙 Optional: role-based admin check

---

## 🛠️ 1. Install NextAuth

```bash
npm install next-auth
```

---

## 🧬 2. Setup `[...nextauth]` API Route

📁 **app/api/auth/[...nextauth]/route.ts**
```ts
import NextAuth from 'next-auth'
import Credentials from 'next-auth/providers/credentials'
import { prisma } from '@/lib/db'
import bcrypt from 'bcryptjs'

const handler = NextAuth({
  providers: [
    Credentials({
      name: 'Credentials',
      credentials: {
        email: {},
        password: {},
      },
      async authorize(credentials) {
        const user = await prisma.user.findUnique({ where: { email: credentials?.email } })
        if (!user) throw new Error('No user found')

        const isValid = await bcrypt.compare(credentials!.password, user.password)
        if (!isValid) throw new Error('Invalid password')

        return { id: user.id, email: user.email }
      }
    })
  ],
  pages: {
    signIn: '/login'
  },
  session: {
    strategy: 'jwt'
  },
  callbacks: {
    async session({ session, token }) {
      if (token) session.user.id = token.sub
      return session
    }
  }
})

export { handler as GET, handler as POST }
```

---

## 📁 3. Update Prisma Schema – Add `User` Model

📁 **prisma/schema.prisma**
```prisma
model User {
  id       String   @id @default(cuid())
  email    String   @unique
  password String
  createdAt DateTime @default(now())
}
```

```bash
npx prisma migrate dev --name add_user_model
```

---

## 🧾 4. Register Page (Signup)

📁 **app/register/page.tsx**
```tsx
'use client'
import { useState } from 'react'
import { useRouter } from 'next/navigation'

export default function RegisterPage() {
  const [form, setForm] = useState({ email: '', password: '' })
  const router = useRouter()

  const submit = async () => {
    const res = await fetch('/api/register', {
      method: 'POST',
      body: JSON.stringify(form)
    })
    if (res.ok) router.push('/login')
    else alert('Registration failed')
  }

  return (
    <div className="max-w-sm mx-auto py-10">
      <h1 className="text-xl font-bold mb-4">Create an Account</h1>
      <input type="email" placeholder="Email" value={form.email} onChange={e => setForm({ ...form, email: e.target.value })} className="p-2 border w-full mb-2" />
      <input type="password" placeholder="Password" value={form.password} onChange={e => setForm({ ...form, password: e.target.value })} className="p-2 border w-full mb-4" />
      <button onClick={submit} className="bg-blue-600 text-white px-4 py-2 rounded w-full">Register</button>
    </div>
  )
}
```

---

📁 **app/api/register/route.ts**
```ts
import { prisma } from '@/lib/db'
import bcrypt from 'bcryptjs'
import { NextResponse } from 'next/server'

export async function POST(req: Request) {
  const body = await req.json()
  const hashed = await bcrypt.hash(body.password, 10)
  const exists = await prisma.user.findUnique({ where: { email: body.email } })

  if (exists) return NextResponse.json({ error: 'User already exists' }, { status: 400 })

  const user = await prisma.user.create({
    data: {
      email: body.email,
      password: hashed
    }
  })

  return NextResponse.json({ user })
}
```

---

## 🔐 5. Login Page

📁 **app/login/page.tsx**
```tsx
'use client'
import { signIn } from 'next-auth/react'
import { useState } from 'react'
import { useRouter } from 'next/navigation'

export default function LoginPage() {
  const [form, setForm] = useState({ email: '', password: '' })
  const router = useRouter()

  const login = async () => {
    const res = await signIn('credentials', {
      ...form,
      redirect: false
    })
    if (res?.ok) router.push('/')
    else alert('Login failed')
  }

  return (
    <div className="max-w-sm mx-auto py-10">
      <h1 className="text-xl font-bold mb-4">Login</h1>
      <input type="email" placeholder="Email" value={form.email} onChange={e => setForm({ ...form, email: e.target.value })} className="p-2 border w-full mb-2" />
      <input type="password" placeholder="Password" value={form.password} onChange={e => setForm({ ...form, password: e.target.value })} className="p-2 border w-full mb-4" />
      <button onClick={login} className="bg-blue-600 text-white px-4 py-2 rounded w-full">Login</button>
    </div>
  )
}
```

---

## 🧠 6. Use Auth in Protected Pages

📁 Example: `app/wishlist/page.tsx`

```tsx
import { getServerSession } from 'next-auth'
import { authOptions } from '@/lib/auth'

export default async function WishlistPage() {
  const session = await getServerSession(authOptions)
  if (!session) return <p>Please login to view your wishlist</p>

  const userId = session.user.id
  // fetch wishlist from DB
}
```

---

## ✅ Final Output:

- ✅ Login/Register system  
- ✅ Session maintained  
- ✅ User-specific data access  
- ✅ Admin/user role expandable  
- ✅ Secure, password hashed with bcrypt

---

## ⏭️ You’re Now Ready for:

- 🛍️ User-specific Wishlist  
- 📦 My Orders History page  
- 🔒 Admin route protection  
- 🌐 Public profile system

**বল “Wishlist / Order history user-wise বানাও” — আমি ওইগুলো এখনি তৈরি করে দেবো!** 😊
