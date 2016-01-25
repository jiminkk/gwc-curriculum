---
layout: post
title: "Chapter 1: JavaScript Basics"
date: 2016-01-24
---

## Variables and Types

### 1. Why we use variables
You can use variables to store values with unique names. You can think of these as storage units with names that describe what the values mean. For example:
<pre><code>
	var number = 7;
	var str = "Sup";
	var bool = true;
</code></pre>

We will go into what these types are in a second.

Accurate syntax is important when naming these variables. Here are the rules you should know:

* Variables must start with a letter or underscore (_)
* The remaining characters can be
	* digits (0-9)
	* letters (A-Z, a-z)

<pre><code>
	var myNumber;		
	var MyNumber;		// different
</code></pre>

### 2. These are the types in javascript
Use `var` to declare any variable in Javascript.
In Javascript, there are many data types that overlap with other languages: 
<pre><code>
	var number = 7;
	var number2 = 5.67778;
	var myString = "Sup";
	var myBoolean = true;
	var nothing = null;
</code></pre>

Whichever value you initialize your variables with, that variable will be defined by that data type. The `var` label is enough to declare all these different data types.

**Number**

> Integers, floating points

**String**

> Anything in \" \" or \' \'

**Boolean**

> False or True

**Undefined**

> The value will come out to be \"undefined\" when you did not initialize it with anything.

<pre><code>
	var value;
	console.log("value is " + value);
</code></pre>
> This prints out *value is undefined*.

**Null**

> Null is when you want to purposely set an empty value.

<pre><code>
	var value = null;
	console.log("value is " + value);
</code></pre>
> This prints out *value is null*.

### 3. What you can do with variables
In addition to just using `var` to declare any type of variable, you can also change its data type after you initialize it. So for instance:
<pre><code>
	var value = 7;
	value = "I am now a string."
</code></pre>

This is technically right, and Javascript will not throw you any error. However, this is **not** good coding. You always want to be consistent with your data types - once you start switching your data types, it will be confusing which variables are which types after numerous lines of code.

You can also concatenate variables together and change their values.
<pre><code>
	var answer = "Value is " + 7;
	console.log(answer);
</code></pre>
> This should print *Value is 7*.









