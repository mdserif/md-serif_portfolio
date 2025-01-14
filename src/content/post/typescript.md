---
layout: ../../layouts/post.astro
title: From JavaScript to TypeScript - Unlocking the Power of Types in Your Code
description: Introduction - TypeScript is  JavaScript with syntax for types.
dateFormatted: Jan 14th, 2025
tags: ["astro", "blogging", "learning in public", "successes"]
---

## Introduction: TypeScript is  JavaScript with syntax for types.

In the world of modern web development, JavaScript reigns supreme as the language of the web. However, as applications grow in complexity, developers often encounter challenges like runtime errors, unclear code intent, and difficulties in scaling. Enter **TypeScript**, a **powerful superset of JavaScript** developed by Microsoft in the year 2012. TypeScript brings the best of both worlds: the flexibility of JavaScript and the reliability of static typing. By adding type safety, robust tooling, and advanced features, TypeScript empowers developers to write cleaner, more maintainable code. 

## What is TypeScript ?

TypeScript is a language that is a **_superset_ of JavaScript**. It is basically a static type checker for JavaScript and some other languages like C# etc. That means it analyzes the code as we type in our text editor or IDE and catches type related errors during development time rather than at runtime.

## Why to Use TypeScript instead of JavaScript ?

Many programming languages like - c++, golang etc have built-in static type checking support that means codes are checked on the go while writing in your IDE, which helps to debug and write better code with type safety, but on the other hand JavaScript only support runtime type checking in-built not static type checking which causes problem in the production code, this limitation of JavaScript can be eliminated by using TypeScript which helps in Static type checking of JavaScript code. TypeScript helps to write more safer and bug free JavaScript code. 

## How TypeScript Internally Works ?

TypeScript can not run in the browser or Node.js directly; it is only a development tool. It installs as a dev dependency in your project (more about installation later). 
The compiled JavaScript code is what actually runs at runtime. Lets discuss in detail about the compilation process of TypeScript code to JavaScript code.

1. ***Input as TypeScript Code*** 
	- We write TypeScript Code ( `.ts` or `.tsx` files) having its extended features like types, interfaces, and decorators etc.
	- Example TypeScript Code -
```
	# file: name.ts
	
	let name: string = "md serif";
	let fullName: string = `my name is ${name}`;
	console.log(fullName);
```

2. ***TypeScript Compiler (`tsc`)***
	- **Parsing -** the `tsc` compiler parses the TypeScript code `(.ts or .tsx)` file into an **Abstract Syntax Tree (AST)**, which represents the structure of the code.
	- **Type Checking -** The compiler validates the codes, if any mismatches happened, it generated compile time errors.
	- **Type Erasure -** TypeScript removes all the types-specific syntax, because JavaScript Does not support them.  This process is called type erasure. Example:
```
	// typescript
	let name: string = "md serif";
```
    
After type erasure:

```
    // javascript
    let name = "md serif";
```

3. After compilation, the whole code of TypeScript `(.ts or .tsx)` file in converted into pure JavaScript that can run in any environment (e.g., `node.js`) that Supports JavaScript.

>Developers can configure the behavior of the TypeScript compiler using a `tsconfig.json` file.
>
>**Common configurations include:**
>
> `target`: Specifies the JavaScript version (e.g., ES5, ES6).
> `module`: Defines the module system (e.g., CommonJS, ESNext).
> `strict`: Enables strict type-checking.
> `include` and `exclude`: Specifies files to include or exclude from compilation.

```
file: tsconfig.json

	{
	  "compilerOptions": {
	    "target": "ES6",
	    "module": "CommonJS",
	    "strict": true
	  },
	  "include": ["src/**/*"],
	  "exclude": ["node_modules"]
	}
```


## Setting Up and Installation Guide of TypeScript

#### *prerequisite*
-  You Should know JavaScript at the first place.
-  You should have node.js (JavaScript runtime environment) installed in your system.
-  You also need a text editor or an IDE (e.g., Eclipse, Sublime Text, VS Code etc ).

#### *installation*
-  We can install TypeScript Globally or Project Specific.
-  To install it globally, means it can be used by any other directory/file or Project in that machine. Command for it is -   `npm install -g typescript`
-  To install it project specific, means it only available for that specific project only. Command for it is -  `npm install --save -dev` 


### Lets learn about the features and types of TypeScript in detail

- TypeScript have Three primitive data types as `string`, `number`, and `boolean` , these are the same names you would find in JavaScript if you use `typeof` operator on a value of those type. 

>In TypeScript `number` indicated all types of numbers, there is no differences between double or decimals etc.

```
	let name: string = "md serif";
	let score: number = 5;
	let score: number = 5.09;
	let isTrue: boolean = false;
```

- `Arrays` - To specify the type of an array like `[1, 2, 3]`, we can use the syntax `number[]`; or `Array<number>` this syntax can also be used for strings and booleans.
- `Any` - This is special type in TypeScript, using this type `any` we can accept any kind of value, that means no type checking is happening here. It is not recommend to use `any` .

```
// using any keyword this kind of errors can happen
	
	let name: any = 5;
	console.log (name);
```

- `function` - for a function we need two types of checking , firstly what type of data it receives as parameter and what type of data it returns. Here is the syntax for a string , it is similar for other types like number etc - 
```
	let myName: string = "md serif";
	function greeting(name: string):string{
	return name;
	}

	greeting(myName);
```

- `Type aliases` -  Sometimes we need to use the same type more than once, then we refer the type by a single name. A _type alias_ is exactly that - a _name_ for any _type_ . Here is the example of type alias :
```
type Point = {
	x: number;
	y: number;
};

function printCoord(pt: Point) {

console.log("The coordinate's x value is " + pt.x);

console.log("The coordinate's y value is " + pt.y);

}

printCoord({ x: 100, y: 100 });
```

`readonly` - If we use this keyword before any variable , we cannot change or re-assign the value of that particular variable. lets see how to use the property `readonly`.

Finally you have learned the basics of TypeScript, It has a lot more things to learn, some advance topics like - Union type, access modifiers, getter and setter types, Abstract classes, interfaces, generics, type narrowing etc., these are very useful types. I will highly encourage you to go to the official documentation of TypeScript and get your hands dirty. 

## Conclusion

TypeScript’s feature set goes beyond just type checking. It enhances productivity, reduces bugs, and ensures maintainable, scalable codebases. Its flexibility and compatibility make it an indispensable tool for modern JavaScript developers. Go give it a try.

> Thank you for your invaluable time. Happy Learning 🤗.  
