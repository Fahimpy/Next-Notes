চল তাহলে শুরু করি —  
# **🧪 পর্ব ২৭: Unit Test & E2E Test Integration (Jest + Playwright)**

আমাদের লক্ষ্য:  
✅ ব্লগ CMS-এ **বাগহীন ফিচার নিশ্চিত** করার জন্য ইউনিট ও E2E টেস্ট সংযুক্ত করা  
✅ 🧪 **Unit Test**: ফাংশন, কম্পোনেন্ট, API ঠিকঠাক কাজ করছে কিনা  
✅ ✅ **E2E Test**: ইউজার হিসেবে Login → Blog Create → View → Comment পুরো flow  
✅ Jest + React Testing Library + Playwright ব্যবহার করবো

---

## 🧪 Step 1: Unit Testing Setup with **Jest + React Testing Library**

### ✅ 1. প্যাকেজ ইন্সটল করো:

```bash
npm install --save-dev jest @testing-library/react @testing-library/jest-dom babel-jest identity-obj-proxy
```

### ✅ 2. `jest.config.js` ফাইল তৈরি করো:

```js
module.exports = {
  testEnvironment: "jsdom",
  moduleNameMapper: {
    "\\.(css|less|scss|sass)$": "identity-obj-proxy",
    "^@/(.*)$": "<rootDir>/src/$1", // যদি alias ইউজ করো
  },
  setupFilesAfterEnv: ["<rootDir>/jest.setup.js"],
};
```

### ✅ 3. `jest.setup.js` ফাইল:

```js
import "@testing-library/jest-dom";
```

---

## ✅ Example Unit Test – `ThemeToggle` Component

📁 **components/ThemeToggle.test.js**

```js
import { render, screen, fireEvent } from "@testing-library/react";
import ThemeToggle from "./ThemeToggle";
import { ThemeContext } from "@/context/ThemeContext";

test("toggles theme when clicked", () => {
  const toggleMock = jest.fn();
  render(
    <ThemeContext.Provider value={{ theme: "light", toggleTheme: toggleMock }}>
      <ThemeToggle />
    </ThemeContext.Provider>
  );

  const button = screen.getByRole("button");
  fireEvent.click(button);
  expect(toggleMock).toHaveBeenCalled();
});
```

```bash
npx jest
```

---

## 🧪 Step 2: E2E Testing Setup with **Playwright**

### ✅ 1. Playwright ইন্সটল করো:

```bash
npx playwright install
```

### ✅ 2. Test Setup Command:

```bash
npx playwright codegen http://localhost:3000
```

👉 এটি ব্রাউজারে ওপেন করবে, তোমার actions রেকর্ড করবে  
👉 তারপর `.spec.ts` ফাইলে সেই কোড কপি করে রাখো

---

## ✅ Example E2E Test – Blog Create Flow

📁 **tests/blog-create.spec.ts**

```ts
import { test, expect } from "@playwright/test";

test("user can login and create a blog", async ({ page }) => {
  await page.goto("http://localhost:3000/login");
  await page.fill('input[name="email"]', "test@example.com");
  await page.fill('input[name="password"]', "password123");
  await page.click("text=Login");

  await page.waitForURL("**/dashboard");

  await page.goto("http://localhost:3000/admin/create");
  await page.fill('input[placeholder="Title"]', "Test Blog");
  await page.fill(".ql-editor", "This is a test blog content.");
  await page.click("text=Submit");

  await expect(page.locator("h1")).toContainText("Test Blog");
});
```

👉 টেস্ট রান করো:

```bash
npx playwright test
```

---

## 🧪 Bonus: GitHub Actions এ Test Automation Setup করো (future)

👉 `.github/workflows/test.yml` ফাইল দিয়ে তুমি সব টেস্ট **CI/CD pipeline** এ চালাতে পারো।

---

## ✅ পর্ব ২৭ এর রেজাল্ট:

| ফিচার | স্টেটাস |
|--------|---------|
| ✅ Jest + RTL Setup | Done |
| ✅ Unit Test Example | Done |
| ✅ Playwright E2E Flow | Done |
| ✅ Login → Blog Create → Assert | Done |
| ✅ CI Ready Structure | ✅ |

---

## 🔜 পরবর্তী পর্ব:
**🧠 SaaS Blog CMS Architecture (Final Boss Level 💪)**  
✅ Multi-user  
✅ Each user has their own dashboard  
✅ Own blog, subdomain, design, analytics  
✅ Subscription ready

🟢 **চলবো কি SaaS Version Build করতে? তুমি চাইলে আমি প্রথমে architecture flow দেখাতে পারি!**
