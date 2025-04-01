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

চল তাহলে! 😊  
আজ আমরা শিখবো **Week 3 – Day 3: SSG (Static Site Generation) vs SSR (Server-Side Rendering)** — Next.js এর সবচেয়ে গুরুত্বপূর্ণ কনসেপ্ট!  
👉 এটা দিয়ে তুমি ঠিক করো: কোনো পেজ **build time এ static বানাবে**, নাকি **প্রতি request এ server থেকে ডেটা এনে দেখাবে**।

---

# 🟡 Day 3: SSG vs SSR – Data fetching in Next.js

---

## ✅ ১. Static Site Generation (SSG)

> 📦 পেজ build time-এ তৈরি হয়ে যায় → পরে ইউজার যখন আসে, তখন আর server call লাগে না।

✅ দ্রুত লোড হয়  
✅ SEO-friendly  
✅ Data খুব কম পরিবর্তন হয় এমন পেজের জন্য perfect

---

### 📘 উদাহরণ – SSG with `getStaticProps`

```jsx
export async function getStaticProps() {
  return {
    props: {
      name: "Hamid"
    }
  };
}

export default function Home({ name }) {
  return <h2>Hello, {name}! (Static Page)</h2>;
}
```

🧠 ব্যাখ্যা:
- এই পেজ build time এ বানানো হবে  
- ইউজার যখন page খুলবে, server call লাগবে না

---

## ✅ ২. Server-Side Rendering (SSR)

> 🖥️ প্রতি request-এ পেজ নতুন করে server থেকে data নিয়ে বানানো হয়।

✅ Real-time Data  
✅ User-specific content  
❌ একটু স্লো, কারণ প্রতি বার data fetch হয়

---

### 📘 উদাহরণ – SSR with `getServerSideProps`

```jsx
export async function getServerSideProps() {
  const time = new Date().toLocaleTimeString();

  return {
    props: {
      time
    }
  };
}

export default function LivePage({ time }) {
  return <h2>Current Time: {time} (Server Rendered)</h2>;
}
```

➡️ এখন তুমি পেজ reload করলেই নতুন সময় পাবে!

---

## ✅ পার্থক্য – এক নজরে

| বিষয়             | SSG                          | SSR                          |
|------------------|------------------------------|------------------------------|
| কখন চালায়?       | Build time                   | প্রতিটি request সময়          |
| Speed            | খুব দ্রুত                    | তুলনামূলক ধীর               |
| SEO              | ভালো                         | ভালো                         |
| Use case         | Static content (e.g. blog)   | Real-time content (e.g. profile, dashboard) |

---

## ✅ ৩. getStaticPaths – Dynamic SSG

> যদি তোমার পেজ dynamic হয়, কিন্তু static generate করতে চাও

---

### 📘 উদাহরণ – `/blog/[id].js` এর জন্য static path তৈরি

```jsx
export async function getStaticPaths() {
  return {
    paths: [
      { params: { id: "1" } },
      { params: { id: "2" } }
    ],
    fallback: false
  };
}

export async function getStaticProps({ params }) {
  return {
    props: {
      id: params.id
    }
  };
}

export default function BlogPost({ id }) {
  return <h2>Static Blog Post #{id}</h2>;
}
```

🧠 ব্যাখ্যা: build time-এ `/blog/1` এবং `/blog/2` পেজ static আকারে বানিয়ে ফেলা হবে

---

## 🛠️ আজকের প্র্যাকটিস:

1. `pages/static.js` → বানাও SSG page (getStaticProps)  
2. `pages/server.js` → বানাও SSR page (getServerSideProps)  
3. `pages/product/[id].js` → বানাও static dynamic page with `getStaticPaths`

---

## ❓ কুইজ:

```jsx
export async function getServerSideProps() {
  return {
    props: { status: "LIVE" }
  };
}
```

👉 এই কোড কোন rendering method ব্যবহার করছে?

---

## ✅ আজকের শেখা:

| কনসেপ্ট | ব্যাখ্যা |
|----------|----------|
| SSG (`getStaticProps`) | পেজ build time এ তৈরি |
| SSR (`getServerSideProps`) | প্রতিবার রিকোয়েস্টে রান করে |
| `getStaticPaths` | ডায়নামিক URL সাপোর্ট করে SSG তে |

---

### 🔜 আগামী টপিক (Day 4):  
**API Routes in Next.js – Backend code লিখো React ছাড়াই!**

👉 তুমি Next.js দিয়ে নিজে API বানাতে পারবে, যেমন: `/api/hello`, `/api/contact`

তুমি কি এখনই API Routes শেখা শুরু করতে চাও? 😄🔧

---

চল তাহলে শুরু করি! 😄  
আজ আমরা করবো **Week 3 – Day 4: API Routes in Next.js**  
👉 এই টপিকে তুমি শিখবে কিভাবে Next.js এর ভিতরেই backend/server logic লিখে নিজস্ব API বানাতে পারো — আলাদা Node.js server ছাড়াই।

---

# 🟧 Day 4: API Routes – Backend কাজ Next.js এ করো

---

## ✅ ১. API Route মানে কী?

👉 Next.js এ `pages/api/` ফোল্ডারে ফাইল বানালে, সেটা একটি **API endpoint** হিসেবে কাজ করে।

> তুমি নিজের বানানো URL দিয়ে data পাঠাতে বা নিতে পারো — ঠিক যেমন Express.js দিয়ে করো।

---

## 🔧 Structure:

```
pages/
 └── api/
      └── hello.js      → /api/hello
```

---

## ✅ ২. Hello API বানাও

`pages/api/hello.js`

```js
export default function handler(req, res) {
  res.status(200).json({ message: "Hello from Next.js API!" });
}
```

🧠 এই API-তে গেলে:  
**http://localhost:3000/api/hello**  
➡️ Output:
```json
{ "message": "Hello from Next.js API!" }
```

---

## ✅ ৩. Query Handle করো (GET Request)

```js
export default function handler(req, res) {
  const { name } = req.query;

  res.status(200).json({
    message: `Hello, ${name || "Guest"}!`
  });
}
```

➡️ Visit: `/api/hello?name=Hamid`  
📤 Output:
```json
{ "message": "Hello, Hamid!" }
```

---

## ✅ ৪. POST Request Handle করো

```js
export default function handler(req, res) {
  if (req.method === "POST") {
    const { name } = req.body;
    return res.status(200).json({ message: `Hello, ${name}` });
  } else {
    res.status(405).json({ error: "Only POST allowed" });
  }
}
```

---

### 👉 Frontend থেকে fetch করো:

```js
const res = await fetch('/api/hello', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name: "Hamid" })
});
const data = await res.json();
console.log(data.message);
```

---

## ✅ ৫. Real-life Example – Contact API

`pages/api/contact.js`

```js
export default function handler(req, res) {
  if (req.method === "POST") {
    const { name, email, message } = req.body;
    console.log("New message from:", name);
    return res.status(200).json({ status: "Message received" });
  }

  res.status(405).json({ error: "Only POST allowed" });
}
```

✅ এবার তোমার frontend form থেকে এই API তে POST করা যাবে।

---

## ✅ Summary: তুমি এখন নিজেই Backend লিখতে পারো!

| বিষয় | ব্যাখ্যা |
|------|----------|
| API route | `pages/api/filename.js` |
| GET method | URL query handle |
| POST method | body থেকে data নেয় |
| req, res | Express.js এর মতোই |

---

## 🛠️ আজকের প্র্যাকটিস:

1. `/api/hello` বানাও — GET request handle করো  
2. `/api/greet` বানাও — name query নাও  
3. `/api/contact` বানাও — POST এ name + message নাও  
4. API তে JSON ফরম্যাটে উত্তর দাও

---

## ❓ কুইজ:

```js
export default function handler(req, res) {
  if (req.method === "GET") {
    return res.status(200).json({ status: "ok" });
  }
}
```

👉 `/api/status` এ গেলে কী রেসপন্স আসবে?

---

### 🔜 আগামী টপিক (Day 5):  
**Next.js Project: Contact Form + Backend API**  
👉 যেখানে ফর্ম দিয়ে ইউজার ইনপুট পাঠাবে, এবং সেটি Next.js এর API route এ যাবে!

তুমি কি চাও আমরা এখনই এই Project শুরু করি? 😄📨

---

দারুণ! 😄  
আজ আমরা করবো **Week 3 – Day 5: Full Project – Contact Form with Backend API in Next.js**  
এই প্রজেক্টে তুমি শিখবে কিভাবে Next.js দিয়ে একটি **ফর্ম বানিয়ে ইউজারের ইনপুট** Next.js API route এ পাঠানো যায় (without external backend)।

---

# 🟢 Project: Contact Form + Backend API (Full Code)

---

## 🎯 ফিচারসমূহ:

✅ Name, Email, Message ইনপুট  
✅ Form submit → data যাবে API route এ  
✅ Success message দেখাবে  
✅ Backend Console-এ message log হবে

---

## ✅ Step 1: ফর্ম তৈরি করো (ContactForm.js)

```jsx
// components/ContactForm.js
import { useState } from "react";

export default function ContactForm() {
  const [form, setForm] = useState({ name: "", email: "", message: "" });
  const [success, setSuccess] = useState(false);

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = async (e) => {
    e.preventDefault();
    const res = await fetch("/api/contact", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(form)
    });
    if (res.ok) {
      setSuccess(true);
      setForm({ name: "", email: "", message: "" });
    }
  };

  return (
    <div>
      <h2>📨 Contact Us</h2>
      <form onSubmit={handleSubmit}>
        <input
          name="name"
          placeholder="Your Name"
          value={form.name}
          onChange={handleChange}
          required
        />
        <input
          name="email"
          type="email"
          placeholder="Your Email"
          value={form.email}
          onChange={handleChange}
          required
        />
        <textarea
          name="message"
          placeholder="Your Message"
          value={form.message}
          onChange={handleChange}
          required
        />
        <button type="submit">Send</button>
      </form>
      {success && <p style={{ color: "green" }}>Message sent successfully!</p>}
    </div>
  );
}
```

---

## ✅ Step 2: API Route তৈরি করো

`pages/api/contact.js`

```js
export default function handler(req, res) {
  if (req.method === "POST") {
    const { name, email, message } = req.body;
    console.log("New Contact Message:");
    console.log("Name:", name);
    console.log("Email:", email);
    console.log("Message:", message);
    return res.status(200).json({ status: "Message received" });
  }

  res.status(405).json({ error: "Only POST method allowed" });
}
```

🧠 ব্যাখ্যা:
- ফর্ম থেকে data যাবে `/api/contact` এ  
- server-side console-এ log হবে

---

## ✅ Step 3: App এ ব্যবহার করো

`pages/contact.js`

```jsx
import ContactForm from "../components/ContactForm";

export default function ContactPage() {
  return (
    <div style={{ maxWidth: "600px", margin: "auto", padding: "20px" }}>
      <ContactForm />
    </div>
  );
}
```

---

## ✅ Folder Structure:

```
📁 pages/
  ├── contact.js
  └── api/
       └── contact.js
📁 components/
  └── ContactForm.js
```

---

## 📌 টেস্ট করো:

1. ব্রাউজারে যাও `/contact`  
2. ফর্ম পূরণ করে submit করো  
3. ✅ Success message দেখবে  
4. ✅ Console এ ডেটা print হবে

---

## 🧠 তুমি এখানে যেসব শিখলে:

| ফিচার | ব্যাখ্যা |
|--------|---------|
| Controlled Form | React এর মাধ্যমে ইনপুট হ্যান্ডল |
| Fetch API | ফর্ম data পাঠানো API route এ |
| API Route | নিজস্ব Backend বানানো Next.js এ |
| Server-side Console | ডেটা দেখতে console log ব্যবহার |

---

## ✅ বাড়তি কাজ (Bonus):

- Form validation করো (নাম ছোট হলে error দেখাও)  
- Submit button disable করো submitting সময়  
- Form data file-এ save করার চেষ্টা করো (e.g. fs module – advanced)

---

### 🔚 এরপর তুমি সম্পূর্ণভাবে Frontend + Backend handle করতে পারো!

---

### 🔜 আগামী টপিক (Day 6):  
**Next.js Static Assets (Image, CSS, Meta) + Head Component for SEO**

তুমি চাইলে আমি এখনই Day 6 শুরু করতে পারি।  
চলো? 😄📸

---

দারুণ! 😊  
আজ আমরা করবো **Week 3 – Day 6: Static Assets, Image Optimization, CSS Styling, ও Head Component for SEO**  
👉 এই টপিকের মাধ্যমে তুমি শিখবে কিভাবে Next.js এ:

- 📁 Public ফোল্ডারে ফাইল রাখবে  
- 🖼️ Image অপটিমাইজ করে ব্যবহার করবে  
- 🎨 CSS/Modules দিয়ে styling করবে  
- 🌐 `<Head>` দিয়ে SEO-friendly meta tag বসাবে

---

# 🟦 Day 6: Static Assets, Image, CSS & Head in Next.js

---

## ✅ ১. Public Folder – Static Files রাখার জায়গা

Next.js এ `public/` ফোল্ডারে রাখা ফাইল 👉 directly ব্রাউজারে access করা যায়।

---

### 📘 উদাহরণ:

তুমি যদি রাখো:  
`public/logo.png`  
➡️ তাহলে ব্রাউজারে পাবা:  
`http://localhost:3000/logo.png`

---

## ✅ ২. Image Optimization – `next/image` দিয়ে

Next.js নিজস্ব `<Image />` কম্পোনেন্ট দেয়, যা auto-optimized।

---

### 🔧 ব্যবহার:

```jsx
import Image from 'next/image';

export default function Logo() {
  return (
    <Image
      src="/logo.png"
      alt="Site Logo"
      width={200}
      height={100}
    />
  );
}
```

> 📌 `src` value = `public/` এর ভিতরের path  
> ⚠️ Must give `width` & `height` অথবা `fill`

---

