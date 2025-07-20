# 🌐 Build Your First ZIN Webpage

Let’s create a simple, dynamic, multi-page website using ZIN Engine.

By the end of this guide, you’ll have a working site with:

- ✅ A shared layout using templates
- ✅ Dynamic time rendering
- ✅ Environment variables for SEO
- ✅ Reusable components (header/footer)



## 🏗️ Step 1: Project Structure

Create a folder called `my-first-zin-site` and inside it, add these files:

```

my-first-zin-site/
├── index.html
├── about.html
├── template.html
├── components/
│   ├── header.html
│   └── footer.html
├── .env
├── .zinignore
└── zin.config

````



## 🔐 Step 2: Set Up `.env`

```env
SITE_NAME="ZIN Demo Site"
````



## 🚫 Step 3: Set Up `.zinignore` (optional)

```bash
.env
.drafts/
```



## 🖼️ Step 4: Create the Base Template

`template.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>{{ process.env.SITE_NAME }}</title>
</head>
<body>

  <zin-include file="components/header.html" />

  <main>
    <!-- Page-specific content will be injected here -->
    {{ .children }}
  </main>

  <zin-include file="components/footer.html" />

</body>
</html>
```



## 🧩 Step 5: Add Reusable Components

`components/header.html`:

```html
<header>
  <h1>{{ process.env.SITE_NAME }}</h1>
  <nav>
    <a href="/index">Home</a> |
    <a href="/about">About</a>
  </nav>
  <hr />
</header>
```

`components/footer.html`:

```html
<hr />
<footer>
  <p>© <zin-time view="year" /> — Built with 💙 and ZIN</p>
</footer>
```



## 📄 Step 6: Create Pages

### `index.html`

```html
<section>
  <h2>Welcome to ZIN!</h2>
  <p>This is the homepage of your first ZIN-powered website.</p>
  <p>Current date: <zin-time view="date" /></p>
</section>
```

### `about.html`

```html
<section>
  <h2>About This Site</h2>
  <p>ZIN helps you build dynamic sites using only HTML + smart tags.</p>
</section>
```



## 🚀 Step 7: Run the Server

Open your terminal and run:

```bash
zin.exe -p 3001 -r "./my-first-zin-site"

# Or simply run
zin
```

Then open your browser and visit:

```
http://localhost:3001
```

Try navigating to:

* `/index`
* `/about`

> You’ll notice no `.html` in the URL — ZIN automatically maps clean URLs to the right files.



## ✅ That’s It!

You’ve now built:

* A working multi-page site
* Shared layout via template
* Header/footer includes
* Dynamic data via `<zin-time>`
* `.env` variable injection

This structure forms the foundation of everything else in ZIN — now you’re ready to explore advanced features like:

* `<zin-repeat>` for loops
* `<zin-data>` for external data
* `<zin-form>` for secure forms
* `<zin-crypto>`, `<zin-set>`, and more

➡️ [Continue to: ZIN Tags →](./Tags/)
