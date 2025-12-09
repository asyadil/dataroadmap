# 🚀 ROADMAP: JavaScript + Vue.js Industry-Ready
## Timeline: 6 Minggu (Week 0 Prep + Week 1-5 Learning)

---

## 📍 WEEK 0: PRE-LEARNING PREPARATION (7 Hari)

### **Tujuan Week 0:**
- Survey & confirm internet spots
- Download semua offline resources
- Setup environment (Arch Linux + tools)
- Test logistics & daily pattern

---

### **Day -7 to -6: Internet Spots Survey**

**Lokasi Survey:**
1. **Perpustakaan IPB Dramaga** (Primary)
   - [ ] Test wifi speed (speedtest.net atau fast.com)
   - [ ] Cek colokan availability di area pilihan
   - [ ] Test duduk 2-3 jam (comfort check)
   - [ ] Cek policy (makan/minum, laptop, musholla)
   - [ ] Note jam sepi vs ramai
   - [ ] Confirm: Terbuka untuk umum (tukar identitas)

2. **Masjid Al-Hurriyah IPB** (Secondary Backup)
   - [ ] Check wifi availability & speed
   - [ ] Cek ruang belajar (ada space untuk laptop?)
   - [ ] Cek jam operasional (24/7 tapi mungkin ada jam tertentu lebih kondusif)
   - [ ] Test konektivitas (signal strength)

3. **Backup Exploration** (Optional)
   - [ ] Walk around kampus IPB - area mana yang bisa catch wifi?
   - [ ] Check gedung-gedung umum (GWW, LSI, dll) - ada wifi publik?

**Deliverable:** "Internet Access Map" (tulis di notes/spreadsheet):
```
PRIMARY: Perpustakaan IPB
- Hours: [hasil survey]
- Wifi: [speed test result]
- Distance: [dari Kampung Manggis]
- Notes: [observations]

BACKUP: Masjid Al-Hurriyah
- Hours: [hasil survey]
- Wifi: [speed test result]
- Notes: [observations]
```

---

### **Day -5 to -4: Arch Linux Setup + Tools Installation**

**System:**
- [ ] Install Arch Linux (jika belum)
- [ ] Performance tweaking (sesuai rencana Anda)
- [ ] Test stability (run beberapa jam, pastikan gak ada crash)

**Development Tools:**
```bash
# Node.js & npm
sudo pacman -S nodejs npm
node --version  # Verify: v18+ or v20+
npm --version   # Verify: 9+ or 10+

# Git
sudo pacman -S git
git --version

# Browser (pilih salah satu)
sudo pacman -S chromium  # atau brave-bin dari AUR
```

**VS Code + Extensions:**
- [ ] Install VS Code: `yay -S visual-studio-code-bin` (atau download manual)
- [ ] Extensions:
  - **Live Server** (Ritwick Dey) - WAJIB
  - **ESLint** (Microsoft) - Recommended
  - **Prettier** (optional)

**Git Configuration:**
```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@anda.com"
```

**Create GitHub Account** (jika belum punya):
- [ ] Sign up di github.com
- [ ] Setup SSH key (optional tapi recommended)

**Test Everything:**
```bash
# Test Node
node -e "console.log('Node works!')"

# Test npm (install test package)
mkdir ~/test-npm && cd ~/test-npm
npm init -y
npm install lodash
# Kalau berhasil download = npm works!
cd ~ && rm -rf ~/test-npm
```

---

### **Day -3: Offline Resources Download**

**Di Perpus/Masjid (butuh internet kenceng):**

**1. Dokumentasi (Save as PDF via browser):**
- [ ] JavaScript.info - Part 1 (all chapters): https://javascript.info
  - Cara: Buka tiap chapter → Print → Save as PDF
  - Atau: Clone repo offline version
- [ ] MDN JavaScript Guide: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide
- [ ] Vue.js Guide: https://vuejs.org/guide/introduction.html
- [ ] Express.js Getting Started: https://expressjs.com/en/starter/installing.html

**2. Video Tutorials (Download via youtube-dl atau browser extension):**
- [ ] Traversy Media - JavaScript Crash Course
- [ ] Web Dev Simplified - JavaScript Basics Playlist
- [ ] The Net Ninja - Vue 3 Composition API (pilih 5-7 video paling essential)

**3. Cheat Sheets (sudah include di Artifact 4 nanti):**
- Akan saya provide dalam artifact terpisah

**4. npm Packages untuk Offline (Pre-download):**
```bash
# Buat folder untuk cache packages
mkdir ~/npm-offline-cache

# Download common packages
cd ~/npm-offline-cache

# Vue & related
npm pack vue@latest
npm pack vite@latest
npm pack vue-router@latest

# Express & related  
npm pack express@latest
npm pack cors@latest
npm pack dotenv@latest

# Utilities
npm pack axios@latest
npm pack lodash@latest
```

**Storage Note:** Semua ini simpan di folder organized:
```
~/learning-materials/
├── docs/
│   ├── javascript-info.pdf
│   ├── mdn-guide.pdf
│   └── vue-guide.pdf
├── videos/
│   ├── js-crash-course.mp4
│   └── vue-basics.mp4
├── npm-cache/
│   └── [.tgz files]
└── code-snippets/
    └── [dari Artifact 5]
```

---

### **Day -2: Folder Structure + Test Offline Mode**

**Create Learning Folder:**
```bash
mkdir -p ~/js-learning/{week-{1..5}/day-{1..7},resources/{cheatsheets,snippets,projects}}
```

**Test Offline Coding:**
- [ ] Buat file HTML sederhana di ~/js-learning/test/
- [ ] Test: bisa buka di browser?
- [ ] Test: VS Code berfungsi normal tanpa internet?
- [ ] Test: Live Server extension works?

**Simulate Daily Pattern:**
- [ ] Pagi: Pergi ke perpus (test commute time)
- [ ] Siang: 3-4 jam di perpus (test stamina & environment)
- [ ] Sore: Pulang, test coding offline di rumah

**Adjust based on simulation:**
- Terlalu capek? Adjust transport method
- Perpus terlalu ramai? Note jam alternatif
- Dll.

---

### **Day -1: Final Prep + Mental Readiness**

**Technical:**
- [ ] Review folder structure (semua ready?)
- [ ] Backup semua downloaded materials (ke external drive/cloud?)
- [ ] Charge devices (laptop, HP for hotspot backup)
- [ ] Prepare notebook fisik (untuk catat bug/insight pas offline)

**Logistics:**
- [ ] Plan tomorrow's schedule (jam bangun, jam ke perpus, jam pulang)
- [ ] Prepare essentials (botol minum, snack, charger, earphone)
- [ ] Set alarms (02:30 untuk experimental time, jam perpus, dll)

**Mental:**
- [ ] Review roadmap Week 1 (tau apa yang akan dipelajari besok)
- [ ] Set intention (kenapa belajar ini? Target akhir apa?)
- [ ] Prepare diri untuk 35 hari intensif (komitmen!)

**Optional:**
- [ ] Istirahat cukup (besok mulai marathon!)
- [ ] Sholat istikharah (kalau perlu peace of mind)

---

## 📚 WEEK 1: JavaScript Fundamentals (7 Hari)

### **Goal Week 1:**
Paham syntax dasar JavaScript + bisa manipulasi DOM untuk bikin interactive webpage

---

### **DAY 1: Variables, Data Types, Operators**

**📖 Learning (4 jam - Perpus/Masjid):**

**Topik:**
1. **Variables** (let, const, var)
   - Kapan pakai let vs const
   - Kenapa avoid var (legacy)
   - Scope basics (global vs local)

2. **Data Types**
   - Primitives: string, number, boolean, null, undefined
   - typeof operator
   - Type coercion (implicit conversion)

3. **Operators**
   - Arithmetic (+, -, *, /, %, **)
   - Assignment (=, +=, -=, dll)
   - Comparison (==, ===, !=, !==, <, >)
   - Logical (&&, ||, !)

**Resources:**
- javascript.info: "JavaScript Fundamentals" → Variables, Data types, Operators
- MDN: JavaScript Basics

**💻 Practice (4 jam - Perpus/Masjid):**
```javascript
// Exercise 1: Variable declarations
let name = "Ahmad";
const age = 25;
console.log(name + " berumur " + age);

// Exercise 2: Data types
let isStudent = true;
let score = 85.5;
let hobby = null;
console.log(typeof isStudent); // "boolean"
console.log(typeof score);     // "number"

// Exercise 3: Operators
let x = 10;
let y = 3;
console.log(x + y);   // 13
console.log(x % y);   // 1 (modulo - sisa bagi)
console.log(x > y);   // true

// Exercise 4: String operations
let firstName = "Ahmad";
let lastName = "Rizki";
let fullName = firstName + " " + lastName;
console.log(fullName);
```

**Mini Project (2 jam - Perpus/Masjid):**
Buat file `calculator.js` yang:
- Input: dua angka & operator (+, -, *, /)
- Output: hasil kalkulasi
- Test dengan berbagai kombinasi

```javascript
// calculator.js
let num1 = 10;
let num2 = 5;
let operator = "+";

let result;
if (operator === "+") {
    result = num1 + num2;
} else if (operator === "-") {
    result = num1 - num2;
} else if (operator === "*") {
    result = num1 * num2;
} else if (operator === "/") {
    result = num1 / num2;
}

console.log(`${num1} ${operator} ${num2} = ${result}`);
```

**🌙 Experimental Time (02:30-Subuh - Rumah, Offline):**

**Suggestion:** Eksplor variasi calculator
- Coba operator lain (%%, **)
- Coba dengan string (gabungkan nama depan + belakang)
- Coba edge cases (bagi dengan 0, dll)
- Bikin versi yang lebih complex (3 angka, nested operations)

**Catatan Penting:**
- Kalau stuck: tulis pertanyaan di notebook → googling besok di perpus
- Fokus eksperimen, gak masalah kalau error (itu bagian dari belajar!)

---

### **DAY 2: Control Flow (If-Else, Switch)**

**📖 Learning (3 jam):**

**Topik:**
1. **If-Else Statements**
   - Single if
   - If-else
   - Else-if chain
   - Nested if
   - Ternary operator (shorthand)

2. **Switch Statements**
   - Syntax & use cases
   - Break statement
   - Default case
   - When to use switch vs if-else

3. **Truthy & Falsy Values**
   - Falsy: false, 0, "", null, undefined, NaN
   - Everything else is truthy
   - Practical implications

**Resources:**
- javascript.info: "Conditional operators: if, ?"
- javascript.info: "Switch statement"

**💻 Practice (5 jam):**

```javascript
// Exercise 1: Grade checker
let score = 85;
let grade;

if (score >= 90) {
    grade = "A";
} else if (score >= 80) {
    grade = "B";
} else if (score >= 70) {
    grade = "C";
} else if (score >= 60) {
    grade = "D";
} else {
    grade = "E";
}
console.log(`Score: ${score}, Grade: ${grade}`);

// Exercise 2: Ternary operator
let age = 17;
let status = age >= 18 ? "Adult" : "Minor";
console.log(status);

// Exercise 3: Switch for days
let day = 3;
let dayName;

switch(day) {
    case 1: dayName = "Senin"; break;
    case 2: dayName = "Selasa"; break;
    case 3: dayName = "Rabu"; break;
    case 4: dayName = "Kamis"; break;
    case 5: dayName = "Jumat"; break;
    case 6: dayName = "Sabtu"; break;
    case 7: dayName = "Minggu"; break;
    default: dayName = "Invalid day";
}
console.log(dayName);
```

**Mini Project (2 jam):**
**"Simple Decision Maker"**
- Input: waktu (jam dalam 24-hour format)
- Output: 
  - 04:00-11:00 → "Pagi - Saatnya Subuh & Belajar"
  - 11:00-15:00 → "Siang - Saatnya Dzuhur"
  - 15:00-18:00 → "Sore - Saatnya Ashar"
  - 18:00-19:00 → "Maghrib"
  - 19:00-04:00 → "Malam - Saatnya Istirahat"