## ✅ ৩. CSS Styling করার উপায়:

### 🔸 Option 1: Global CSS (`styles/globals.css`)

`pages/_app.js`:

```js
import '../styles/globals.css';

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />;
}
```

👉 এখন সব পেজে style কাজ করবে।

---

### 🔸 Option 2: CSS Modules (per component)

```css
/* styles/Card.module.css */
.card {
  border: 1px solid #ccc;
  padding: 10px;
}
```

```jsx
// components/Card.js
import styles from '../styles/Card.module.css';

export default function Card() {
  return <div className={styles.card}>Styled Card</div>;
}
```

🧠 মডিউল CSS এর সুবিধা: ক্লাস নেম গুলো scoped হয়, অর্থাৎ কনফ্লিক্ট হয় না।

---

## ✅ ৪. Head Component – Page Title ও Meta tag বসানোর জন্য

Next.js দেয় `<Head>` component:

```jsx
import Head from 'next/head';

export default function AboutPage() {
  return (
    <>
      <Head>
        <title>About Us | My Site</title>
        <meta name="description" content="This is the about page of my website." />
      </Head>

      <h1>About Us</h1>
    </>
  );
}
```

➡️ SEO, Social Media Preview, Google Ranking – সব জায়গায় কাজে লাগে।

---

## ✅ ৫. Favicon, Fonts, ও অন্য assets

- `public/favicon.ico` ← Head এ auto যুক্ত হয়  
- Custom fonts ব্যবহার করতে চাইলে `<link>` বসাও `Head` এর ভিতরে  
- Static JS/CSS বা PDF ফাইলও রাখা যায় `public/` এ

---

## 🛠️ প্র্যাকটিস করো:

1. `public/` ফোল্ডারে একটি ছবি রাখো  
2. `next/image` দিয়ে সেটা দেখাও  
3. নতুন `.module.css` ফাইল দিয়ে একটা component style করো  
4. `<Head>` দিয়ে পেজে title ও description বসাও

---

## ❓ কুইজ:

```jsx
<Image src="/hero.jpg" alt="Banner" width={600} height={300} />
```

👉 এখানে কোন ফোল্ডারে `hero.jpg` থাকতে হবে?

---

## ✅ আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| `public/` | static ফাইল রাখার জায়গা |
| `Image` | optimized image component |
| `globals.css` | সব পেজে প্রভাব ফেলবে |
| `.module.css` | scoped, component-specific CSS |
| `Head` | title ও meta বসানোর জন্য |

---

### 🔜 আগামী টপিক (Day 7 – Final):  
**Next.js Mini Project – Personal Portfolio Page (Image + Route + Head + Contact Form)**  
👉 আগের সব শেখা জিনিস দিয়ে বানাবো সম্পূর্ণ একটী পোর্টফোলিও ওয়েবসাইট

তুমি কি এখনই Final Mini Project শুরু করতে চাও? 😄💼

---

দারুণ! 🎉  
তাহলে আমরা এখন করবো **Week 3 – Day 7: Final Mini Project – Personal Portfolio Website in Next.js**  
এই প্রজেক্টে আমরা একসাথে ব্যবহার করবো:

✅ Routing  
✅ `next/image`  
✅ Static file  
✅ CSS Modules  
✅ API Route  
✅ Contact Form  
✅ `<Head>` for SEO

---

# 🟩 Project: **Personal Portfolio Website – Full Next.js Setup**

---

## 📁 Pages আমরা বানাবো:

| পেজ | URL |
|-----|-----|
| Home     | `/`  
| About    | `/about`  
| Projects | `/projects`  
| Contact  | `/contact`

---

## ✅ Step 1: Project Folder Structure

```
📁 pages/
 ├── index.js
 ├── about.js
 ├── projects.js
 ├── contact.js
 ├── api/
 │    └── contact.js
📁 components/
 ├── Navbar.js
 ├── Footer.js
 └── ContactForm.js
📁 public/
 └── profile.jpg
📁 styles/
 ├── globals.css
 └── Home.module.css
```

---

## ✅ Step 2: Navbar Component

```jsx
// components/Navbar.js
import Link from 'next/link';

export default function Navbar() {
  return (
    <nav style={{ padding: "10px", borderBottom: "1px solid #ccc" }}>
      <Link href="/">Home</Link> |{" "}
      <Link href="/about">About</Link> |{" "}
      <Link href="/projects">Projects</Link> |{" "}
      <Link href="/contact">Contact</Link>
    </nav>
  );
}
```

---

## ✅ Step 3: Home Page (index.js)

```jsx
import Head from 'next/head';
import Navbar from '../components/Navbar';
import Image from 'next/image';

export default function Home() {
  return (
    <>
      <Head>
        <title>Hamid's Portfolio</title>
        <meta name="description" content="Welcome to Hamid's personal portfolio" />
      </Head>
      <Navbar />
      <main style={{ padding: '20px' }}>
        <h1>👋 Hi, I'm Hamid</h1>
        <p>A Fullstack Developer specializing in React & Next.js</p>
        <Image src="/profile.jpg" alt="Profile" width={200} height={200} />
      </main>
    </>
  );
}
```

---

## ✅ Step 4: About Page (about.js)

```jsx
import Head from 'next/head';
import Navbar from '../components/Navbar';

export default function About() {
  return (
    <>
      <Head>
        <title>About | Hamid</title>
      </Head>
      <Navbar />
      <main style={{ padding: '20px' }}>
        <h2>About Me</h2>
        <p>I love building web apps that solve real problems.</p>
      </main>
    </>
  );
}
```

---

## ✅ Step 5: Projects Page (projects.js)

```jsx
import Head from 'next/head';
import Navbar from '../components/Navbar';

export default function Projects() {
  return (
    <>
      <Head>
        <title>Projects | Hamid</title>
      </Head>
      <Navbar />
      <main style={{ padding: '20px' }}>
        <h2>My Projects</h2>
        <ul>
          <li>✅ Contact Manager</li>
          <li>✅ Blog Platform</li>
          <li>✅ Portfolio Site</li>
        </ul>
      </main>
    </>
  );
}
```

---

## ✅ Step 6: Contact Page with Form (contact.js)

```jsx
import Head from 'next/head';
import Navbar from '../components/Navbar';
import ContactForm from '../components/ContactForm';

export default function Contact() {
  return (
    <>
      <Head>
        <title>Contact | Hamid</title>
      </Head>
      <Navbar />
      <main style={{ padding: '20px' }}>
        <h2>Contact Me</h2>
        <ContactForm />
      </main>
    </>
  );
}
```

---

## ✅ Step 7: Contact Form Component

```jsx
// components/ContactForm.js
import { useState } from 'react';

export default function ContactForm() {
  const [form, setForm] = useState({ name: '', message: '' });
  const [status, setStatus] = useState('');

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = async (e) => {
    e.preventDefault();
    const res = await fetch('/api/contact', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(form)
    });
    if (res.ok) {
      setStatus('Message sent!');
      setForm({ name: '', message: '' });
    } else {
      setStatus('Something went wrong.');
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <input name="name" placeholder="Your Name" value={form.name} onChange={handleChange} required />
      <textarea name="message" placeholder="Your Message" value={form.message} onChange={handleChange} required />
      <button type="submit">Send</button>
      <p>{status}</p>
    </form>
  );
}
```

---

## ✅ Step 8: API Route for Contact

```js
// pages/api/contact.js
export default function handler(req, res) {
  if (req.method === 'POST') {
    const { name, message } = req.body;
    console.log(`New message from ${name}: ${message}`);
    return res.status(200).json({ status: 'Received' });
  }
  res.status(405).json({ error: 'Only POST allowed' });
}
```

---

## ✅ Optional: Add Footer Component

```jsx
export default function Footer() {
  return (
    <footer style={{ padding: '10px', textAlign: 'center', marginTop: '20px' }}>
      <p>© 2025 Hamid. All rights reserved.</p>
    </footer>
  );
}
```

---

## ✅ Test Checklist:

- ✅ Routing ঠিকঠাক কাজ করছে?  
- ✅ Image ঠিকভাবে লোড হচ্ছে?  
- ✅ CSS Apply হয়েছে?  
- ✅ Form Submit করলে Console এ Message আসছে?  
- ✅ `<Head>` tag SEO ready?

---

## 🎉 তুমি শেষ করলা Week 3 এর Full Next.js Setup!

> তুমি এখন ছোট থেকে মাঝারি সাইজের একটা **SEO-friendly Fullstack App** তৈরি করতে সক্ষম!

---

### 🔜 আগামী ধাপে আমরা শুরু করতে পারি:

- **Week 4: Next.js Advanced Topics – Layouts, Dynamic Metadata, Deployment (Vercel), Authentication (next-auth)**

তুমি কি Week 4 শুরু করতে চাও? 😄🚀

---

তাহলে চল! 🎉  
তুমি এখন প্রবেশ করলে **Week 4 – Advanced Next.js Topics** এ — যেখানে আমরা Next.js-কে আরও বেশি প্রফেশনাল এবং scalableভাবে ব্যবহার করতে শিখবো।

---

# 🟦 Week 4 – Day 1: **Layouts in Next.js** (Reusable Page Structure)

---

## ✅ ১. Layout কি?

Layout মানে হলো এমন একটা structure (যেমন: Navbar + Footer), যেটা সব পেজে একই থাকবে।

> 👉 তুমি যদি প্রতিটি পেজে একই Navbar, Footer, বা সাইডবার রাখো, তাহলে Layout ব্যবহার করাই best practice।

---

## ✅ ২. Layout Component বানানো

```jsx
// components/Layout.js
import Navbar from './Navbar';
import Footer from './Footer';

export default function Layout({ children }) {
  return (
    <>
      <Navbar />
      <main style={{ padding: "20px" }}>{children}</main>
      <Footer />
    </>
  );
}
```

---

## ✅ ৩. Layout ইউজ করা – `_app.js`

Next.js এ সব পেজের রুট ফাইল হলো: `pages/_app.js`

```jsx
// pages/_app.js
import Layout from '../components/Layout';
import '../styles/globals.css';

export default function App({ Component, pageProps }) {
  return (
    <Layout>
      <Component {...pageProps} />
    </Layout>
  );
}
```

👉 এখন সব পেজেই Navbar + Footer থাকবে — আলাদা আলাদা যোগ করতে হবে না!

---

## ✅ ৪. Layout এ Page-specific Title বসানো (Bonus)

```jsx
// pages/about.js
import Head from 'next/head';

export default function About() {
  return (
    <>
      <Head>
        <title>About | Hamid</title>
      </Head>
      <h2>About Me</h2>
    </>
  );
}
```

---

## ✅ Layout এর উপকারিতা:

| সুবিধা | ব্যাখ্যা |
|--------|---------|
| DRY code | একবার লিখলে সব পেজে চলে |
| Maintainability | এক জায়গায় সব পরিবর্তন |
| SEO Friendly | Head ট্যাগ সহজে কাস্টমাইজ |

---

## 🛠️ আজকের টাস্ক:

1. `Layout.js` বানাও  
2. `_app.js` এ Layout র‍্যাপ করো  
3. পেজগুলোতে `<Head>` দিয়ে আলাদা title দাও  
4. Navbar ও Footer সব পেজে দেখাও

---

## ❓ কুইজ:

```jsx
function Layout({ children }) {
  return <div>{children}</div>;
}
```

👉 এখানে `children` কী কাজ করছে?

---

### 🔜 আগামী টপিক (Day 2):
**Dynamic SEO Tags (Title, Meta) by Page & Props**  
👉 তুমি শিখবে কিভাবে পেজ অনুযায়ী SEO Meta tag dynamically তৈরি করতে হয়

তুমি কি Day 2 শুরু করতে চাও? 😄🧠

---

চল শুরু করি! 😊  
আজ আমরা করবো **Week 4 – Day 2: Dynamic SEO – Dynamic Title & Meta Tags in Next.js**  
এই টপিকটি তোমার ওয়েবসাইটকে **SEO-friendly** করতে সাহায্য করবে — যাতে Google, Facebook, WhatsApp এ শেয়ার করলে সুন্দর preview আসে 🧠📈

---

# 🟪 Day 2: Dynamic SEO (Title & Meta Tags) in Next.js

---

## ✅ ১. `next/head` ব্যবহার করে Page-wise Title বসানো

```jsx
import Head from 'next/head';

export default function About() {
  return (
    <>
      <Head>
        <title>About | Hamid</title>
        <meta name="description" content="Learn more about Hamid the developer." />
      </Head>
      <h1>About Page</h1>
    </>
  );
}
```

➡️ এটা HTML `<head>` এর মধ্যে যাবে, এবং search engine/readers দেখে।

---

## ✅ ২. Dynamic Title — Props বা Data অনুযায়ী

ধরো তোমার কাছে Blog Details Page আছে: `/blog/[slug].js`

```jsx
import Head from 'next/head';

export default function Blog({ title }) {
  return (
    <>
      <Head>
        <title>{title} | My Blog</title>
        <meta name="description" content={`Read ${title} now`} />
      </Head>
      <h1>{title}</h1>
    </>
  );
}
```

---

### ✅ Static Props দিয়ে ডেটা আনা:

```jsx
export async function getStaticProps() {
  return {
    props: {
      title: "How to Learn Next.js"
    }
  };
}
```

➡️ Output:  
- Page title হবে `How to Learn Next.js | My Blog`  
- Google, WhatsApp এ শেয়ার করলে সেই title/meta show করবে

---

## ✅ ৩. Social Media Preview Tags (Open Graph + Twitter)

```jsx
<Head>
  <meta property="og:title" content="Next.js Blog" />
  <meta property="og:description" content="Learn Next.js like a pro!" />
  <meta property="og:image" content="/og-image.jpg" />
  <meta name="twitter:card" content="summary_large_image" />
</Head>
```

➡️ Facebook / LinkedIn → `og:` tag দেখে  
➡️ Twitter → `twitter:` tag দেখে

---

