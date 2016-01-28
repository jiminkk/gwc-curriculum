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
	alert("value is " + value);
</code></pre>
> This prints out *value is undefined*.

**Null**

> Null is when you want to purposely set an empty value.

<pre><code>
	var value = null;
	alert("value is " + value);
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
	alert(answer);
</code></pre>
> This should print *Value is 7*.

* * *

## Logic Flow

### 1. If/Else Statements

Here is the logic: If the condition is true, execute. If not, then do not execute.

<pre><code>
	if (restaurant == "empty"){
		eat(we);
		pay(money);
	}
	else
		add_to_list(restaurant);
</code></pre>

If the restaurant is empty, we would go inside, eat, and pay for the food. If not, we add this restaurant to our wishlist for next time. The code below, however, would add the restaurant - whether or not it is empty:

<pre><code>
	if (restaurant == "empty"){
		eat(we);
		pay(money);
	}
	add_to_list(restaurant);
</code></pre>

### 2. Loops

Loops are used to handle repetitive tasks - we do not want to repeat the same code over and over again. Here are the two common types of loops.

**for loops**

We usually use for loops when we know clearly how many times we want to repeat the code segment inside.

Here is the structure of a for-loop:
<pre><code>
	var sum=0;
	for(var i=0; i<3; i++){
		sum += i;
		alert("This is the sum so far: " + sum);
	}
</code></pre>

> This would print out
>
>> \"This is the sum so far: 0\"
>
>> \"This is the sum so far: 1\"
>
>> \"This is the sum so far: 3\"
>

**while loops**

While loops are typically useful when we want to execute the code segment until we no longer satisfy the condition inside the statement. Here is the structure:
<pre><code>
	var sum=0;
	while(sum<3){
		sum += 1;
		alert("This is the sum so far: " + sum);
	}
</code></pre>

> This would print out
>
>> \"This is the sum so far: 1\"
>
>> \"This is the sum so far: 2\"
>
>> \"This is the sum so far: 3\"
>

Now going back to our previous example, we can now add one more characteristic to it:

<pre><code>
	while(is_hungry(we)){
		if (restaurant == "empty"){
			eat(we);
			pay(money);
		}
		else{
			add_to_list(restaurant);
			move_to_another();
		}
	}
</code></pre>

While we are still hungry, we would repeat the code segment inside the loop. But every time we eat, we should maybe keep a count so that when it reaches a certain limit, we are no longer hungry.

<pre><code>
	while(is_hungry(we)){
		if (restaurant == "empty"){
			eat(we);
			pay(money);
			full_index++;		// increment full_index
		}
		else{
			add_to_list(restaurant);
			move_to_another();
		}
		if(full_index > 5)
			is_hungry(we) = false;
	}
</code></pre>

The last line would make the condition inside while statement false, thus breaking out of the loop.