```javascript
let hour = 14; // Test dengan berbagai jam

if (hour >= 4 && hour < 11) {
    console.log("Pagi - Saatnya Subuh & Belajar");
} else if (hour >= 11 && hour < 15) {
    console.log("Siang - Saatnya Dzuhur");
} // ... dst
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Bikin CLI Decision Tree
- Misal: "Sistem Rekomendasi Belajar"
  - Input: jam, mood, topik kesulitan
  - Output: rekomendasi (lanjut belajar / istirahat / review materi lama)
- Eksplor nested if-else yang complex
- Coba refactor pakai switch (mana yang lebih readable?)

---

### **DAY 3: Loops (For, While, For-Each)**

**📖 Learning (4 jam):**

**Topik:**
1. **For Loop**
   - Syntax: initialization, condition, increment
   - Use cases (iterate N times)
   - Break & continue

2. **While Loop**
   - Syntax & use cases
   - Difference vs for loop
   - Do-while variant

3. **For...of Loop** (Modern ES6)
   - Iterate over arrays easily
   - Cleaner syntax

**SPECIAL FOCUS:** Konsep iterasi (karena ini pain point Anda dari Python)

**Analogi Konkret:**
```
Array = Daftar belanja [Beras, Telur, Minyak]
Loop = Proses satu per satu:
  - Ambil item pertama (Beras)
  - Ambil item kedua (Telur)  
  - Ambil item ketiga (Minyak)
  - Selesai (gak ada lagi)
```

**Resources:**
- javascript.info: "Loops: while and for"
- Praktek langsung (trial-error until "click")

**💻 Practice (4 jam):**

```javascript
// Exercise 1: For loop basics
for (let i = 0; i < 5; i++) {
    console.log("Iterasi ke-" + i);
}
// Output: Iterasi ke-0, ke-1, ke-2, ke-3, ke-4

// Exercise 2: Loop through array
let cities = ["Jakarta", "Bandung", "Surabaya"];
for (let i = 0; i < cities.length; i++) {
    console.log(cities[i]);
}

// Exercise 3: Modern for...of (lebih gampang!)
for (let city of cities) {
    console.log(city); // Lebih simple, gak perlu index!
}

// Exercise 4: While loop
let count = 0;
while (count < 5) {
    console.log("Count: " + count);
    count++; // PENTING! Tanpa ini = infinite loop
}

// Exercise 5: Break & Continue
for (let i = 0; i < 10; i++) {
    if (i === 5) break; // Stop di 5
    if (i % 2 === 0) continue; // Skip even numbers
    console.log(i); // Output: 1, 3
}
```

**Mini Project (2 jam):**
**"Prayer Times Display"**
```javascript
let prayerTimes = [
    { name: "Subuh", time: "04:30" },
    { name: "Dzuhur", time: "12:00" },
    { name: "Ashar", time: "15:15" },
    { name: "Maghrib", time: "18:00" },
    { name: "Isya", time: "19:15" }
];

// Display semua menggunakan loop
console.log("=== Jadwal Sholat ===");
for (let prayer of prayerTimes) {
    console.log(`${prayer.name}: ${prayer.time}`);
}

// Challenge: Hitung berapa jam dari sekarang ke sholat berikutnya
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Loop Challenges
1. **FizzBuzz Classic:**
   - Loop 1-100
   - Kalau angka habis dibagi 3: print "Fizz"
   - Kalau habis dibagi 5: print "Buzz"  
   - Kalau habis dibagi 3 DAN 5: print "FizzBuzz"
   - Selain itu: print angka

2. **Pattern Printing:**
```
*
**
***
****
*****
```

3. **Reverse Array:** Pakai loop untuk balik urutan array tanpa .reverse()

4. **Sum Calculator:** Loop untuk jumlahkan semua angka dalam array

**Fokus:** Eksperimen sampai "click" dengan konsep iterasi!

---

### **DAY 4: Functions**

**📖 Learning (4 jam):**

**Topik:**
1. **Function Declaration**
   - Syntax, parameters, return value
   - Calling functions
   - Default parameters

2. **Function Expression**
   - Assign function ke variable
   - Anonymous functions

3. **Arrow Functions** (Modern ES6)
   - Concise syntax
   - When to use

4. **Scope & Closures** (Introduction)
   - Local vs global scope
   - Function scope

**Resources:**
- javascript.info: "Functions"
- javascript.info: "Function expressions and arrows"

**💻 Practice (4 jam):**

```javascript
// Exercise 1: Basic function
function greet(name) {
    return "Assalamualaikum, " + name;
}
console.log(greet("Ahmad")); // "Assalamualaikum, Ahmad"

// Exercise 2: Function with multiple parameters
function add(a, b) {
    return a + b;
}
console.log(add(5, 3)); // 8

// Exercise 3: Default parameters
function multiply(a, b = 2) {
    return a * b;
}
console.log(multiply(5));    // 10 (5 * 2)
console.log(multiply(5, 3)); // 15 (5 * 3)

// Exercise 4: Arrow function (modern & concise)
const subtract = (a, b) => a - b;
console.log(subtract(10, 3)); // 7

// Exercise 5: Arrow function with block
const calculateGrade = (score) => {
    if (score >= 90) return "A";
    else if (score >= 80) return "B";
    else if (score >= 70) return "C";
    else return "D";
};
console.log(calculateGrade(85)); // "B"
```

**Mini Project (2 jam):**
**"Utility Functions Library"**

Buat file `utils.js` dengan berbagai helper functions:
```javascript
// Temperature converter
const celsiusToFahrenheit = (celsius) => (celsius * 9/5) + 32;
const fahrenheitToCelsius = (fahrenheit) => (fahrenheit - 32) * 5/9;

// String utilities
const capitalize = (str) => str.charAt(0).toUpperCase() + str.slice(1);
const reverseString = (str) => str.split('').reverse().join('');

// Array utilities
const getMax = (arr) => Math.max(...arr);
const getMin = (arr) => Math.min(...arr);
const getAverage = (arr) => arr.reduce((a,b) => a+b) / arr.length;

// Prayer time checker
function getNextPrayer(currentHour) {
    if (currentHour < 4) return "Subuh";
    if (currentHour < 12) return "Dzuhur";
    if (currentHour < 15) return "Ashar";
    if (currentHour < 18) return "Maghrib";
    if (currentHour < 19) return "Isya";
    return "Subuh (besok)";
}

// Test functions
console.log(celsiusToFahrenheit(25));
console.log(capitalize("hello"));
console.log(getNextPrayer(14));
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Build Personal Function Library
- Bikin functions yang relate dengan daily life Anda
  - Calculator for sadaqah/zakat
  - Ayat randomizer (array of ayat, random pick)
  - Study time tracker (input: start time, end time → output: duration)
- Eksperimen: refactor kemarin punya code jadi reusable functions
- Challenge: Bikin function yang accept function sebagai parameter (higher-order function intro)

---

### **DAY 5: Arrays Deep Dive**

**📖 Learning (4 jam):**

**Topik:**
1. **Array Basics**
   - Create, access, modify
   - Length property
   - Add/remove elements (push, pop, shift, unshift)

2. **Array Methods** (Yang Sering Dipakai)
   - **map()** - Transform setiap element
   - **filter()** - Ambil element yang memenuhi kondisi
   - **find()** - Cari 1 element
   - **forEach()** - Loop modern
   - **some() & every()** - Boolean checks

3. **Array Manipulation**
   - slice() vs splice()
   - concat() & spread operator
   - sort() & reverse()

**KHUSUS FOKUS:** map(), filter(), forEach() - ini SERING BANGET dipakai di industri!

**Resources:**
- javascript.info: "Arrays" & "Array methods"
- MDN: Array reference

**💻 Practice (4 jam):**

```javascript
// Exercise 1: Array basics
let fruits = ["Apple", "Banana", "Orange"];
console.log(fruits[0]);      // "Apple"
console.log(fruits.length);  // 3

fruits.push("Mango");        // Add ke akhir
console.log(fruits);         // ["Apple", "Banana", "Orange", "Mango"]

// Exercise 2: forEach (loop modern)
fruits.forEach(fruit => {
    console.log(fruit);
});

// Exercise 3: map (transform array)
let numbers = [1, 2, 3, 4, 5];
let doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8, 10]

// Exercise 4: filter (ambil yang memenuhi kondisi)
let ages = [12, 15, 18, 21, 25, 30];
let adults = ages.filter(age => age >= 18);
console.log(adults); // [18, 21, 25, 30]

// Exercise 5: find (cari 1 element)
let users = [
    { name: "Ahmad", age: 17 },
    { name: "Budi", age: 25 },
    { name: "Citra", age: 30 }
];
let adult = users.find(user => user.age >= 18);
console.log(adult); // { name: "Budi", age: 25 }

// Exercise 6: Chaining methods (POWERFUL!)
let scores = [75, 88, 92, 65, 80];
let topScores = scores
    .filter(score => score >= 80)  // Ambil >= 80
    .map(score => score + 5)       // Bonus 5 poin
    .sort((a, b) => b - a);        // Sort descending
console.log(topScores); // [97, 93, 85]
```

**Mini Project (2 jam):**
**"Student Grade Processor"**

```javascript
let students = [
    { name: "Ahmad", score: 85 },
    { name: "Budi", score: 72 },
    { name: "Citra", score: 95 },
    { name: "Dewi", score: 68 },
    { name: "Eko", score: 88 }
];

// Task 1: Tambahkan grade ke setiap student
let studentsWithGrade = students.map(student => {
    let grade;
    if (student.score >= 90) grade = "A";
    else if (student.score >= 80) grade = "B";
    else if (student.score >= 70) grade = "C";
    else grade = "D";
    
    return { ...student, grade }; // Spread operator
});
console.log(studentsWithGrade);

// Task 2: Filter yang lulus (>= 70)
let passed = students.filter(s => s.score >= 70);
console.log("Passed students:", passed);

// Task 3: Hitung rata-rata score
let average = students.reduce((sum, s) => sum + s.score, 0) / students.length;
console.log("Average score:", average);

// Task 4: Cari student dengan score tertinggi
let topStudent = students.reduce((max, s) => s.score > max.score ? s : max);
console.log("Top student:", topStudent);
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Array Challenges
1. **To-Do List Manager** (pure array operations):
   - Add task
   - Remove task
   - Mark as complete
   - Filter: completed vs pending
   
2. **Prayer Times Finder:**
   - Array of cities dengan jadwal sholat masing-masing
   - Input: city name
   - Output: jadwal sholat city tersebut
   - Challenge: Find city dengan Subuh paling pagi

3. **Data Transformation:**
   - Convert array of objects ke format lain
   - Misal: [{name, score}] → {name: score, name2: score2}

---

### **DAY 6-7: DOM Manipulation & Events (CRITICAL!)**

**📖 Learning (6 jam across 2 days):**

**Topik:**
1. **DOM Basics**
   - What is DOM (Document Object Model)?
   - Selecting elements:
     - getElementById()
     - querySelector() & querySelectorAll()
     - getElementsByClassName()
   
2. **Modifying Elements**
   - textContent vs innerHTML
   - Changing styles (element.style.property)
   - Adding/removing classes (classList)
   - Creating & removing elements

3. **Event Listeners**
   - What are events? (click, input, submit, etc)
   - addEventListener()
   - Event object (e.target, e.preventDefault())
   - Event delegation (advanced)

**Resources:**
- javascript.info: "Document" section
- javascript.info: "Events" section

**💻 Practice (8 jam across 2 days):**

**Day 6 Focus: Selection & Modification**

```html
<!-- practice.html -->
<!DOCTYPE html>
<html>
<head>
    <title>DOM Practice</title>
    <style>
        .highlight { background-color: yellow; }
        .hidden { display: none; }
    </style>
</head>
<body>
    <h1 id="title">Hello World</h1>
    <p class="text">Paragraph 1</p>
    <p class="text">Paragraph 2</p>
    <button id="btn">Click Me</button>
    
    <script src="script.js"></script>
</body>
</html>
```

```javascript
// script.js - Day 6 exercises

// Exercise 1: Select & modify
let title = document.getElementById('title');
title.textContent = "Assalamualaikum!";
title.style.color = "blue";

// Exercise 2: Select multiple elements
let paragraphs = document.querySelectorAll('.text');
paragraphs.forEach(p => {
    p.classList.add('highlight');
});

// Exercise 3: Create new element
let newP = document.createElement('p');
newP.textContent = "This is a new paragraph";
document.body.appendChild(newP);

// Exercise 4: Remove element
let firstP = document.querySelector('.text');
firstP.remove();
```

**Day 7 Focus: Events & Interactivity**

```html
<!-- interactive.html -->
<!DOCTYPE html>
<html>
<head>
    <title>Interactive Page</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        .task { margin: 10px 0; padding: 10px; border: 1px solid #ddd; }
        .completed { text-decoration: line-through; opacity: 0.6; }
    </style>
</head>
<body>
    <h1>Simple To-Do List</h1>
    
    <input type="text" id="taskInput" placeholder="Enter task...">
    <button id="addBtn">Add Task</button>
    
    <div id="taskList"></div>
    
    <script src="app.js"></script>
</body>
</html>
```

