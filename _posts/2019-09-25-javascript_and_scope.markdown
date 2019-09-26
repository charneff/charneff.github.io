---
layout: post
title:      "JavaScript & Scope"
date:       2019-09-25 19:52:18 -0400
permalink:  javascript_and_scope
---

Below is an example JS function named scopey... Based on the function below, what do you think each statement log to the console will be when the function is called? Our conditional should always evaluate to true. Don't cheat, just take a guess... 

**BEGIN COPYING**

```
function scopey() {

    var a = "first Value"
    let b = "first Value"
    const c = "first Value"
    d = "first Value"
		
    if (true) {
      var a = "second Value"
      let b = "second Value"
      const c = "second Value"
      d = "second Value"
			}
		
    //What will each statement log to the console?
		
    console.log("a (var) is,", a)
    console.log("b (let) is,", b)
    console.log("c (const) is,", c)
    console.log("d (evil) is,", d)
		
		}
```
		
**END COPYING**

Call your function by typing scopey() in your console to see the results... 

a (var) is, second Value
b (let) is, first Value
c (const) is, first Value
d (evil) is, second Value

How did your guess stack up? Let's talk this through. 

As var a is declared within scopey, it has functional scope, meaning it is accessible throughout the function. var a is hoisted and then assigned "first Value" inside of the scopey function. var a IS NOT block scoped. This means that inside of the if statement, we have access to and are capable of reassigning the value of a. a is then reassigned to "secondValue". Again, as it is not blocked scoped, the value remains as "second Value" as it leaves the if statement and return to the outermost part of scopey.

let b is block-scoped, meaning inside of the 'if' statement, b will evaluate to "secondValue". However, we console.log(b) after the closing of the 'if' block and therefore outside it's scope.  Inside of the function scope but outside of the if block,  b is "first Value".

Similar to let, const is also block-scoped! 

Variable assignments without declarations of const + let (and occasionally var) always have a global scope and capable of being reassigned. Basically as we reach the line of code "d=....", the variable bubbles up through the layers of scope looking for a variable declaration of the given name or the global object. Try typing just the letter 'd' in your console. You will see it evaluates to "second Value". This is because it's scope is global.

Lastly, one important distinction, let can be reassigned... Refresh the page, copy and paste the below code in your console.
	
```
function let() {
let a = "firstValue"

a = "secondValue"

console.log(a)
}
```

Type let() in your console to call the function. The console will output "secondValue" because variables declared with 'let' can be reassigned.

Variables declared with const are constants, meaning they cannot be reassigned or redeclared. Just as you did above, copy the code below, paste it in console and then call the function. 

```
function constant() {
const c = "firstValue"

c = "secondValue"

console.log(c)
}
```

You will receive a TypeError: Assignment to constant variable.

***NOTE: Best practices are to use let and const only, not var. Never assign a variable without a declaration of let, const, or var as their scope will be global and reassignment possible. 
	
	
	



