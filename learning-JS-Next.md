একদম ঠিক জায়গায় আছো! 🧠💪 আমি তোমার জন্য বাংলা ভাষায় **৮ সপ্তাহের একদম গোছানো Fullstack Next.js শেখার রোডম্যাপ** বানিয়ে দিলাম, যেখানে জাভাস্ক্রিপ্ট, রিয়্যাক্ট, আর ফ্রন্টএন্ড থেকে শুরু করে ফুলস্ট্যাক Next.js শিখে রিয়েল প্রজেক্ট বানাতে পারবে।

---

# 🗓️ ৮ সপ্তাহে Fullstack Next.js শেখার বাংলা রোডম্যাপ

---

### ✅ **WEEK 1: JavaScript ES6+ মজবুত করা (প্রতিদিন ২ ঘন্টা)**
শিখবে ও প্র্যাকটিস করবে:
- `let`, `const` – কেন var বাদ?
- Arrow function: `()=>{}`  
- Destructuring: `const {name} = obj;`  
- Spread & Rest: `[...arr]`, `(...args)`  
- Template literals: `` `Hello ${name}` ``
- Promises: `.then().catch()`, `async/await`
- Array methods: `.map()`, `.filter()`, `.reduce()`

📚 Practice: [JavaScript.info](https://javascript.info/)  
🎯 Project: Simple To-Do App (Vanilla JS)

---

### ✅ **WEEK 2: React.js Basics (JSX + Component Structure)**
শিখবে:
- JSX কি ও কিভাবে কাজ করে
- React component বানানো (function-based)
- `props` দিয়ে data পাঠানো
- `useState` দিয়ে data রাখার নিয়ম
- `useEffect` দিয়ে side effects হ্যান্ডেল

🎯 Project:  
- Color Picker  
- Counter App  
- Weather API fetch with `useEffect`

📚 [React Official Tutorial](https://reactjs.org/tutorial/tutorial.html)

---

### ✅ **WEEK 3: React Routing + Component Structure**
শিখবে:
- `react-router-dom` দিয়ে routing  
- Reusable components (Navbar, Footer)
- Props drilling vs state lifting
- Controlled Form (input, textarea, button)

🎯 Project: Simple Blog UI with Navigation  
✏️ UI Design: TailwindCSS শিখে ইন্টিগ্রেট করো

---

### ✅ **WEEK 4: Next.js এর মূল বিষয়গুলো**
শিখবে:
- File-based Routing (`pages/`)
- Static Generation: `getStaticProps()`
- Server-side Rendering: `getServerSideProps()`
- Dynamic Routing: `[slug].js`
- Image optimization: `next/image`
- Head tag ব্যবহারে SEO boost

🎯 Project:  
- Static Blog Homepage  
- Blog Post Details Page (SSG + dynamic route)

📚 [Next.js Official Tutorial](https://nextjs.org/learn)

---

### ✅ **WEEK 5: API Routes ও Backend Logic**
শিখবে:
- `pages/api/hello.js` দিয়ে API বানানো  
- Request handling (GET, POST)
- JSON response দেয়া
- MongoDB Connect (with Mongoose or Prisma)
- ENV file ব্যাবহার করা

🎯 Project:  
- Contact Form → stores data in MongoDB  
- Newsletter Signup → API + DB save

---

### ✅ **WEEK 6: Authentication System**
শিখবে:
- `next-auth` দিয়ে login/signup  
- JWT token vs session cookies  
- Protected routes  
- User context তৈরি করা (React context API)

🎯 Project:  
- Login/Register UI  
- Profile page (Protected route)

---

### ✅ **WEEK 7: Fullstack Mini Project**
🎯 Project: **Task Manager / Notes App**  
ফিচার:
- Signup/Login  
- Notes Add/Edit/Delete  
- MongoDB backend  
- API Routes  
- Responsive UI (Tailwind)

এই প্রজেক্টে তুমি সব শিখা প্র্যাকটিস করবে।

---

### ✅ **WEEK 8: Final Project + Deploy**
🎯 Project: **Blog CMS**  
- Admin login  
- Add/Edit/Delete blog  
- Show blog list  
- Dynamic SEO pages  
- Deploy to Vercel  
- Use `slug` for blog routing

📌 Tools:
- MongoDB Atlas  
- Tailwind CSS  
- Vercel for free hosting

---

## 🏁 What You'll Achieve:
✅ JavaScript Mastery  
✅ React & JSX fluency  
✅ Full understanding of Next.js  
✅ Own Portfolio Projects  
✅ Deployment knowledge  
✅ Ready for Freelance / Job / SaaS building!

---

তুমি চাইলে আমি এই পুরো রোডম্যাপকে একটা **সপ্তাহভিত্তিক গুগল ডকস ট্র্যাকার বা PDF** বানিয়ে দিতে পারি, যাতে তোমার শেখা ট্র্যাক করা সহজ হয়।  
কি বলো, বানিয়ে দিই? 📘📅

---

দারুণ! এখন থেকে আমরা একদম শুরুর থেকে, **১ম সপ্তাহ (WEEK 1: JavaScript ES6+)** শুরু করবো। আমি একেকটি টপিককে খুব সহজ করে, ছোট উদাহরণসহ, ধাপে ধাপে শেখাবো যেন তুমি একবার পড়লেই বুঝে ফেলো। আজ আমরা শুরু করবো **`let` এবং `const`** দিয়ে।

---

# 🟢 JavaScript ES6+ – Day 1: `let`, `const`, এবং `var`

## 🧠 কনসেপ্ট বোঝো:

আগে আমরা সবসময় **`var`** ব্যবহার করতাম। কিন্তু এখন JavaScript-এ আধুনিকভাবে আমরা `let` ও `const` ব্যবহার করি।  
এগুলো দিয়ে **ভেরিয়েবল (data container)** ডিক্লেয়ার করা হয়।

---

## 📌 Syntax:
```javascript
let name = "Hamid";
const country = "Bangladesh";
```

---

## ⚖️ পার্থক্য (Real-life Example সহ)

| Feature      | `var`                | `let`                          | `const`                         |
|--------------|----------------------|--------------------------------|----------------------------------|
| পুনরায় ডিক্লেয়ার | পারা যায়               | পারা যায় না                    | পারা যায় না                     |
| মান পরিবর্তন | পারা যায়               | পারা যায়                      | পারা যায় না (Fixed মান)        |
| Scope        | Function-scoped       | Block-scoped                   | Block-scoped                    |

---

## 🎯 সহজ উদাহরণ:

### 🔹 `let` Example: 
```javascript
let age = 25;
age = 26; // মান বদলানো যাবে
console.log(age); // Output: 26
```

👉 **ব্যাখ্যা:** তুমি কোনো user এর বয়স ধরে রাখছো। বয়স তো পরিবর্তন হতে পারে, তাই `let` ব্যবহার করো।

---

### 🔹 `const` Example:
```javascript
const myName = "Sadia";
myName = "Nusrat"; // ❌ Error: const এর মান বদলানো যায় না
```

👉 **ব্যাখ্যা:** তোমার নাম একবার ডিক্লেয়ার করলে তা বদলায় না, তাই `const` ব্যবহার।

---

### 🔹 `var` Example (avoid করা উচিত):
```javascript
var name = "Anika";
var name = "Fatima"; // ✅ পারা যায়, কিন্তু এটা dangerous
console.log(name); // Output: Fatima
```

👉 **ব্যাখ্যা:** একই ভেরিয়েবল বারবার ডিক্লেয়ার করলে ভুল হতে পারে। তাই `let`/`const` বেশি নিরাপদ।

---

## 🚧 Scope (Block-scoped vs Function-scoped)

```javascript
{
  let x = 10;
  const y = 20;
  var z = 30;
}
console.log(z); // ✅ 30 (var is function-scoped)
console.log(x); // ❌ Error
console.log(y); // ❌ Error
```

👉 `let` এবং `const` ব্লকের বাইরে কাজ করে না — যেমন if বা for loop এর বাইরে।  
`var` সব জাগায় চলে যায় — যা সমস্যা করতে পারে।

---

## ✅ আজকের প্র্যাকটিস:
তুমি নিচের কাজগুলো করে নিজে চেস্টা করো:

1. তোমার নাম, বয়স, পছন্দের দেশ `const` দিয়ে লেখো  
2. আজকের তারিখ `let` দিয়ে লেখো, পরে সেটাকে পরিবর্তন করো  
3. একটা `var` দিয়ে কিছু লেখো, তারপর সেটা আবার declare করো — দেখো কী হয়

---

## ❓তোমার জন্য কুইজ:

```javascript
let a = 5;
a = 10;
console.log(a); // কী আসবে?

const b = "Hi";
// b = "Hello"; // এই লাইন চালু করলে কী হবে?
```

উত্তরটা নিজে বোঝার চেষ্টা করো। আমি চাইলে ব্যাখ্যা করে দিবো 😊

---

তুমি যদি আজকেরটা বুঝে থাকো, তাহলে বলো — আমি পরের টপিক **Arrow Function** শেখানো শুরু করবো 🔜  
নাকি একটু প্র্যাকটিস গাইড বা কুইজ আরো দেই? 📝

---
চমৎকার! 🎉 তাহলে আমরা এখন Week 1 এর **দ্বিতীয় টপিক: Arrow Function** এ এগিয়ে যাচ্ছি।

---

# 🟨 Day 2: Arrow Function (=>) — সহজ ভাষায়

## ✅ কি জিনিস এটা?

Arrow Function হলো **function লেখার একটা ছোট এবং আধুনিক স্টাইল**। ES6 থেকে এটা JavaScript-এ এসেছে।

🔁 আগের দিনে আমরা ফাংশন লিখতাম:
```javascript
function sayHello(name) {
  return "Hello " + name;
}
```

⚡️ এখন আমরা লিখতে পারি:
```javascript
const sayHello = (name) => {
  return "Hello " + name;
}
```

---

## 🧠 কেন ব্যবহার করবো?
- কোড ছোট ও ক্লিন হয়
- সহজে এক লাইনে ফাংশন লেখা যায়
- `this` keyword নিয়ে ঝামেলা কম

---

## ✅ উদাহরণ দিয়ে বুঝি

### 🔹 সাধারণ ফাংশন vs অ্যারো ফাংশন:

**সাধারণ ফাংশন:**
```javascript
function add(a, b) {
  return a + b;
}
```

**Arrow Function:**
```javascript
const add = (a, b) => {
  return a + b;
}
```

**আরও শর্ট:**
```javascript
const add = (a, b) => a + b;
```

👉 যদি **return** করার জন্য শুধু একটা লাইনে কাজ থাকে, তাহলে `{}` না দিলেও চলে।

---

## 💡 বাস্তব উদাহরণ:

ধরো তুমি একটা ওয়েবসাইটে user এর নাম greet করতে চাও:

```javascript
const greetUser = (name) => `Welcome, ${name}!`;

console.log(greetUser("Hamid")); // Output: Welcome, Hamid!
```

---

## ✅ আরও ছোট ছোট উদাহরণ:

🔸 ১টা সংখ্যা ২ দিয়ে গুণ করো:
```javascript
const double = (num) => num * 2;
console.log(double(5)); // Output: 10
```

🔸 কোন সংখ্যা জোড় নাকি বিজোড়, তা বলো:
```javascript
const isEven = (num) => num % 2 === 0;
console.log(isEven(4)); // true
```

---

## 🛑 যখন parameter ১টিই হয়:
```javascript
const square = n => n * n;
```
👉 `()` দরকার নেই যদি শুধু ১টা প্যারামিটার থাকে।

---

## ⚠️ Arrow Function এর একটা আলাদা বিষয় – `this`

আমরা এটা পরবর্তীতে বুঝবো, কিন্তু মনে রাখো:  
👉 Arrow Function এ `this` ভিন্নভাবে কাজ করে, যা object/class এ বুঝতে হবে।

---

## 📌 প্র্যাকটিস করো:

1. একটি ফাংশন লেখো যেটা তোমার বয়স ৫ দিয়ে গুণ করে  
2. একটি ফাংশন লেখো যেটা দেখে সংখ্যা ১০ এর বেশি কিনা  
3. একটি ফাংশন লেখো যেটা string নেয়, এবং "Hello, ___" আউটপুট দেয়

---

## ✅ কুইক কুইজ:
```javascript
const greet = name => "Hi " + name;
console.log(greet("Sadia"));
```
উত্তর কী হবে?

---

👉 তুমি যদি এই অংশটা বুঝে ফেলো, তাহলে পরের স্টেপ হবে:  
**Day 3: Destructuring – array/object থেকে ডাটা বের করার সহজ নিয়ম**

শুরু করবো? 😄

---
তোমার শেখার স্পিড ও আগ্রহ দেখে আমি মুগ্ধ! 🧠🔥  
এখন আমরা Week 1 এর **Day 3: Destructuring** টপিকে যাবো।

---

# 🟦 Day 3: Destructuring — Object বা Array থেকে ডেটা বের করার সহজ টেকনিক

## ✅ কী এটা?

Destructuring মানে হলো – **Object বা Array-এর ভেতর থেকে data আলাদা করে সহজভাবে বের করে নেয়া।**  
👉 মানে data কে “ভেঙে” বের করে আনা — that's why নাম হলো *Destructuring*।

---

## 📦 Object Destructuring (বাস্তব উদাহরণ সহ)

ধরো, তোমার কাছে একটা ইউজারের ইনফো আছে:
```javascript
const user = {
  name: "Hamid",
  age: 25,
  country: "Bangladesh"
};
```

🎯 এখন যদি তুমি name বের করতে চাও, traditionally লিখতে হতো:
```javascript
console.log(user.name); // Hamid
```

✅ এখন Destructuring দিয়ে:
```javascript
const { name, age } = user;
console.log(name); // Hamid
console.log(age);  // 25
```

👉 এখানে আমরা `user` object থেকে `name` ও `age` সরাসরি বের করে নিয়েছি।

---

## 🔁 Real-life উদাহরণ:

ধরো তুমি একটি ব্লগ সাইটে author info পাচ্ছো:

```javascript
const author = {
  fullName: "Dr. Safia",
  profession: "Aesthetic Dermatologist",
  city: "Dhaka"
};

const { fullName, city } = author;
console.log(`Author: ${fullName}, Location: ${city}`);
```

---

## 🔷 Array Destructuring

ধরো একটা array:
```javascript
const numbers = [10, 20, 30];
```

👉 traditionally:
```javascript
const a = numbers[0];
const b = numbers[1];
```

✅ Destructuring:
```javascript
const [a, b, c] = numbers;
console.log(a); // 10
console.log(b); // 20
console.log(c); // 30
```

---

## 💡 শুধু প্রথম item বা কিছু বাদ দিতে চাইলে:
```javascript
const [, second] = [1, 2, 3];
console.log(second); // 2
```

---

## 🧠 Default value set করা:
```javascript
const { name = "Guest", age = 18 } = {};
console.log(name); // Guest
```

👉 যদি object এ value না থাকে, তাহলে default মান সেট করা যাবে।

---

## 🔁 Function এর ভেতরে Destructuring:
```javascript
const printUser = ({ name, age }) => {
  console.log(`${name} is ${age} years old`);
};

printUser({ name: "Sadia", age: 22 });
```

---

## ✅ প্র্যাকটিস করো:

1. নিচের object থেকে destructure করে name ও skill বের করো:
```javascript
const dev = { name: "Nusrat", skill: "Next.js", level: "Beginner" };
```

2. নিচের array থেকে destructure করে ১ম ও ৩য় item বের করো:
```javascript
const fruits = ["apple", "banana", "mango"];
```

---

## ❓ কুইজ:
```javascript
const person = { name: "Anik", city: "Dhaka" };
const { name } = person;
console.log(name); // Output কী হবে?
```

---

👉 তুমি যদি এইটা বুঝে ফেলো, তাহলে পরবর্তী টপিক:
### **Day 4: Spread Operator & Rest Parameter** – এগুলো দিয়ে তুমি object/array কপি, marge, এবং dynamic arguments হ্যান্ডেল করতে পারবে।

শুরু করবো? 🧩

---
চল তাহলে শুরু করি! 😊  
আজ আমরা Week 1 এর **Day 4: Spread Operator & Rest Parameter** শিখবো—এই দুইটা দেখতে প্রায় একরকম হলেও কাজ একদম আলাদা।

---

# 🟠 Day 4: Spread Operator (`...`) এবং Rest Parameter (`...`) — একদম সহজ ভাষায়

## ✅ Spread Operator (`...`) — “**বিস্তার**” করে

Spread Operator মানে হলো —  
👉 **Object বা Array এর সব উপাদানকে খুলে ফেলা বা ছড়িয়ে দেওয়া।**

---

### 📦 উদাহরণ 1: Array কপি/মার্জ করা
```javascript
const nums = [1, 2, 3];
const newNums = [...nums, 4, 5];

console.log(newNums); // [1, 2, 3, 4, 5]
```

🔎 **ব্যাখ্যা:** `...nums` দিয়ে পুরানো array এর সব মান বের করে আনছি, এরপর নতুন মান জুড়ছি।

---

### 📦 উদাহরণ 2: Object কপি করা
```javascript
const user = { name: "Hamid", age: 25 };
const copyUser = { ...user };

console.log(copyUser); // { name: "Hamid", age: 25 }
```

🔎 ব্যাখ্যা: `...user` দিয়ে পুরো object এর মান নতুন object এ কপি করা হলো।

---

### 📦 উদাহরণ 3: Object এর মান override করা
```javascript
const user = { name: "Sadia", age: 22 };
const updatedUser = { ...user, age: 23 };

console.log(updatedUser); // age হবে 23
```

👉 Spread দিয়ে পুরানো মান আনলাম, তারপর age কে override করলাম।

---

## ✅ Rest Parameter (`...`) — “**বাকি সব ধরো**”

👉 এটা function এর ভেতর **অজানা সংখ্যক argument** ধরতে ব্যবহার হয়।

---

### 🧮 উদাহরণ:
```javascript
const sum = (...numbers) => {
  return numbers.reduce((acc, curr) => acc + curr, 0);
};

console.log(sum(1, 2, 3));      // Output: 6
console.log(sum(5, 10, 15, 20)); // Output: 50
```

🔎 ব্যাখ্যা: `...numbers` মানে সব ইনপুটগুলোকে array বানিয়ে নিচ্ছে।

---

### 📦 আরেকটা উদাহরণ (named argument + rest):
```javascript
const greet = (greeting, ...names) => {
  names.forEach(name => console.log(`${greeting}, ${name}!`));
};

greet("Hello", "Hamid", "Sadia", "Nusrat");
// Output:
// Hello, Hamid!
// Hello, Sadia!
// Hello, Nusrat!
```

---

## ⚠️ মূল পার্থক্য:

| Feature             | Spread (`...`)                         | Rest (`...`)                              |
|---------------------|----------------------------------------|-------------------------------------------|
| কাজ                 | Value ছড়িয়ে দেয়                      | বাকি সব value ধরে নেয় function-এ        |
| কোথায় ব্যবহার হয়    | Function call, object, array           | Function definition                       |
| উদাহরণ              | `[...arr]`, `{...obj}`                 | `(...args)`                               |

---

## ✅ প্র্যাকটিস করো:

1. একটা array কে spread করে নতুন মান যোগ করে দেখো  
2. একটা ফাংশন লেখো যেটা যেকোনো সংখ্যার সংখ্যাগুলোর গড় (average) বের করবে  
3. একটা object নিয়ে spread দিয়ে তার কোনো মান override করো  

---

## ❓ কুইজ:

```javascript
const person = { name: "Anik", city: "Dhaka" };
const updated = { ...person, city: "Chittagong" };
console.log(updated.city); // Output কী হবে?

const multiply = (...nums) => nums.map(n => n * 2);
console.log(multiply(1, 2, 3)); // Output কী হবে?
```

---

👉 যদি এই টপিকগুলো বুঝে ফেলো, তাহলে আমরা কাল শিখবো:
### **Day 5: Template Literals (`Hello ${name}`)** – JS এ smart string বানানোর সহজ উপায়।

তুমি কী বলতে চাও আমি পরের টপিকেই এগিয়ে যাই? 😄

---
তুমি একদম চমৎকার গতিতে শিখছো! 🧠💪  
এখন আমরা Week 1 এর **Day 5: Template Literals** নিয়ে শিখবো — এটা JavaScript-এ string বানানোর **সবচেয়ে সহজ আর প্রফেশনাল উপায়**।

---

# 🟩 Day 5: Template Literals — `${}` দিয়ে স্মার্ট স্ট্রিং বানানো

## ✅ কী এটা?

Template Literals হলো JavaScript-এর এমন একটা ফিচার, যেখানে তুমি **স্ট্রিং-এর মধ্যে ভেরিয়েবল বা এক্সপ্রেশন ইনজেক্ট** করতে পারো `${}` ব্যবহার করে।

---

## 📌 পুরনো পদ্ধতি vs নতুন পদ্ধতি:

### 🔸 পুরনো পদ্ধতিতে:
```javascript
const name = "Hamid";
const message = "Hello " + name + ", welcome!";
console.log(message);
```

### ✅ Template Literal দিয়ে:
```javascript
const name = "Hamid";
const message = `Hello ${name}, welcome!`;
console.log(message);
```

👉 তুমি এখন আর `+` দিয়ে ভেরিয়েবল বসাও না — `${}` দিয়ে সরাসরি বসাও।

---

## 💡 বাস্তব উদাহরণ ১: Greeting Message
```javascript
const user = "Sadia";
const time = "morning";
const greet = `Good ${time}, ${user}!`;
console.log(greet); // Good morning, Sadia!
```

---

## 💡 বাস্তব উদাহরণ ২: HTML এর ভিতরে ডাটা বসানো
```javascript
const title = "Next.js Tutorial";
const author = "Dr. Safia";

const html = `
  <h1>${title}</h1>
  <p>Written by ${author}</p>
`;

console.log(html);
```

👉 এটা React বা DOM এর ভিতরে Dynamic Content বসাতে খুব কাজে আসে।

---

## 🔁 Expression বসানো যায়:
```javascript
const a = 5;
const b = 10;
const result = `Sum is ${a + b}`;
console.log(result); // Sum is 15
```

---

## 📝 Multi-line স্ট্রিং লেখা যায় সহজে:
```javascript
const poem = `
Roses are red,
Violets are blue,
Next.js শেখা,
Best for you!
`;
console.log(poem);
```

👉 পুরনো স্টাইলে multi-line লেখতে `\n` লাগতো, এখানে লাগবে না।

---

## ✅ প্র্যাকটিস করো:

1. তোমার নাম, বয়স, শহর নিয়ে একটা sentence বানাও template literal দিয়ে  
2. দুইটা সংখ্যা নিয়ে "Total is ___" টাইপ মেসেজ বানাও  
3. একটা multi-line message বানাও যার মধ্যে একাধিক `${}` বসানো আছে

---

## ❓ কুইজ:

```javascript
const name = "Nusrat";
const job = "Developer";
console.log(`${name} is a ${job}.`);
```

উত্তর কী হবে?

---

🎯 যদি Template Literals পরিষ্কার বুঝে ফেলো, তাহলে কাল আমরা যাবো **Day 6: Promises** — JavaScript এর asynchronous কাজ হ্যান্ডেল করার ফাউন্ডেশন।

তুমি কি Promises শিখতে প্রস্তুত? 😄✨
---

তোমার শেখার আগ্রহ সত্যিই প্রশংসনীয়! 🧠🚀  
আজ আমরা Week 1 এর **Day 6: Promises** শিখবো — JavaScript-এ **asynchronous** কাজ (যেমন: API call, file read, delay) হ্যান্ডেল করার একটি স্ট্যান্ডার্ড উপায়।

---

# 🟪 Day 6: Promises — সময় লাগবে এমন কাজের জন্য প্রতিশ্রুতি!

## ✅ কী এটা?

👉 Promise হচ্ছে **"ভবিষ্যতে" একটা কাজ শেষ হলে আমাকে জানাবে"** এই চিন্তা।  
একটি Promise তিনটা অবস্থায় থাকতে পারে:

1. **Pending** – কাজ চলছে  
2. **Resolved (Fulfilled)** – কাজ শেষ, সফল  
3. **Rejected** – কাজ শেষ, কিন্তু ব্যর্থ

---

## 🎯 রিয়েল লাইফ উদাহরণ:

ধরো, তুমি একজন বন্ধুকে কল দাও—সে বলে:  
> “আমি পরে বলব কি করব।”

এটাই হলো একটা **Promise** — কারণ সে তখনই কিছু বলে না, পরে জানাবে।

---

## 📦 Promise বানানো (সিনট্যাক্স):
```javascript
const myPromise = new Promise((resolve, reject) => {
  // কিছু কাজ করো
  const success = true;

  if (success) {
    resolve("Task completed!");
  } else {
    reject("Task failed.");
  }
});
```

---

## 🔁 Promise ব্যবহার (then / catch দিয়ে):

```javascript
myPromise
  .then(result => {
    console.log("✅ Success:", result);
  })
  .catch(error => {
    console.log("❌ Error:", error);
  });
```

---

## 💡 বাস্তব উদাহরণ: Delay করা কাজ
```javascript
const waitFor3Seconds = () => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("3 seconds done!");
    }, 3000);
  });
};

waitFor3Seconds().then(msg => {
  console.log(msg); // 3 seconds done!
});
```

👉 এখানে আমরা ৩ সেকেন্ড অপেক্ষা করছি, তারপর মেসেজ দিচ্ছি।

---

## ✅ Practical API Call উদাহরণ (প্রথমবার দেখে রাখো):
```javascript
fetch('https://jsonplaceholder.typicode.com/posts/1')
  .then(response => response.json())
  .then(data => console.log("Post Title:", data.title))
  .catch(error => console.log("Error fetching data:", error));
```

---

## 🧠 `resolve()` মানে কাজ সফলভাবে শেষ — তখন `.then()` চলে  
## 🧠 `reject()` মানে কাজ ব্যর্থ — তখন `.catch()` চলে

---

## ✅ প্র্যাকটিস করো:

1. একটা Promise বানাও যেটা ২ সেকেন্ড পর “Done!” লিখে কনসোল করবে  
2. একটা Promise বানাও যেটা success বা error randomly দেখায়  
3. `.then()` এবং `.catch()` দিয়ে বুঝে নাও কখন কোনটা চলে

---

## ❓ কুইজ:

```javascript
const promiseTest = new Promise((resolve, reject) => {
  const pass = false;
  pass ? resolve("Success!") : reject("Failed!");
});

promiseTest
  .then(msg => console.log("✅", msg))
  .catch(err => console.log("❌", err));
```

👉 আউটপুট কী হবে?

---

🎯 তুমি যদি এটা ভালোভাবে বুঝে ফেলো, তাহলে পরবর্তী টপিক হবে:

### **Day 7: Array Methods — map, filter, reduce (ছোট data structure নিয়ে খেলা)**

শুরু করবো? 😄📊

---

চলো তাহলে এগিয়ে যাই! 😊  
আজ আমরা Week 1 এর **Day 7: JavaScript Array Methods – `map`, `filter`, `reduce`** শিখবো।  
এই তিনটি হলো JavaScript-এ **array নিয়ে কাজ করার সবচেয়ে শক্তিশালী এবং ব্যবহারিক ফাংশন।**

---

# 🟨 Day 7: `map()`, `filter()`, `reduce()` — ছোট ডাটা নিয়ে জাদু করার কৌশল

---

## ✅ ১. `map()` – প্রতিটি item থেকে নতুন value বানানো

### ➕ কাজ: প্রতিটি array element এর উপর কাজ করে **একটি নতুন array** তৈরি করে

---

### 📌 উদাহরণ ১: প্রতিটি সংখ্যাকে ২ দিয়ে গুণ করা

```javascript
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);

console.log(doubled); // [2, 4, 6, 8]
```

👉 ব্যাখ্যা: `map()` প্রতিটি item নেয়, তার উপর কাজ করে, এবং নতুন array দেয়।

---

### 📌 উদাহরণ ২: নামের লিস্টকে `Mr.` দিয়ে সাজানো

```javascript
const names = ["Hamid", "Sadia", "Nusrat"];
const titled = names.map(name => `Mr./Ms. ${name}`);

console.log(titled); // ["Mr./Ms. Hamid", "Mr./Ms. Sadia", "Mr./Ms. Nusrat"]
```

---

## ✅ ২. `filter()` – নির্দিষ্ট শর্ত অনুযায়ী item বেছে আনা

### ➕ কাজ: যেসব item নির্দিষ্ট শর্ত পূরণ করে, শুধু সেগুলো **new array** এ রাখে

---

### 📌 উদাহরণ ১: শুধু জোড় সংখ্যা বের করা

```javascript
const numbers = [1, 2, 3, 4, 5, 6];
const even = numbers.filter(num => num % 2 === 0);

console.log(even); // [2, 4, 6]
```

---

### 📌 উদাহরণ ২: শুধু পাস করা student এর নাম বের করা

```javascript
const students = [
  { name: "A", mark: 85 },
  { name: "B", mark: 45 },
  { name: "C", mark: 60 }
];

const passed = students.filter(s => s.mark >= 50);
console.log(passed); // A & C এর object
```

---

## ✅ ৩. `reduce()` – সব কিছু মিলিয়ে একটা মান তৈরি করা

### ➕ কাজ: পুরো array এর উপর কাজ করে **একটি single value** তৈরি করে

---

### 📌 উদাহরণ ১: সংখ্যার যোগফল বের করা

```javascript
const numbers = [10, 20, 30];
const total = numbers.reduce((acc, curr) => acc + curr, 0);

console.log(total); // 60
```

👉 ব্যাখ্যা:
- `acc` → accumulator (সঞ্চয় করে)
- `curr` → বর্তমান item
- `0` → শুরুতে acc এর মান

---

### 📌 উদাহরণ ২: object এর ভিতর সব student এর total mark বের করা

```javascript
const students = [
  { name: "A", mark: 50 },
  { name: "B", mark: 70 },
  { name: "C", mark: 80 }
];

const totalMarks = students.reduce((sum, student) => sum + student.mark, 0);
console.log(totalMarks); // 200
```

---

## 📋 পার্থক্য এক নজরে:

| Method   | কি করে | Output | Return |
|----------|--------|--------|--------|
| `map()`   | সব item থেকে নতুন মান তৈরি | Array | Same size array |
| `filter()`| নির্দিষ্ট শর্তে item বেছে নেয় | Array | ছোট বা সমান array |
| `reduce()`| সব item থেকে একটা মান বানায় | Value | একক মান (number, string, object) |

---

## ✅ প্র্যাকটিস করো:

1. একটা নামের list থেকে সব নাম `Hello, ___` ফরম্যাটে বানাও – `map()`  
2. একটা সংখ্যা list থেকে সব বিজোড় সংখ্যা বের করো – `filter()`  
3. একটা array দিয়ে সব সংখ্যার গড় বের করো – `reduce()` ব্যবহার করে

---

## ❓ কুইজ:

```javascript
const nums = [1, 2, 3, 4];

const result = nums
  .filter(n => n % 2 === 0)
  .map(n => n * 10);

console.log(result); // কী হবে?
```

---

🎯 যদি তুমি map-filter-reduce বুঝে ফেলো, তাহলে **কাল Week 1 এর Day 8: Final Practice & Mini Project Idea** নিয়ে এগোতে পারি।

তুমি কি সেটা চাইছো? 😄📚

---

চল তাহলে এগিয়ে যাই! 🟩  
আজ Week 1 এর **শেষ দিন – Day 8: রিভিশন + Mini Project Idea**!  
এই দিন আমরা যা শিখেছি তা রিভিশন করবো এবং সবগুলো কনসেপ্ট একসাথে প্র্যাকটিস করবো ছোট্ট একটি প্রজেক্ট আইডিয়ার মাধ্যমে।

---

# 🧪 Day 8: রিভিশন + Mini Project (JavaScript only)

---

## 🔁 যা শিখেছো এই সপ্তাহে (স্মার্ট রিভিশন)

| 🔢 টপিক | ✅ কাজ |
|--------|--------|
| `let`, `const` | ভেরিয়েবল ডিক্লেয়ার |  
| Arrow Function | শর্ট ফাংশন লিখা |  
| Destructuring | Object/Array থেকে মান বের করা |  
| Spread / Rest | মান ছড়ানো বা ধরা |  
| Template Literals | `${}` দিয়ে স্মার্ট স্ট্রিং |  
| Promises | সময়সাপেক্ষ async কাজ হ্যান্ডেল |  
| map/filter/reduce | Array নিয়ে জাদু |

---

# 📦 Mini Project: **Student Marks Manager**

### 🎯 Project Summary:
তুমি একটি ছোট প্রোগ্রাম বানাবে যেখানে:
- Student লিস্ট থাকবে (object আকারে)
- তাদের নাম, mark থাকবে
- তুমি map/filter/reduce ব্যবহার করে:
  - ✅ পাস করা ছাত্রদের বের করবে
  - ✅ নামসহ মেসেজ বানাবে
  - ✅ মোট নম্বর বের করবে

---

### ✅ Step 1: Student List (Object Array)
```javascript
const students = [
  { name: "Hamid", mark: 80 },
  { name: "Sadia", mark: 45 },
  { name: "Nusrat", mark: 70 },
  { name: "Anik", mark: 30 },
];
```

---

### ✅ Step 2: Filter – কে কে পাশ করলো?
```javascript
const passed = students.filter(student => student.mark >= 50);
console.log("Passed Students:", passed);
```

---

### ✅ Step 3: Map – সবাইকে অভিনন্দন দাও
```javascript
const greetings = passed.map(student => `🎉 Congrats, ${student.name}!`);
console.log(greetings);
```

---

### ✅ Step 4: Reduce – মোট মার্ক কত?
```javascript
const totalMarks = students.reduce((sum, student) => sum + student.mark, 0);
console.log("Total Marks of All Students:", totalMarks);
```

---

### ✅ Bonus: Average Mark
```javascript
const avg = totalMarks / students.length;
console.log("Average Mark:", avg.toFixed(2));
```

---

### 🔚 Output:
```
Passed Students: [Hamid, Nusrat]
["🎉 Congrats, Hamid!", "🎉 Congrats, Nusrat!"]
Total Marks: 225
Average Mark: 56.25
```

---

## 🎁 What You Practiced:
- Object array
- map, filter, reduce
- Arrow function
- Template literals
- Destructuring (try adding!)
- Clean code

---

## 📌 চাইলে তুমি এইটাকে একটা HTML UI দিয়ে বানাতে পারো, আর input নিতে পারো ইউজার থেকে। সেটা আমরা React/Next.js শিখে করবো।

---

## ✅ তোমার Week 1 সফলভাবে শেষ! 🎉

👉 এখন তুমি JavaScript এর এমন সব ফিচার শিখেছো যা React/Next.js শেখার জন্য একদম প্রস্তুত করে দিয়েছে।

---

### 🔜 আগামী সপ্তাহে শুরু হচ্ছে:  
# **WEEK 2: React.js – Component, Props, useState, useEffect**

তুমি কি প্রস্তুত আগামীকাল থেকে React শুরু করার জন্য? 😄📦  
তাহলে আমি Week 2 এর Day 1 প্ল্যান নিয়ে আসবো!

---

চমৎকার! 💥 তুমি একদম প্রস্তুত — এখন আমরা শুরু করবো **Week 2: React.js** এর শেখা।  
আজ আমাদের **Day 1: React Introduction + JSX + Component বানানো**।

---

# 🟦 Week 2 – Day 1: React Basics (JSX + Component + Structure)

---

## ✅ ১. React কি?

React হলো Facebook-এর তৈরি একটি JavaScript লাইব্রেরি, যেটা দিয়ে আমরা **interactive UI (User Interface)** বানাতে পারি।

👉 সহজভাবে বললে:
> React দিয়ে তুমি "পেইজ" বানাও ছোট ছোট **Component** আকারে—যেগুলো বারবার ব্যবহার করা যায়।

---

## 📦 ২. JSX – JavaScript XML

JSX হলো JavaScript-এর মধ্যে HTML লেখার একটি সুন্দর উপায়।

```jsx
const element = <h1>Hello World</h1>;
```

👉 উপরের কোডটি JavaScript + HTML এর মিশ্রণ — একে বলে JSX।

---

## 🧠 JSX নিয়ম:
1. একটা component **একটাই parent element** return করতে পারে  
2. সব tag properly বন্ধ করতে হবে (`<br />`, `<img />`)  
3. class এর বদলে `className` ব্যবহার করতে হবে  
4. inline style দিলে object আকারে দিতে হয়

---

## ✅ ৩. Component – React এর হৃদয়

React এ প্রতিটি UI অংশ = ১টি **Component**।

### 🔹 ২ ধরনের Component:
- **Functional Component (সবচেয়ে বেশি ব্যবহৃত)** ✅  
- Class Component (আগে ব্যবহার হতো)

---

### 📘 Functional Component উদাহরণ:
```jsx
function Welcome() {
  return <h1>Welcome to React!</h1>;
}
```

🔁 অথবা arrow function:
```jsx
const Welcome = () => {
  return <h1>Welcome to React!</h1>;
};
```

---

## ✅ ৪. Component কীভাবে কাজ করে?

- Component মানে একটা ফাংশন যেটা HTML (JSX) রিটার্ন করে  
- তুমি Component কে `<ComponentName />` দিয়ে ব্যবহার করো

### উদাহরণ:

```jsx
function Header() {
  return <h2>This is the header</h2>;
}

function App() {
  return (
    <div>
      <Header />
      <p>This is main content</p>
    </div>
  );
}
```

---

## 🧪 প্র্যাকটিস টাস্ক:

1. `HelloWorld` নামে একটা Component বানাও  
2. সেই Component এর ভেতরে `<h1>Hello, React!</h1>` রিটার্ন করো  
3. `App` Component এর ভিতরে `HelloWorld` Component কে ব্যবহার করো

---

## ❓ কুইজ:

```jsx
const Message = () => {
  return <p>Hello JSX!</p>;
};

function App() {
  return (
    <div>
      <Message />
    </div>
  );
}
```

👉 এখানে কী হবে output?

---

## ✅ আজকের শেখা:

| টপিক        | ব্যাখ্যা |
|-------------|---------|
| React কি?    | UI বানানোর জন্য JS লাইব্রেরি |
| JSX         | HTML + JS এর মিশ্রণ |
| Component   | Code ভাগ করার ছোট reusable block |
| Functional Component | ফাংশনের মতো কাজ করে, JSX return দেয় |

---

### 🔜 আগামীকাল:  
**Day 2 – Props এবং Component এর মধ্যে ডেটা পাঠানো**  
(মানে, কিভাবে এক component থেকে আরেকটায় তথ্য পাঠানো যায়)

তুমি প্রস্তুত থাকলে আমি পরের ক্লাস দিই! 😄✅

---

তাহলে চল! 😄  
আজ আমরা **Week 2 – Day 2: Props in React** শিখবো। এটা React-এর একদম মেইন কনসেপ্ট — এর মাধ্যমে এক Component থেকে অন্য Component-এ data পাঠানো যায়।

---

# 🟩 Day 2: **Props – Component এর মধ্যে তথ্য পাঠানো**

---

## ✅ ১. Props কি?

👉 **Props** মানে হচ্ছে "**properties**"। এগুলো parent component → child component এ data পাঠাতে ব্যবহৃত হয়।

> তুমি একটি component-এ value পাঠাও, এবং সেই component সেই value ব্যবহার করে।

---

## 📦 উদাহরণ:

### 🔹 Step 1: Parent থেকে data পাঠানো
```jsx
<Welcome name="Hamid" />
```

👉 এখানে `name="Hamid"` হচ্ছে **prop**

---

### 🔹 Step 2: Child Component এ props রিসিভ করা

```jsx
function Welcome(props) {
  return <h2>Hello, {props.name}!</h2>;
}
```

🧠 `props` হলো object – তুমি এর মধ্য থেকে value পেতে পারো `props.name` দিয়ে।

---

## ✅ ২. Destructuring করে আরো ছোটভাবে লেখা যায়:

```jsx
function Welcome({ name }) {
  return <h2>Hello, {name}!</h2>;
}
```

👉 এটা হলো ES6 destructuring – আগেই Week 1 এ শিখেছিলে!

---

## 🔁 বাস্তব উদাহরণ:

```jsx
function UserInfo({ name, age }) {
  return <p>{name} is {age} years old.</p>;
}

function App() {
  return (
    <div>
      <UserInfo name="Sadia" age={22} />
      <UserInfo name="Hamid" age={25} />
    </div>
  );
}
```

👉 Output:
```
Sadia is 22 years old.
Hamid is 25 years old.
```

---

## ✅ Props দিয়ে Image ও পাঠানো যায়:

```jsx
function Profile({ img, name }) {
  return (
    <div>
      <img src={img} alt="User" />
      <h3>{name}</h3>
    </div>
  );
}

function App() {
  return (
    <Profile 
      name="Nusrat" 
      img="https://example.com/user.jpg" 
    />
  );
}
```

---

## 💡 মনে রাখো:
- Props **read-only** → component ভিতরে পরিবর্তন করা যাবে না
- Props data পাঠাতে হয় parent → child দিকে
- Props নাম তোমার ইচ্ছামতো রাখতে পারো

---

## ✅ প্র্যাকটিস করো:

1. `PersonCard` নামে একটি Component বানাও  
   যেখানে name, age এবং hobby props হিসেবে যাবে  
2. App Component থেকে দুইজন ব্যক্তির data পাঠাও  
3. প্রতিটা person's details `p` tag এ দেখাও

---

## ❓ কুইজ:

```jsx
function Greet({ name }) {
  return <h2>Hello, {name}!</h2>;
}

function App() {
  return <Greet name="Nabila" />;
}
```

👉 Output কী হবে?

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Props | Component এ data পাঠানোর উপায় |
| Destructuring | props কে ছোট করে ব্যবহার করা |
| Parent → Child | data শুধু parent থেকে পাঠানো যায় |

---

### 🔜 আগামীকাল:  
**Day 3 – useState: Component এ data রাখা এবং update করার কৌশল**

👉 তুমি চাইলে আগেই শুরু করে দিতে পারি!

তুমি কি প্রস্তুত `useState` শিখতে? 😄📦

---

তাহলে চল! 😄  
আজ আমরা **Week 2 – Day 3: `useState`** শিখবো — এটা React-এ **Component এর ভিতরে data রাখার ও update করার সবচেয়ে গুরুত্বপূর্ণ কনসেপ্ট।**

---

# 🔵 Day 3: `useState()` – React Component এর ভিতরে data রাখো এবং বদলাও

---

## ✅ ১. `useState` কি?

React এ component এর ভিতরে কোনো data/মান রাখার জন্য `useState` ব্যবহার করা হয়।  
👉 Component যখন rerender হয়, তখন এই `state` এর মান ঠিকঠাক থাকে।

---

## 📦 Syntax:

```jsx
const [stateVariable, setStateFunction] = useState(initialValue);
```

### উদাহরণ:
```jsx
const [count, setCount] = useState(0);
```

- `count` → মান রাখে
- `setCount` → সেই মান পরিবর্তন করে
- `0` → প্রাথমিক মান

---

## ✅ ২. Counter App উদাহরণ:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h2>Count: {count}</h2>
      <button onClick={() => setCount(count + 1)}>➕</button>
      <button onClick={() => setCount(count - 1)}>➖</button>
    </div>
  );
}
```

👉 ব্যাখ্যা:
- যখন button-এ ক্লিক করো, `setCount()` নতুন মান দেয়
- Component আবার rerender হয়, এবং নতুন মান দেখায়

---

## 💡 তুমি চাইলেই text, boolean, array, object – সব টাইপের state রাখতে পারো।

---

### ✅ ৩. Text Input – Real-time update:

```jsx
function NameInput() {
  const [name, setName] = useState("");

  return (
    <div>
      <input 
        type="text" 
        onChange={(e) => setName(e.target.value)} 
        placeholder="Your name"
      />
      <p>Hello, {name}!</p>
    </div>
  );
}
```

👉 ব্যাখ্যা: ইউজার ইনপুট দিলে `setName()` দিয়ে মান পরিবর্তন হয়, তারপর পেজে দেখায়।

---

### ✅ ৪. Boolean Toggle:

```jsx
function Toggle() {
  const [isOn, setIsOn] = useState(false);

  return (
    <div>
      <p>Switch is {isOn ? "ON" : "OFF"}</p>
      <button onClick={() => setIsOn(!isOn)}>Toggle</button>
    </div>
  );
}
```

👉 ব্যাখ্যা: `!isOn` মানে "বর্তমানে যা আছে তার উল্টো", মানে true হলে false হবে, false হলে true হবে।

---

## 🛠️ প্র্যাকটিস করো:

1. Counter App – Add, Subtract, Reset button সহ
2. Text input → user name দেখাও live
3. ON/OFF toggle switch বানাও

---

## ❓ কুইজ:

```jsx
const [likes, setLikes] = useState(10);

<button onClick={() => setLikes(likes + 5)}>Like +5</button>
```

👉 ৩ বার ক্লিক করলে মান কত হবে?

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| useState | component এর ভিতরে মান রাখা |
| setState | মান পরিবর্তন করার function |
| Rerender | state update হলে UI আবার দেখায় |

---

### 🔜 আগামীকাল:  
**Day 4 – useEffect: React Component এ Side Effect হ্যান্ডেল করা (যেমন: API call, time delay)**

👉 তুমি যদি চাও, আমরা এখনই useEffect শিখে নিতে পারি।  
শুরু করবো? 😄🧪

---

তুমি অসাধারণভাবে এগিয়ে যাচ্ছো! 😎  
আজ আমরা **Week 2 – Day 4: `useEffect()`** শিখবো — এটি React-এর এমন একটি হুক, যা দিয়ে **side effects** হ্যান্ডেল করা হয়, যেমন:

- API থেকে data আনা  
- time delay দেওয়া  
- browser title পরিবর্তন করা  
- event listener add/remove করা

---

# 🟣 Day 4: `useEffect()` – React Component-এ কাজ চালানোর সময় ঠিক করা

---

## ✅ ১. useEffect কি?

👉 `useEffect()` হলো React এর একটি Hook, যা Component render হওয়ার পর কিছু **side effect** চালাতে দেয়।

> 💬 সহজভাবে: “Component render হলে আমি কিছু করতে চাই”—এই কাজের জন্যই useEffect!

---

## 📦 Syntax:
```jsx
import { useEffect } from 'react';

useEffect(() => {
  // এখানে তোমার কাজ (effect)
}, [dependency]);
```

---

## ✅ ২. বাস্তব উদাহরণ: Console log যখন Component render হয়

```jsx
import React, { useEffect } from 'react';

function Hello() {
  useEffect(() => {
    console.log("Component rendered!");
  }, []);

  return <h2>Hello World!</h2>;
}
```

👉 ব্যাখ্যা:
- `[]` মানে → component প্রথমবার render হলে effect চলবে
- console log হবে একবারই

---

## ✅ ৩. State update দেখে effect চালানো

```jsx
import React, { useState, useEffect } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log(`Count updated: ${count}`);
  }, [count]);

  return (
    <div>
      <button onClick={() => setCount(count + 1)}>Count: {count}</button>
    </div>
  );
}
```

👉 ব্যাখ্যা: যখনই `count` আপডেট হয়, তখন useEffect এর ভিতরের কাজ আবার চলে।

---

## ✅ ৪. API Call করা – খুব গুরুত্বপূর্ণ 🔥

```jsx
import React, { useEffect, useState } from 'react';