```javascript
// app.js - Day 7 project

let taskInput = document.getElementById('taskInput');
let addBtn = document.getElementById('addBtn');
let taskList = document.getElementById('taskList');

let tasks = [];

// Add task on button click
addBtn.addEventListener('click', function() {
    let taskText = taskInput.value;
    
    if (taskText === '') {
        alert('Please enter a task!');
        return;
    }
    
    // Create task object
    let task = {
        id: Date.now(),
        text: taskText,
        completed: false
    };
    
    tasks.push(task);
    taskInput.value = '';
    renderTasks();
});

// Toggle task completion
function toggleTask(id) {
    let task = tasks.find(t => t.id === id);
    if (task) {
        task.completed = !task.completed;
        renderTasks();
    }
}

// Delete task
function deleteTask(id) {
    tasks = tasks.filter(t => t.id !== id);
    renderTasks();
}

// Render all tasks
function renderTasks() {
    taskList.innerHTML = '';
    
    tasks.forEach(task => {
        let taskDiv = document.createElement('div');
        taskDiv.className = 'task' + (task.completed ? ' completed' : '');
        taskDiv.innerHTML = `
            <input 
                type="checkbox" 
                ${task.completed ? 'checked' : ''}
                onchange="toggleTask(${task.id})"
            >
            <span>${task.text}</span>
            <button onclick="deleteTask(${task.id})">Delete</button>
        `;
        taskList.appendChild(taskDiv);
    });
}

// Enter key support
taskInput.addEventListener('keypress', (e) => {
    if (e.key === 'Enter') {
        addBtn.click();
    }
});
```

**🌙 Experimental Time (02:30-Subuh - Rumah, Offline):**

**Suggestion:** Polish Your To-Do List
- Add "Edit" functionality (double-click task to edit text)
- Add "Clear Completed" button
- Add filter buttons (All / Active / Completed)
- Add task counter ("3 tasks remaining")
- Save to localStorage (persist data on page reload)
- Add categories/tags to tasks
- Add due dates
- Experiment with different UI styles

**Week 1 Checkpoint:**
- [ ] Can create interactive webpage with HTML/CSS/JS
- [ ] Understand variables, loops, functions, arrays
- [ ] Can manipulate DOM (select, modify, create elements)
- [ ] Can handle events (clicks, inputs, forms)
- [ ] Built functional To-Do List from scratch

**Confidence check:** Rate 1-10, how confident you feel about Week 1 topics?
- If < 7: Review weak areas before Week 2
- If 7-8: Ready for Week 2!
- If 9-10: Excellent! Consider adding bonus challenges

---

## 📚 WEEK 2: Modern JavaScript + Async (7 Hari)

### **Goal Week 2:**
Master ES6+ features + asynchronous programming (Promises, async/await, Fetch API)

---

### **DAY 8: ES6+ Essentials Part 1**

**📖 Learning (4 jam - Perpus/Masjid):**

**Topik:**
1. **Destructuring**
   - Array destructuring
   - Object destructuring
   - Nested destructuring
   - Default values

2. **Spread Operator (...)**
   - Array spreading
   - Object spreading
   - Function arguments
   - Copying vs reference

3. **Rest Parameters**
   - Collecting arguments
   - Difference from spread

**Resources:**
- javascript.info: "Destructuring assignment"
- javascript.info: "Rest parameters and spread syntax"

**💻 Practice (4 jam - Perpus/Masjid):**

```javascript
// Exercise 1: Array destructuring
let colors = ['red', 'green', 'blue'];
let [first, second, third] = colors;
console.log(first);  // "red"
console.log(second); // "green"

// Skip elements
let [primary, , tertiary] = colors;
console.log(tertiary); // "blue"

// Rest in destructuring
let [head, ...tail] = colors;
console.log(head); // "red"
console.log(tail); // ["green", "blue"]

// Exercise 2: Object destructuring
let user = {
    name: "Ahmad",
    age: 25,
    city: "Bogor"
};

let { name, age } = user;
console.log(name); // "Ahmad"

// Rename variables
let { name: fullName, age: years } = user;
console.log(fullName); // "Ahmad"

// Default values
let { country = "Indonesia" } = user;
console.log(country); // "Indonesia"

// Exercise 3: Spread operator
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let combined = [...arr1, ...arr2];
console.log(combined); // [1, 2, 3, 4, 5, 6]

// Copy array (not reference!)
let original = [1, 2, 3];
let copy = [...original];
copy.push(4);
console.log(original); // [1, 2, 3] (unchanged!)
console.log(copy);     // [1, 2, 3, 4]

// Object spread
let person = { name: "Ahmad", age: 25 };
let employee = { ...person, job: "Developer" };
console.log(employee); 
// { name: "Ahmad", age: 25, job: "Developer" }

// Exercise 4: Rest parameters
function sum(...numbers) {
    return numbers.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3, 4, 5)); // 15

function greet(greeting, ...names) {
    return `${greeting} ${names.join(', ')}!`;
}
console.log(greet("Hello", "Ahmad", "Budi", "Citra"));
// "Hello Ahmad, Budi, Citra!"
```

**Mini Project (2 jam - Perpus/Masjid):**
**"Data Transformer"**

```javascript
// Transform array of user objects using destructuring & spread

let users = [
    { firstName: "Ahmad", lastName: "Rizki", age: 25, city: "Bogor" },
    { firstName: "Budi", lastName: "Santoso", age: 30, city: "Jakarta" },
    { firstName: "Citra", lastName: "Dewi", age: 22, city: "Bandung" }
];

// Task 1: Extract full names
let fullNames = users.map(({ firstName, lastName }) => 
    `${firstName} ${lastName}`
);
console.log(fullNames);

// Task 2: Add new property to all users
let usersWithCountry = users.map(user => ({
    ...user,
    country: "Indonesia"
}));

// Task 3: Merge two user lists (no duplicates)
let newUsers = [
    { firstName: "Eko", lastName: "Prasetyo", age: 28, city: "Surabaya" }
];
let allUsers = [...users, ...newUsers];

// Task 4: Function that accepts any number of user objects
function combineUsers(...userLists) {
    return userLists.flat();
}
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Destructuring Playground
- Refactor kemarin's To-Do code pakai destructuring
- Experiment dengan nested destructuring (objects dalam array)
- Create utility functions pakai rest parameters
- Challenge: Swap variables tanpa temporary variable (using destructuring)

---

### **DAY 9: ES6+ Essentials Part 2**

**📖 Learning (4 jam):**

**Topik:**
1. **Template Literals**
   - Basic interpolation
   - Multi-line strings
   - Tagged templates (advanced)

2. **Arrow Functions Deep Dive**
   - Syntax variations
   - Implicit return
   - this binding differences

3. **Enhanced Object Literals**
   - Shorthand properties
   - Shorthand methods
   - Computed property names

**Resources:**
- javascript.info: "Arrow functions revisited"
- MDN: Template literals

**💻 Practice (4 jam):**

```javascript
// Exercise 1: Template literals
let name = "Ahmad";
let age = 25;

// Old way
console.log("My name is " + name + " and I'm " + age + " years old.");

// New way
console.log(`My name is ${name} and I'm ${age} years old.`);

// Multi-line
let html = `
    <div class="user">
        <h2>${name}</h2>
        <p>Age: ${age}</p>
    </div>
`;

// Expressions inside
console.log(`Next year I'll be ${age + 1}`);
console.log(`Am I adult? ${age >= 18 ? 'Yes' : 'No'}`);

// Exercise 2: Arrow functions
// Traditional
function add(a, b) {
    return a + b;
}

// Arrow (full)
const add = (a, b) => {
    return a + b;
};

// Arrow (implicit return)
const add = (a, b) => a + b;

// Single parameter (parentheses optional)
const square = x => x * x;

// No parameters
const greet = () => console.log("Hello!");

// Returning object (need parentheses!)
const makePerson = (name, age) => ({ name, age });

// Exercise 3: this in arrow functions
let user = {
    name: "Ahmad",
    
    // Regular function - this = user object
    greetRegular: function() {
        console.log(`Hello, ${this.name}`);
    },
    
    // Arrow function - this = lexical (outer scope)
    greetArrow: () => {
        console.log(`Hello, ${this.name}`); // undefined!
    },
    
    // Useful in callbacks
    delayedGreet: function() {
        setTimeout(() => {
            console.log(`Hello, ${this.name}`); // Works!
        }, 1000);
    }
};

// Exercise 4: Enhanced object literals
let name = "Ahmad";
let age = 25;

// Shorthand properties
let person = { name, age }; // Instead of { name: name, age: age }

// Shorthand methods
let calculator = {
    // Old way
    add: function(a, b) {
        return a + b;
    },
    
    // New way
    subtract(a, b) {
        return a - b;
    },
    
    // Arrow function
    multiply: (a, b) => a * b
};

// Computed property names
let propName = "score";
let student = {
    name: "Ahmad",
    [propName]: 95,  // Dynamic property name!
    [`${propName}Percentage`]: 95 + "%"
};
console.log(student); // { name: "Ahmad", score: 95, scorePercentage: "95%" }
```

**Mini Project (2 jam):**
**"Student Report Generator"**

```javascript
let students = [
    { name: "Ahmad", math: 85, science: 90, english: 88 },
    { name: "Budi", math: 78, science: 82, english: 85 },
    { name: "Citra", math: 92, science: 95, english: 90 }
];

// Use arrow functions, template literals, destructuring
const generateReport = ({ name, math, science, english }) => {
    const average = ((math + science + english) / 3).toFixed(2);
    const grade = average >= 90 ? 'A' : 
                  average >= 80 ? 'B' : 
                  average >= 70 ? 'C' : 'D';
    
    return `
╔════════════════════════════════════╗
║ STUDENT REPORT CARD                ║
╠════════════════════════════════════╣
║ Name:    ${name.padEnd(24)} ║
║ Math:    ${math.toString().padEnd(24)} ║
║ Science: ${science.toString().padEnd(24)} ║
║ English: ${english.toString().padEnd(24)} ║
║ Average: ${average.padEnd(24)} ║
║ Grade:   ${grade.padEnd(24)} ║
╚════════════════════════════════════╝
    `.trim();
};

students.forEach(student => {
    console.log(generateReport(student));
});
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Refactor Everything!
- Go back to ALL previous projects (calculator, todo, etc)
- Refactor using: template literals, arrow functions, enhanced objects
- Notice how much cleaner the code becomes!
- Challenge: Rewrite without using `function` keyword at all

---

### **DAY 10-11: Async JavaScript - Promises (2 Hari)**

**📖 Learning (6 jam across 2 days):**

**Topik:**
1. **What is Asynchronous Programming?**
   - Synchronous vs Asynchronous
   - Blocking vs Non-blocking
   - Why async matters (UI responsiveness, API calls)

2. **Callbacks** (Brief intro - old way)
   - Callback hell problem
   - Why we moved away

3. **Promises** (Modern way - FOCUS HERE!)
   - Creating promises
   - Promise states (pending, fulfilled, rejected)
   - .then() and .catch()
   - .finally()
   - Chaining promises
   - Promise.all()
   - Promise.race()

**CRITICAL:** This is where Python "file handling" struggle might resurface - async is conceptually similar to handling operations that "take time". Take it slow!

**Resources:**
- javascript.info: "Introduction: callbacks"
- javascript.info: "Promises, async/await" (Promises section)
- Watch downloaded video on Promises

**💻 Practice (Day 10 - 4 jam):**