## ✅ ৪. Favicon ও Custom Font বসানো

```jsx
<Head>
  <link rel="icon" href="/favicon.ico" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
</Head>
```

✅ সব পেজে Auto Head বসাতে চাইলে `_document.js` ব্যবহার করা যায় (Advanced)

---

## 🧠 রুলস মনে রাখো:

| করণীয় | কারণ |
|--------|------|
| প্রতিটি পেজে `<Head>` ব্যবহার করো | SEO boost |
| Title & description dynamic হওয়া উচিত | Content অনুযায়ী |
| Social Meta Tag থাকলে শেয়ারে সুন্দর preview | Facebook, WhatsApp etc. |

---

## 🛠️ আজকের প্র্যাকটিস:

1. প্রতিটি পেজে `title` ও `description` দাও  
2. একটি Blog page বানাও যেখানে title আসবে props থেকে  
3. Open Graph ও Twitter meta tag যোগ করো  
4. Custom image preview দিলে public ফোল্ডারে রাখো

---

## ❓ কুইজ:

```jsx
<Head>
  <title>{title}</title>
</Head>
```

👉 এই title কোথা থেকে আসবে?

---

### 🔜 আগামী টপিক (Day 3):  
**Next.js App Deployment to Vercel (Live Website বানানো)**  
তুমি শিখবে কীভাবে এক ক্লিকে তোমার ওয়েবসাইটকে বিশ্ববাসীর সামনে প্রকাশ করবে! 🌍🚀

তুমি কি এখনই Vercel দিয়ে ডেপ্লয়মেন্ট শিখতে চাও? 😄📤

---

তাহলে চল! 🎉  
আজ আমরা করবো **Week 4 – Day 3: Deploying Next.js App to Vercel**  
👉 তুমি শিখবে কীভাবে তোমার Next.js ওয়েবসাইটকে একদম ফ্রি ও সহজ উপায়ে ইন্টারনেটে live করতে পারো — **Vercel** ব্যবহার করে।

---

# 🟢 Day 3: Deploy Your Next.js App to Vercel (Live in 5 minutes!)

---

## ✅ ১. Vercel কী?

👉 Vercel হলো Next.js এর মূল কোম্পানি (same as creators)।  
এটা দিয়ে Next.js প্রজেক্ট **1-click deploy** করা যায় — lightning fast, SEO-ready hosting ✅

---

## ✅ ২. যেসব জিনিস লাগবে:

