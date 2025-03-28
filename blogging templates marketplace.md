চল তাহলে শুরু করি —  
# **📦 পর্ব ২৬: Blogging Templates Marketplace Integration**

আমাদের লক্ষ্য:  
✅ ইউজার বিভিন্ন **প্রিমেইড ব্লগ টেমপ্লেট ডিজাইন** থেকে বেছে নিতে পারবে  
✅ প্রতিটি টেমপ্লেটের **Preview + Apply বাটন** থাকবে  
✅ ইউজারের সিলেক্ট করা টেমপ্লেট **প্রেজার্ভ** হবে (localStorage বা DB)  
✅ Frontend dynamically সেই টেমপ্লেট অনুযায়ী রেন্ডার হবে

---

## 📦 Step 1: টেমপ্লেট কনফিগারেশন তৈরি করো

📁 **lib/templates.js**

```js
export const blogTemplates = {
  minimal: {
    name: "Minimal",
    font: "font-sans",
    card: "rounded-md border shadow-sm",
    color: "text-gray-900 bg-white",
  },
  modern: {
    name: "Modern",
    font: "font-serif",
    card: "rounded-lg border-2 border-gray-300",
    color: "text-gray-800 bg-gray-100",
  },
  darkElegance: {
    name: "Dark Elegance",
    font: "font-mono",
    card: "rounded-xl border border-gray-700",
    color: "text-white bg-gray-900",
  },
};
```

---

## 🧠 Step 2: ThemeContext এ Template Support যুক্ত করো

📁 **context/ThemeContext.js** আপডেট করো:

```js
import { blogTemplates } from "@/lib/templates";

...

const [template, setTemplate] = useState("minimal");

useEffect(() => {
  const stored = localStorage.getItem("template");
  if (stored && blogTemplates[stored]) setTemplate(stored);
}, []);

const applyTemplate = (name) => {
  if (blogTemplates[name]) {
    setTemplate(name);
    localStorage.setItem("template", name);
  }
};

return (
  <ThemeContext.Provider value={{ theme, toggleTheme, template, applyTemplate }}>
    {children}
  </ThemeContext.Provider>
);
```

---

## 🎨 Step 3: TemplateSelector Component তৈরি করো

📁 **components/TemplateSelector.js**

```js
import { useContext } from "react";
import { blogTemplates } from "@/lib/templates";
import { ThemeContext } from "@/context/ThemeContext";

export default function TemplateSelector() {
  const { template, applyTemplate } = useContext(ThemeContext);

  return (
    <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
      {Object.entries(blogTemplates).map(([key, config]) => (
        <div
          key={key}
          className={`p-4 border rounded ${template === key ? "ring-2 ring-blue-600" : ""}`}
        >
          <h3 className="font-bold mb-2">{config.name}</h3>
          <p className="text-sm mb-2">Font: {config.font}</p>
          <button
            onClick={() => applyTemplate(key)}
            className="bg-blue-600 text-white px-3 py-1 rounded"
          >
            Apply Template
          </button>
        </div>
      ))}
    </div>
  );
}
```

---

## 📄 Step 4: Dashboard Settings পেইজে যুক্ত করো

📁 **pages/admin/settings.js** (নতুন পেইজ)

```js
import TemplateSelector from "@/components/TemplateSelector";

export default function SettingsPage() {
  return (
    <div className="max-w-4xl mx-auto py-10">
      <h1 className="text-3xl font-bold mb-6">🛠️ Blog Appearance Settings</h1>
      <TemplateSelector />
    </div>
  );
}
```

---

## 🧩 Step 5: Blog Card এবং Layout গুলোতে Template Apply করো

📁 **components/BlogCard.js**

```js
import { useContext } from "react";
import { ThemeContext } from "@/context/ThemeContext";
import { blogTemplates } from "@/lib/templates";

export default function BlogCard({ blog }) {
  const { template } = useContext(ThemeContext);
  const styles = blogTemplates[template];

  return (
    <div className={`${styles.card} p-4 ${styles.font} ${styles.color}`}>
      <h2 className="text-xl font-semibold">{blog.title}</h2>
      <p className="text-sm">{blog.content.substring(0, 100)}...</p>
    </div>
  );
}
```

👉 একইভাবে layout, buttons, sidebar এ apply করো।

---

## ✅ পর্ব ২৬ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Template Config | Done |
| ✅ Preview + Apply | Done |
| ✅ Persisted Choice | Done |
| ✅ Real-Time Change | Done |
| ✅ Template-based Design | ✅ |

---

## 🔜 পরবর্তী পর্ব:
**🧪 পর্ব ২৭: Unit & E2E Testing Integration**  
✅ Component-level Unit Test  
✅ Blog Creation Flow E2E Test (Login → Create → View)  
✅ Tools: Jest, React Testing Library, Playwright/Cypress

🟢 **চলবো কি টেস্টিং এ? তুমি চাইলে আমি পুরো config + example লিখে দিচ্ছি!**