```javascript
// Exercise 1: Understanding async with setTimeout
console.log('Start');

setTimeout(() => {
    console.log('This runs after 2 seconds');
}, 2000);

console.log('End');

// Output order:
// "Start"
// "End"
// "This runs after 2 seconds" (after 2 sec delay)
// Why? setTimeout is ASYNC - doesn't block execution!

// Exercise 2: Creating a Promise
let myPromise = new Promise((resolve, reject) => {
    let success = true;
    
    setTimeout(() => {
        if (success) {
            resolve("Operation succeeded!");
        } else {
            reject("Operation failed!");
        }
    }, 2000);
});

// Using the promise
myPromise
    .then(result => {
        console.log("Success:", result);
    })
    .catch(error => {
        console.error("Error:", error);
    })
    .finally(() => {
        console.log("Promise completed");
    });

// Exercise 3: Practical example - Fake API call
function fetchUser(userId) {
    return new Promise((resolve, reject) => {
        console.log('Fetching user...');
        
        setTimeout(() => {
            // Simulate API response
            if (userId > 0) {
                resolve({
                    id: userId,
                    name: "Ahmad",
                    email: "ahmad@example.com"
                });
            } else {
                reject("Invalid user ID");
            }
        }, 1500);
    });
}

// Usage
fetchUser(1)
    .then(user => {
        console.log("User:", user);
    })
    .catch(error => {
        console.error("Error:", error);
    });

// Exercise 4: Promise chaining
function getUser(id) {
    return new Promise(resolve => {
        setTimeout(() => {
            resolve({ id, name: "Ahmad" });
        }, 1000);
    });
}

function getUserPosts(user) {
    return new Promise(resolve => {
        setTimeout(() => {
            resolve([
                { id: 1, title: "Post 1" },
                { id: 2, title: "Post 2" }
            ]);
        }, 1000);
    });
}

// Chain them
getUser(1)
    .then(user => {
        console.log("User:", user);
        return getUserPosts(user);  // Return promise for chaining
    })
    .then(posts => {
        console.log("Posts:", posts);
    })
    .catch(error => {
        console.error("Error:", error);
    });

// Exercise 5: Promise.all (run multiple async operations)
let promise1 = Promise.resolve(3);
let promise2 = new Promise(resolve => setTimeout(() => resolve(2), 1000));
let promise3 = Promise.resolve(1);

Promise.all([promise1, promise2, promise3])
    .then(results => {
        console.log(results); // [3, 2, 1] after 1 second
    });
```

**💻 Practice (Day 11 - 4 jam):**

```javascript
// Exercise 6: Error handling in chains
function riskyOperation(shouldFail) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            if (shouldFail) {
                reject("Something went wrong!");
            } else {
                resolve("Success!");
            }
        }, 1000);
    });
}

riskyOperation(false)
    .then(result => {
        console.log(result);
        return riskyOperation(true); // This will fail
    })
    .then(result => {
        console.log("This won't run");
    })
    .catch(error => {
        console.error("Caught error:", error);
    });

// Exercise 7: Promise utilities
// Promise.all - Wait for all (fails if ANY fails)
let task1 = Promise.resolve(1);
let task2 = Promise.resolve(2);
let task3 = Promise.reject("Error!");

Promise.all([task1, task2, task3])
    .then(results => console.log(results))
    .catch(error => console.error(error)); // "Error!" - one failed!

// Promise.allSettled - Wait for all (doesn't fail)
Promise.allSettled([task1, task2, task3])
    .then(results => {
        console.log(results);
        // [
        //   { status: 'fulfilled', value: 1 },
        //   { status: 'fulfilled', value: 2 },
        //   { status: 'rejected', reason: 'Error!' }
        // ]
    });

// Promise.race - First one wins
let slow = new Promise(resolve => setTimeout(() => resolve("slow"), 2000));
let fast = new Promise(resolve => setTimeout(() => resolve("fast"), 1000));

Promise.race([slow, fast])
    .then(result => console.log(result)); // "fast" (after 1 sec)
```

**Mini Project (Day 11 - 2 jam):**
**"Multi-Step Form with Async Validation"**

```javascript
// Simulate async validation (like checking email with server)
function validateEmail(email) {
    return new Promise((resolve, reject) => {
        console.log('Validating email...');
        setTimeout(() => {
            if (email.includes('@')) {
                resolve(true);
            } else {
                reject('Invalid email format');
            }
        }, 1000);
    });
}

function validateUsername(username) {
    return new Promise((resolve, reject) => {
        console.log('Checking username availability...');
        setTimeout(() => {
            if (username.length >= 3) {
                resolve(true);
            } else {
                reject('Username too short');
            }
        }, 1500);
    });
}

// HTML
/*
<form id="signupForm">
    <input type="text" id="username" placeholder="Username">
    <input type="email" id="email" placeholder="Email">
    <button type="submit">Sign Up</button>
    <div id="status"></div>
</form>
*/

let form = document.getElementById('signupForm');
let status = document.getElementById('status');

form.addEventListener('submit', (e) => {
    e.preventDefault();
    
    let username = document.getElementById('username').value;
    let email = document.getElementById('email').value;
    
    status.textContent = 'Validating...';
    status.style.color = 'blue';
    
    // Validate both (parallel)
    Promise.all([
        validateUsername(username),
        validateEmail(email)
    ])
    .then(() => {
        status.textContent = 'Success! Account created.';
        status.style.color = 'green';
    })
    .catch(error => {
        status.textContent = `Error: ${error}`;
        status.style.color = 'red';
    });
});
```

**🌙 Experimental Time (Both nights):**

**Day 10 Night:** Promise Playground
- Create "delay" utility function using Promises
- Simulate a "loading" sequence (3 steps, each takes time)
- Build a simple "traffic light" sequence (red → yellow → green with delays)

**Day 11 Night:** Race Conditions
- Create multiple "API calls" with different delays
- Use Promise.race to show "whichever loads first"
- Experiment with timeout patterns (reject if takes too long)

---

### **DAY 12: Async/Await (Modern Async)**

**📖 Learning (4 jam):**

**Topik:**
1. **Async/Await Syntax**
   - async functions
   - await keyword
   - Why it's cleaner than .then()

2. **Error Handling**
   - try-catch with async/await
   - Handling multiple awaits

3. **Await in Loops**
   - Sequential vs parallel
   - Performance implications

**Resources:**
- javascript.info: "Async/await"
- Compare Promise chains vs async/await

**💻 Practice (4 jam):**

```javascript
// Exercise 1: Basic async/await
// OLD WAY (Promises)
function fetchUserOld(id) {
    return fetch(`api/users/${id}`)
        .then(response => response.json())
        .then(data => {
            console.log(data);
            return data;
        })
        .catch(error => {
            console.error(error);
        });
}

// NEW WAY (async/await) - Much cleaner!
async function fetchUser(id) {
    try {
        let response = await fetch(`api/users/${id}`);
        let data = await response.json();
        console.log(data);
        return data;
    } catch (error) {
        console.error(error);
    }
}

// Exercise 2: Multiple async operations
async function getUserWithPosts(userId) {
    try {
        // Sequential (one after another)
        let user = await fetchUser(userId);
        let posts = await fetchPosts(userId);
        
        return { user, posts };
    } catch (error) {
        console.error('Error:', error);
    }
}

// Exercise 3: Parallel async (faster!)
async function getUserWithPostsParallel(userId) {
    try {
        // Both start at same time!
        let [user, posts] = await Promise.all([
            fetchUser(userId),
            fetchPosts(userId)
        ]);
        
        return { user, posts };
    } catch (error) {
        console.error('Error:', error);
    }
}

// Exercise 4: Async in loops
let userIds = [1, 2, 3, 4, 5];

// Sequential (SLOW - one at a time)
async function fetchAllSequential(ids) {
    let users = [];
    for (let id of ids) {
        let user = await fetchUser(id);  // Wait for each
        users.push(user);
    }
    return users;
}

// Parallel (FAST - all at once)
async function fetchAllParallel(ids) {
    let promises = ids.map(id => fetchUser(id));
    let users = await Promise.all(promises);
    return users;
}

// Exercise 5: Error handling patterns
async function robustFetch(url) {
    try {
        let response = await fetch(url);
        
        if (!response.ok) {
            throw new Error(`HTTP error! Status: ${response.status}`);
        }
        
        let data = await response.json();
        return data;
    } catch (error) {
        console.error('Fetch failed:', error);
        // You can return default value or rethrow
        throw error;
    }
}

// Exercise 6: Timeout pattern
function timeout(ms) {
    return new Promise((_, reject) => 
        setTimeout(() => reject(new Error('Timeout!')), ms)
    );
}

async function fetchWithTimeout(url, ms) {
    try {
        let result = await Promise.race([
            fetch(url),
            timeout(ms)
        ]);
        return result;
    } catch (error) {
        console.error('Request timed out or failed:', error);
    }
}
```

**Mini Project (2 jam):**
**"Loading Dashboard with Multiple Data Sources"**

```javascript
// Simulate APIs
async function fetchWeather() {
    await delay(1000);
    return { temp: 28, condition: "Sunny" };
}

async function fetchTasks() {
    await delay(1500);
    return [
        { id: 1, task: "Morning prayer" },
        { id: 2, task: "Code review" }
    ];
}

async function fetchQuote() {
    await delay(800);
    return "Sesungguhnya bersama kesulitan ada kemudahan.";
}

// Dashboard loader
async function loadDashboard() {
    let statusEl = document.getElementById('status');
    statusEl.textContent = 'Loading dashboard...';
    
    try {
        // Load all in parallel
        let [weather, tasks, quote] = await Promise.all([
            fetchWeather(),
            fetchTasks(),
            fetchQuote()
        ]);
        
        // Display
        document.getElementById('weather').textContent = 
            `${weather.temp}°C - ${weather.condition}`;
        document.getElementById('tasks').innerHTML = 
            tasks.map(t => `<li>${t.task}</li>`).join('');
        document.getElementById('quote').textContent = quote;
        
        statusEl.textContent = 'Dashboard loaded!';
        statusEl.style.color = 'green';
    } catch (error) {
        statusEl.textContent = 'Failed to load dashboard';
        statusEl.style.color = 'red';
    }
}

// Helper
function delay(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

// Load on page ready
loadDashboard();
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** Async Challenges
- Refactor ALL previous Promise code to async/await
- Build "sequential animation" system (elements fade in one by one)
- Create "retry" mechanism (if API fails, try again 3 times)
- Challenge: Build async queue (process items one at a time, but queue accepts many)

---

### **DAY 13: Fetch API & Working with Real APIs**

**📖 Learning (3 jam):**

**Topik:**
1. **Fetch API Basics**
   - Making GET requests
   - Handling responses
   - Response.json(), Response.text()

2. **HTTP Methods**
   - GET (read)
   - POST (create)
   - PUT (update)
   - DELETE (delete)

3. **Request Options**
   - Headers
   - Body
   - Modes (cors, no-cors)

4. **Error Handling**
   - Network errors
   - HTTP errors (404, 500, etc)

**Resources:**
- javascript.info: "Fetch"
- MDN: Fetch API
- Free API: JSONPlaceholder (https://jsonplaceholder.typicode.com/)

**💻 Practice (5 jam):**

```javascript
// Exercise 1: Basic GET request
async function getUsers() {
    try {
        let response = await fetch('https://jsonplaceholder.typicode.com/users');
        
        // Always check response.ok!
        if (!response.ok) {
            throw new Error(`HTTP error! Status: ${response.status}`);
        }
        
        let users = await response.json();
        console.log(users);
        return users;
    } catch (error) {
        console.error('Error fetching users:', error);
    }
}

// Exercise 2: POST request (create data)
async function createPost(title, body) {
    try {
        let response = await fetch('https://jsonplaceholder.typicode.com/posts', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                title: title,
                body: body,
                userId: 1
            })
        });
        
        let data = await response.json();
        console.log('Created:', data);
        return data;
    } catch (error) {
        console.error('Error creating post:', error);
    }
}

// Exercise 3: PUT request (update data)
async function updatePost(id, title, body) {
    try {
        let response = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`, {
            method: 'PUT',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                id: id,
                title: title,
                body: body,
                userId: 1
            })
        });
        
        let data = await response.json();
        console.log('Updated:', data);
        return data;
    } catch (error) {
        console.error('Error updating post:', error);
    }
}

// Exercise 4: DELETE request
async function deletePost(id) {
    try {
        let response = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`, {
            method: 'DELETE'
        });
        
        if (response.ok) {
            console.log('Deleted successfully');
        }
    } catch (error) {
        console.error('Error deleting post:', error);
    }
}

