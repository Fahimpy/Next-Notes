চমৎকার! 🚀 এখন শুরু করছি **STEP 2: Advanced Content Editor Integration** — যাতে তুমি প্রোডাক্ট বা ব্লগ পেইজে rich content ব্যবহার করতে পারো।

---

## ✅ GOAL:

- 🔠 Block-style editor (Heading, Paragraph, List, Image, etc.)
- 📝 DB-তে content save হবে (JSON format)
- ✍️ Use inside **Product Add/Edit** page

We'll use: **Editor.js** – fast, extensible, open-source editor.

---

## 📦 1. Install Editor.js & Tools

```bash
npm install --save @editorjs/editorjs
npm install --save @editorjs/header @editorjs/image @editorjs/paragraph @editorjs/list
```

---

## 📁 2. Create `EditorBlock` Component

📁 **components/EditorBlock.tsx**
```tsx
'use client'

import EditorJS from '@editorjs/editorjs'
import Header from '@editorjs/header'
import List from '@editorjs/list'
import Paragraph from '@editorjs/paragraph'
import { useEffect, useRef } from 'react'

export default function EditorBlock({
  data,
  onChange,
}: {
  data?: any
  onChange: (data: any) => void
}) {
  const ref = useRef<EditorJS>()

  useEffect(() => {
    if (!ref.current) {
      const editor = new EditorJS({
        holder: 'editorjs',
        placeholder: 'Write product details...',
        data: data || {},
        tools: {
          header: Header,
          list: List,
          paragraph: Paragraph,
        },
        async onChange(api) {
          const output = await api.saver.save()
          onChange(output)
        },
      })

      ref.current = editor
    }

    return () => {
      ref.current?.destroy()
      ref.current = undefined
    }
  }, [])

  return <div id="editorjs" className="border rounded p-4 bg-white" />
}
```

---

## 🧾 3. Update Product Add Page (`/admin/products/new`)

📁 **app/admin/products/new/page.tsx** (Add `EditorBlock`)

```tsx
import EditorBlock from '@/components/EditorBlock'

const [editorData, setEditorData] = useState<any>(null)

const onSubmit = async (data: FormValues) => {
  const res = await fetch('/api/products', {
    method: 'POST',
    body: JSON.stringify({ ...data, content: editorData }) // add content
  })
  const result = await res.json()
  setMessage(result.message || 'Submitted!')
}
```

📄 Add in the form:

```tsx
<EditorBlock onChange={setEditorData} />
```

---

## 🛢️ 4. Update Prisma Schema to Save Content

📁 **prisma/schema.prisma**
```prisma
content Json?  // Add this in Product model
```

```bash
npx prisma migrate dev --name add_content_editor
```

---

## 🔄 5. Update Product API to Save & Load Editor Content

📁 **app/api/products/route.ts** (POST handler)

```ts
const product = await prisma.product.create({
  data: {
    title: body.title,
    description: body.description,
    price: body.price,
    stock: body.stock,
    categoryId: body.categoryId,
    content: body.content, // ✅ Added
    metaTitle: body.metaTitle,
    metaDesc: body.metaDesc,
    indexable: body.indexable ?? true,
  }
})
```

📁 **Edit Page:** use `reset(data.product)`  
and set `setEditorData(data.product.content)` after fetch.

---

## ✅ Final Output:

- ✅ Rich text editor (heading, list, paragraph)
- ✅ Saves as structured JSON
- ✅ Uses Editor.js (modular & extendable)
- ✅ Ready for product/blog/custom content

---

## ⏭️ Next Step:

➡️ **Step 3: SSLCommerz / bKash Payment Integration**

> বলো “Payment Integration শুরু করো” — আমি করব full payment redirect system ✅  
Ready? 😊