function PostTitle() {
  const [title, setTitle] = useState("");

  useEffect(() => {
    fetch('https://jsonplaceholder.typicode.com/posts/1')
      .then(res => res.json())
      .then(data => setTitle(data.title));
  }, []);

  return <h2>Post: {title}</h2>;
}
```

👉 ব্যাখ্যা: Component প্রথমবার render হলে API থেকে title এনে দেখানো হয়।

---

## 💡 Dependency Array: `[ ]`

| Dependency | ব্যাখ্যা |
|------------|----------|
| `[]` | শুধু প্রথমবার চলবে |
| `[count]` | count পরিবর্তন হলে চলবে |
| না দিলে | প্রতি render-এ চলবে (⚠️ avoid করো)

---

## 🛠️ প্র্যাকটিস করো:

1. একটা API থেকে ইউজারের নাম দেখাও (https://jsonplaceholder.typicode.com/users/1)  
2. যখনই কাউন্ট বাড়ে, তখন console log করো `Count updated`  
3. Component render হলে alert দেখাও (শুধু একবার)

---

## ❓ কুইজ:

```jsx
useEffect(() => {
  console.log("I run every time!");
});
```

👉 এটা কতবার চলবে?

---

## ✅ আজকের শেখা:

| useEffect() ব্যবহার | ব্যাখ্যা |
|----------------------|----------|
| Component load হলে | effect চালাতে |
| State change হলে     | নতুন কাজ চালাতে |
| API থেকে data আনতে | fetch দিয়ে async কাজ |

---

### 🔜 পরবর্তী টপিক:
**Day 5 – Controlled Input Form Handling in React**  
(ইনপুট ফিল্ডে টাইপ করলে ডেটা কিভাবে state এ রাখা হয়)

তুমি কি ফর্ম হ্যান্ডলিং শিখতে প্রস্তুত? 😄📝

---

তাহলে চল! 😊  
আজ আমরা শিখবো **Week 2 – Day 5: Controlled Input Form Handling in React**।  
এই টপিকটি তোমার ভবিষ্যতের **লগইন, রেজিস্ট্রেশন, সার্চ বক্স, কমেন্ট বক্স, কাস্টম ফর্ম**—সব কিছুর জন্য কাজে লাগবে।

---

# 🟢 Day 5: Controlled Form Input – React-এ ফর্ম কিভাবে কাজ করে?

---

## ✅ ১. Controlled Component কী?

👉 যখন একটি input element এর মান (value) কে React state এর মাধ্যমে নিয়ন্ত্রণ করা হয়, তখন তাকে বলে **controlled component**।

> তুমি যা টাইপ করো, সেটা state এ যায় → আর state থেকে দেখানো হয়।

---

### 📦 উদাহরণ: Name Input Box

```jsx
import React, { useState } from 'react';