// Exercise 5: Query parameters
async function searchPosts(userId) {
    let url = `https://jsonplaceholder.typicode.com/posts?userId=${userId}`;
    
    try {
        let response = await fetch(url);
        let posts = await response.json();
        return posts;
    } catch (error) {
        console.error('Error:', error);
    }
}
```

**Mini Project (2 jam):**
**"Blog Post Viewer"**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Blog Viewer</title>
    <style>
        body {
            font-family: Arial;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        .post {
            border: 1px solid #ddd;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 8px;
        }
        .post h2 {
            margin-top: 0;
            color: #333;
        }
        .loading {
            text-align: center;
            color: #666;
        }
        button {
            padding: 10px 20px;
            background: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-bottom: 20px;
        }
        button:disabled {
            background: #ccc;
            cursor: not-allowed;
        }
    </style>
</head>
<body>
    <h1>📝 Blog Posts</h1>
    <button id="loadBtn">Load Posts</button>
    <button id="refreshBtn">Refresh</button>
    
    <div id="status" class="loading" style="display: none;">Loading...</div>
    <div id="posts"></div>
    
    <script>
        let loadBtn = document.getElementById('loadBtn');
        let refreshBtn = document.getElementById('refreshBtn');
        let status = document.getElementById('status');
        let postsContainer = document.getElementById('posts');
        
        async function loadPosts() {
            try {
                // Show loading
                status.style.display = 'block';
                loadBtn.disabled = true;
                postsContainer.innerHTML = '';
                
                // Fetch posts
                let response = await fetch('https://jsonplaceholder.typicode.com/posts');
                
                if (!response.ok) {
                    throw new Error('Failed to fetch posts');
                }
                
                let posts = await response.json();
                
                // Display first 10 posts
                posts.slice(0, 10).forEach(post => {
                    let postEl = document.createElement('div');
                    postEl.className = 'post';
                    postEl.innerHTML = `
                        <h2>${post.title}</h2>
                        <p>${post.body}</p>
                        <small>Post ID: ${post.id}</small>
                    `;
                    postsContainer.appendChild(postEl);
                });
                
                status.textContent = 'Posts loaded!';
                setTimeout(() => status.style.display = 'none', 2000);
                
            } catch (error) {
                status.textContent = 'Error loading posts!';
                status.style.color = 'red';
                console.error(error);
            } finally {
                loadBtn.disabled = false;
            }
        }
        
        loadBtn.addEventListener('click', loadPosts);
        refreshBtn.addEventListener('click', loadPosts);
        
        // Auto-load on page load
        loadPosts();
    </script>
</body>
</html>
```

**🌙 Experimental Time (02:30-Subuh):**

**Suggestion:** API Explorer
- Try different free APIs (list provided in offline materials):
  - Weather: OpenWeatherMap
  - Islamic: Aladhan API (prayer times)
  - Random: DummyJSON, ReqRes
- Build "API testing tool" (input URL, see response)
- Add pagination to blog viewer
- Add search/filter functionality

---

### **DAY 14: Week 2 Project + Review**

**🎯 Full Day Project (8-10 jam):**

**"Prayer Times App with Weather"**

Combine everything from Week 2: async/await, Fetch API, DOM manipulation, modern JS syntax.

**Features:**
1. Get user's city (input)
2. Fetch prayer times from Aladhan API
3. Fetch weather from OpenWeatherMap
4. Display both nicely
5. Show next prayer countdown
6. Save preferred city (localStorage)

**Starter Code:**

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prayer Times & Weather</title>
    <style>
        /* Your styling here - make it beautiful! */
    </style>
</head>
<body>
    <div class="container">
        <h1>🕌 Prayer Times & Weather</h1>
        
        <div class="search">
            <input type="text" id="cityInput" placeholder="Enter city (e.g., Jakarta)">
            <button id="searchBtn">Search</button>
        </div>
        
        <div id="weather" class="weather-card"></div>
        <div id="prayerTimes" class="prayer-times"></div>
        <div id="nextPrayer" class="next-prayer"></div>
    </div>
    
    <script>
        // Your code here!
        // API endpoints:
        // Prayer: http://api.aladhan.com/v1/timingsByCity?city=Jakarta&country=Indonesia
        // Weather: https://api.openweathermap.org/data/2.5/weather?q=Jakarta&appid=YOUR_KEY
        
        async function getPrayerTimes(city) {
            // Implement this
        }
        
        async function getWeather(city) {
            // Implement this
        }
        
        function displayData(prayerData, weatherData) {
            // Implement this
        }
        
        // Event listeners, etc.
    </script>
</body>
</html>
```

**🌙 Experimental Time (02:30-Subuh):**
Polish the app! Add animations, better error handling, loading spinners, etc.

**Week 2 Checkpoint:**
- [ ] Understand destructuring, spread, rest
- [ ] Comfortable with arrow functions & template literals
- [ ] Understand Promises vs async/await
- [ ] Can fetch data from real APIs
- [ ] Can handle errors properly
- [ ] Built real app consuming APIs

**Confidence check:** Rate 1-10 for Week 2 topics?

---

## ⚛️ WEEK 3: VUE.JS (7 Hari)

### **Goal Week 3:**
Master Vue.js Composition API + Build component-based applications

---

### **DAY 15: Vue.js Setup & Basics**

**📖 Learning (3 jam - Perpus/Masjid):**

**Topik:**
1. **What is Vue.js?**
   - Framework vs library
   - Why Vue? (compared to vanilla JS)
   - Composition API vs Options API (we use Composition!)

2. **Setup**
   - Using Vite
   - Project structure
   - Single File Components (.vue)

3. **Vue Basics**
   - Template syntax
   - Data binding ({{ }})
   - Directives (v-bind, v-on)
   - Reactive data (ref)

**Resources:**
- Vue.js Guide: Getting Started
- Vue.js Guide: Essentials section

**💻 Setup & Practice (5 jam - Perpus/Masjid):**

```bash
# At perpus (with internet)
npm create vite@latest my-vue-app -- --template vue
cd my-vue-app
npm install

# Run dev server
npm run dev
```

**Project structure:**
```
my-vue-app/
├── src/
│   ├── App.vue          # Main component
│   ├── main.js          # Entry point
│   ├── components/      # Reusable components
│   └── assets/          # Images, CSS
├── public/
├── index.html
└── package.json
```

**Exercise: Modify App.vue**

```vue
<template>
  <div class="app">
    <h1>{{ title }}</h1>
    <p>Count: {{ count }}</p>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="reset">Reset</button>
    
    <hr>
    
    <input v-model="message" placeholder="Type something">
    <p>You typed: {{ message }}</p>
    
    <hr>
    
    <img :src="imageUrl" :alt="imageAlt">
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Reactive data
const title = ref('My First Vue App');
const count = ref(0);
const message = ref('');
const imageUrl = ref('https://vuejs.org/images/logo.png');
const imageAlt = ref('Vue logo');

// Methods
const increment = () => {
  count.value++;
};

const decrement = () => {
  count.value--;
};

const reset = () => {
  count.value = 0;
};
</script>

<style scoped>
.app {
  text-align: center;
  padding: 20px;
}

button {
  margin: 5px;
  padding: 10px 20px;
  background: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background: #359268;
}

input {
  padding: 10px;
  margin: 10px;
  border: 2px solid #42b983;
  border-radius: 5px;
}
</style>
```

**Key Concepts Practice:**

```vue
<template>
  <!-- Data binding -->
  <p>{{ message }}</p>
  
  <!-- v-bind (attribute binding) - shorthand: : -->
  <img :src="imageSrc">
  <div :class="{ active: isActive }"></div>
  <div :style="{ color: textColor }"></div>
  
  <!-- v-on (event handling) - shorthand: @ -->
  <button @click="handleClick">Click</button>
  <input @input="handleInput">
  <form @submit.prevent="handleSubmit">
  
  <!-- v-model (two-way binding) -->
  <input v-model="text">
  
  <!-- v-if / v-else-if / v-else (conditional) -->
  <p v-if="score >= 90">Grade: A</p>
  <p v-else-if="score >= 80">Grade: B</p>
  <p v-else>Grade: C</p>
  
  <!-- v-show (toggle visibility) -->
  <div v-show="isVisible">Toggle me!</div>
  
  <!-- v-for (list rendering) -->
  <ul>
    <li v-for="item in items" :key="item.id">
      {{ item.name }}
    </li>
  </ul>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('Hello Vue!');
const imageSrc = ref('/logo.png');
const isActive = ref(true);
const textColor = ref('blue');
const text = ref('');
const score = ref(85);
const isVisible = ref(true);
const items = ref([
  { id: 1, name: 'Item 1' },
  { id: 2, name: 'Item 2' },
  { id: 3, name: 'Item 3' }
]);

const handleClick = () => {
  console.log('Clicked!');
};

const handleInput = (e) => {
  console.log(e.target.value);
};

const handleSubmit = () => {
  console.log('Form submitted');
};
</script>
```

**🌙 Experimental Time (02:30-Subuh - OFFLINE!):**

**Important:** Create Vue project di perpus, copy ke rumah untuk offline work!

**Suggestion:** Vue Playground
- Modify counter to have "step" input (increment by custom amount)
- Add input validation (prevent negative numbers)
- Create "theme toggle" (dark/light mode)
- Experiment with different v-for patterns

---

### **DAY 16-17: Vue Components & Props (2 Hari)**

**📖 Learning (Day 16 - 4 jam):**

**Topik:**
1. **Component Basics**
   - Why components?
   - Creating components
   - Importing & using components

2. **Props** (Parent → Child communication)
   - Defining props
   - Prop types & validation
   - Default values

3. **Events** (Child → Parent communication)
   - Emitting events
   - Listening to events
   - Passing data with events

**Resources:**
- Vue Guide: Components Basics
- Vue Guide: Props
- Vue Guide: Events

**💻 Practice (Day 16 - 4 jam):**

```vue
<!-- UserCard.vue (Child Component) -->
<template>
  <div class="user-card">
    <img :src="user.avatar" :alt="user.name">
    <h3>{{ user.name }}</h3>
    <p>{{ user.email }}</p>
    <button @click="handleClick">View Profile</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

// Define props
const props = defineProps({
  user: {
    type: Object,
    required: true
  }
});

// Define emits
const emit = defineEmits(['view-profile']);

const handleClick = () => {
  emit('view-profile', props.user.id);
};
</script>

<style scoped>
.user-card {
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
}

.user-card img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}
</style>
```

```vue
<!-- App.vue (Parent Component) -->
<template>
  <div class="app">
    <h1>User Directory</h1>
    
    <div class="user-grid">
      <UserCard 
        v-for="user in users" 
        :key="user.id"
        :user="user"
        @view-profile="handleViewProfile"
      />
    </div>
    
    <div v-if="selectedUser" class="modal">
      <h2>{{ selectedUser.name }}'s Profile</h2>
      <p>Email: {{ selectedUser.email }}</p>
      <button @click="selectedUser = null">Close</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import UserCard from './components/UserCard.vue';

const users = ref([
  { id: 1, name: 'Ahmad', email: 'ahmad@ex.com', avatar: '/avatar1.jpg' },
  { id: 2, name: 'Budi', email: 'budi@ex.com', avatar: '/avatar2.jpg' },
  { id: 3, name: 'Citra', email: 'citra@ex.com', avatar: '/avatar3.jpg' }
]);

const selectedUser = ref(null);

const handleViewProfile = (userId) => {
  selectedUser.value = users.value.find(u => u.id === userId);
};
</script>

<style>
.user-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.3);
}
</style>
```

**💻 Practice (Day 17 - 6 jam):**

**Mini Project: "Task Manager with Components"**

```
components/
├── TaskForm.vue      # Add new task
├── TaskItem.vue      # Single task display
├── TaskList.vue      # List of tasks
└── TaskFilter.vue    # Filter buttons
```

```vue
<!-- TaskItem.vue -->
<template>
  <div class="task-item" :class="{ completed: task.completed }">
    <input 
      type="checkbox" 
      :checked="task.completed"
      @change="$emit('toggle', task.id)"
    >
    <span class="task-text">{{ task.text }}</span>
    <button @click="$emit('delete', task.id)" class="delete-btn">
      ×
    </button>
  </div>
</template>

<script setup>
defineProps({
  task: {
    type: Object,
    required: true
  }
});

defineEmits(['toggle', 'delete']);
</script>

<style scoped>
.task-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 15px;
  background: #f9f9f9;
  border-radius: 5px;
  margin-bottom: 10px;
}

.task-item.completed {
  opacity: 0.6;
}

.task-item.completed .task-text {
  text-decoration: line-through;
}

.task-text {
  flex: 1;
}

.delete-btn {
  background: #f44336;
  color: white;
  border: none;
  padding: 5px 10px;
  border-radius: 3px;
  cursor: pointer;
}
</style>
```

```vue
<!-- TaskList.vue -->
<template>
  <div class="task-list">
    <TaskItem 
      v-for="task in tasks" 
      :key="task.id"
      :task="task"
      @toggle="$emit('toggle', $event)"
      @delete="$emit('delete', $event)"
    />
    
    <p v-if="tasks.length === 0" class="empty">
      No tasks yet. Add one to get started!
    </p>
  </div>
</template>

<script setup>
import TaskItem from './TaskItem.vue';

defineProps({
  tasks: {
    type: Array,
    required: true
  }
});