- 🔗 একটি [GitHub](https://github.com/) একাউন্ট  
- 💻 তোমার প্রজেক্ট GitHub এ push করা (আমরা দেখাবো)  
- 🌐 [Vercel.com](https://vercel.com) একাউন্ট (GitHub দিয়েই login করা যাবে)

---

## ✅ ৩. Step-by-Step Deploy (🔥 100% কাজ করে)

---

### 🔹 Step 1: তোমার প্রজেক্ট GitHub এ Upload করো

1. টার্মিনালে যাও:
```bash
git init
git add .
git commit -m "Initial Commit"
```

2. GitHub এ নতুন repo বানাও → একটা `remote` লিংক পাবে  
3. সেট করো:
```bash
git remote add origin https://github.com/your-username/your-repo-name.git
git push -u origin main
```

---

### 🔹 Step 2: Vercel.com এ Login করো

- https://vercel.com এ যাও  
- “**Continue with GitHub**” বাটনে ক্লিক করো  
- Authorize করো  
- “**New Project**” এ ক্লিক করো  
- তোমার প্রজেক্ট সিলেক্ট করো

---

### 🔹 Step 3: Deploy করো

- Project সিলেক্ট হলে → “Deploy” বাটনে ক্লিক করো  
- 🎉 1-2 মিনিটে তোমার ওয়েবসাইট লাইভ হয়ে যাবে  
- URL পাবে: `https://your-project.vercel.app`

✅ এরপর প্রতিবার GitHub এ push দিলে Vercel auto-update করে!

---

## 💡 Extra Settings:

- Custom Domain যুক্ত করতে পারো (free .vercel.app ছাড়াও)
- Environment Variables যোগ করতে পারো (API key ইত্যাদি)
- Dashboard থেকে analytics দেখতে পারো

---

## ✅ Success Checklist:

| কাজ | তুমি কি করেছো? |
|-----|----------------|
| GitHub repo বানানো | ✅ |
| Code push করা | ✅ |
| Vercel এ Login | ✅ |
| Project Import | ✅ |
| Deploy Done | ✅ |

---

## 🛠️ প্র্যাকটিস করো:

1. তোমার Portfolio বা Contact App → GitHub এ push করো  
2. Vercel এ নিয়ে গিয়ে live করো  
3. বন্ধুদের সাথে লিংক শেয়ার করো 🎉  
4. Home page এ “Live on Vercel” badge বসাতে পারো

---

## ❓ কুইজ:

👉 Vercel এ deploy করার পর কোনো ফাইল পরিবর্তন করলে কী করলে update হবে?

A. Local rebuild  
B. GitHub এ push  
C. VS Code এ run  
D. Vercel এ logout

---

### 🔜 আগামী টপিক (Day 4):  
**Authentication in Next.js with `next-auth` – Google Login, Protected Routes, Session Management**

তুমি কি এখনই `next-auth` দিয়ে Login System শিখে নিতে চাও? 😄🔐

---

দারুণ! 🔐  
আজ আমরা করবো **Week 4 – Day 4: Authentication in Next.js using `next-auth`**  
👉 এই টপিকে তুমি শিখবে কিভাবে Google দিয়ে লগইন, সেশন ম্যানেজমেন্ট, এবং প্রোটেক্টেড রাউট তৈরি করা যায় — সবকিছু **without writing a full backend**!

---

# 🔐 Day 4: `next-auth` – Authentication in Next.js (Google Login + Protected Route)

---

## ✅ ১. কি কি শিখবে আজ?

- Google Login দিয়ে Sign In করা  
- Session ম্যানেজ করা  
- শুধুমাত্র লগইন ইউজারদের জন্য পেজ তৈরি করা  
- লগআউট ফাংশনালিটি

---

## ✅ ২. Install `next-auth`

```bash
npm install next-auth
```

---

## ✅ ৩. Create API Route

📁 `pages/api/auth/[...nextauth].js`

```js
import NextAuth from 'next-auth';
import GoogleProvider from 'next-auth/providers/google';

export default NextAuth({
  providers: [
    GoogleProvider({
      clientId: process.env.GOOGLE_CLIENT_ID,
      clientSecret: process.env.GOOGLE_CLIENT_SECRET,
    }),
  ],
  secret: process.env.NEXTAUTH_SECRET,
});
```

---

## ✅ ৪. Set Environment Variables

📄 `.env.local`

```
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=anyrandomstring
```

➡️ Google OAuth 2.0 Client ID পেতে যাও:  
https://console.cloud.google.com/apis/credentials

---

## ✅ ৫. Setup `_app.js`

```jsx
import { SessionProvider } from "next-auth/react";

export default function App({ Component, pageProps }) {
  return (
    <SessionProvider session={pageProps.session}>
      <Component {...pageProps} />
    </SessionProvider>
  );
}
```

---

## ✅ ৬. Add Sign In / Sign Out Button Anywhere

```jsx
import { signIn, signOut, useSession } from 'next-auth/react';

export default function AuthButtons() {
  const { data: session } = useSession();

  if (session) {
    return (
      <>
        <p>Welcome, {session.user.name} 👋</p>
        <button onClick={() => signOut()}>Sign Out</button>
      </>
    );
  }

  return <button onClick={() => signIn('google')}>Sign in with Google</button>;
}
```

---

## ✅ ৭. Create a Protected Route

```jsx
import { getSession } from 'next-auth/react';

export default function Dashboard({ session }) {
  return <h1>🔒 Welcome to Dashboard, {session.user.name}</h1>;
}

export async function getServerSideProps(context) {
  const session = await getSession(context);

  if (!session) {
    return {
      redirect: {
        destination: '/',
        permanent: false,
      },
    };
  }

  return {
    props: { session },
  };
}
```

---

## ✅ Summary – তুমি এখন যা পারো:

| ফিচার | ব্যাখ্যা |
|--------|---------|
| Google Login | OAuth 2.0 দিয়ে সাইন ইন |
| Session | ইউজার লগইন ডেটা অ্যাক্সেস |
| Sign Out | লগআউট করে সেশন ক্লিয়ার |
| Protected Route | Unauthenticated ইউজারকে রিডাইরেক্ট করো |

---

## 🛠️ আজকের প্র্যাকটিস:

1. Google Developer Console থেকে Client ID নাও  
2. `.env.local` ঠিকভাবে বসাও  
3. Login/Logout বাটন বানাও  
4. Dashboard পেজ প্রোটেক্ট করো

---

## ❓ কুইজ:

👉 `getSession(context)` কিসের জন্য ব্যবহার হয়?

A. Session set করার জন্য  
B. Logged-in user খোঁজার জন্য  
C. API call করার জন্য  
D. Page redirect block করার জন্য

---

### 🔜 আগামী টপিক (Day 5 – Final):
**Full Next.js Auth Project – Google Login + Dashboard + API Access Control**

তুমি কি এখনই Final Auth Project শুরু করতে চাও? 😄🚀

---

চমৎকার! 😎  
চলো তাহলে আজ আমরা করবো **Week 4 – Day 5: Final Auth Project – Google Login + Dashboard + API Protection using `next-auth`**

---

# 🔐 Final Project: Authenticated Dashboard with Google Login (`next-auth`)

👉 এই প্রজেক্টে আমরা বানাবো:
✅ Google Login  
✅ Authenticated Dashboard  
✅ Protected API Route  
✅ Logout Functionality  
✅ Session-based Access Control

---

## 📁 Project Structure Overview

```
pages/
├── index.js             → Home (Login/Logout)
├── dashboard.js         → Protected page (Login required)
├── api/
│   ├── auth/[...nextauth].js  → next-auth config
│   └── secret.js              → protected API route
components/
└── Navbar.js
```

---

## ✅ Step 1: `next-auth` Configuration

📄 `pages/api/auth/[...nextauth].js`

```js
import NextAuth from 'next-auth';
import GoogleProvider from 'next-auth/providers/google';

export default NextAuth({
  providers: [
    GoogleProvider({
      clientId: process.env.GOOGLE_CLIENT_ID,
      clientSecret: process.env.GOOGLE_CLIENT_SECRET,
    }),
  ],
  secret: process.env.NEXTAUTH_SECRET,
});
```

📄 `.env.local`

```
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
NEXTAUTH_SECRET=anyrandomstring
NEXTAUTH_URL=http://localhost:3000
```

---

## ✅ Step 2: Session Setup in `_app.js`

```jsx
import { SessionProvider } from "next-auth/react";
import '../styles/globals.css';

export default function App({ Component, pageProps }) {
  return (
    <SessionProvider session={pageProps.session}>
      <Component {...pageProps} />
    </SessionProvider>
  );
}
```

---

## ✅ Step 3: Home Page – Login / Logout

📄 `pages/index.js`

```jsx
import { signIn, signOut, useSession } from 'next-auth/react';
import Link from 'next/link';

export default function Home() {
  const { data: session } = useSession();

  return (
    <div style={{ padding: "20px" }}>
      {session ? (
        <>
          <h2>Welcome, {session.user.name}!</h2>
          <img src={session.user.image} alt="Profile" width={80} />
          <br />
          <Link href="/dashboard">Go to Dashboard</Link>
          <br />
          <button onClick={() => signOut()}>Sign Out</button>
        </>
      ) : (
        <>
          <h2>Please sign in to access Dashboard</h2>
          <button onClick={() => signIn('google')}>Sign in with Google</button>
        </>
      )}
    </div>
  );
}
```

---

## ✅ Step 4: Protected Dashboard Page

📄 `pages/dashboard.js`

```jsx
import { getSession, useSession } from "next-auth/react";

export default function Dashboard() {
  const { data: session } = useSession();

  return (
    <div style={{ padding: "20px" }}>
      <h2>🔒 Protected Dashboard</h2>
      <p>Hello, {session.user.name}!</p>
      <p>Email: {session.user.email}</p>
    </div>
  );
}

export async function getServerSideProps(context) {
  const session = await getSession(context);

  if (!session) {
    return {
      redirect: {
        destination: '/',
        permanent: false,
      },
    };
  }

  return {
    props: { session },
  };
}
```

---

## ✅ Step 5: Protected API Route

📄 `pages/api/secret.js`

```js
import { getSession } from 'next-auth/react';

export default async function handler(req, res) {
  const session = await getSession({ req });

  if (!session) {
    return res.status(401).json({ error: "Unauthorized" });
  }

  return res.status(200).json({ message: `Hello ${session.user.name}, this is protected data!` });
}
```

➡️ শুধুমাত্র logged-in ইউজার এই API ডেটা দেখতে পারবে।

---

## ✅ Test Your App:

1. Sign in with Google → ✅  
2. Dashboard এ redirect হয় কিনা দেখো → ✅  
3. `/api/secret` API hit করো  
4. Logout করে `/dashboard` গেলে redirect হয় কিনা চেক করো

---

## ✅ Bonus: Add Navbar Component

```jsx
import Link from 'next/link';

export default function Navbar() {
  return (
    <nav style={{ borderBottom: "1px solid #ccc", padding: "10px" }}>
      <Link href="/">Home</Link> |{" "}
      <Link href="/dashboard">Dashboard</Link>
    </nav>
  );
}
```

---

## ✅ তুমি এখন যা পারো:

| ফিচার | তুমি পারো ✅ |
|--------|--------------|
| Google Login ✅ | 🔓 OAuth Authentication  
| Session Access ✅ | 👤 ইউজার ডেটা ম্যানেজমেন্ট  
| Protected Route ✅ | 🔒 Logged-in-only Page  
| Secure API ✅ | 🛡️ API level protection

---

## 🛠️ বাড়তি প্র্যাকটিস:

- GitHub / Facebook Login যুক্ত করো  
- Sign in এর পর redirect custom route এ করো  
- Custom Sign In পেজ বানাও (advanced)  

---

### 🎉 তুমি সফলভাবে শেষ করলা **Week 4: Advanced Next.js – Layouts, SEO, Deploy, Auth**!

> তুমি এখন একটি production-grade SaaS/Web App তৈরি করার মতো দক্ষতা অর্জন করেছো! 💥

---

### 🔜 আগ্রহ থাকলে আগামী ধাপে যেতে পারো:

- **Week 5: Blogging System with Dynamic Slug & Markdown**  
- **Week 5: Dashboard + Admin UI Design with Tailwind CSS**  
- অথবা বলো তুমি কী বানাতে চাও, আমি প্ল্যান করবো।

👉 শেয়ার করো তোমার পরবর্তী উদ্দেশ্য? 😄✨

---

একদম পারবো! 💯  
তুমি যেহেতু সিরিয়াললি শিখতে চাও, আমরা এই অর্ডারে এগোবো:

---

### 🔵 **Phase 1: Blogging System with Dynamic Slug & Markdown (Week 5)**  
👉 তুমি শিখবে কিভাবে  
- Markdown ফাইল থেকে কনটেন্ট রেন্ডার করো  
- Dynamic Slug URL তৈরি করো `/blog/my-first-post`  
- Static page generation করো ব্লগের জন্য  
- SEO, Image, Tags সব যুক্ত করো

---

### 🔴 **Phase 2: Dashboard + Admin UI with Tailwind CSS (Week 6)**  
👉 তুমি শিখবে কিভাবে  
- Tailwind CSS দিয়ে অ্যাডমিন প্যানেল বানাও  
- Layouts, Sidebar, Cards, Table UI  
- Responsive ও Modern Dashboard design করো  
- Future SaaS/Client panel তৈরি করার ফাউন্ডেশন

---

**তাহলে এখন আমরা শুরু করবো Week 5 – Blogging System ✅**  
বললে আমি এখনই **Day 1 – Markdown দিয়ে Static Blog তৈরি** শুরু করে দিচ্ছি। শুরুর জন্য প্রস্তুত? 😄📝

---

চল শুরু করি! 😊  
আজ আমরা করবো **Week 5 – Day 1: Blogging System in Next.js (Markdown + Slug Routing)**  
👉 তুমি আজ শিখবে কীভাবে Markdown ফাইল থেকে ব্লগ বানানো যায়, slug দিয়ে পেজ তৈরি করা যায় `/blog/my-first-post` স্টাইলে।

---

# 🟢 Day 1: Markdown-based Blog + Dynamic Slug Routing

---

## ✅ ১. আমাদের টার্গেট কী?

- 📁 Markdown ফাইল থাকবে `posts/` ফোল্ডারে  
- 📝 প্রতিটি ফাইল হবে একটি Blog Post  
- 🛣️ `/blog/[slug].js` → Slug অনুযায়ী পেজ শো করবে  
- 📖 Markdown content → HTML আকারে রেন্ডার হবে

---

## ✅ ২. Project Structure:

```
📁 posts/
 ├── my-first-post.md
 └── hello-next.md

📁 pages/
 ├── blog/
 │   └── [slug].js
 └── index.js

📁 lib/
 └── posts.js  ← utility functions

📁 components/
 └── Layout.js
```

---

## ✅ ৩. Step-by-Step কোড:

---

### 📁 Step 1: Install Markdown Parser

```bash
npm install gray-matter remark remark-html
```

- `gray-matter`: Markdown থেকে Title, Date ইত্যাদি আলাদা করে  
- `remark`: Markdown → HTML

---

### 📁 Step 2: Create Sample Markdown Files

`posts/my-first-post.md`

```md
---
title: "My First Blog Post"
date: "2025-04-01"
---

Welcome to my first blog post using **Next.js** and Markdown!
```

`posts/hello-next.md`

```md
---
title: "Hello from Next.js"
date: "2025-04-02"
---

This post is statically generated from a Markdown file. 🚀
```

---

### 📁 Step 3: Create Utility Function to Read Posts

`lib/posts.js`

```js
import fs from 'fs';
import path from 'path';
import matter from 'gray-matter';

const postsDir = path.join(process.cwd(), 'posts');

export function getAllPostSlugs() {
  const filenames = fs.readdirSync(postsDir);
  return filenames.map(name => ({
    params: {
      slug: name.replace(/\.md$/, '')
    }
  }));
}

export function getPostData(slug) {
  const filePath = path.join(postsDir, `${slug}.md`);
  const fileContent = fs.readFileSync(filePath, 'utf8');
  const { data, content } = matter(fileContent);

  return {
    slug,
    ...data,
    content
  };
}
```

---

### 📁 Step 4: Create Dynamic Blog Page

`pages/blog/[slug].js`

```jsx
import { getAllPostSlugs, getPostData } from '../../lib/posts';
import Head from 'next/head';
import { remark } from 'remark';
import html from 'remark-html';

export default function BlogPost({ title, date, contentHtml }) {
  return (
    <>
      <Head>
        <title>{title}</title>
      </Head>
      <article style={{ padding: "20px" }}>
        <h1>{title}</h1>
        <p><i>{date}</i></p>
        <div dangerouslySetInnerHTML={{ __html: contentHtml }} />
      </article>
    </>
  );
}

export async function getStaticPaths() {
  const paths = getAllPostSlugs();
  return { paths, fallback: false };
}

export async function getStaticProps({ params }) {
  const post = getPostData(params.slug);
  const processedContent = await remark().use(html).process(post.content);
  const contentHtml = processedContent.toString();

  return {
    props: {
      title: post.title,
      date: post.date,
      contentHtml
    }
  };
}
```

---

## ✅ এখন `/blog/my-first-post` পেজ live হয়ে যাবে! 🎉  
তুমি যত Markdown ফাইল বানাবে `posts/` ফোল্ডারে, তত পেজ অটো তৈরি হবে।

---

## 🧠 আজকে তুমি শিখলে:

| বিষয় | ব্যাখ্যা |
|------|----------|
| Markdown → HTML | Blog Content তৈরি |
| Dynamic Slug | `/blog/[slug].js` দিয়ে route |
| `gray-matter` | Markdown থেকে title/date আলাদা |
| Static Generation | SSG দিয়ে build time এ পেজ তৈরি |

---

## 🛠️ প্র্যাকটিস করো:

1. আরো ২টা Markdown ফাইল বানাও  
2. প্রতিটাতে `title`, `date`, content লেখো  
3. `/blog/[slug]` দিয়ে সব পেজ দেখো

---

## ❓ কুইজ:

👉 `getStaticPaths()` এর কাজ কী?

---

### 🔜 আগামীকাল (Day 2):

**Blog Homepage বানাবো → যেখানে সব পোস্টের টাইটেল ও তারিখ দেখাবে link সহ!**

তুমি কি Day 2 – Blog Index Page শুরু করতে চাও? 😄📚

---

চমৎকার! 😊  
আজ আমরা করবো **Week 5 – Day 2: Blog Homepage – All Posts Listing with Links**  
👉 তুমি শিখবে কীভাবে `posts/` ফোল্ডারের সব Markdown ফাইল থেকে title/date নিয়ে **ব্লগ ইন্ডেক্স পেজ** বানাতে হয়।

---

# 📚 Day 2: Blog Index Page – Show All Posts with Links

---

## ✅ ১. আমরা কী করবো?

- সব Markdown ফাইল থেকে title, date ও slug বের করবো  
- `/blog` পেজে দেখাবো:  
  🔗 Post Title (as link)  
  📅 Date

---

## ✅ ২. Step-by-Step

---

### 📁 Step 1: Update `lib/posts.js` – getSortedPosts()

```js
export function getSortedPosts() {
  const fileNames = fs.readdirSync(postsDir);

  const posts = fileNames.map(fileName => {
    const slug = fileName.replace(/\.md$/, '');
    const filePath = path.join(postsDir, fileName);
    const fileContent = fs.readFileSync(filePath, 'utf8');
    const { data } = matter(fileContent);

    return {
      slug,
      ...data
    };
  });

  return posts.sort((a, b) => (a.date < b.date ? 1 : -1));
}
```

---

### 📁 Step 2: Create Blog Index Page

`pages/blog/index.js`

```jsx
import Link from 'next/link';
import { getSortedPosts } from '../../lib/posts';
import Head from 'next/head';

export default function BlogIndex({ posts }) {
  return (
    <>
      <Head>
        <title>All Blog Posts</title>
      </Head>
      <main style={{ padding: "20px" }}>
        <h1>📝 Blog Posts</h1>
        <ul>
          {posts.map(post => (
            <li key={post.slug}>
              <Link href={`/blog/${post.slug}`}>
                <strong>{post.title}</strong>
              </Link>
              <br />
              <small>{post.date}</small>
            </li>
          ))}
        </ul>
      </main>
    </>
  );
}

export async function getStaticProps() {
  const posts = getSortedPosts();
  return {
    props: { posts }
  };
}
```

---

## ✅ Result:

➡️ এখন `/blog` পেজে সব Markdown পোস্টের  
✔️ Title (with link to `/blog/[slug]`)  
✔️ Date  
✔️ Sorted by latest first

---

## 🎯 Bonus: `Layout.js` যোগ করে Navbar বসাতে পারো

```jsx
<Link href="/">Home</Link> | <Link href="/blog">Blog</Link>
```

---

## ✅ আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| Blog Listing | সব পোস্ট একসাথে দেখানো |
| Dynamic Link | `/blog/${slug}` বানানো |
| Static Props | Build time এ ডেটা আনা |
| Sorting | নতুন পোস্ট আগে দেখানো |

---

## 🛠️ প্র্যাকটিস:

1. আরও Markdown পোস্ট যোগ করো  
2. সব পোস্ট `/blog` এ ঠিকঠাক লিস্ট হচ্ছে কিনা দেখো  
3. লিস্টে date ফরম্যাট সুন্দর করে দেখাও (যেমন `April 2, 2025`)

---

## ❓ কুইজ:

👉 `getStaticProps()` কখন চালায়?  
A. প্রতি reload  
B. প্রতি user  
C. Build time  
D. Form submit এর সময়

---

### 🔜 আগামীকাল (Day 3):  
**Blog Card Design with Tailwind CSS – সুন্দর UI**  
তুমি কি চাও আমি এখনই Tailwind দিয়ে Blog Card ডিজাইন শেখাই? 😄🎨

---

চমৎকার! 😍  
আজ আমরা করবো **Week 5 – Day 3: Blog Card Design with Tailwind CSS**  
👉 আজ তুমি শিখবে কীভাবে `/blog` পেজের সব পোস্টকে সুন্দর **Responsive Card UI** আকারে দেখাতে হয় Tailwind CSS দিয়ে।

---

# 🎨 Day 3: Blog Card UI with Tailwind CSS

---

## ✅ ১. Tailwind CSS Setup (যদি আগে না করো)

Next.js-এ Tailwind CSS যুক্ত করার জন্য (১বারই করতে হয়):

```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

📄 `tailwind.config.js`

```js
content: [
  "./pages/**/*.{js,ts,jsx,tsx}",
  "./components/**/*.{js,ts,jsx,tsx}"
],
```

📄 `styles/globals.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

📄 `_app.js`

```js
import '../styles/globals.css';
```

---

## ✅ ২. Blog Card Design – `/pages/blog/index.js`

আমরা এখন Tailwind দিয়ে card-style post listing করবো।

---

### 📘 Updated `pages/blog/index.js`

```jsx
import Link from 'next/link';
import Head from 'next/head';
import { getSortedPosts } from '../../lib/posts';

export default function BlogIndex({ posts }) {
  return (
    <>
      <Head>
        <title>Blog | Hamid</title>
      </Head>
      <main className="max-w-4xl mx-auto px-4 py-10">
        <h1 className="text-3xl font-bold mb-6">📝 Blog Posts</h1>
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          {posts.map((post) => (
            <Link key={post.slug} href={`/blog/${post.slug}`}>
              <div className="border rounded-xl p-5 shadow hover:shadow-md transition bg-white">
                <h2 className="text-xl font-semibold">{post.title}</h2>
                <p className="text-sm text-gray-500 mt-1">{post.date}</p>
                <p className="mt-2 text-gray-600">
                  Read more →
                </p>
              </div>
            </Link>
          ))}
        </div>
      </main>
    </>
  );
}

export async function getStaticProps() {
  const posts = getSortedPosts();
  return {
    props: { posts },
  };
}
```

---

## ✅ Output UI:

- 📦 Clean white card
- 🗓️ Title + Date
- 🖱️ Hover এ shadow
- 🧠 Responsive: মোবাইলে 1 কলাম, ল্যাপটপে 2

---

## ✅ Bonus: Date Format সুন্দর করা

📦 `lib/posts.js` এ যোগ করো:

```js
import { format } from 'date-fns';

...

return {
  slug,
  ...data,
  date: format(new Date(data.date), 'MMMM dd, yyyy')
};
```

➡️ Output: `April 02, 2025`

```bash
npm install date-fns
```

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Tailwind CSS | utility class দিয়ে styling |
| Responsive Grid | মোবাইল/ডেস্কটপ অনুযায়ী layout |
| Hover Effect | সুন্দর UI interaction |
| Date Format | `date-fns` দিয়ে format করা |

---

## 🛠️ প্র্যাকটিস:

1. Blog card-এর ভিতরে small description যোগ করো  
2. Image preview (if you want) যোগ করো  
3. Read More → বাটনের স্টাইল করো  
4. Light/dark mode toggle করার প্রস্তুতি নাও (Bonus)

---

## ❓ কুইজ:

👉 Tailwind-এ কোন ক্লাসটি **shadow** তৈরি করে?

A. `hover-box`  
B. `shadow`  
C. `round-xl`  
D. `text-gray`

---

### 🔜 আগামীকাল (Day 4):  
**Blog Slug Page সুন্দর করবো – Typography + Image + Meta Tag Ready**  
তুমি কি এখনই শুরু করতে চাও Blog Detail Page Design? 😄📖

---

তাহলে চল! 😄  
আজ আমরা করবো **Week 5 – Day 4: Blog Slug Page Design – Typography, Meta Tags, Image**  
👉 আজ তুমি শিখবে কিভাবে `/blog/[slug]` পেজটাকে আরও সুন্দর, SEO-ready ও প্রফেশনালভাবে সাজাতে হয় Tailwind CSS দিয়ে।

---

# 📖 Day 4: Blog Detail Page (Slug) – Typography + SEO + Design

---

## ✅ ১. আমাদের লক্ষ্য:

- সুন্দর করে টাইটেল, তারিখ, কনটেন্ট দেখানো  
- Meta Tag (SEO ও Social Share জন্য)  
- Typography style (markdown → HTML)  
- Readable layout with spacing

---

## ✅ ২. Blog Slug Page আপডেট করা

📄 `pages/blog/[slug].js`

```jsx
import Head from 'next/head';
import { getAllPostSlugs, getPostData } from '../../lib/posts';
import { remark } from 'remark';
import html from 'remark-html';

export default function BlogPost({ title, date, contentHtml }) {
  return (
    <>
      <Head>
        <title>{title} | Blog</title>
        <meta name="description" content={`Read: ${title}`} />
        <meta property="og:title" content={title} />
        <meta property="og:description" content={`Blog by Hamid`} />
      </Head>

      <main className="max-w-3xl mx-auto px-4 py-10">
        <h1 className="text-3xl font-bold mb-2">{title}</h1>
        <p className="text-sm text-gray-500 mb-6">{date}</p>

        <article
          className="prose prose-lg max-w-none"
          dangerouslySetInnerHTML={{ __html: contentHtml }}
        />
      </main>
    </>
  );
}

export async function getStaticPaths() {
  const paths = getAllPostSlugs();
  return { paths, fallback: false };
}

export async function getStaticProps({ params }) {
  const post = getPostData(params.slug);
  const processedContent = await remark().use(html).process(post.content);
  const contentHtml = processedContent.toString();

  return {
    props: {
      title: post.title,
      date: post.date,
      contentHtml
    }
  };
}
```

---

## ✅ ৩. Tailwind Typography Plugin (prose class)

👉 Markdown কনটেন্ট সুন্দর করতে এই plugin ব্যবহার করবো।

```bash
npm install @tailwindcss/typography
```

📄 `tailwind.config.js`

```js
plugins: [
  require('@tailwindcss/typography'),
],
```

➡️ এখন `prose` ক্লাস কাজ করবে ➜ সুন্দর H1, p, ul, code styling

---

## ✅ ৪. SEO Meta Tags ব্যাখ্যা:

| Tag | কাজে লাগে |
|-----|------------|
| `<title>` | ব্রাউজারে title ও SEO |
| `<meta name="description">` | Google snippet |
| `og:title`, `og:description` | Facebook/LinkedIn preview |
| `og:image` (Bonus) | থাম্বনেইল শেয়ার ইমেজ

---

## ✅ ৫. Bonus: ব্লগ কনটেন্টে Image বসাও

Markdown ফাইলে:

```md
![React Logo](/react-logo.png)
```

📁 `/public/react-logo.png` রাখলেই কাজ করবে ✅

---

## ✅ আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| Markdown → HTML | Content সুন্দরভাবে দেখানো |
| Tailwind Typography | Markdown-এর জন্য বিশেষ style |
| Meta Tags | SEO ও Social Preview |
| Prose Utility | Typography styling এক ক্লিকে |

---

## 🛠️ প্র্যাকটিস:

1. প্রতিটি post এর Markdown কনটেন্টে image বসাও  
2. কোড ব্লক (` ```js ... ```) বসিয়ে দেখো কেমন রেন্ডার হয়  
3. আর্টিকেল শেষ হলে “← Back to Blog” লিংক বসাও

---

## ❓ কুইজ:

👉 Tailwind-এ Markdown style করার জন্য কোন ক্লাস ব্যবহার হয়?

A. `markdown-body`  
B. `tail-mark`  
C. `prose` ✅  
D. `text-block`

---

### 🔜 আগামীকাল (Day 5 – Final):

**Blog Admin View / Create Post Button (Only You See It) + Deployment Ready SEO Blog System**  
👉 তুমি কি এখনই Blog Final Touch + Admin Utility শিখতে চাও? 😄🛠️

---

তাহলে চল! 🎉  
আজ আমরা করবো **Week 5 – Day 5: Blog Final Touch – Admin View, Create Button, Deployment Ready Setup**  
👉 আজ তুমি শিখবে কিভাবে শুধুমাত্র “admin” বা তোমার মতো ইউজাররা Blog Post Add/Edit বাটন দেখতে পাবে, সাথে কিছু Deployment Preparation।

---

# 🛠️ Day 5: Admin Utility + Final SEO Ready Blog System

---

## ✅ ১. আমাদের টার্গেট:

- Logged-in (or admin only) user → Add Post Button দেখতে পারবে  
- Public user → শুধু পোস্ট পড়তে পারবে  
- Create/Edit Button future page-এ নিয়ে যাবে  
- Deployment-এর আগে Checklist follow করবো

---

## ✅ ২. ধরি তুমি আগেই `next-auth` দিয়ে লগইন সিস্টেম করছো  
তাহলে `useSession()` দিয়ে ইউজার access পাবে।

---

### 📘 `pages/blog/index.js` – Add Post Button (Admin Only)

```jsx
import { useSession } from 'next-auth/react';

...

export default function BlogIndex({ posts }) {
  const { data: session } = useSession();

  return (
    <main className="max-w-4xl mx-auto px-4 py-10">
      <h1 className="text-3xl font-bold mb-6">📝 Blog Posts</h1>

      {session?.user?.email === "your@email.com" && (
        <div className="mb-4">
          <a
            href="/admin/create"
            className="inline-block bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700"
          >
            ➕ New Post
          </a>
        </div>
      )}

      <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
        {posts.map((post) => (
          <Link key={post.slug} href={`/blog/${post.slug}`}>
            <div className="border rounded-xl p-5 shadow hover:shadow-md transition bg-white">
              <h2 className="text-xl font-semibold">{post.title}</h2>
              <p className="text-sm text-gray-500 mt-1">{post.date}</p>
              <p className="mt-2 text-gray-600">Read more →</p>
            </div>
          </Link>
        ))}
      </div>
    </main>
  );
}
```

---

## ✅ ৩. Admin Page তৈরি করো (Placeholder)

📄 `pages/admin/create.js`

```jsx
import { useSession } from 'next-auth/react';

export default function CreatePost() {
  const { data: session } = useSession();

  if (session?.user?.email !== "your@email.com") {
    return <p className="text-center p-10">⛔ Unauthorized Access</p>;
  }

  return (
    <main className="max-w-2xl mx-auto px-4 py-10">
      <h1 className="text-2xl font-bold mb-4">Create New Post</h1>
      <p>This page will later include form to add Markdown files.</p>
    </main>
  );
}
```

---

## ✅ ৪. Deployment Preparation ✅

### ✅ Final Checklist:

✅ SEO Title & Description Everywhere  
✅ Favicon Added (`/public/favicon.ico`)  
✅ Open Graph Image Support  
✅ 404 Page Ready  
✅ Deployment on **Vercel**  
✅ `robots.txt`, `sitemap.xml` (Optional for advanced SEO)  
✅ `og:image` → Blog থাম্বনেইল future ready

---

## 🛠️ Extra Features (Future Upgrade Ideas)

| ফিচার | ব্যাখ্যা |
|-------|---------|
| CMS Integration | যেমন Contentlayer / Notion / Sanity  
| Comment System | Utterances / Giscus  
| Newsletter | Mailchimp integration  
| Dark Mode | Tailwind Toggle  
| Tags & Categories | `/blog/tags/react` এর মতো

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Admin Only UI | Email check দিয়ে control  
| Add Post Button | Create page future routing  
| Deployment Ready | SEO, Styling, Routing ঠিক আছে কিনা  
| Future Proofing | পরবর্তীতে সহজে feature যোগ করা যাবে

---

## ❓ কুইজ:

👉 কিভাবে Tailwind button hover effect দেওয়া হয়?

A. `hover:bg-blue-600` ✅  
B. `:hover-blue`  
C. `hoverEffect-blue`  
D. `hover:active-bg`

---

### 🎉 তুমি সফলভাবে শেষ করলা:

> ✅ Blogging System with Markdown + Dynamic Slug  
> ✅ Tailwind CSS UI  
> ✅ SEO Meta Tag + Responsive Design  
> ✅ Admin Utility + Deploy Ready Setup

---

### 🔜 এখন আমরা শুরু করতে পারি:

🟧 **Week 6: Dashboard + Admin UI Design with Tailwind CSS**  
👉 তুমি এখানে শিখবে professional admin panel বানানো, table, sidebar, layout, responsive UI design

**শুরু করবো Week 6 – Day 1? 😄📊**

---

চল তাহলে শুরু করি! 😎  
আজ থেকে তুমি শিখবে **Week 6 – Admin Dashboard UI Design with Tailwind CSS**  
👉 এই সপ্তাহে তুমি নিজের হাতে বানাতে শিখবে একদম প্রফেশনাল লেভেলের অ্যাডমিন প্যানেল – ঠিক যেমন দেখা যায় SaaS বা client panel গুলোতে!

---

# 📊 Week 6 – Day 1: Admin Dashboard Layout with Sidebar + Topbar

---

## ✅ ১. আজকের লক্ষ্য:

- Layout component তৈরি করবো  
- Sidebar (navigation) এবং Topbar (logo + logout) থাকবে  
- সব Dashboard page এর মধ্যে এই layout reuse করবো  
- Tailwind দিয়ে সুন্দর UI বানাবো

---

## ✅ ২. Project Structure (for dashboard):

```
pages/
├── dashboard/
│   ├── index.js         → Dashboard Home
│   └── users.js         → Users Table Page (later)
components/
├── DashboardLayout.js   → Sidebar + Topbar
└── SidebarLink.js       → Sidebar menu link
```

---

## ✅ ৩. Step-by-Step: DashboardLayout

📄 `components/DashboardLayout.js`

```jsx
import Link from "next/link";

export default function DashboardLayout({ children }) {
  return (
    <div className="flex h-screen bg-gray-100">
      {/* Sidebar */}
      <aside className="w-64 bg-white shadow-md p-4 hidden md:block">
        <h2 className="text-2xl font-bold mb-6">Admin Panel</h2>
        <ul className="space-y-3">
          <li><Link href="/dashboard" className="text-blue-600">📊 Dashboard</Link></li>
          <li><Link href="/dashboard/users">👥 Users</Link></li>
          <li><Link href="#">⚙️ Settings</Link></li>
        </ul>
      </aside>

      {/* Main Content */}
      <div className="flex-1 flex flex-col">
        {/* Topbar */}
        <header className="bg-white shadow p-4 flex justify-between items-center">
          <h1 className="text-xl font-semibold">Welcome Admin</h1>
          <button className="text-sm text-red-600">Logout</button>
        </header>

        {/* Page content */}
        <main className="p-6 overflow-y-auto">{children}</main>
      </div>
    </div>
  );
}
```

---

## ✅ ৪. Dashboard Home Page

📄 `pages/dashboard/index.js`

```jsx
import DashboardLayout from '../../components/DashboardLayout';

export default function DashboardHome() {
  return (
    <DashboardLayout>
      <h2 className="text-2xl font-bold mb-4">📊 Dashboard Overview</h2>
      <p>Here you can manage users, posts, and system settings.</p>
    </DashboardLayout>
  );
}
```

---

## ✅ ৫. Tailwind UI Explanation

| ক্লাস | কাজ |
|------|-----|
| `flex` | Layout বানানো |
| `h-screen` | ফুল স্ক্রিন হাইট |
| `bg-gray-100` | হালকা ব্যাকগ্রাউন্ড |
| `shadow-md` | বক্স শ্যাডো |
| `p-4`, `p-6` | প্যাডিং |
| `text-xl`, `font-bold` | বড় ও মোটা লেখা |

---

## ✅ ৬. Bonus – Responsive Sidebar Hide on Mobile  
✅ আমরা `hidden md:block` দিয়ে ছোট স্ক্রিনে সাইডবার লুকিয়ে রাখছি।

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Layout Component | sidebar + topbar রিইউজেবল কম্পোনেন্ট |
| Tailwind Flex Layout | Column layout বানানো |
| Dashboard Routing | `/dashboard/*` সব পেজে layout থাকবে |
| Responsive Design | মোবাইল/ডেস্কটপে আলাদা লুক |

---

## 🛠️ প্র্যাকটিস করো:

1. নতুন একটি `/dashboard/users.js` পেজ বানাও  
2. DashboardLayout এ সেট করো  
3. Side menu থেকে লিংকে ক্লিক করলে পেজ চেঞ্জ হয় কিনা দেখো  
4. Mobile স্ক্রিনে sidebar hide হচ্ছে কিনা চেক করো

---

## ❓ কুইজ:

👉 `flex h-screen` কী করে?

A. হরিজন্টাল পজিশনিং  
B. স্ক্রল বন্ধ করে  
C. ফুল স্ক্রিন হাইটে লেআউট দেয় ✅  
D. মেনু হাইড করে

---

### 🔜 আগামীকাল (Day 2):  
**User Table UI – Table Design with Tailwind CSS + Sample Data**

তুমি কি চাও আমি এখনই Day 2 – User Table Design শুরু করে দিই? 😄📋

---

তাহলে চল! 😄  
আজ আমরা করবো **Week 6 – Day 2: User Table UI Design using Tailwind CSS**  
👉 আজ তুমি শিখবে কিভাবে একটা সুন্দর, প্রফেশনাল **User Table** বানানো হয় Tailwind CSS দিয়ে — যেটা future-এ ডেটাবেইজ/এপিআই এর সাথে কানেক্ট হবে।

---

# 📋 Day 2: Responsive User Table UI with Tailwind CSS

---

## ✅ ১. আমাদের লক্ষ্য:

- User list দেখাবে টেবিল আকারে  
- প্রতি row-তে: নাম, ইমেইল, রোল  
- Table scrollbar থাকবে  
- Future ready: API থেকে data load করা যাবে

---

## ✅ ২. Dummy Data তৈরি করো

📄 `data/users.js`

```js
const users = [
  {
    id: 1,
    name: "Hamid Uddin",
    email: "hamid@example.com",
    role: "Admin",
  },
  {
    id: 2,
    name: "Sadia Rahman",
    email: "sadia@example.com",
    role: "Editor",
  },
  {
    id: 3,
    name: "Nusrat Jahan",
    email: "nusrat@example.com",
    role: "Viewer",
  },
];

export default users;
```

---

## ✅ ৩. Create User Table Page

📄 `pages/dashboard/users.js`

```jsx
import DashboardLayout from "@/components/DashboardLayout";
import users from "@/data/users";

export default function UsersPage() {
  return (
    <DashboardLayout>
      <h2 className="text-2xl font-bold mb-6">👥 Users</h2>

      <div className="overflow-x-auto bg-white rounded-lg shadow p-4">
        <table className="min-w-full table-auto text-left">
          <thead>
            <tr className="bg-gray-100 text-gray-600 uppercase text-sm leading-normal">
              <th className="py-3 px-6">Name</th>
              <th className="py-3 px-6">Email</th>
              <th className="py-3 px-6">Role</th>
            </tr>
          </thead>
          <tbody className="text-gray-700 text-sm">
            {users.map((user) => (
              <tr key={user.id} className="border-b hover:bg-gray-50">
                <td className="py-3 px-6 font-medium">{user.name}</td>
                <td className="py-3 px-6">{user.email}</td>
                <td className="py-3 px-6">
                  <span className={`px-2 py-1 rounded-full text-xs font-semibold
                    ${user.role === "Admin" ? "bg-red-100 text-red-600" :
                      user.role === "Editor" ? "bg-blue-100 text-blue-600" :
                        "bg-gray-100 text-gray-600"}`}>
                    {user.role}
                  </span>
                </td>
              </tr>
            ))}
          </tbody>
        </table>
      </div>
    </DashboardLayout>
  );
}
```

---

## ✅ ৪. Tailwind Explanation:

| ক্লাস | কাজ |
|------|-----|
| `overflow-x-auto` | ছোট স্ক্রিনে টেবিল scroll হয়  
| `table-auto` | Table layout auto adjust  
| `bg-white rounded shadow` | সুন্দর কার্ডের মতো টেবিল  
| `hover:bg-gray-50` | হোভার ইফেক্ট  
| `badge-style role` | Role অনুযায়ী রঙ

---

## ✅ ৫. Output:

✔️ সুন্দর টেবিল  
✔️ মোবাইল-ফ্রেন্ডলি  
✔️ হোভার ইফেক্ট  
✔️ Role এর ভিত্তিতে কালার

---

## 🧠 আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| Table UI | ডেটা দেখানোর প্রফেশনাল স্টাইল  
| Tailwind Table Classes | padding, border, hover effect  
| Role Styling | conditionally class যোগ  
| Responsive Table | ছোট স্ক্রিনেও usable

---

## 🛠️ প্র্যাকটিস করো:

1. আরো ৩টি user যোগ করো  
2. Table এ "Status" কলাম যোগ করো: Active/Inactive  
3. Table এর নিচে pagination (dummy) বসাও  
4. Table data future এ API থেকে আনতে পারবে এমন করে ভাবো

---

## ❓ কুইজ:

👉 `overflow-x-auto` ক্লাস কী কাজ করে?

A. Scroll বন্ধ করে  
B. টেবিল ভাঙে  
C. Horizontal Scroll যোগ করে ✅  
D. Row delete করে

---

### 🔜 আগামীকাল (Day 3):

**Dashboard Stats Card – Total Users, Active Users, Posts Count – Tailwind Grid Cards**  
তুমি কি এখনই Statistics Card (like admin panel summary) design শিখতে চাও? 😄📈

---

চমৎকার! 😊  
আজ আমরা করবো **Week 6 – Day 3: Dashboard Stats Cards – Total Users, Posts, Active Count**  
👉 আজ তুমি শিখবে কিভাবে Tailwind CSS দিয়ে **statistics card UI** বানানো হয় — যেটা সব Admin Panel-এ শুরুতেই থাকে।

---

# 📈 Day 3: Dashboard Overview Cards with Tailwind CSS

---

## ✅ ১. আমাদের লক্ষ্য:

- Total Users, Active Users, Total Posts ইত্যাদি দেখাবে  
- প্রতিটি Card হবে আলাদা রঙে  
- Responsive grid layout (mobile → 1 column, desktop → 3)

---

## ✅ ২. Sample Stat Data

📄 `data/stats.js`

```js
const stats = [
  {
    id: 1,
    title: "Total Users",
    value: 128,
    icon: "👥",
    color: "bg-blue-100 text-blue-700"
  },
  {
    id: 2,
    title: "Active Users",
    value: 86,
    icon: "✅",
    color: "bg-green-100 text-green-700"
  },
  {
    id: 3,
    title: "Total Posts",
    value: 57,
    icon: "📝",
    color: "bg-yellow-100 text-yellow-700"
  },
];

export default stats;
```

---

## ✅ ৩. Dashboard Home Page – Add Cards

📄 `pages/dashboard/index.js`

```jsx
import DashboardLayout from '@/components/DashboardLayout';
import stats from '@/data/stats';

export default function DashboardHome() {
  return (
    <DashboardLayout>
      <h2 className="text-2xl font-bold mb-6">📊 Dashboard Overview</h2>

      {/* Stats Grid */}
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
        {stats.map(stat => (
          <div key={stat.id} className={`rounded-xl p-6 shadow ${stat.color}`}>
            <div className="text-4xl">{stat.icon}</div>
            <h3 className="text-lg font-semibold mt-2">{stat.title}</h3>
            <p className="text-3xl font-bold mt-1">{stat.value}</p>
          </div>
        ))}
      </div>
    </DashboardLayout>
  );
}
```

---

## ✅ ৪. Tailwind Grid Explanation:

| ক্লাস | কাজ |
|------|-----|
| `grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3` | responsive 1 → 2 → 3 columns  
| `rounded-xl p-6 shadow` | কার্ড স্টাইল  
| `${stat.color}` | ডায়নামিক রঙ যোগ করলাম  

---

## ✅ Output:

- ✔️ 3টি সুন্দর রঙিন কার্ড  
- ✔️ মোবাইল/ট্যাব/ডেস্কটপে responsive layout  
- ✔️ প্রতি কার্ডে Emoji/Icon + Title + সংখ্যা

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Stat Cards | Admin summary দেখানোর UI  
| Tailwind Grid | responsive গ্রিড  
| Dynamic Classes | একাধিক কালার handle  
| Componentized Layout | কার্ড UI বারবার ব্যবহার করা যাবে

---

## 🛠️ প্র্যাকটিস করো:

1. একটি নতুন কার্ড যোগ করো – যেমন: “Pending Reviews”  
2. Icon পরিবর্তন করো – Emoji বা SVG ব্যবহার করো  
3. Number count animation future-এ ভাবো (Bonus)  
4. Dark mode থাকলে কালার ম্যাচ করো

---

## ❓ কুইজ:

👉 `grid-cols-1 sm:grid-cols-2 md:grid-cols-3` এই ক্লাস কী করে?

A. সবসময় 3 কলাম  
B. responsive 1→2→3 কলাম ✅  
C. ফিক্সড কলাম  
D. রোল-বেসড layout

---

### 🔜 আগামীকাল (Day 4):

**Sidebar Active Link Highlight + Mobile Toggle Button + Responsive UX Upgrade**  
তুমি কি এখনই সাইডবারে active page highlight + মোবাইলে টগল শেখতে চাও? 😄📱

---

চমৎকার! 😊  
আজ আমরা করবো **Week 6 – Day 4: Sidebar Active Link Highlight + Mobile Toggle Sidebar**  
👉 আজ তুমি শিখবে কিভাবে Tailwind CSS দিয়ে sidebar এর current/active link highlight করা যায় এবং মোবাইলে sidebar toggle করা যায় — **responsive Admin UX** এর জন্য খুবই দরকারি।

---

# 📱 Day 4: Sidebar UX – Active Link Highlight + Mobile Toggle Menu

---

## ✅ ১. আমাদের টার্গেট:

- Sidebar এ কোন লিংকে এখন আছো সেটা highlight হবে  
- মোবাইলে toggle বাটন দিয়ে sidebar দেখানো/লুকানো যাবে  
- সব কিছু responsive হবে Tailwind দিয়ে

---

## ✅ ২. Use `useRouter()` to Get Current Page

📄 `components/DashboardLayout.js`

```jsx
import Link from 'next/link';
import { useRouter } from 'next/router';
import { useState } from 'react';

