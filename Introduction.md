# 👋 Introduction to ZIN Engine

Welcome to **ZIN Engine** — a lightweight, HTML-first engine that lets you build dynamic, SEO-friendly websites **without** the overhead of modern frontend frameworks or complex backend setups.

ZIN is designed to **keep your code close to HTML**, but give it superpowers like templating, data loading, secure form handling, and environment configuration — all without writing JavaScript or spinning up a full stack.

## 🧠 Why ZIN?

Building even the simplest website today — a landing page, portfolio, product site, or business contact page — often means:

- Creating templates and shared headers/footers
- Securing form submissions (e.g. with reCAPTCHA)
- Writing server-side scripts for dynamic content
- Managing environment variables and secrets
- Configuring routes, clean URLs, and SEO basics
- Choosing between heavy frameworks (React, Next.js, PHP, etc.)

### 🤯 All that, just to build a few pages?

That’s where **ZIN** comes in. It handles all of the above with **zero JavaScript**, **zero frameworks**, and just **plain HTML** + smart configuration.

## 🪄 What Can ZIN Do?

With ZIN, you can:

✅ Build with plain HTML + zin-tags  
✅ Use reusable templates, includes, and partials  
✅ Load dynamic data from CSV, JSON, APIs, MySQL, or Google Sheets  
✅ Securely handle form submissions with built-in reCAPTCHA support  
✅ Configure environment variables with `.env`  
✅ Set up clean URLs and route rewriting  
✅ Auto-generate and update `sitemap.xml` and `robots.txt`

## 🧰 Who is ZIN For?

ZIN is perfect for:

- **Freelancers and indie devs** building multiple client sites
- **Small teams** who want to avoid JS-heavy stacks
- **Web designers** who prefer working in HTML but need some dynamic logic
- **Developers** who want clean, fast, secure, low-maintenance websites

## ⚡ ZIN Philosophy

> The web was built on HTML. ZIN respects that.

Instead of forcing you into a framework, ZIN gives you flexible, composable tools that work *with* how the web was meant to be built.

## 📦 How Does It Work?

Just point ZIN to your project folder and run:

```bash
zin -p 3001 -r "/path/to/my-site"

# Or Simply run it on current directory
zin -p 3001

# Or Just run it on default port 9001, on current directory
zin
````

That’s it.

ZIN watches your HTML files, processes dynamic `zin-tags`, applies templates, rewrites routes, and serves your site on a local or production server.

## 🧩 Next: What You’ll Learn

In the docs ahead, you’ll learn how to:

* Set up and configure ZIN
* Structure a project with reusable templates and includes
* Use zin-tags to load data, handle forms, and transform content
* Secure your site with `.env` and control visibility with `.zinignore`
* Deploy your ZIN-powered site

## 💬 Final Thought

You don’t need React to build a website.
You don’t need PHP just to submit a form.

With ZIN, **HTML is your superpower again**.