function NameForm() {
  const [name, setName] = useState("");

  return (
    <div>
      <input 
        type="text"
        value={name}
        onChange={(e) => setName(e.target.value)}
        placeholder="Enter your name"
      />
      <p>Your name is: {name}</p>
    </div>
  );
}
```

👉 ব্যাখ্যা:
- `value={name}` → input box এর মান state থেকে নিয়ন্ত্রিত হচ্ছে
- `onChange` → টাইপ করলে `setName()` দিয়ে state আপডেট হয়

---

## ✅ ২. ফর্ম সাবমিশন হ্যান্ডল করা

```jsx
function SimpleForm() {
  const [email, setEmail] = useState("");

  const handleSubmit = (e) => {
    e.preventDefault(); // default page reload বন্ধ
    alert(`Your email: ${email}`);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input 
        type="email" 
        value={email} 
        onChange={(e) => setEmail(e.target.value)} 
        placeholder="Enter email"
      />
      <button type="submit">Submit</button>
    </form>
  );
}
```

👉 ব্যাখ্যা:
- ফর্ম সাবমিট করলে alert দেখায়
- `e.preventDefault()` দিয়ে পেজ রিলোড বন্ধ করি

---

## ✅ ৩. Multiple Input Field Handle করা

```jsx
function SignupForm() {
  const [form, setForm] = useState({ name: "", email: "" });

  const handleChange = (e) => {
    setForm({
      ...form,
      [e.target.name]: e.target.value
    });
  };

  return (
    <div>
      <input name="name" placeholder="Name" onChange={handleChange} />
      <input name="email" placeholder="Email" onChange={handleChange} />
      <p>Name: {form.name}, Email: {form.email}</p>
    </div>
  );
}
```

👉 এখানে `name` attribute দিয়ে বুঝি কোন ফিল্ড আপডেট হবে।

---

## ✅ তুমি যেকোনো input ট্যাগে এই নিয়মে কাজ করতে পারো:
- `text`
- `email`
- `number`
- `password`
- `textarea`

---

## 🧠 সংক্ষেপে মনে রাখো:
| জিনিস | কাজ |
|-------|-----|
| `value={state}` | input box এর মান নিয়ন্ত্রণ করে |
| `onChange={(e) => setState(e.target.value)}` | টাইপ করলে state আপডেট করে |
| `preventDefault()` | ফর্ম সাবমিটে পেজ রিলোড বন্ধ করে |

---

## 🛠️ প্র্যাকটিস করো:

1. `LoginForm` বানাও – email & password ইনপুট  
2. টাইপ করলে নিচে Live preview দেখাও  
3. Submit করলে alert করো “Welcome, [email]”

---

## ❓ কুইজ:

```jsx
const [msg, setMsg] = useState("");
<input value={msg} onChange={(e) => setMsg(e.target.value)} />
<p>{msg}</p>
```

👉 ইউজার টাইপ করলে কী হবে?

---

### ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Controlled Input | input এর মান state দিয়ে নিয়ন্ত্রণ |
| onChange | টাইপ করলে state আপডেট |
| Form Submit | সাবমিটে কাস্টম function চালানো |

---

### 🔜 আগামীকাল:
**Day 6 – Conditional Rendering & List Rendering in React**  
(যখন কিছু দেখাবো, কখন দেখাবো, কিভাবে দেখাবো – সবকিছুর কৌশল!)

👉 তুমি প্রস্তুত থাকলে আমি এখনই Day 6 শুরু করতে পারি। চালিয়ে দেবো? 😄📋

---

তাহলে চল! 😊  
আজ আমরা শিখবো **Week 2 – Day 6: Conditional Rendering & List Rendering in React**  
👉 React এ কিভাবে "যদি এই হয় তাহলে এটা দেখাও, না হলে ওটা" — এই টাইপ কাজ করা হয়, এবং কিভাবে লিস্ট (array) থেকে অনেকগুলো component দেখানো হয়।

---

# 🔷 Day 6: Conditional Rendering + List Rendering

---

## ✅ Part 1: **Conditional Rendering** – শর্তসাপেক্ষে কিছু দেখানো

> তুমি চাইছো: user logged in থাকলে তার নাম দেখাও, না থাকলে “Please log in” দেখাও।

---

### 📦 উদাহরণ ১: Simple if...else এর মতো

```jsx
function Welcome({ isLoggedIn }) {
  if (isLoggedIn) {
    return <h2>Welcome back!</h2>;
  } else {
    return <h2>Please log in.</h2>;
  }
}
```

---

### 📦 উদাহরণ ২: Inline ternary operator

```jsx
function Greet({ user }) {
  return (
    <h2>
      {user ? `Hello, ${user}` : "Guest, please log in"}
    </h2>
  );
}
```

🧠 **ব্যাখ্যা:**  
- `user ?` → যদি user থাকে  
- `: "..."` → না থাকলে এইটা

---

### 📦 উদাহরণ ৩: Show/hide based on condition

```jsx
function Message({ show }) {
  return (
    <div>
      {show && <p>This message is visible!</p>}
    </div>
  );
}
```

👉 `show && <p>` → show true হলে paragraph দেখাবে।

---

## ✅ Part 2: **List Rendering** – Array থেকে অনেক Component দেখানো

ধরো তোমার কাছে ইউজারদের একটা list আছে:

```jsx
const users = ["Hamid", "Sadia", "Nusrat"];
```

### 📦 `map()` দিয়ে Component তৈরি করো:

```jsx
function UserList() {
  const users = ["Hamid", "Sadia", "Nusrat"];

  return (
    <ul>
      {users.map((user, index) => (
        <li key={index}>👤 {user}</li>
      ))}
    </ul>
  );
}
```

👉 **ব্যাখ্যা:** `map()` দিয়ে প্রতিটা নাম `<li>` আকারে দেখানো হয়েছে  
👉 `key={index}` → React কে সাহায্য করে element track রাখতে

---

### 📦 Object Array থেকে list দেখানো:

```jsx
const students = [
  { id: 1, name: "Hamid", mark: 80 },
  { id: 2, name: "Sadia", mark: 75 },
];

