Episode 4: Functions and Variable Environments (Summary)

📌 Key Concepts

Hoisting: Functions and variables are lifted to the top of their scope during memory allocation.

Local vs Global Scope: Variables declared inside a function (var x) are local and do not affect global variables with the same name.

Execution Contexts:

Global Execution Context (GEC): Created first, contains global variables and function definitions.

Local Execution Context (EC): Created when a function is called, contains local variables and parameters.

Call Stack: Keeps track of currently executing contexts. LIFO structure (Last In, First Out).

📌 Code Example
var x = 1;

a();
b();

console.log(x); // 1

function a() {
    var x = 10;
    console.log(x); // 10
}

function b() {
    var x = 100;
    console.log(x); // 100
}

📌 Output
10
100
1

📌 Summary of Execution

GEC is created; x = undefined, a and b functions hoisted.

Global x assigned 1.

a() → local x = 10 → prints 10 → EC removed.

b() → local x = 100 → prints 100 → EC removed.

Global console.log(x) prints 1.

📌 Quick Review Questions

Output of code? → 10, 100, 1

Why can we call functions before declaration? → Hoisting

Are local variables the same as global ones? → No, they are separate

Role of Call Stack? → Track execution contexts

What happens after function execution? → Local EC removed from Call Stack