defineEmits(['toggle', 'delete']);
</script>
```

```vue
<!-- TaskForm.vue -->
<template>
  <form @submit.prevent="handleSubmit" class="task-form">
    <input 
      v-model="taskText"
      type="text" 
      placeholder="What needs to be done?"
      class="task-input"
    >
    <button type="submit" class="add-btn">Add Task</button>
  </form>
</template>

<script setup>
import { ref } from 'vue';

const taskText = ref('');
const emit = defineEmits(['add']);

const handleSubmit = () => {
  if (taskText.value.trim()) {
    emit('add', taskText.value);
    taskText.value = '';
  }
};
</script>
```

```vue
<!-- App.vue - Main orchestrator -->
<template>
  <div class="app">
    <h1>📝 Vue Task Manager</h1>
    
    <TaskForm @add="addTask" />
    
    <TaskFilter 
      :filter="currentFilter"
      @change="currentFilter = $event"
    />
    
    <TaskList 
      :tasks="filteredTasks"
      @toggle="toggleTask"
      @delete="deleteTask"
    />
    
    <div class="stats">
      <p>{{ remainingTasks }} tasks remaining</p>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';
import TaskForm from './components/TaskForm.vue';
import TaskList from './components/TaskList.vue';
import TaskFilter from './components/TaskFilter.vue';

const tasks = ref([]);
const currentFilter = ref('all');
let nextId = 1;

// Computed
const filteredTasks = computed(() => {
  if (currentFilter.value === 'active') {
    return tasks.value.filter(t => !t.completed);
  } else if (currentFilter.value === 'completed') {
    return tasks.value.filter(t => t.completed);
  }
  return tasks.value;
});

const remainingTasks = computed(() => {
  return tasks.value.filter(t => !t.completed).length;
});

// Methods
const addTask = (text) => {
  tasks.value.push({
    id: nextId++,
    text,
    completed: false
  });
};

const toggleTask = (id) => {
  const task = tasks.value.find(t => t.id === id);
  if (task) {
    task.completed = !task.completed;
  }
};

const deleteTask = (id) => {
  tasks.value = tasks.value.filter(t => t.id !== id);
};
</script>
```

**🌙 Experimental Time (Both nights):**

**Day 16:** Component Design
- Break down a complex UI into components (sketch on paper first!)
- Create reusable Button, Card, Input components
- Experiment with different prop patterns

**Day 17:** Component Communication
- Add more features to Task Manager (priority, categories, due dates)
- Each feature = new component
- Practice proper event emission

---

### **DAY 18-19: Computed, Watchers & Lifecycle (2 Hari)**

**📖 Learning (Day 18 - 4 jam):**

**Topik:**
1. **Computed Properties**
   - What are computed properties?
   - vs Methods
   - Caching benefits
   - Writable computed (advanced)

2. **Watchers**
   - When to use watch
   - vs Computed
   - Deep watching
   - Immediate execution

3. **Lifecycle Hooks**
   - onMounted
   - onUnmounted
   - onUpdated
   - When to use each

**Resources:**
- Vue Guide: Computed Properties
- Vue Guide: Watchers
- Vue Guide: Lifecycle Hooks

**💻 Practice (Day 18-19 - 8 jam total):**

```vue
<template>
  <div class="shopping-cart">
    <h2>Shopping Cart</h2>
    
    <div v-for="item in cart" :key="item.id" class="cart-item">
      <span>{{ item.name }} - ${{ item.price }}</span>
      <input 
        type="number" 
        v-model.number="item.quantity"
        min="1"
      >
      <span>${{ itemTotal(item) }}</span>
    </div>
    
    <hr>
    
    <div class="totals">
      <p>Subtotal: ${{ subtotal }}</p>
      <p>Tax (10%): ${{ tax }}</p>
      <p>Shipping: ${{ shipping }}</p>
      <h3>Total: ${{ total }}</h3>
    </div>
    
    <p v-if="hasDiscount" class="discount-message">
      🎉 You got a discount!
    </p>
  </div>
</template>

<script setup>
import { ref, computed, watch, onMounted } from 'vue';

const cart = ref([
  { id: 1, name: 'Product A', price: 29.99, quantity: 2 },
  { id: 2, name: 'Product B', price: 49.99, quantity: 1 },
  { id: 3, name: 'Product C', price: 19.99, quantity: 3 }
]);

// Computed (auto-recalculate when dependencies change)
const subtotal = computed(() => {
  return cart.value.reduce((sum, item) => {
    return sum + (item.price * item.quantity);
  }, 0).toFixed(2);
});

const tax = computed(() => {
  return (subtotal.value * 0.1).toFixed(2);
});

const shipping = computed(() => {
  return subtotal.value > 100 ? 0 : 10;
});

const total = computed(() => {
  return (parseFloat(subtotal.value) + 
          parseFloat(tax.value) + 
          parseFloat(shipping.value)).toFixed(2);
});

const hasDiscount = computed(() => {
  return subtotal.value > 100;
});

// Watchers (side effects when value changes)
watch(total, (newTotal, oldTotal) => {
  console.log(`Total changed from ${oldTotal} to ${newTotal}`);
  
  if (newTotal > 200) {
    alert('Wow! Big purchase! 🎉');
  }
});

// Deep watch (watch nested properties)
watch(cart, (newCart) => {
  console.log('Cart updated:', newCart);
  // Save to localStorage
  localStorage.setItem('cart', JSON.stringify(newCart));
}, { deep: true });

// Immediate watch (run immediately on mount)
watch(subtotal, (value) => {
  console.log('Subtotal:', value);
}, { immediate: true });

// Lifecycle hooks
onMounted(() => {
  console.log('Component mounted!');
  
  // Load cart from localStorage
  const savedCart = localStorage.getItem('cart');
  if (savedCart) {
    cart.value = JSON.parse(savedCart);
  }
});

// Methods (called manually, not cached)
const itemTotal = (item) => {
  return (item.price * item.quantity).toFixed(2);
};
</script>
```

**Advanced Pattern: Debounced Search**

```vue
<template>
  <div class="search">
    <input 
      v-model="searchQuery"
      placeholder="Search..."
    >
    <p v-if="searching">Searching...</p>
    <ul>
      <li v-for="result in results" :key="result.id">
        {{ result.name }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue';

const searchQuery = ref('');
const results = ref([]);
const searching = ref(false);

// Debounced search (wait 300ms after user stops typing)
let debounceTimer;

watch(searchQuery, (newQuery) => {
  clearTimeout(debounceTimer);
  
  if (!newQuery) {
    results.value = [];
    return;
  }
  
  searching.value = true;
  
  debounceTimer = setTimeout(async () => {
    // Simulate API call
    const response = await fetch(`/api/search?q=${newQuery}`);
    results.value = await response.json();
    searching.value = false;
  }, 300);
});
</script>
```

**🌙 Experimental Time (Both nights):**

**Day 18:** Computed Deep Dive
- Build calculator that uses only computed properties
- Create form with complex validation (all computed)
- Experiment with chained computed properties

**Day 19:** Watchers & Lifecycle
- Build auto-save feature (watch data, save after delay)
- Create countdown timer (use lifecycle to start/stop)
- Implement undo/redo (watch for changes, maintain history)

---

### **DAY 20-21: Vue Router & Composables (2 Hari)**

**📖 Learning (Day 20 - 4 jam):**

**Topik:**
1. **Vue Router Basics**
   - Installing router
   - Defining routes
   - router-link & router-view
   - Programmatic navigation

2. **Route Parameters**
   - Dynamic routes
   - Accessing params
   - Query strings

3. **Composables** (Reusable Logic)
   - What are composables?
   - Creating composables
   - When to use

**Setup Vue Router:**

```bash
# At perpus
npm install vue-router@4
```

```javascript
// src/router/index.js
import { createRouter, createWebHistory } from 'vue-router';
import Home from '../views/Home.vue';
import About from '../views/About.vue';
import UserProfile from '../views/UserProfile.vue';

const routes = [
  { 
    path: '/', 
    name: 'Home',
    component: Home 
  },
  { 
    path: '/about', 
    name: 'About',
    component: About 
  },
  { 
    path: '/user/:id', 
    name: 'UserProfile',
    component: UserProfile 
  }
];

const router = createRouter({
  history: createWebHistory(),
  routes
});

export default router;
```

```javascript
// src/main.js
import { createApp } from 'vue';
import App from './App.vue';
import router from './router';

createApp(App)
  .use(router)
  .mount('#app');
```

**💻 Practice (Day 20-21 - 8 jam):**

```vue
<!-- App.vue -->
<template>
  <div id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/products">Products</router-link>
    </nav>
    
    <router-view />
  </div>
</template>
```

```vue
<!-- views/Home.vue -->
<template>
  <div class="home">
    <h1>Welcome Home</h1>
    <p>Latest products:</p>
    <div class="product-grid">
      <div 
        v-for="product in products" 
        :key="product.id"
        class="product-card"
      >
        <h3>{{ product.name }}</h3>
        <p>${{ product.price }}</p>
        <router-link :to="`/product/${product.id}`">
          View Details
        </router-link>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const products = ref([
  { id: 1, name: 'Product A', price: 29.99 },
  { id: 2, name: 'Product B', price: 49.99 },
  { id: 3, name: 'Product C', price: 19.99 }
]);
</script>
```

```vue
<!-- views/ProductDetail.vue -->
<template>
  <div class="product-detail">
    <h1>{{ product.name }}</h1>
    <p>Price: ${{ product.price }}</p>
    <p>{{ product.description }}</p>
    
    <button @click="goBack">Go Back</button>
    <button @click="addToCart">Add to Cart</button>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { useRoute, useRouter } from 'vue-router';

const route = useRoute();
const router = useRouter();

const product = ref({});

onMounted(async () => {
  // Get product ID from route params
  const id = route.params.id;
  
  // Fetch product (simulated)
  product.value = {
    id,
    name: `Product ${id}`,
    price: 29.99,
    description: 'This is an amazing product!'
  };
});

const goBack = () => {
  router.go(-1); // or router.push('/')
};

const addToCart = () => {
  // Add to cart logic
  alert('Added to cart!');
  router.push('/cart');
};
</script>
```

**Composables (Reusable Logic):**

```javascript
// src/composables/useCounter.js
import { ref } from 'vue';

export function useCounter(initialValue = 0) {
  const count = ref(initialValue);
  
  const increment = () => count.value++;
  const decrement = () => count.value--;
  const reset = () => count.value = initialValue;
  
  return {
    count,
    increment,
    decrement,
    reset
  };
}
```

```javascript
// src/composables/useFetch.js
import { ref } from 'vue';

export function useFetch(url) {
  const data = ref(null);
  const error = ref(null);
  const loading = ref(false);
  
  const fetchData = async () => {
    loading.value = true;
    error.value = null;
    
    try {
      const response = await fetch(url);
      data.value = await response.json();
    } catch (err) {
      error.value = err.message;
    } finally {
      loading.value = false;
    }
  };
  
  return {
    data,
    error,
    loading,
    fetchData
  };
}
```

```vue
<!-- Using composables in component -->
<template>
  <div>
    <h2>Counter: {{ count }}</h2>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
    <button @click="reset">Reset</button>
    
    <hr>
    
    <button @click="fetchData">Load Data</button>
    <p v-if="loading">Loading...</p>
    <p v-if="error">Error: {{ error }}</p>
    <pre v-if="data">{{ data }}</pre>
  </div>
</template>

<script setup>
import { useCounter } from '../composables/useCounter';
import { useFetch } from '../composables/useFetch';

const { count, increment, decrement, reset } = useCounter(10);
const { data, error, loading, fetchData } = useFetch('https://api.example.com/data');
</script>
```

**🌙 Experimental Time (Both nights):**

**Day 20:** Multi-Page App
- Build complete multi-page site with router
- Add 404 page (catch-all route)
- Implement navigation guards (authentication check)

**Day 21:** Composables Library
- Create library of reusable composables:
  - useLocalStorage
  - useDebounce
  - useMousePosition
  - useOnline (detect internet connection)
- Use them in various components

**Week 3 Checkpoint:**
- [ ] Understand Vue reactivity (ref, reactive)
- [ ] Can create & use components
- [ ] Master props & events
- [ ] Comfortable with computed & watchers
- [ ] Can use Vue Router
- [ ] Can create composables
- [ ] Built complete multi-component app

---

## 🖥️ WEEK 4: FULL-STACK DEVELOPMENT (7 Hari)

### **Goal Week 4:**
Backend with Node.js + Express, Database (SQL), Build & deploy full-stack app

---

### **DAY 22-23: Node.js & Express Basics (2 Hari)**

**📖 Learning (Day 22 - 4 jam):**

**Topik:**
1. **Node.js Basics**
   - What is Node.js?
   - CommonJS vs ES Modules
   - File system basics
   - NPM packages

2. **Express Setup**
   - Installing Express
   - Creating basic server
   - Routes & HTTP methods
   - Middleware concept

**Resources:**
- Node.js docs (downloaded)
- Express Getting Started guide

**💻 Setup & Practice (Day 22 - 4 jam - Perpus):**

```bash
# Create backend project
mkdir my-api
cd my-api
npm init -y

# Install dependencies
npm install express cors dotenv
npm install --save-dev nodemon
```

**package.json scripts:**
```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  },
  "type": "module"
}
```

**Basic Express Server:**

```javascript
// server.js
import express from 'express';
import cors from 'cors';
import dotenv from 'dotenv';