export default function DashboardLayout({ children }) {
  const router = useRouter();
  const [menuOpen, setMenuOpen] = useState(false);

  const menuItems = [
    { name: "Dashboard", path: "/dashboard", icon: "📊" },
    { name: "Users", path: "/dashboard/users", icon: "👥" },
    { name: "Settings", path: "#", icon: "⚙️" },
  ];

  return (
    <div className="flex h-screen bg-gray-100">
      {/* Sidebar */}
      <aside className={`${menuOpen ? 'block' : 'hidden'} md:block w-64 bg-white shadow-md p-4`}>
        <h2 className="text-2xl font-bold mb-6">Admin Panel</h2>
        <ul className="space-y-3">
          {menuItems.map((item) => (
            <li key={item.path}>
              <Link
                href={item.path}
                className={`block px-4 py-2 rounded-lg hover:bg-gray-100 ${
                  router.pathname === item.path
                    ? 'bg-blue-100 text-blue-700 font-semibold'
                    : 'text-gray-700'
                }`}
              >
                {item.icon} {item.name}
              </Link>
            </li>
          ))}
        </ul>
      </aside>

      {/* Main Content */}
      <div className="flex-1 flex flex-col">
        {/* Topbar */}
        <header className="bg-white shadow p-4 flex justify-between items-center">
          <div className="md:hidden">
            <button
              onClick={() => setMenuOpen(!menuOpen)}
              className="text-gray-700 bg-gray-200 px-3 py-1 rounded"
            >
              ☰ Menu
            </button>
          </div>
          <h1 className="text-xl font-semibold hidden md:block">Welcome Admin</h1>
          <button className="text-sm text-red-600">Logout</button>
        </header>

        {/* Page content */}
        <main className="p-6 overflow-y-auto">{children}</main>
      </div>
    </div>
  );
}
```

---

## ✅ Output:

- ✅ Current page link bold & blue highlight  
- ✅ মোবাইলে ☰ Menu বাটনে টিপলে sidebar দেখায়  
- ✅ Desktop এ সবসময় sidebar দেখা যায়  
- ✅ Toggle বন্ধ করলে sidebar গায়েব হয়

---

## ✅ Tailwind Breakdown:

| ক্লাস | ব্যাখ্যা |
|------|---------|
| `router.pathname` | Active route চেক করতে  
| `hidden md:block` | ছোট স্ক্রিনে hide  
| `bg-blue-100 text-blue-700` | active স্টাইল  
| `setMenuOpen(!menuOpen)` | toggle sidebar state

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| Active Link | route চেক করে হাইলাইট  
| Mobile Menu | toggle state দিয়ে menu show/hide  
| Responsive Sidebar | ছোট স্ক্রিনে menu কাজ করে  
| Tailwind Utility | class conditionally handle করা

---

## 🛠️ প্র্যাকটিস করো:

1. আরেকটা page যোগ করো – `/dashboard/settings.js`  
2. সেটাকে menu-তে বসাও  
3. সেই পেজেও active highlight কাজ করে কিনা দেখো  
4. Mobile থেকে টেস্ট করো sidebar toggle

---

## ❓ কুইজ:

👉 কোন Tailwind ক্লাস দিয়ে মোবাইলে লুকানো যায়?

A. `none-md`  
B. `mobile:hidden`  
C. `hidden md:block` ✅  
D. `sm:invisible`

---

### 🔜 আগামীকাল (Day 5 – Final):
**Dashboard Table Actions – Edit/Delete Buttons, Confirm Modal (UI only)**  
👉 তুমি শিখবে কিভাবে টেবিল row-তে Action বাটন দেখানো হয় এবং UI modal খোলা যায়

তুমি কি এখনই Final Dashboard Table Actions শেখা শুরু করতে চাও? 😄🛠️

---

দারুণ! 😄  
আজ আমরা করবো **Week 6 – Day 5: Dashboard Table Actions – Edit/Delete Buttons + Modal UI (UI only)**  
👉 এই টপিকে তুমি শিখবে কিভাবে Dashboard টেবিলে প্রতিটি ইউজারের পাশে **Edit/Delete বাটন** রাখা হয় এবং **Confirmation Modal UI** তৈরি করা হয় Tailwind CSS দিয়ে।

---

# 🛠️ Day 5: User Table Row Actions + Confirmation Modal

---

## ✅ ১. আজ আমরা করবো:

- প্রতি ইউজার row-তে “Edit” ও “Delete” বাটন  
- Delete চাপলে একটি modal confirm করবে  
- Edit এখন placeholder রাখবো (future-ready)

---

## ✅ ২. Update `pages/dashboard/users.js`

### 🔁 Update Table Row:

```jsx
<tbody className="text-gray-700 text-sm">
  {users.map((user) => (
    <tr key={user.id} className="border-b hover:bg-gray-50">
      <td className="py-3 px-6 font-medium">{user.name}</td>
      <td className="py-3 px-6">{user.email}</td>
      <td className="py-3 px-6">
        <span className={`px-2 py-1 rounded-full text-xs font-semibold
          ${user.role === "Admin" ? "bg-red-100 text-red-600" :
            user.role === "Editor" ? "bg-blue-100 text-blue-600" :
              "bg-gray-100 text-gray-600"}`}>
          {user.role}
        </span>
      </td>
      <td className="py-3 px-6">
        <button className="text-blue-600 hover:underline mr-3">Edit</button>
        <button
          onClick={() => handleDelete(user)}
          className="text-red-600 hover:underline"
        >
          Delete
        </button>
      </td>
    </tr>
  ))}
