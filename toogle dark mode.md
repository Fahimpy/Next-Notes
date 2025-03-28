🔧 আমি এখন পর্ব ২৫ শুরু করছি:  
# **🎨 পর্ব ২৫: UI Theme System (Dark/Light + Custom Templates)**

একটু পরেই শুরু করছি পুরো কোড, লজিক ও ব্যাখ্যা সহ।  
🟢 প্রস্তুত তো? আমি শুরু করি?

চল তাহলে শুরু করি —  
# **🎨 পর্ব ২৫: UI Theme System – Dark/Light Mode + Custom Template Support**

আমাদের লক্ষ্য:  
✅ ব্লগ CMS-এ **Dark/Light mode** টগল সাপোর্ট  
✅ ভবিষ্যতে সহজে **Custom Template** (Font, Layout, Color) সাপোর্ট  
✅ ইউজারের পছন্দ **localStorage / DB**-তে সংরক্ষণ  
✅ Next.js + Tailwind CSS + Context API দিয়ে সহজ ও মডুলার ইমপ্লিমেন্টেশন

---

## 📦 Step 1: Tailwind Config Setup for Dark Mode

📁 **tailwind.config.js** আপডেট করো:

```js
module.exports = {
  darkMode: 'class', // ✅ class-based dark mode toggle
  content: ['./pages/**/*.{js,ts,jsx,tsx}', './components/**/*.{js,ts,jsx,tsx}'],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

---

## 🧠 Step 2: Theme Context তৈরি করো

📁 **context/ThemeContext.js**

```js
import { createContext, useEffect, useState } from "react";

export const ThemeContext = createContext();

export const ThemeProvider = ({ children }) => {
  const [theme, setTheme] = useState("light");

  useEffect(() => {
    const stored = localStorage.getItem("theme");
    if (stored) setTheme(stored);
    else setTheme("light");
  }, []);

  useEffect(() => {
    const root = window.document.documentElement;
    root.classList.remove("light", "dark");
    root.classList.add(theme);
    localStorage.setItem("theme", theme);
  }, [theme]);

  const toggleTheme = () => {
    setTheme(theme === "light" ? "dark" : "light");
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};
```

---

## 🧱 Step 3: _app.js এ Context যুক্ত করো

📁 **pages/_app.js**

```js
import "@/styles/globals.css";
import { ThemeProvider } from "@/context/ThemeContext";

export default function App({ Component, pageProps }) {
  return (
    <ThemeProvider>
      <Component {...pageProps} />
    </ThemeProvider>
  );
}
```

---

## 🌓 Step 4: Header বা Navbar-এ Toggle Button যুক্ত করো

📁 **components/ThemeToggle.js**

```js
import { useContext } from "react";
import { ThemeContext } from "@/context/ThemeContext";

export default function ThemeToggle() {
  const { theme, toggleTheme } = useContext(ThemeContext);

  return (
    <button
      onClick={toggleTheme}
      className="text-sm px-3 py-1 rounded border border-gray-400 hover:bg-gray-100 dark:hover:bg-gray-800"
    >
      {theme === "light" ? "🌙 Dark Mode" : "☀️ Light Mode"}
    </button>
  );
}
```

📁 **Header.js** বা Layout-এ ব্যবহার করো:

```js
import ThemeToggle from "./ThemeToggle";
...
<ThemeToggle />
```

---

## 🎨 Step 5: Dark Mode Style Tailwind-এ প্রয়োগ করো

```html
<div className="bg-white text-black dark:bg-gray-900 dark:text-white">
  ...
</div>
```

✅ Tailwind এ `dark:` prefix দিয়ে যেকোনো element এর Dark styling দিতে পারো।

---

## 🧪 Step 6: Future Custom Template Support – Expandable Logic

📁 **theme.config.js** ফাইল তৈরি করো (future use):

```js
export const TEMPLATES = {
  minimal: {
    font: "font-sans",
    bg: "bg-white",
    text: "text-gray-900",
  },
  modern: {
    font: "font-serif",
    bg: "bg-gray-100",
    text: "text-gray-800",
  },
  darkElegance: {
    font: "font-mono",
    bg: "bg-gray-900",
    text: "text-white",
  },
};
```

📁 ThemeContext.js ফাইলে future-ready context রাখতে পারো:

```js
const [template, setTemplate] = useState("minimal");
const applyTemplate = (name) => setTemplate(name);
```

✅ Future marketplace থেকে টেমপ্লেট সিলেক্ট করলে এই `applyTemplate()` কাজ করবে।

---

## ✅ পর্ব ২৫ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Dark/Light Mode Toggle | Done |
| ✅ Context API Driven | Done |
| ✅ LocalStorage Persist | Done |
| ✅ Tailwind Dark Styling | Done |
| ✅ Future Template Ready | ✅ |

---

## 🔜 পরবর্তী পর্ব:  
**📦 পর্ব ২৬: Blogging Templates Marketplace Integration**  
✅ Multiple UI Layouts/Templates  
✅ Preview + Apply Option  
✅ DB বা Local Setting অনুযায়ী ইউজার সেটিংস সেভ  

🟢 **চলবো কি Template Marketplace-এ? তুমি চাইলে কিছু ডিজাইন অপশনও দেখাতে পারি!**