function StudentList() {
  return (
    <div>
      {students.map((s) => (
        <p key={s.id}>{s.name} - {s.mark} marks</p>
      ))}
    </div>
  );
}
```

---

## 🛠️ প্র্যাকটিস করো:

1. ইউজার login থাকলে Welcome দেখাও, না থাকলে Login button দেখাও  
2. একটি নামের লিস্ট নিয়ে map() করে সব নাম দেখাও  
3. ৫টি প্রোডাক্ট এর নাম, দাম দিয়ে list দেখাও (object array)

---

## ❓ কুইজ:

```jsx
const items = ["Pen", "Book"];
return (
  <ul>
    {items.map(item => <li>{item}</li>)}
  </ul>
);
```

👉 এই কোডে কী দেখাবে?

---

## ✅ আজকের শেখা:

| টপিক               | ব্যাখ্যা                           |
|--------------------|------------------------------------|
| Conditional Rendering | যদি কোনো শর্ত সত্য হয় তবে কিছু দেখাও |
| `? :`               | inline শর্ত ব্যবহারে |
| List Rendering      | `map()` দিয়ে অনেক Component দেখানো |
| `key`               | প্রতিটি item এর unique identity |

---

### 🔜 আগামী টপিক:
**Day 7 – React Project: Profile Card + Button Toggle (JSX, Props, useState, Conditional)**  
এই পর্যন্ত শেখা জিনিস দিয়ে একটা মিনি প্রজেক্ট তৈরি করবো!

তুমি কি চাও আমি এখনই প্রজেক্ট শুরু করি? 😄📦

---

চমৎকার! 😎  
আজ আমরা করবো **Week 2 – Day 7: Mini React Project – Profile Card + Button Toggle**  
এই প্রজেক্টে আমরা একসাথে ব্যবহার করবো:  
✅ JSX, ✅ Props, ✅ useState, ✅ Conditional Rendering, ✅ List Rendering — সব কিছু!  

---

# 🧩 Day 7: React Mini Project – Profile Card App

---

## 🎯 প্রজেক্ট: ইউজারের প্রোফাইল কার্ড লিস্ট দেখানো  
+ show/hide বাটনের মাধ্যমে কার্ডগুলো টগল করা যাবে।

---

### ✅ Step 1: Dummy User Data (Array of objects)

```jsx
const users = [
  {
    id: 1,
    name: "Hamid",
    age: 25,
    profession: "Developer"
  },
  {
    id: 2,
    name: "Sadia",
    age: 22,
    profession: "Designer"
  },
  {
    id: 3,
    name: "Nusrat",
    age: 24,
    profession: "Marketer"
  }
];
```

---

### ✅ Step 2: ProfileCard Component (Reusable)

```jsx
function ProfileCard({ name, age, profession }) {
  return (
    <div style={{ border: "1px solid #ccc", padding: "10px", margin: "10px" }}>
      <h3>{name}</h3>
      <p>Age: {age}</p>
      <p>Profession: {profession}</p>
    </div>
  );
}
```

---

### ✅ Step 3: Main App Component

```jsx
import React, { useState } from 'react';

