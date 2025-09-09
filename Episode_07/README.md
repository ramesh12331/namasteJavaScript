# Scope, Scope Chain & Lexical Environment in JavaScript  

## 📌 What is Scope?  
- **Scope** defines where variables and functions are accessible.  
- It is directly related to the **Lexical Environment**.  
- **Lexical Environment = Local Memory + Reference to Outer Environment**.  

---

## 📌 Example 1: Global Variable Access  

```js
function a() {
  console.log(b); // 10
}
var b = 10;
a();
```

👉 Function `a()` can access global variable `b`.  

---

## 📌 Example 2: Nested Function Access  

```js
function a() {
  c();
  function c() {
    console.log(b); // 10
  }
}
var b = 10;
a();
```

👉 Even nested functions can access global variables.  

---

## 📌 Example 3: Local Variable Shadowing Global  

```js
function a() {
  c();
  function c() {
    var b = 100;
    console.log(b); // 100
  }
}
var b = 10;
a();
```

👉 Local variable `b` overrides (shadows) global `b`.  

---

## 📌 Example 4: Global vs Local Access  

```js
function a() {
  var b = 10;
  c();
  function c() {
    console.log(b); // 10
  }
}
a();
console.log(b); // ❌ ReferenceError
```

👉 Functions can access outer variables, but global scope **cannot access local variables**.  

---

## 📌 Key Points to Remember  

1. **Local scope > Global scope** (local variable wins → shadowing).  
2. Functions can access variables from their **outer environment** (Lexical Scope).  
3. Global scope cannot access local function variables.  
4. **Scope Chain** = Variable lookup chain → Local → Parent → Global.  

---

## 📖 Simple Summary  

- **Scope** → Defines accessibility of variables.  
- **Lexical Environment** → Memory + reference to parent scope.  
- **Scope Chain** → How JS looks up variables step by step.  
- Local variables shadow global variables if same name.  
- Global scope cannot access inside function variables.  

---

## 🎯 Interview Questions & Answers  

**Q1. What is Scope in JS?**  
👉 Scope defines where variables and functions can be accessed.  

**Q2. What is Lexical Environment?**  
👉 It is the local memory + a reference to the parent environment.  

**Q3. What is Scope Chain?**  
👉 The process of resolving variables by looking into local → parent → global environments.  

**Q4. Can functions access outer variables?**  
👉 ✅ Yes, functions can access variables from their parent scope.  

**Q5. Can global scope access local variables?**  
👉 ❌ No, local variables are private to their function.  

**Q6. What happens if the same variable exists in both local and global scope?**  
👉 Local variable takes precedence (variable shadowing).  