dotenv.config();

const app = express();
const PORT = process.env.PORT || 3000;

// Middleware
app.use(cors());
app.use(express.json());

// Logging middleware
app.use((req, res, next) => {
    console.log(`${req.method} ${req.path}`);
    next();
});

// Routes
app.get('/', (req, res) => {
    res.json({ message: 'Welcome to API!' });
});

app.get('/api/test', (req, res) => {
    res.json({ 
        message: 'API is working!',
        timestamp: new Date()
    });
});

// Start server
app.listen(PORT, () => {
    console.log(`Server running on http://localhost:${PORT}`);
});
```

**💻 Practice (Day 23 - 8 jam):**

**Build CRUD API for Tasks:**

```javascript
// server.js - Complete CRUD
import express from 'express';
import cors from 'cors';

const app = express();
const PORT = 3000;

app.use(cors());
app.use(express.json());

// In-memory database (temporary)
let tasks = [
    { id: 1, title: 'Learn Node.js', completed: false },
    { id: 2, title: 'Build API', completed: false }
];
let nextId = 3;

// GET all tasks
app.get('/api/tasks', (req, res) => {
    res.json(tasks);
});

// GET single task
app.get('/api/tasks/:id', (req, res) => {
    const id = parseInt(req.params.id);
    const task = tasks.find(t => t.id === id);
    
    if (!task) {
        return res.status(404).json({ error: 'Task not found' });
    }
    
    res.json(task);
});

// POST create task
app.post('/api/tasks', (req, res) => {
    const { title } = req.body;
    
    if (!title) {
        return res.status(400).json({ error: 'Title is required' });
    }
    
    const newTask = {
        id: nextId++,
        title,
        completed: false,
        createdAt: new Date()
    };
    
    tasks.push(newTask);
    res.status(201).json(newTask);
});

// PUT update task
app.put('/api/tasks/:id', (req, res) => {
    const id = parseInt(req.params.id);
    const { title, completed } = req.body;
    
    const taskIndex = tasks.findIndex(t => t.id === id);
    
    if (taskIndex === -1) {
        return res.status(404).json({ error: 'Task not found' });
    }
    
    if (title !== undefined) tasks[taskIndex].title = title;
    if (completed !== undefined) tasks[taskIndex].completed = completed;
    tasks[taskIndex].updatedAt = new Date();
    
    res.json(tasks[taskIndex]);
});

// DELETE task
app.delete('/api/tasks/:id', (req, res) => {
    const id = parseInt(req.params.id);
    const initialLength = tasks.length;
    
    tasks = tasks.filter(t => t.id !== id);
    
    if (tasks.length === initialLength) {
        return res.status(404).json({ error: 'Task not found' });
    }
    
    res.json({ message: 'Task deleted successfully' });
});

// Error handling middleware
app.use((err, req, res, next) => {
    console.error(err.stack);
    res.status(500).json({ error: 'Something went wrong!' });
});

app.listen(PORT, () => {
    console.log(`API running on http://localhost:${PORT}`);
});
```

**Test API dengan Thunder Client (VS Code extension) atau curl**

**🌙 Experimental Time (Both nights):**

**Day 22:** Node.js Exploration
- Read/write files using fs module
- Create simple CLI tool
- Experiment with different npm packages

**Day 23:** API Enhancement
- Add filtering (?completed=true)
- Add pagination (?page=1&limit=10)
- Add sorting (?sort=createdAt)
- Input validation middleware

---

### **DAY 24-25: Database Integration (2 Hari)**

**📖 Learning (Day 24 - 3 jam - Perpus):**

**Topik:**
1. **SQL Basics**
   - Tables, rows, columns
   - Primary keys, foreign keys
   - CRUD: SELECT, INSERT, UPDATE, DELETE
   - WHERE, ORDER BY, LIMIT

2. **SQLite Setup**
   - Why SQLite (simple, file-based)
   - No separate server needed
   - Perfect for learning

**Resources:**
- SQL tutorial (downloaded)
- SQLite documentation

**💻 Setup (Day 24 - Perpus):**

```bash
# Install SQLite package
npm install better-sqlite3
```

**💻 Practice (Day 24-25 - 10 jam total):**

**Database Setup:**

```javascript
// db.js
import Database from 'better-sqlite3';

const db = new Database('tasks.db');

// Create tables
db.exec(`
    CREATE TABLE IF NOT EXISTS users (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        username TEXT UNIQUE NOT NULL,
        password TEXT NOT NULL,
        created_at DATETIME DEFAULT CURRENT_TIMESTAMP
    )
`);

db.exec(`
    CREATE TABLE IF NOT EXISTS tasks (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        user_id INTEGER NOT NULL,
        title TEXT NOT NULL,
        description TEXT,
        completed BOOLEAN DEFAULT 0,
        created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
        updated_at DATETIME DEFAULT CURRENT_TIMESTAMP,
        FOREIGN KEY (user_id) REFERENCES users(id)
    )
`);

export default db;
```

**Refactor server.js with database:**

```javascript
// server.js
import express from 'express';
import cors from 'cors';
import db from './db.js';

const app = express();
const PORT = 3000;

app.use(cors());
app.use(express.json());