function App() {
  const [show, setShow] = useState(true);

  const users = [
    { id: 1, name: "Hamid", age: 25, profession: "Developer" },
    { id: 2, name: "Sadia", age: 22, profession: "Designer" },
    { id: 3, name: "Nusrat", age: 24, profession: "Marketer" },
  ];

  return (
    <div>
      <h2>👥 User Profile Cards</h2>
      <button onClick={() => setShow(!show)}>
        {show ? "Hide Profiles" : "Show Profiles"}
      </button>

      {show && (
        <div>
          {users.map(user => (
            <ProfileCard 
              key={user.id}
              name={user.name}
              age={user.age}
              profession={user.profession}
            />
          ))}
        </div>
      )}
    </div>
  );
}
```

---

## 💡 এখানে যা ব্যবহার করলাম:

| ফিচার | কাজ |
|-------|-----|
| `props` | ProfileCard এ data পাঠানো |
| `map()` | user list থেকে একাধিক কার্ড বানানো |
| `useState` | show/hide টগল কন্ট্রোল করা |
| `Conditional Rendering` | show সত্য হলে কার্ড দেখানো |

---

### ✅ Output:
```
👥 User Profile Cards
[Hide Profiles Button]

📋 Hamid - Developer  
📋 Sadia - Designer  
📋 Nusrat - Marketer
```

---

## 🛠️ চ্যালেঞ্জ (তুমি বাড়িতে করো):

1. একটা Search Input দাও → নাম দিয়ে ইউজার ফিল্টার করো  
2. পছন্দের ইউজার Card এ একটি ❤️ Like বাটন দাও  
3. ProfileCard Component এ Image যোগ করো (placeholder বা avatar)

---

## ✅ আজকের শেখা:

| কনসেপ্ট | রিয়েল প্রয়োগ |
|----------|--------------|
| Props    | Card এ data পাঠানো |
| JSX      | UI তৈরি |
| useState | show/hide কন্ট্রোল |
| map      | list থেকে UI বানানো |
| Conditional Rendering | টগল ফিচার |

---

### 🔚 Tomorrow:  
**Day 8 – Week 2 Final Project Idea + Review**  
(React এর সব শিখা একসাথে ব্যবহার করে বড় কিছু তৈরি করার প্রস্তুতি)

তুমি কি Week 2 এর ফাইনাল রিভিউ এবং প্রজেক্ট আইডিয়া নিয়েও এগোতে চাও এখনই? 😄🔥

---

তুমি সত্যিই অসাধারণভাবে ধারাবাহিকতা ধরে রেখেছো! 🧠🔥  
আজ আমরা করবো **Week 2 – Day 8: Final Review + Full React Mini Project Idea**  
এটা তোমার জন্য একটা বড় recap হবে — আর আমরা সাজিয়ে দেবো একটা **React Mini Project** যা Week 2 এর সবকিছু একসাথে প্র্যাকটিস করাবে।

---

# 🧠 Day 8: Final Recap + Full React Project Idea

---

## 🔁 রিভিশন: Week 2 এ তুমি যা শিখেছো

| দিন | শিখেছো |
|-----|--------|
| ✅ Day 1 | React intro, JSX, Functional Component |
| ✅ Day 2 | Props দিয়ে data পাঠানো |
| ✅ Day 3 | useState দিয়ে ডেটা রাখা ও আপডেট |
| ✅ Day 4 | useEffect দিয়ে side effect চালানো |
| ✅ Day 5 | Controlled Form (input handling) |
| ✅ Day 6 | Conditional rendering + map() list rendering |
| ✅ Day 7 | Profile Card Mini App with toggle |

---

## 🎯 Final Project Idea: **React Contact List App**

> এটা একধরনের "Digital Phone Book" — যেখানে ইউজারদের নাম, ফোন নম্বর যোগ করা, দেখা, খোঁজা যাবে।

---

## ✅ Feature List:

1. **Add Contact** – ফর্ম দিয়ে নাম ও ফোন নম্বর ইনপুট  
2. **Show All Contacts** – map() করে কার্ড আকারে দেখানো  
3. **Toggle Show/Hide List** – বাটন দিয়ে কন্ট্রোল  
4. **Search Contact by Name** – live input দিয়ে filter  
5. ✅ Bonus: like button, delete button

---

## 🛠️ Structure:

```jsx
<App />
  ├── <ContactForm />     ← নাম, নম্বর ইনপুট
  ├── <SearchBox />       ← ফিল্টার করার ইনপুট
  └── <ContactList />     ← সব কন্টাক্টের কার্ড
        └── <ContactCard /> ← প্রতিটি ইউজারের তথ্য