</tbody>
```

---

## ✅ ৩. Add Delete Modal (UI only)

```jsx
import { useState } from 'react';
import users from '@/data/users';
import DashboardLayout from '@/components/DashboardLayout';

export default function UsersPage() {
  const [showModal, setShowModal] = useState(false);
  const [selectedUser, setSelectedUser] = useState(null);

  const handleDelete = (user) => {
    setSelectedUser(user);
    setShowModal(true);
  };

  const closeModal = () => {
    setShowModal(false);
    setSelectedUser(null);
  };

  const confirmDelete = () => {
    console.log("Deleted:", selectedUser.name);
    closeModal();
  };

  return (
    <DashboardLayout>
      <h2 className="text-2xl font-bold mb-6">👥 Users</h2>

      {/* Table... (from before) */}

      {/* Modal */}
      {showModal && (
        <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
          <div className="bg-white rounded-xl p-6 w-full max-w-sm text-center shadow-lg">
            <h3 className="text-xl font-semibold mb-4">Confirm Delete</h3>
            <p>Are you sure you want to delete <strong>{selectedUser.name}</strong>?</p>
            <div className="mt-6 flex justify-center gap-4">
              <button onClick={confirmDelete} className="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700">Yes, Delete</button>
              <button onClick={closeModal} className="bg-gray-200 px-4 py-2 rounded hover:bg-gray-300">Cancel</button>
            </div>
          </div>
        </div>
      )}
    </DashboardLayout>
  );
}
```

---

## ✅ Output:

- ✅ প্রতিটি row-তে Edit/Delete  
- ✅ Delete চাপলে modal খুলে confirm চায়  
- ✅ “Yes” চাপলে console log করে  
- ✅ “Cancel” চাপলে modal বন্ধ হয়

---

## ✅ Tailwind Breakdown:

| ক্লাস | কাজ |
|------|------|
| `fixed inset-0` | স্ক্রিনজুড়ে overlay  
| `bg-opacity-50` | অল্প কালো ব্যাকগ্রাউন্ড  
| `z-50` | সব কিছুর উপর দেখায়  
| `rounded-xl shadow` | সুন্দর popup UI  
| `text-center`, `gap-4` | সুন্দর layout ও alignment

---

## ✅ আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| Edit/Delete Buttons | Row-level action buttons  
| Modal UI | Confirmation popup তৈরি  
| State Handling | `useState` দিয়ে modal toggle  
| Tailwind Modal Style | Responsive ও সুন্দর ডিজাইন

---

## 🛠️ প্র্যাকটিস করো:

1. Modal এর ভিতরে ইউজারের রোল দেখাও  
2. Edit বাটন future redirect করার জন্য `Link` ব্যবহার করো  
3. Confirm delete এ Toast/Message দেখাও (optional)  
4. Modal responsive কিনা টেস্ট করো মোবাইল/ট্যাবে

---

## ❓ কুইজ:

👉 কোন Tailwind ক্লাস সব কিছুর উপরে modal দেখাতে ব্যবহৃত হয়?

A. `absolute-top`  
B. `overlay`  
C. `z-50` ✅  
D. `layer-max`

---

### 🎉 তুমি সফলভাবে শেষ করলা:

✅ Week 6 – Full Admin Dashboard UI Design with Tailwind CSS  
✅ Sidebar, Topbar, Routing  
✅ Table + Actions + Stats Cards  
✅ Fully Responsive Layout

---

### 🔜 এবার তুমি চাইলে যেতে পারো:

- **Week 7: Blog Admin CRUD with File/Markdown Management**  
- **Week 7: User Table Dynamic with API & Database (Supabase / Prisma)**  
- অথবা তুমি যা বানাতে চাও সেটাও আমি গাইড করবো।

**তোমার পরবর্তী টার্গেট কী? 😄🔥**

---


একদম ঠিক! ✅  
তোমার শেখার অগ্রগতি অনুযায়ী এখন উপযুক্ত সময় **Week 7 – Fullstack Mini Project** শুরু করার — যাতে তুমি আগের সব কনসেপ্ট বাস্তবে প্রয়োগ করতে পারো।

---

# 📚 Week 7: Fullstack Mini Project – Task Manager / Notes App

## 🎯 ফিচারসমূহ:

✅ Signup/Login (next-auth or custom)  
✅ Notes: Add / Edit / Delete  
✅ MongoDB সংযুক্তি (with Mongoose or Prisma)  
✅ API Routes দিয়ে Backend তৈরি  
✅ Tailwind CSS দিয়ে Responsive UI  

---

## 💡 শেখা হবে একসাথে:

| বিষয় | ব্যাখ্যা |
|------|----------|
| Authentication | Secure login system  
| API Routing | Client ↔ Server ↔ Database  
| MongoDB Integration | Notes save, edit, delete  
| React Hooks | Form, CRUD functionality  
| Tailwind UI | Cards, Forms, Grid, Modal, Mobile Responsive  

---

✅ আমি এখন শুরু করবো **Day 1 – Project Setup + MongoDB Connection + Note Schema তৈরি**

তুমি কি প্রস্তুত শুরু করার জন্য? 😄🧠  
**বললেই আমি শুরু করি Day 1 – Setup** ✅

---

চমৎকার! 🎉  
তাহলে চল আমরা শুরু করি **Week 7 – Day 1: Project Setup + MongoDB Integration + Note Schema Design**  
👉 আজ আমরা বানাবো Fullstack Notes App এর বেস — যেখানে থাকবে MongoDB কানেকশন ও Note Schema।

---

# 🛠️ Day 1: Project Setup + MongoDB Connection + Note Schema

---

## ✅ ১. Project Structure Overview

```
📁 pages/
 ├── index.js           → Homepage (Notes list)
 ├── api/
 │    └── notes/
 │        ├── index.js   → GET/POST notes
 │        └── [id].js    → DELETE/PUT note by id
