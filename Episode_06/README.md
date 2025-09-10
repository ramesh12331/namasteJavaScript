# Undefined vs Not Defined in JavaScript

## 📌 What is undefined?

During the memory allocation phase, JavaScript assigns each declared
variable a placeholder called `undefined`.

**undefined means:** the variable is declared but no value is assigned
yet.

## 📌 What is "Not Defined"?

If a variable is not declared at all in the memory allocation phase and
you try to access it, JS throws an error → **"Not Defined"**.

**Not Defined !== Undefined**

------------------------------------------------------------------------

## 📌 Examples

### Example 1: undefined

``` js
console.log(x); // undefined
var x = 25;
console.log(x); // 25
```

👉 Here, `x` was allocated memory and initialized with `undefined`.
Later, it was assigned the value `25`.

### Example 2: Not Defined

``` js
console.log(a); 
// ❌ Uncaught ReferenceError: a is not defined
```

👉 Since `a` was never declared, JavaScript cannot find it in memory, so
it throws an error.

------------------------------------------------------------------------

## 📌 JavaScript is Loosely Typed

JavaScript is a **loosely typed / weakly typed language**.

A variable is not bound to any one data type.

``` js
var a = 5;       // number  
a = true;        // boolean  
a = "hello";     // string  
```

------------------------------------------------------------------------

## ⚠️ Best Practice

❌ Never assign `undefined` manually to a variable.\
✅ Let JavaScript assign `undefined` automatically when a variable is
declared but not initialized.

------------------------------------------------------------------------

## 📖 Simple Summary

-   **undefined** → variable is declared but not yet assigned a value.\
-   **Not Defined** → variable is never declared in memory.\
-   **JavaScript** → loosely typed, variable type can change
    dynamically.

Always allow JS to handle `undefined` automatically.

------------------------------------------------------------------------

## 🎯 Interview Questions & Answers

**Q1. What is the difference between undefined and not defined in
JavaScript?**\
👉 undefined: variable is declared but not assigned a value.\
👉 not defined: variable is not declared at all but is being accessed.

**Q2. What does JavaScript assign to variables during the memory
creation phase?**\
👉 It assigns `undefined`.

**Q3. Why should we not assign undefined manually to variables?**\
👉 Because `undefined` is a special placeholder by JavaScript. Manually
assigning it makes the code confusing and error-prone.

**Q4. What type of language is JavaScript in terms of variable
typing?**\
👉 JavaScript is **loosely typed (weakly typed)**. Variables can change
their type dynamically.

**Q5. What happens if we access a variable that was declared with var
but not initialized?**\
👉 It returns `undefined`.

**Q6. What happens if we access a variable that was never declared?**\
👉 It throws a **ReferenceError: variable is not defined**.

------------------------------------------------------------------------

# 🔹 JavaScript లో Undefined vs Not Defined

## 📌 undefined అంటే ఏమిటి?

Memory allocation phase లో, JavaScript ప్రతి variable కి ఒక placeholder
`undefined` ఇస్తుంది.

**undefined అంటే:** variable declare అయ్యింది కానీ value assign చేయలేదు.

## 📌 "Not Defined" అంటే ఏమిటి?

ఒక variable అసలు declare చెయ్యకపోతే మరియు దాన్ని access చేయడానికి
ప్రయత్నిస్తే, JavaScript → **"Not Defined"** error ఇస్తుంది.

**Not Defined !== Undefined**

------------------------------------------------------------------------

## 📌 Examples

### Example 1: undefined

``` js
console.log(x); // undefined
var x = 25;
console.log(x); // 25
```

👉 ఇక్కడ `x` కి ముందుగా `undefined` ఇవ్వబడింది. తర్వాత value `25` assign
అయ్యింది.

### Example 2: Not Defined

``` js
console.log(a); 
// ❌ Uncaught ReferenceError: a is not defined
```

👉 `a` అసలు declare కాలేదు, అందుకే error వచ్చింది.

------------------------------------------------------------------------

## 📌 JavaScript ఒక Loosely Typed Language

JavaScript → **loosely typed / weakly typed**.

Variable కి fixed type ఉండదు → type మార్చుకోవచ్చు.

``` js
var a = 5;       // number  
a = true;        // boolean  
a = "hello";     // string  
```

------------------------------------------------------------------------

## ⚠️ Best Practice

❌ Variable కి `undefined` మనమే assign చేయకూడదు.\
✅ JavaScript స్వయంగా `undefined` ఇస్తుంది (variable declare చేసి value
assign చేయకపోతే).

------------------------------------------------------------------------

## 📖 Simple Summary (తెలుగులో)

-   **undefined** → variable declare అయ్యింది కానీ value లేదు.\
-   **Not Defined** → variable అసలు declare కాలేదు.\
-   **JavaScript** → loosely typed, variable type మారిపోతుంది.

`undefined` assign చేయడం JS కి వదిలేయాలి.

------------------------------------------------------------------------

## 🎯 Interview Questions (తెలుగులో)

**Q1. undefined మరియు not defined మధ్య తేడా ఏమిటి?**\
👉 undefined: variable declare అయింది కానీ value లేదు.\
👉 not defined: variable declare కాలేదు కానీ access చేయబడ్డది.

**Q2. Memory creation phase లో variables కి ఏం assign అవుతుంది?**\
👉 `undefined` assign అవుతుంది.

**Q3. మనమే undefined assign చెయ్యాలా?**\
👉 ❌ వద్దు. JavaScript స్వయంగా ఇస్తుంది.

**Q4. JavaScript variable typing ఏ విధంగా ఉంటుంది?**\
👉 JavaScript ఒక loosely typed language. Variable type మార్చుకోవచ్చు.

**Q5. ఒక variable declare అయి కానీ value assign చేయకపోతే ఏమవుతుంది?**\
👉 అది `undefined` అవుతుంది.

**Q6. అసలు declare కాలేని variable access చేస్తే ఏమవుతుంది?**\
👉 `ReferenceError: variable is not defined` వస్తుంది.