```

---

## 🔧 Core Concepts You'll Use:

| কনসেপ্ট | প্রয়োগ |
|---------|--------|
| `useState` | contacts add, search, show/hide |
| `props` | data পাঠানো child components-এ |
| `map()` | list দেখানো |
| `filter()` | search logic |
| `conditional rendering` | show/hide, message |

---

## 📌 Example Output:

```
📱 My Contacts
[Search by name: ________ ]

👤 Sadia | 📞 017...
👤 Hamid | 📞 018...
[Add New Contact]
```

---

## ✅ তুমি চাইলে আমি এই Full Project এর Step-by-Step কোড + গাইড দিয়ে দিতে পারি  
👉 এটা Week 3 এ গিয়ে করতে পারো বা এখনই চাইলে শুরু করতে পারো।

তুমি কি চাও আমি Contact List Project এর full plan & code শুরু করে দিই? 😄📲  
নাকি Week 3 (Next.js Start) তে যাই?

---

দারুণ! 🎉  
তাহলে আমরা এখন করবো তোমার চাহিদামতো **React Full Project – Contact List App**  
এই প্রজেক্টে আমরা একসাথে ব্যবহার করবো:

✅ `useState`  
✅ `props`  
✅ Controlled Form  
✅ List Rendering  
✅ Search Filter  
✅ Conditional Rendering  

---

# 🟢 Project: **React Contact List App** (Full Code with Comments)

---

### ✅ Step 1: `App.js`

```jsx
import React, { useState } from "react";
import ContactForm from "./ContactForm";
import ContactCard from "./ContactCard";
import SearchBox from "./SearchBox";