// GET all tasks
app.get('/api/tasks', (req, res) => {
    try {
        const tasks = db.prepare('SELECT * FROM tasks ORDER BY created_at DESC').all();
        res.json(tasks);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

// GET single task
app.get('/api/tasks/:id', (req, res) => {
    try {
        const task = db.prepare('SELECT * FROM tasks WHERE id = ?').get(req.params.id);
        
        if (!task) {
            return res.status(404).json({ error: 'Task not found' });
        }
        
        res.json(task);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

// POST create task
app.post('/api/tasks', (req, res) => {
    try {
        const { title, description, user_id } = req.body;
        
        if (!title) {
            return res.status(400).json({ error: 'Title is required' });
        }
        
        const result = db.prepare(`
            INSERT INTO tasks (title, description, user_id)
            VALUES (?, ?, ?)
        `).run(title, description || null, user_id || 1);
        
        const newTask = db.prepare('SELECT * FROM tasks WHERE id = ?').get(result.lastInsertRowid);
        
        res.status(201).json(newTask);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

// PUT update task
app.put('/api/tasks/:id', (req, res) => {
    try {
        const { title, description, completed } = req.body;
        const id = req.params.id;
        
        const task = db.prepare('SELECT * FROM tasks WHERE id = ?').get(id);
        if (!task) {
            return res.status(404).json({ error: 'Task not found' });
        }
        
        db.prepare(`
            UPDATE tasks 
            SET title = ?, 
                description = ?, 
                completed = ?,
                updated_at = CURRENT_TIMESTAMP
            WHERE id = ?
        `).run(
            title !== undefined ? title : task.title,
            description !== undefined ? description : task.description,
            completed !== undefined ? completed : task.completed,
            id
        );
        
        const updatedTask = db.prepare('SELECT * FROM tasks WHERE id = ?').get(id);
        res.json(updatedTask);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

// DELETE task
app.delete('/api/tasks/:id', (req, res) => {
    try {
        const result = db.prepare('DELETE FROM tasks WHERE id = ?').run(req.params.id);
        
        if (result.changes === 0) {
            return res.status(404).json({ error: 'Task not found' });
        }
        
        res.json({ message: 'Task deleted successfully' });
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

app.listen(PORT, () => {
    console.log(`Server running on http://localhost:${PORT}`);
});
```

**🌙 Experimental Time (Both nights):**

**Day 24:** SQL Practice
- Practice complex queries (JOIN, GROUP BY, HAVING)
- Create users table and relate to tasks
- Experiment with indexes

**Day 25:** Database Optimization
- Add search functionality (LIKE queries)
- Implement pagination with LIMIT/OFFSET
- Add data validation before INSERT

---

### **DAY 26-27: Authentication & Frontend Connection (2 Hari)**

**📖 Learning (Day 26 - 3 jam):**

**Topik:**
1. **Authentication Flow**
   - Registration vs Login
   - Password hashing (bcrypt)
   - JWT tokens
   - Protected routes

2. **Frontend Integration**
   - Axios setup
   - Sending auth headers
   - Handling token storage

**Setup (Perpus):**

```bash
# Backend
npm install bcrypt jsonwebtoken

# Frontend (Vue project)
npm install axios
```

**💻 Practice (Day 26-27 - 10 jam):**

**Backend Auth (auth.js):**

```javascript
// auth.js
import bcrypt from 'bcrypt';
import jwt from 'jsonwebtoken';
import db from './db.js';

const JWT_SECRET = process.env.JWT_SECRET || 'your-secret-key-change-in-production';

export async function register(username, password) {
    // Check if user exists
    const existing = db.prepare('SELECT * FROM users WHERE username = ?').get(username);
    if (existing) {
        throw new Error('Username already exists');
    }
    
    // Hash password
    const hashedPassword = await bcrypt.hash(password, 10);
    
    // Store user
    const result = db.prepare(`
        INSERT INTO users (username, password)
        VALUES (?, ?)
    `).run(username, hashedPassword);
    
    return { id: result.lastInsertRowid, username };
}

export async function login(username, password) {
    // Find user
    const user = db.prepare('SELECT * FROM users WHERE username = ?').get(username);
    
    if (!user) {
        throw new Error('Invalid credentials');
    }
    
    // Verify password
    const valid = await bcrypt.compare(password, user.password);
    
    if (!valid) {
        throw new Error('Invalid credentials');
    }
    
    // Generate token
    const token = jwt.sign(
        { id: user.id, username: user.username },
        JWT_SECRET,
        { expiresIn: '7d' }
    );
    
    return { 
        token, 
        user: { id: user.id, username: user.username } 
    };
}

export function verifyToken(token) {
    try {
        return jwt.verify(token, JWT_SECRET);
    } catch (error) {
        throw new Error('Invalid token');
    }
}

// Auth middleware
export function authMiddleware(req, res, next) {
    const token = req.headers.authorization?.replace('Bearer ', '');
    
    if (!token) {
        return res.status(401).json({ error: 'No token provided' });
    }
    
    try {
        const decoded = verifyToken(token);
        req.user = decoded;
        next();
    } catch (error) {
        res.status(401).json({ error: 'Invalid token' });
    }
}
```

**Update server.js with auth routes:**

```javascript
// Add to server.js
import { register, login, authMiddleware } from './auth.js';

// Public routes
app.post('/api/register', async (req, res) => {
    try {
        const { username, password } = req.body;
        
        if (!username || !password) {
            return res.status(400).json({ error: 'Username and password required' });
        }
        
        const user = await register(username, password);
        res.status(201).json({ message: 'User created', user });
    } catch (error) {
        res.status(400).json({ error: error.message });
    }
});

app.post('/api/login', async (req, res) => {
    try {
        const { username, password } = req.body;
        const result = await login(username, password);
        res.json(result);
    } catch (error) {
        res.status(401).json({ error: error.message });
    }
});

// Protected routes (add authMiddleware)
app.get('/api/tasks', authMiddleware, (req, res) => {
    try {
        // Get only user's tasks
        const tasks = db.prepare('SELECT * FROM tasks WHERE user_id = ? ORDER BY created_at DESC')
            .all(req.user.id);
        res.json(tasks);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});

app.post('/api/tasks', authMiddleware, (req, res) => {
    try {
        const { title, description } = req.body;
        
        if (!title) {
            return res.status(400).json({ error: 'Title is required' });
        }
        
        const result = db.prepare(`
            INSERT INTO tasks (title, description, user_id)
            VALUES (?, ?, ?)
        `).run(title, description || null, req.user.id);
        
        const newTask = db.prepare('SELECT * FROM tasks WHERE id = ?').get(result.lastInsertRowid);
        
        res.status(201).json(newTask);
    } catch (error) {
        res.status(500).json({ error: error.message });
    }
});
```

**Frontend Integration (Vue):**

```javascript
// src/api/index.js
import axios from 'axios';

const api = axios.create({
    baseURL: 'http://localhost:3000/api'
});

// Add token to requests
api.interceptors.request.use(config => {
    const token = localStorage.getItem('token');
    if (token) {
        config.headers.Authorization = `Bearer ${token}`;
    }
    return config;
});

// Handle 401 errors
api.interceptors.response.use(
    response => response,
    error => {
        if (error.response?.status === 401) {
            localStorage.removeItem('token');
            window.location.href = '/login';
        }
        return Promise.reject(error);
    }
);

export default api;
```

```vue
<!-- Login.vue -->
<template>
  <div class="login-container">
    <h2>Login</h2>
    <form @submit.prevent="handleLogin">
      <input 
        v-model="username" 
        placeholder="Username" 
        required
      >
      <input 
        v-model="password" 
        type="password" 
        placeholder="Password" 
        required
      >
      <button type="submit" :disabled="loading">
        {{ loading ? 'Loading...' : 'Login' }}
      </button>
      <p v-if="error" class="error">{{ error }}</p>
    </form>
    <p>Don't have account? <router-link to="/register">Register</router-link></p>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
import api from '../api';

const router = useRouter();
const username = ref('');
const password = ref('');
const error = ref('');
const loading = ref(false);

async function handleLogin() {
    loading.value = true;
    error.value = '';
    
    try {
        const response = await api.post('/login', {
            username: username.value,
            password: password.value
        });
        
        localStorage.setItem('token', response.data.token);
        localStorage.setItem('user', JSON.stringify(response.data.user));
        
        router.push('/tasks');
    } catch (err) {
        error.value = err.response?.data?.error || 'Login failed';
    } finally {
        loading.value = false;
    }
}
</script>
```

**🌙 Experimental Time (Both nights):**

**Day 26:** Auth Deep Dive
- Add "remember me" checkbox
- Implement password reset flow (simulated)
- Add user profile page

**Day 27:** Full Integration
- Build complete Register + Login + Tasks flow
- Add logout functionality
- Handle token expiration gracefully
- Add loading & error states everywhere

---

### **DAY 28: Main Project - Complete Full-Stack App**

**🎯 All Day Project (10 jam):**

Build "Taskeen" - Task Manager untuk Muslim Professionals

**Features:**
1. ✅ User auth (register/login)
2. ✅ CRUD tasks with categories
3. ✅ Prayer time integration (from Aladhan API)
4. ✅ Auto-schedule tasks around prayer times
5. ✅ Task priorities & due dates
6. ✅ Search & filter
7. ✅ Responsive design

**Project Structure:**
```
taskeen/
├── backend/
│   ├── server.js
│   ├── db.js
│   ├── auth.js
│   ├── tasks.db
│   └── package.json
└── frontend/
    ├── src/
    │   ├── views/
    │   │   ├── Login.vue
    │   │   ├── Register.vue
    │   │   ├── Tasks.vue
    │   │   └── Profile.vue
    │   ├── components/
    │   │   ├── TaskForm.vue
    │   │   ├── TaskList.vue
    │   │   ├── TaskItem.vue
    │   │   └── PrayerTimes.vue
    │   ├── api/
    │   │   └── index.js
    │   ├── router/
    │   │   └── index.js
    │   └── App.vue
    └── package.json
```

**Deliverable:** Fully functional app ready for portfolio!

**🌙 Experimental Time:** Start deployment prep

**Week 4 Checkpoint:**
- [ ] Understand Node.js & Express
- [ ] Can build REST API with CRUD
- [ ] Can integrate SQL database
- [ ] Understand authentication (JWT)
- [ ] Can connect frontend to backend
- [ ] Built complete full-stack application

---

## 🎓 WEEK 5: POLISH & JOB READINESS (7 Hari)

### **Goal Week 5:**
TypeScript basics, Docker awareness, Deploy everything, Interview prep

---

### **DAY 29-30: TypeScript Essentials (2 Hari)**

**📖 Learning (Day 29 - 4 jam):**

**Topik:**
1. **Why TypeScript?**
   - Type safety
   - Better IDE support
   - Catch errors early

2. **Basic Types**
   - string, number, boolean
   - Arrays & tuples
   - Objects & interfaces
   - Union & literal types

3. **Functions**
   - Parameter & return types
   - Optional & default params
   - Function overloads

**Resources:**
- TypeScript Handbook (download)

**💻 Setup (Perpus):**

```bash
# Install TypeScript
npm install -g typescript

# Create tsconfig.json
tsc --init
```

**💻 Practice (Day 29-30 - 8 jam):**

```typescript
// basics.ts

// Basic types
let username: string = "Ahmad";
let age: number = 25;
let isActive: boolean = true;

// Arrays
let numbers: number[] = [1, 2, 3];
let names: Array<string> = ["Ahmad", "Budi"];

// Objects with interfaces
interface User {
    id: number;
    name: string;
    email: string;
    age?: number; // Optional
    readonly createdAt: Date; // Readonly
}

const user: User = {
    id: 1,
    name: "Ahmad",
    email: "ahmad@example.com",
    createdAt: new Date()
};

// Functions
function greet(name: string): string {
    return `Hello, ${name}!`;
}

function add(a: number, b: number): number {
    return a + b;
}

// Optional & default params
function buildName(first: string, last?: string): string {
    return last ? `${first} ${last}` : first;
}

function multiply(a: number, b: number = 2): number {
    return a * b;
}

// Union types
type ID = string | number;
type Status = "pending" | "active" | "completed";

interface Task {
    id: ID;
    title: string;
    status: Status;
}

// Type alias
type Point = {
    x: number;
    y: number;
};

// Generics (basic)
function identity<T>(value: T): T {
    return value;
}

identity<string>("hello");
identity<number>(42);

// Array methods with types
interface Product {
    id: number;
    name: string;
    price: number;
}

const products: Product[] = [
    { id: 1, name: "Product A", price: 100 },
    { id: 2, name: "Product B", price: 200 }
];

const expensiveProducts = products.filter((p: Product) => p.price > 150);
```

**Convert JS project to TS:**

```typescript
// Before (JS)
async function fetchUser(id) {
    const response = await fetch(`/api/users/${id}`);
    return response.json();
}

// After (TS)
interface User {
    id: number;
    name: string;
    email: string;
}

async function fetchUser(id: number): Promise<User> {
    const response = await fetch(`/api/users/${id}`);
    const user: User = await response.json();
    return user;
}
```

**🌙 Experimental Time (Both nights):**

**Day 29:** TS Practice
- Convert previous JS projects to TS
- Practice defining interfaces for all data structures
- Use strict mode (`"strict": true` in tsconfig)

**Day 30:** Vue + TypeScript
- Create Vue project with TS template
- Define props with TypeScript
- Type all API responses

---

### **DAY 31: Docker Awareness**

**📖 Learning (4 jam - Perpus):**

**Topik:**
1. **What is Docker?**
   - Containers vs VMs
   - Images vs Containers
   - Why developers use it

2. **Basic Commands**
   - docker run
   - docker ps
   - docker stop
   - docker images

3. **Reading Dockerfiles**
   - FROM, WORKDIR, COPY, RUN, CMD
   - Understanding layers

**Goal:** Awareness level - can use Docker, understand basics

**Resources:**
- Docker Get Started (download)

**💻 Practice (4 jam - Perpus):**

```bash
# Pull & run container
docker run hello-world

# Run nginx
docker run -d -p 8080:80 nginx
# Visit http://localhost:8080

# See running containers
docker ps

# Stop container
docker stop <container_id>

# Remove container
docker rm <container_id>
```

**Understanding Dockerfile:**

```dockerfile
# Node.js app Dockerfile
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "server.js"]
```

**What each line means:**
- FROM: Base image (Node 18 on Alpine Linux)
- WORKDIR: Working directory inside container
- COPY: Copy files from host to container
- RUN: Execute command during build
- EXPOSE: Document port (doesn't publish)
- CMD: Command to run when container starts

**🌙 Experimental Time:**
Run PostgreSQL in Docker, connect your app to it

---

### **DAY 32-33: Deploy Everything (2 Hari)**

**🚀 Day 32: Portfolio Website (8 jam):**

Build personal portfolio!

**Sections:**
1. Hero/About
2. Projects showcase (with live demos!)
3. Skills
4. Contact

**Use:** Vue or simple HTML/CSS

**Day 33: Deployment (8 jam - Perpus):**

```bash
# Frontend (Vercel)
npm run build
vercel

# Backend (Railway.app)
# Push to GitHub, connect to Railway

# Database
# Use Railway PostgreSQL or keep SQLite in repo
```

**Checklist:**
- [ ] Taskeen app deployed (frontend + backend)
- [ ] 2-3 other projects deployed
- [ ] Portfolio site live
- [ ] All GitHub repos have good READMEs
- [ ] Everything mobile-responsive

**🌙 Experimental Time:** Polish UI, fix bugs, optimize performance

---

### **DAY 34-35: Interview Preparation (2 Hari)**

**📚 Day 34: Technical Review (8 jam):**

**Morning (4 hrs):**
- Review all cheat sheets
- Practice LeetCode Easy (10 problems)
- Common algorithms: reverse string, palindrome, fizzbuzz

**Afternoon (4 hrs):**
- Mock technical interview (record yourself!)
- Practice explaining projects
- Prepare answers for:
  - "Walk me through your task manager"
  - "How does authentication work?"
  - "What was hardest part?"
  - "How would you add [feature]?"

**📝 Day 35: Behavioral Prep & Apply (8 jam):**

**Morning (4 hrs): STAR Method Answers**

1. **"Tell me about yourself"** (2-min pitch)
2. **"Why web development?"**
3. **"Tell me about a challenge"**
4. **"Walk me through a project"**
5. **"Why should we hire you?"**

**Afternoon (4 hrs): Application Materials**

- [ ] Resume updated
- [ ] Cover letter template
- [ ] LinkedIn profile
- [ ] GitHub profile README
- [ ] Apply to first 5-10 jobs!

**🌙 Experimental Time:** Practice, practice, practice!

---

## 🎉 COMPLETION!

**Week 5 Achievements:**
- [ ] TypeScript basics covered
- [ ] Docker awareness achieved
- [ ] Everything deployed
- [ ] Portfolio ready
- [ ] Interview prep done
- [ ] First applications sent

---

## 🚀 WEEK 6+: JOB HUNTING

**Daily Routine:**
- Morning: Apply to 3-5 jobs
- Afternoon: Keep coding (LeetCode, projects)
- Evening: Network, blog, improve portfolio

**Metrics:**
- Applications: 50-100 target
- Response rate: ~5-10%
- Timeline: 1-3 months for first job

**Tips:**
- Don't get discouraged by rejections
- Each interview = learning
- Keep improving meanwhile
- Stay consistent

---

## ✅ FINAL CHECKLIST: INDUSTRY-READY?

### Technical ✅
- [ ] Interactive web pages (HTML/CSS/JS)
- [ ] JavaScript fundamentals & modern features
- [ ] Async programming (Promises, async/await)
- [ ] API integration
- [ ] Vue.js with components
- [ ] REST API (Node/Express)
- [ ] Database CRUD (SQL)
- [ ] Authentication (JWT)
- [ ] Git version control
- [ ] Full-stack app deployed
- [ ] TypeScript & Docker awareness

### Portfolio ✅
- [ ] 1 main full-stack project
- [ ] 2-3 supporting projects
- [ ] Portfolio website
- [ ] GitHub profile
- [ ] LinkedIn updated

### Job Ready ✅
- [ ] Resume ready
- [ ] Interview prep done
- [ ] Applied to first jobs

---

## 🎓 CONGRATULATIONS!

You've completed the journey from **zero JavaScript** to **full-stack developer**!

**Remember:**
- Imposter syndrome is normal
- You know enough to start
- First job is hardest
- Keep learning always

**Your transformation:**
- ✅ Week 1: JavaScript basics
- ✅ Week 2: Modern JS & Async
- ✅ Week 3: Vue.js
- ✅ Week 4: Full-stack
- ✅ Week 5: Polish & Ready
- 🎯 Week 6+: Land that job!

**You're ready. Go apply! 🚀**

Semoga Allah SWT memberkahi usaha dan ilmu Anda. Aamiin! 🤲

---

**END OF ROADMAP**