📁 models/
 └── Note.js             → Mongoose Schema
📁 lib/
 └── db.js               → MongoDB connection
📁 components/
 └── NoteCard.js         → Single note display
📄 .env.local             → MongoDB URI
```

---

## ✅ ২. Step-by-Step Setup

---

### ✅ Step 1: Create Next.js Project

```bash
npx create-next-app@latest notes-app
cd notes-app
```

---

### ✅ Step 2: Install Packages

```bash
npm install mongoose
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

---

### ✅ Step 3: Configure Tailwind

📄 `tailwind.config.js`

```js
content: [
  "./pages/**/*.{js,ts,jsx,tsx}",
  "./components/**/*.{js,ts,jsx,tsx}",
]
```

📄 `styles/globals.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

📄 `pages/_app.js`

```js
import '../styles/globals.css';

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />;
}
```

---

## ✅ ৩. MongoDB Setup

### ✅ Step 1: Create MongoDB Cluster  
👉 Go to [https://cloud.mongodb.com](https://cloud.mongodb.com)  
- Create free account  
- Create cluster  
- Whitelist IP: `0.0.0.0/0`  
- Create a user/password  
- Copy connection string

---

### ✅ Step 2: Add to `.env.local`

📄 `.env.local`

```
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/notes-app?retryWrites=true&w=majority
```

---

## ✅ ৪. Create MongoDB Connect File

📄 `lib/db.js`

```js
import mongoose from 'mongoose';

const connectDB = async () => {
  if (mongoose.connections[0].readyState) return;

  await mongoose.connect(process.env.MONGODB_URI, {
    useNewUrlParser: true,
    useUnifiedTopology: true
  });

  console.log("✅ MongoDB Connected");
};

export default connectDB;
```

---

## ✅ ৫. Create Note Model

📄 `models/Note.js`

```js
import mongoose from 'mongoose';

const NoteSchema = new mongoose.Schema({
  title: {
    type: String,
    required: true,
  },
  content: {
    type: String,
    required: true,
  }
}, {
  timestamps: true
});

export default mongoose.models.Note || mongoose.model('Note', NoteSchema);
```

---

## ✅ Test: Console MongoDB Connect

📄 `pages/api/test.js`

```js
import connectDB from '@/lib/db';
import Note from '@/models/Note';

export default async function handler(req, res) {
  await connectDB();
  const test = await Note.find({});
  res.status(200).json({ success: true, notes: test });
}
```

➡️ Run server: `npm run dev`  
➡️ Visit: `http://localhost:3000/api/test` → ✅ MongoDB connected!

---

## ✅ আজকের শেখা:

| টপিক | ব্যাখ্যা |
|------|----------|
| MongoDB Atlas | Free remote DB  
| Mongoose | Schema & model handle  
| API Route | Database fetch করার পাথ  
| Tailwind Setup | Responsive UI প্রস্তুত

---

## 🛠️ প্র্যাকটিস করো:

1. MongoDB URI `.env.local` এ ঠিকভাবে রেখো  
2. `db.js` এর connect ফাংশন রিইউজেবল করো  
3. Note Schema-তে `title`, `content` ছাড়া অন্য ফিল্ড চাইলে add করো

---

## ❓ কুইজ:

👉 `mongoose.models.Note || mongoose.model()` কেন ব্যবহার করা হয়?

A. সবসময় নতুন মডেল বানানোর জন্য  
B. Schema validate না করানোর জন্য  
C. Hot reload এ multiple model creation রোধ করতে ✅  
D. MongoDB বন্ধ করতে

---

### 🔜 আগামীকাল (Day 2):

**API Routes – Create, Fetch, Update, Delete Notes (Full CRUD in Next.js)**

তুমি কি এখনই Notes API (CRUD) শেখা শুরু করতে চাও? 😄📩

---

চমৎকার! 😊  
আজ আমরা করবো **Week 7 – Day 2: API Routes – Create, Read, Update, Delete (CRUD) for Notes**  
👉 তুমি আজ শিখবে কিভাবে Next.js API Routes ব্যবহার করে MongoDB এর সাথে কানেক্টেড **পুরো CRUD অপারেশন** করা যায়!

---

# 📩 Day 2: Full CRUD API for Notes in Next.js (MongoDB)

---

## ✅ ১. আমাদের লক্ষ্য:

- `GET` → সব নোট দেখাও  
- `POST` → নতুন নোট তৈরি  
- `DELETE` → নির্দিষ্ট নোট মুছে ফেলো  
- `PUT` → নির্দিষ্ট নোট আপডেট করো

---

## ✅ ২. API Routes Overview

📁 `pages/api/notes/`  
```
├── index.js       → GET, POST (All notes, create note)
└── [id].js        → GET, PUT, DELETE (Single note actions)
```

---

## ✅ ৩. `pages/api/notes/index.js`

```js
import connectDB from '@/lib/db';
import Note from '@/models/Note';

export default async function handler(req, res) {
  await connectDB();

  if (req.method === 'GET') {
    const notes = await Note.find({});
    return res.status(200).json({ notes });
  }

  if (req.method === 'POST') {
    const { title, content } = req.body;
    if (!title || !content) {
      return res.status(400).json({ error: 'Title and content required' });
    }

    const note = await Note.create({ title, content });
    return res.status(201).json({ note });
  }

  res.status(405).json({ error: 'Method not allowed' });
}
```

---

## ✅ ৪. `pages/api/notes/[id].js`

```js
import connectDB from '@/lib/db';
import Note from '@/models/Note';

export default async function handler(req, res) {
  await connectDB();
  const { id } = req.query;

  if (req.method === 'GET') {
    const note = await Note.findById(id);
    if (!note) return res.status(404).json({ error: 'Not found' });
    return res.status(200).json({ note });
  }

  if (req.method === 'PUT') {
    const { title, content } = req.body;
    const updated = await Note.findByIdAndUpdate(
      id,
      { title, content },
      { new: true }
    );
    return res.status(200).json({ updated });
  }

  if (req.method === 'DELETE') {
    await Note.findByIdAndDelete(id);
    return res.status(204).end();
  }

  res.status(405).json({ error: 'Method not allowed' });
}
```

---

## ✅ ৫. Test with Postman / Thunder Client (VS Code Extension)

**GET:**  
- `http://localhost:3000/api/notes`  
➡️ সব নোট দেখা যাবে

**POST:**  
- Body:
```json
{
  "title": "Test Note",
  "content": "This is a test note."
}
```

**DELETE:**  
- `http://localhost:3000/api/notes/<note-id>`

**PUT:**  
- Body:
```json
{
  "title": "Updated Title",
  "content": "Updated Content"
}
```

---

## ✅ আজকের শেখা:

| কাজ | ব্যাখ্যা |
|-----|----------|
| API Route | Next.js এর মাধ্যমে backend বানানো  
| MongoDB CRUD | Note Add/Edit/Delete করা  
| `req.method` | HTTP Method অনুযায়ী কাজ করা  
| REST API | Frontend থেকে কানেক্ট করার সুবিধা

---

## 🛠️ প্র্যাকটিস করো:

1. Thunder Client / Postman দিয়ে সব API call করে দেখো  
2. Title বা Content না থাকলে error আসে কিনা চেক করো  
3. Update করলে নতুন ডেটা ঠিক আসে কিনা verify করো  
4. Notes Collection MongoDB Atlas Console থেকে দেখো

---

## ❓ কুইজ:

👉 নিচের কোন HTTP Method দিয়ে ডেটা আপডেট করা হয়?

A. `GET`  
B. `POST`  
C. `PUT` ✅  
D. `DELETE`

---