function App() {
  const [contacts, setContacts] = useState([]);
  const [searchTerm, setSearchTerm] = useState("");
  const [showList, setShowList] = useState(true);

  const handleAddContact = (contact) => {
    setContacts([...contacts, contact]);
  };

  const filteredContacts = contacts.filter(c =>
    c.name.toLowerCase().includes(searchTerm.toLowerCase())
  );

  return (
    <div style={{ maxWidth: "600px", margin: "auto", padding: "20px" }}>
      <h2>📱 My Contacts</h2>

      <button onClick={() => setShowList(!showList)}>
        {showList ? "Hide Contacts" : "Show Contacts"}
      </button>

      <SearchBox searchTerm={searchTerm} setSearchTerm={setSearchTerm} />
      <ContactForm onAdd={handleAddContact} />

      {showList && (
        <div>
          {filteredContacts.length === 0 ? (
            <p>No contacts found.</p>
          ) : (
            filteredContacts.map((contact, index) => (
              <ContactCard key={index} name={contact.name} phone={contact.phone} />
            ))
          )}
        </div>
      )}
    </div>
  );
}

export default App;
```

---

### ✅ Step 2: `ContactForm.js`

```jsx
import React, { useState } from "react";

function ContactForm({ onAdd }) {
  const [form, setForm] = useState({ name: "", phone: "" });

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    if (form.name.trim() && form.phone.trim()) {
      onAdd(form);
      setForm({ name: "", phone: "" });
    }
  };

  return (
    <form onSubmit={handleSubmit} style={{ marginTop: "20px" }}>
      <input
        name="name"
        placeholder="Name"
        value={form.name}
        onChange={handleChange}
        required
      />
      <input
        name="phone"
        placeholder="Phone"
        value={form.phone}
        onChange={handleChange}
        required
      />
      <button type="submit">Add Contact</button>
    </form>
  );
}

export default ContactForm;
```

---

### ✅ Step 3: `ContactCard.js`

```jsx
import React from "react";

function ContactCard({ name, phone }) {
  return (
    <div style={{ border: "1px solid #ccc", margin: "10px", padding: "10px" }}>
      <h3>{name}</h3>
      <p>📞 {phone}</p>
    </div>
  );
}

export default ContactCard;
```

---

### ✅ Step 4: `SearchBox.js`

```jsx
import React from "react";

