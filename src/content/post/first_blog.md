---
layout: ../../layouts/post.astro
title: Astro Explained - A Beginner's Guide to Creating Static Sites with Minimal JavaScript
description: Introduction to Astro - The Modern Web Framework for Beginners
dateFormatted: Dec 26th, 2024
tags: ["astro", "blogging", "learning in public", "successes"]
---


<!-- # Astro Explained: A Beginner's Guide to Creating Static Sites with Minimal JavaScript -->

## Introduction to Astro : The Modern Web Framework for Beginners


In the ever-evolving landscape of Web development, choosing the right framework can be daunting, especially for beginners. Astro, a modern web framework, has emerges as a compelling choice for developers who value simplicity, performance and flexibility. In this blog post, we will explore Astro, understand what it offers, and guide you through the basics of getting started.

## What is [Astro](https://astro.build/)?

Astro is a modern and highly customizable JavaScript web framework optimized for building fast, content-driven websites. It supports multiple front-end frameworks like React, Vue, Svelte etc. Astro is best-known for pioneering a new frontend architecture named as [Islands architecture](https://docs.astro.build/en/concepts/islands/) to reduce JavaScript overhead and complexity compared to other frameworks.

## Why Choose Astro 🤔?

***For beginners, Astro offers several advantages:***
- **Simple Learning Curve:** The `.astro` UI language is a superset of HTML, any valid HTML is valid Astro templating syntax. Astro having simple syntax and minimal boiler plate code is very easy to learn for beginner's.

- **Static-Site Generation (SSG) by default:** Astro is designed for building static site out of the box, which is perfect for content heavy websites like blogs, portfolio and documentation websites. 

- **Performance-First Approach:** Astro reduces JavaScript overhead by default, making your site faster. It prioritizes server-rendered content and hydrated interactive components on the client side. An Astro website can [load 40% faster with 90% less JavaScript](https://docs.astro.build/en/concepts/why-astro/#fast-by-default) than the same site built with the most popular React web framework.

- **Flexible With Frameworks:** Astro allows you to use multiple front-end framework together. You can mix and match different frameworks to get your work done.

## How much similar and Dissimilar Astro is with other popular web frameworks present in the market? 

> Astro take advantage of server-side rendering over client-side rendering in the browser as much as possible and uses Multi-Page App (MPA) approach. These are the same approach that traditional frameworks - PHP, WordPress, Laravel, Ruby on Rails, etc. have been using for decades. But this approach stands in contrast to other modern JavaScript web framework like next.js, SvelteKit, Nuxt, Remix, and others. These frameworks were built for client-side rendering mostly and leverages the Single-Page App (SPA) approach.

## Setting Up Astro 

#### *Prerequisites* 

- First ensure you have Node.js ( ` v18.17.1 ` or `v20.3.0, v22.0.0` or higher ) installed on your system.
- Then you also need a Text editor, Astro recommends **VS Code** but you are free to choose any of the Text editors present in the market.
- You can use `bash, powershell` or any other terminal of your choice.

#### *Installation*

1. Run the following command in your terminal and you will be prompted to select a project name and project template (e.g., a basic starter or a blog template ).

```
	# Create a new project with npm
	npm create astro@latest
```

2.  After completion of your setup, navigate to your project folder then install all the dependencies. Finally run the development server using the commands listed below. 

```
	cd your-project-name
	npm install
	npm run dev
```

3. After successfully completing all the steps above, now you can see live preview of your Astro project in `http://localhost:4321` .

#### *Folder Structure of Your Project*

```
	/
	|-- public/
		-- favicon.svg
	|-- src/
		|-- layouts/
			|-- layout.
		|-- pages/
			|-- index.astro
	|-- package.json
	|-- astro.config.mjs
	|-- tsconfig.json
```

After completion of successful installation, your project directory in your code editor will looks like this. Lets deep dive into the project directory.
- `src/*` - All Your project source code (components, pages, styles, images, etc.) will be in this directory or folder.
- `public/*` - All Your non-code, unprocessed assets (fonts, icons, etc.) will be in this directory or folder.
- `package.json` - This file is used by JavaScript package managers to manage your dependencies.
- `astro.config.mjs` -  An Astro configuration file.
- `tsconfig.json` - A TypeScript configuration file.

#### *Build Your First Astro Component*

In Astro, Components are defined using `.astro` file extension. Lets create a simple component that displays greeting message. 
At first create a folder named `components`  inside the `src` folder. Then create a file named `Greeting.astro` inside the `components` folder and paste the below code inside the file `Greeting.astro`.

```
# Here the contents within this (---) symbol is called frontmatter. Here we can write JavaScript variables, functions etc.

file:Greeting.astro
	---
	const name = "Md Serif";
	---
	<h1>Hello,{name}! Welcome to Astro</h1> 
```

#### *Build Your First Page in Astro*

Before building a new page we must know that every `.astro` page inside the `\src\pages\` directory is also a route of this page as Astro uses the page routing technique to render its pages and components.
At first delete all the contents present in the `index.astro` file and then paste the below code in this file.
 
```
file: index.astro
	---
	import Greeting from './components/Greeting.astro';
	---
	<Greeting />
```

Now if you go to  `http://localhost:4321/` of your machine, you can see the below output.

```
	output:
	Hello,Md Serif! Welcome to Astro

```


Congratulations! Finally You have created your first basic Astro project. To learn more about Astro I will encourage you to visit the official [Astro Docs](https://docs.astro.build/en/getting-started/). 

#### *Conclusion*

Astro is an excellent framework for beginners seeking a balance between simplicity and performance. Its developer-friendly architecture make it a strong contender for modern web development projects.
so, why not give Astro a try? Start experimenting and build something extraordinary!

Thank You for your valuable time. Happy Learning 🤗.

