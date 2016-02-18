---
layout: post
title: "Chapter 3: Functions"
date: 2016-02-11
---

## Functions

### 1. What and Why Functions?

A function is a block of code that executes something specific. Well, we design it so that it only performs that particular task.

Why functions?

* We don\'t want to repeat what we already coded again. By calling these functions by their names, we can reduce the amount of code we have to write by a LOT.

* Using functions is a good way to organize which block of code executes what task when code gets really long.

### 2. The Syntax, Forms, and Usage

Okay, so a JS function looks something like this:

<pre><code>
	function add(x, y)
	{
		return x+y;		// returns addition of x and y
	}
</code></pre>

You write the word \"function\" first to specify that you will be declaring a function and follow it with a name for it. In this case, it is \"add\". Then right after the name, you include parameters (or none) separated by commas inside parentheses. Whether you have parameters, you always need to include the parentheses. Then, you write whatever code you want to execute inside a pair of brackets after the function declaration:


function *name*(*parameter 1*, *parameter 2*) {

>// *something here*  

}

### 3. Calling functions

So functions will not be executed unless we actually call (or \"invoke\") them. A function will run when:

* a user clicks a button on a website and invokes a JS event

* somewhere in the code calls the function

* it invokes itself

### 4. Parameters and Returning results

As you may have noticed, functions normally return whatever is computed inside the code block. If it is an add function, it returns the sum value of the parameters passed into the function.

**Parameters** are one or more data types that are passed into a function. The function can use the values that are passed through the parameters. You can think of these as **inputs** into a basic block.

![blackBox]({{ site.url }} /assets/IO_box.png)


A basic block would be whatever is being computed inside the function.

**Return** is a statement that spits out the result of whatever was computed inside the basic block. You can think of this as the **output** of the block.

Something important to remember: return will ALWAYS stop whatever is being executed inside the function and come out of the basic block. So, even if there is code in the following lines after the return statement, they will never be executed as long as the return statement is executed.

Let\'s see some examples now.

<pre><code>
	function print(x){
		console.log(x);		// prints out whatever is in x
		return;
	}

	print("HELLO");			// HELLO
</code></pre>

This does not return any value, but it does indicate the function to stop executing by that line. We actually don\'t need to include a return statement here, since the ending bracket will finish the function call.

<pre><code>
	function printArray(x){
		var len = x.length;
		for(var i=0; i<len; i++){
			console.log(x[i]);		// prints out each element in array
		}
		return len;
	}

	var fruits = ["apple", "banana", "pear"];
	printArray(fruits);				// actually calls printArray
</code></pre>

You can also use functions as variables, and we will see examples below.

### 5. Make A Calculator

<pre><code>
	function add(x, y){
		return x+y;		// returns addition of x and y
	}

	function subtract(x, y){
		// ... 
	}

	function multiply(x, y){
		// ...
	}

	function divide(x, y){
		// ...
	}

	/*

	*/
</code></pre>










