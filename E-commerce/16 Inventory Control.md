চল দেই! 🚀 এখন স্টার্ট করছি তোমার বলা **বাকি ৪টি ফিচার**, এক এক করে পুরোপুরি প্রোডাকশন-রেডি করে ফেলি:

---

## ✅ এই ৪টি ফিচার করবো:

1. **📦 Product Inventory Control (Stock System)**  
2. **🧾 Review System per Product**  
3. **⚠️ Prevent Add to Cart if Out of Stock**  
4. **📧 Email Invoice via SendGrid**

---

## 🧩 Step-by-step Plan:

| Step | Feature | Status |
|------|---------|--------|
| 1️⃣ | Stock System (Decrease on order, Show remaining stock) | 🔄 Doing now |
| 2️⃣ | Review Form + List per product (logged-in only) | 🔜 Next |
| 3️⃣ | Block cart for out-of-stock | 🔜 After that |
| 4️⃣ | Email invoice to customer | 🔜 Final |

---

## 📦 STEP 1: Inventory Control System

### 🧠 Plan:

- Each product has `stock: number`  
- Checkout করলে stock কমবে  
- প্রোডাক্ট কার্ডে স্টক count দেখাবে  
- Out-of-stock হলে “Add to Cart” disabled

---

### 1. Prisma Schema (already has it, confirm):

```prisma
model Product {
  id       String   @id @default(cuid())
  title    String
  price    Float
  stock    Int      @default(10) // stock control
  ...
}
```

---

### 2. Decrease Stock on Order

📁 **app/api/checkout/route.ts** — add after order created:
```ts
for (const item of items) {
  await prisma.product.update({
    where: { id: item.id },
    data: {
      stock: { decrement: item.quantity }
    }
  })
}
```

---

### 3. Product Card: Show stock

📁 **ProductGrid.tsx** (or ProductCard)
```tsx
<p className="text-sm text-gray-500">In stock: {prod.stock}</p>
```

---

### 4. Block Add to Cart if stock = 0

📁 **AddToCartButton.tsx**
```tsx
if (product.stock <= 0) {
  return <p className="text-red-600 mt-2">Out of stock</p>
}
```

✅ স্টক না থাকলে Add to Cart বাটন থাকবে না।

---

## ✅ Step 1 Complete: Stock System Done!

---

> এখন বলো “Next Step করো” — আমি করবো:

➡️ **🧾 Step 2: Review System per Product** – login user only  
➡️ তারপর: Out of stock এ cart block (done),  
➡️ তারপর: **📧 Email Invoice via SendGrid**

Ready? 😊