function SearchBox({ searchTerm, setSearchTerm }) {
  return (
    <input
      type="text"
      placeholder="Search by name"
      value={searchTerm}
      onChange={(e) => setSearchTerm(e.target.value)}
      style={{ margin: "15px 0", width: "100%" }}
    />
  );
}

export default SearchBox;
```

---

## ✅ ফোল্ডার স্ট্রাকচার সাজাও এভাবে:
```
📁 src/
├── App.js
├── ContactForm.js
├── ContactCard.js
└── SearchBox.js
```

---

## 🧠 তুমি এখন কী শিখলে এই প্রজেক্ট থেকে:

| ফিচার | প্রয়োগ |
|-------|--------|
| `useState` | data রাখার জন্য (contacts, searchTerm, showList) |
| `props` | form → App → card এ data পাঠানো |
| `map()` | list দেখানো |
| `filter()` | খোঁজা |
| Form Handling | controlled input |
| Conditional Rendering | Show/hide, no result message |

---

✅ এখন তুমি চাইলে এই প্রজেক্টে ✅ delete button, ✅ localStorage (data save) ✅ validation message – এসব ফিচারও যোগ করতে পারো।

---

### 🔜 এখন তুমি একদম প্রস্তুত **Week 3: Next.js শেখা** শুরু করার জন্য!  
তুমি চাইলে আমি এখনই **Week 3 – Day 1: Next.js Intro + Page Routing** দিয়ে শুরু করতে পারি।

**তাই বলো — Next.js নিয়ে যাত্রা শুরু করবো? 😄🚀**

---

অসাধারণ! 🎉 তুমি সফলভাবে React-এর ভিত্তি তৈরি করে ফেলেছো।  
এখন আমরা শুরু করবো **Fullstack Web Development with Next.js – Week 3**  
👉 আজ: **Day 1 – Next.js Introduction + File-based Routing System**

---

# 🟦 Week 3 – Day 1: Next.js Intro + Page Routing

---

## ✅ ১. Next.js কি?

Next.js হলো React-এর উপর ভিত্তি করে বানানো একটি **Fullstack Framework**, যা দিয়ে তুমি:
- Static ও Dynamic Page বানাতে পারো  
- Server-side rendering (SSR) ও Static Site Generation (SSG) করতে পারো  
- API Route ও Backend logic লিখতে পারো  
- SEO-friendly ওয়েবসাইট খুব সহজে বানাতে পারো

> 👉 Next.js = React + Routing + SSR + API + Optimization ✅

---

## ✅ ২. Next.js প্রজেক্ট শুরু করার নিয়ম:

### 🔧 Step-by-Step:

```bash
npx create-next-app@latest my-next-app
```

👉 তারপর টাইপ করো:
```bash
cd my-next-app
npm run dev
```

➡️ তোমার ব্রাউজারে চালাও:  
**http://localhost:3000**

---

## ✅ ৩. ফোল্ডার স্ট্রাকচার:

```
📁 pages/         ← তোমার সব পেজ থাকবে এখানে
📁 public/        ← image, asset file
📁 styles/        ← CSS ফাইল
📁 app/ (v13+)    ← App Router (নতুন ভার্সনে)
```

---

## ✅ ৪. Page বানানো – File-Based Routing

Next.js এ route বানাতে কোনো “React Router” লাগবে না।  
তুমি শুধু ফাইল তৈরি করলেই route হয়ে যাবে!

---

### 📘 উদাহরণ ১: Home Page

`pages/index.js`

```jsx
export default function Home() {
  return <h1>🏠 Welcome to Home Page</h1>;
}
```

➡️ URL: **http://localhost:3000**

---

### 📘 উদাহরণ ২: About Page

`pages/about.js`

```jsx
export default function About() {
  return <h1>About Us</h1>;
}
```

➡️ URL: **http://localhost:3000/about**

---

### 📘 উদাহরণ ৩: Contact Page

`pages/contact.js`

```jsx
export default function Contact() {
  return <h1>Contact Us</h1>;
}
```

➡️ URL: **http://localhost:3000/contact**

---

## ✅ ৫. Component বানিয়ে Import করো

`components/Header.js`

```jsx
export default function Header() {
  return <h2>This is the Header</h2>;
}
```

`pages/index.js` এ ব্যবহার করো:

```jsx
import Header from '../components/Header';

export default function Home() {
  return (
    <div>
      <Header />
      <p>Welcome to my site!</p>
    </div>
  );
}
```

---

## ✅ ৬. Link ব্যবহার – SPA Navigation

Next.js এ `<a>` ট্যাগ না দিয়ে **`<Link />`** ব্যবহার করতে হয়:

```jsx
import Link from 'next/link';

export default function Navbar() {
  return (
    <nav>
      <Link href="/">Home</Link> |
      <Link href="/about">About</Link> |
      <Link href="/contact">Contact</Link>
    </nav>
  );
}
```

👉 এটি SEO-friendly এবং fast navigation দেয়

---

## ✅ আজকের প্র্যাকটিস:

1. Next.js App তৈরি করো  
2. ৩টি পেজ বানাও – Home, About, Contact  
3. Navbar component বানাও এবং `<Link>` দিয়ে রাউটিং করো  
4. প্রতিটি পেজে আলাদা করে `<Header />` দেখাও

---

## ❓ কুইজ:

```jsx
// pages/blog.js

export default function Blog() {
  return <h1>My Blog</h1>;
}
```

➡️ কোন URL এ এটা দেখা যাবে?

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Next.js | React-এর ওপর বানানো Fullstack Framework |
| File-based Routing | ফাইল বানালেই route হয়ে যায় |
| Link Component | Page navigation করার উপায় |
| Component Import | React Component এর মতোই |

---

### 🔜 আগামীকাল:
**Day 2 – Dynamic Pages (Routing with Parameters), Nested Routing, Custom 404 Page**

তুমি চাইলে আমি এখনই **Day 2** শুরু করে দিতে পারি।  
তুমি কি প্রস্তুত Next.js এর Dynamic Routing শেখার জন্য? 😄📂

---

তাহলে চল! 😎  
আজ আমরা করবো **Week 3 – Day 2: Dynamic Routing + Nested Routes + Custom 404 Page**  
এই টপিকের মাধ্যমে তুমি বুঝবে কিভাবে Next.js এ dynamic URL তৈরি করা হয়—যেমন `/product/123` বা `/user/hamid`—একদমই React Router ছাড়াই!

---

# 🔷 Day 2: Dynamic Routes, Nested Routes, Custom 404

---

## ✅ ১. Dynamic Routing (URL-এর ভিতরের ডাটা ধরো)

Next.js এ Dynamic Page বানানোর জন্য তুমি `[]` bracket ব্যবহার করো।

---

### 📘 উদাহরণ: `/blog/[id].js`

`pages/blog/[id].js` ফাইল বানাও 👇

```jsx
import { useRouter } from 'next/router';

export default function BlogPost() {
  const router = useRouter();
  const { id } = router.query;

  return <h1>📝 Blog ID: {id}</h1>;
}
```

👉 এখন তুমি গেলে `/blog/5` বা `/blog/hello` — সব কাজ করবে!

---

## 💡 ব্যাখ্যা:

| Route             | Component Path         | Value of `id` |
|------------------|------------------------|----------------|
| `/blog/123`      | `pages/blog/[id].js`   | `"123"`        |
| `/blog/react-js` | `pages/blog/[id].js`   | `"react-js"`   |

---

## ✅ ২. Nested Routes (ভেতরে ভেতরে page structure)

Next.js এ folder বানিয়ে nested page বানানো যায়।

---

### 📘 উদাহরণ:

```
pages/
 └── products/
      ├── index.js          → /products
      └── [productId].js    → /products/123
```

`products/index.js`:
```jsx
export default function ProductList() {
  return <h2>📦 All Products</h2>;
}
```

`products/[productId].js`:
```jsx
import { useRouter } from 'next/router';

export default function ProductDetails() {
  const { productId } = useRouter().query;

  return <h2>Product ID: {productId}</h2>;
}
```

---

## ✅ ৩. Custom 404 Page

`pages/404.js` ফাইল বানাও। যখন কোনো page পাওয়া যাবে না, তখন এটিই দেখাবে।

```jsx
export default function Custom404() {
  return (
    <div style={{ textAlign: 'center', marginTop: '100px' }}>
      <h1>😢 404 - Page Not Found</h1>
      <p>The page you're looking for doesn't exist.</p>
    </div>
  );
}
```

➡️ এখন যদি তুমি `/something-wrong` টাইপ route দেখো যা নেই, এটা show করবে।

---

## ✅ প্র্যাকটিস করো:

1. `pages/blog/[id].js` বানাও এবং ID দেখাও  
2. `pages/user/[username].js` বানাও — সেখানে ইউজারের নাম দেখাও  
3. `products/` ফোল্ডারে nested dynamic route তৈরি করো  
4. Custom 404 পেজ বানাও

---

## ❓ কুইজ:

তুমি যদি ফাইল বানাও: `pages/user/[id].js`  
👉 কোন URL এ এটা কাজ করবে?

---

## ✅ আজকের শেখা:

| টপিক             | ব্যাখ্যা |
|------------------|----------|
| Dynamic Route     | [] দিয়ে variable route তৈরি |
| Nested Routing    | ফোল্ডার দিয়ে ভেতরে পেজ বানানো |
| useRouter         | URL থেকে ডেটা বের করার হুক |
| Custom 404 Page   | নিজস্ব Not Found পেজ তৈরি |

---

### 🔜 আগামীকাল:
**Day 3 – Static Site Generation (SSG) & Server-side Rendering (SSR)**  
👉 তুমি শিখবে কখন কীভাবে page data build-এ আনবে, আর কখন server থেকে আনবে।

তুমি কি Day 3 শুরু করতে চাও? 😄🧠

---