### 🔜 আগামীকাল (Day 3):

**Frontend Note UI: Add Note Form + List Notes with Tailwind Cards**  
👉 তুমি শিখবে কিভাবে form দিয়ে নতুন note যোগ করতে হয় এবং আগের notes সুন্দরভাবে দেখাতে হয়।

**চলো, Frontend UI নিয়ে কাজ শুরু করি? 😄📋**

---

চমৎকার! 😄  
আজ আমরা করবো **Week 7 – Day 3: Frontend UI – Add Note Form + Show All Notes (Tailwind Cards)**  
👉 আজ তুমি শিখবে কিভাবে:

- ✅ নতুন নোট add করো form দিয়ে  
- ✅ সব নোট fetch করে UI তে দেখাও  
- ✅ Tailwind দিয়ে সুন্দর responsive card layout বানাও

---

# 📝 Day 3: Note Form + Notes List (Frontend UI)

---

## ✅ ১. আমাদের লক্ষ্য:

- Create Note form (`title`, `content`)  
- `POST /api/notes` দিয়ে নতুন note save  
- `GET /api/notes` দিয়ে সব note list  
- Tailwind দিয়ে সুন্দর card UI

---

## ✅ ২. NoteCard Component বানাও

📁 `components/NoteCard.js`

```jsx
export default function NoteCard({ note }) {
  return (
    <div className="bg-white p-4 rounded shadow hover:shadow-md transition">
      <h3 className="text-xl font-bold">{note.title}</h3>
      <p className="text-gray-600 mt-2">{note.content}</p>
    </div>
  );
}
```

---

## ✅ ৩. Homepage বানাও: `pages/index.js`

```jsx
import { useEffect, useState } from 'react';
import NoteCard from '@/components/NoteCard';

export default function Home() {
  const [notes, setNotes] = useState([]);
  const [form, setForm] = useState({ title: '', content: '' });

  // Fetch notes on load
  useEffect(() => {
    fetchNotes();
  }, []);

  const fetchNotes = async () => {
    const res = await fetch('/api/notes');
    const data = await res.json();
    setNotes(data.notes);
  };

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = async (e) => {
    e.preventDefault();
    if (!form.title || !form.content) return alert("Fill all fields");

    const res = await fetch('/api/notes', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(form)
    });

    if (res.ok) {
      setForm({ title: '', content: '' });
      fetchNotes(); // Reload notes
    }
  };

  return (
    <div className="max-w-4xl mx-auto px-4 py-10">
      <h1 className="text-3xl font-bold mb-6">🗒️ My Notes</h1>

      {/* Add Note Form */}
      <form onSubmit={handleSubmit} className="space-y-4 mb-10 bg-white p-6 rounded shadow">
        <input
          name="title"
          placeholder="Note Title"
          value={form.title}
          onChange={handleChange}
          className="w-full border px-4 py-2 rounded"
        />
        <textarea
          name="content"
          placeholder="Note Content"
          value={form.content}
          onChange={handleChange}
          className="w-full border px-4 py-2 rounded"
        />
        <button
          type="submit"
          className="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700"
        >
          ➕ Add Note
        </button>
      </form>

      {/* Note List */}
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
        {notes.map((note) => (
          <NoteCard key={note._id} note={note} />
        ))}
      </div>
    </div>
  );
}
```

---

## ✅ Output:

- ✅ নতুন নোট ফর্ম পূরণ করলে API call করে Note যোগ হয়  
- ✅ নিচে সব নোট দেখা যাচ্ছে সুন্দর কার্ড আকারে  
- ✅ মোবাইল, ট্যাব, ডেস্কটপ responsive layout

---

## ✅ আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| React Form | `useState` দিয়ে controlled form  
| API Integration | Frontend → Backend POST/GET  
| useEffect | লোডের সময় note আনো  
| Tailwind Grid | সুন্দর responsive layout

---

## 🛠️ প্র্যাকটিস করো:

1. Note add হলে Toast/message দেখাও  
2. Card এ তারিখ (createdAt) দেখাও  
3. Empty থাকলে "No notes found" মেসেজ দাও  
4. Notes গুলো sort করো — নতুন আগে দেখাও

---

## ❓ কুইজ:

👉 `useEffect(() => { fetchNotes() }, [])` এর অর্থ কী?

A. যখনই notes চেঞ্জ হয়  
B. বারবার fetch করে  
C. প্রথম বার পেজ লোড হলে ১বার fetch করে ✅  
D. কোনো effect দেয় না

---

### 🔜 আগামীকাল (Day 4):

**Edit/Delete Functionality (PUT/DELETE) + Modal + Dynamic Reload**  
তুমি কি এখনই Edit & Delete শেখা শুরু করতে চাও? 😄✏️🗑️

---

দারুণ! 😊  
আজ আমরা করবো **Week 7 – Day 4: Edit & Delete Functionality for Notes – with Modal UI + API Integration**  
👉 আজ তুমি শিখবে কিভাবে প্রতিটি note কার্ডে **Edit** ও **Delete** বাটন যুক্ত করা যায় এবং modal UI দিয়ে update করা যায়।

---

# ✏️🗑️ Day 4: Edit & Delete Notes – Modal UI + CRUD Integration

---

## ✅ ১. আমাদের লক্ষ্য:

- প্রতিটি নোটের পাশে Edit ও Delete বাটন  
- Edit চাপলে modal form খুলবে  
- Update হলে নোট রিফ্রেশ হবে  
- Delete করলে confirm করে remove করবে

---

## ✅ ২. Update `NoteCard.js` – Add Buttons

📄 `components/NoteCard.js`

```jsx
export default function NoteCard({ note, onEdit, onDelete }) {
  return (
    <div className="bg-white p-4 rounded shadow hover:shadow-md transition">
      <h3 className="text-xl font-bold">{note.title}</h3>
      <p className="text-gray-600 mt-2">{note.content}</p>

      <div className="flex gap-4 mt-4 text-sm">
        <button
          onClick={() => onEdit(note)}
          className="text-blue-600 hover:underline"
        >
          ✏️ Edit
        </button>
        <button
          onClick={() => onDelete(note._id)}
          className="text-red-600 hover:underline"
        >
          🗑️ Delete
        </button>
      </div>
    </div>
  );
}
```

---

## ✅ ৩. Update `pages/index.js` – Modal + Functions

```jsx
import { useState, useEffect } from "react";
import NoteCard from "@/components/NoteCard";

export default function Home() {
  const [notes, setNotes] = useState([]);
  const [form, setForm] = useState({ title: "", content: "" });
  const [editingNote, setEditingNote] = useState(null);

  useEffect(() => {
    fetchNotes();
  }, []);

  const fetchNotes = async () => {
    const res = await fetch("/api/notes");
    const data = await res.json();
    setNotes(data.notes.reverse()); // latest first
  };

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleEdit = (note) => {
    setEditingNote(note);
    setForm({ title: note.title, content: note.content });
  };

  const handleDelete = async (id) => {
    const confirm = window.confirm("Are you sure?");
    if (!confirm) return;

    await fetch(`/api/notes/${id}`, {
      method: "DELETE",
    });
    fetchNotes();
  };

  const handleSubmit = async (e) => {
    e.preventDefault();
    if (!form.title || !form.content) return;

    if (editingNote) {
      // UPDATE
      await fetch(`/api/notes/${editingNote._id}`, {
        method: "PUT",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(form),
      });
      setEditingNote(null);
    } else {
      // CREATE
      await fetch("/api/notes", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(form),
      });
    }

    setForm({ title: "", content: "" });
    fetchNotes();
  };

  return (
    <div className="max-w-4xl mx-auto px-4 py-10">
      <h1 className="text-3xl font-bold mb-6">🗒️ My Notes</h1>

      {/* Form */}
      <form onSubmit={handleSubmit} className="space-y-4 mb-10 bg-white p-6 rounded shadow">
        <input
          name="title"
          placeholder="Note Title"
          value={form.title}
          onChange={handleChange}
          className="w-full border px-4 py-2 rounded"
        />
        <textarea
          name="content"
          placeholder="Note Content"
          value={form.content}
          onChange={handleChange}
          className="w-full border px-4 py-2 rounded"
        />
        <button
          type="submit"
          className="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700"
        >
          {editingNote ? "✏️ Update Note" : "➕ Add Note"}
        </button>
      </form>

      {/* Notes */}
      <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
        {notes.map((note) => (
          <NoteCard
            key={note._id}
            note={note}
            onEdit={handleEdit}
            onDelete={handleDelete}
          />
        ))}
      </div>
    </div>
  );
}
```

---

## ✅ Output:

- ✅ প্রতিটি নোটের পাশে Edit/Delete  
- ✅ Edit করলে উপরের form ফিলাপ হয়  
- ✅ Update চাপলে note আপডেট হয়  
- ✅ Delete দিলে confirm করে remove হয়

---

## ✅ আজকের শেখা:

| ফিচার | ব্যাখ্যা |
|-------|----------|
| Edit Mode | form এ ডেটা বসানো  
| PUT Method | Update করতে  
| DELETE Method | remove note by id  
| Modal/Inline Form | update UI inside same form  

---

## 🛠️ প্র্যাকটিস করো:

1. Edit করলে ফর্ম রঙ পরিবর্তন করো (blue background ইত্যাদি)  
2. Toast/message বসাও “Note updated”  
3. Modal pop-up করে Edit form দেখাতে পারো (next upgrade)  
4. Validation: title বা content ফাঁকা রাখলে error দেখাও

---

## ❓ কুইজ:

👉 কোন HTTP Method ডেটা মুছে ফেলার জন্য ব্যবহার হয়?

A. `POST`  
B. `GET`  
C. `PUT`  
D. `DELETE` ✅

---

### 🔜 আগামীকাল (Day 5 – Final):

**UI Polish + Responsive Fix + Ready for Vercel Deployment**  
তুমি শিখবে Final Touch দিতে, মোবাইল responsive বানাতে ও প্রজেক্ট Vercel এ Live করার পুরো প্রক্রিয়া

**তুমি কি এখনই Final Polish + Deployment স্টেপে যেতে চাও? 😄🚀**

---

চল তাহলে শেষ ধাপে যাওয়া যাক! 🎉  
আজ আমরা করবো **Week 7 – Day 5: Final UI Polish + Responsive Fix + Deploy to Vercel**  
👉 তুমি আজ শিখবে কিভাবে:

- ✅ Project এর UI final polish দেবে  
- ✅ Mobile/tablet responsive check করবে  
- ✅ Live deploy করবে Vercel এ — একদম production-ready!

---

# 🚀 Day 5: Final Polish + Responsive UX + Deploy to Vercel

---

## ✅ ১. Final UI Polish

📌 ফোকাস করবো:

- Input ফোকাস স্টাইল  
- Error Message  
- Button hover  
- Empty state

---

### 🔧 Add Input Focus & Transitions

```html
<input
  className="w-full border px-4 py-2 rounded focus:outline-none focus:ring-2 focus:ring-blue-400 transition"
/>
```

---

### ❗ Show Error if fields empty

```js
if (!form.title || !form.content) {
  alert("Please fill all fields");
  return;
}
```

---

### ➕ Empty state message

```jsx
{notes.length === 0 && (
  <p className="text-gray-500">No notes found. Start by adding one!</p>
)}
```

---

## ✅ ২. Mobile Responsive Check ✅

Tailwind দিয়ে mobile-first responsive already আছে:

| স্ক্রিন | ক্লাস |
|--------|--------|
| মোবাইল | `grid-cols-1`  
| ট্যাব | `sm:grid-cols-2`  
| ডেস্কটপ | `md:grid-cols-3`

---

## ✅ ৩. Vercel এ Deploy 🚀

---

### ✅ Step-by-step Deploy

1. 🧑‍💻 GitHub Repo বানাও  
2. Terminal:
```bash
git init
git add .
git commit -m "Initial Commit"
git remote add origin https://github.com/yourname/notes-app.git
git push -u origin main
```

3. 🌐 Vercel এ যাও → [https://vercel.com](https://vercel.com)  
4. “**New Project**” → GitHub থেকে Import করো  
5. `.env` variables বসাও:
```
MONGODB_URI=your-full-mongo-uri
```

6. ✅ Deploy বাটনে ক্লিক করো  
7. 🎉 Live link পাবে: `https://notes-app.vercel.app`

---

## ✅ আজকের শেখা:

| বিষয় | ব্যাখ্যা |
|------|----------|
| UI Polish | focus, error, spacing  
| Responsive Grid | ছোট স্ক্রিনে সুন্দর লুক  
| Deployment | GitHub → Vercel  
| ENV Setup | MongoDB URI live environment এ

---

## ✅ Final Project Summary

| ফিচার | যুক্ত ✅ |
|--------|--------|
| Auth (Skip/Optional) | ❌ (future add করবো)  
| Notes Create         | ✅  
| Notes List           | ✅  
| Edit / Delete        | ✅  
| MongoDB Connected    | ✅  
| Fully Responsive UI  | ✅  
| Vercel Deploy        | ✅  

---

## ❓ কুইজ:

👉 `.env.local` এ Mongo URI রাখা কেন দরকার?

A. Code secure রাখতে ✅  
B. UI সুন্দর হয়  
C. Mongo চালু থাকে  
D. Google rank বাড়ে

---

### 🎉 তুমি সফলভাবে শেষ করলা:

✅ Week 7 – Fullstack Mini Project: Notes App  
✅ Full CRUD + MongoDB + Tailwind + Responsive + Deployment

---

### 🔜 এখন তুমি চাইলে শিখতে পারো:

- 🔐 **Auth System যোগ করা (Google Login / JWT)**  
- 🗃️ **Pagination, Search, Filter যুক্ত করা**  
- 🔧 **Admin Panel বানানো এই App এর জন্য**  
- 📦 **Next.js App with Prisma / Supabase Integration**  

**তোমার পরবর্তী টার্গেট কী? আমি প্ল্যান সাজিয়ে দেবো! 😄📘**

---

