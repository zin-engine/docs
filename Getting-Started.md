# 🚀 Getting Started with ZIN Engine

This guide will walk you through setting up your first ZIN-powered project in just a few minutes.

## 📦 Prerequisites

- A computer running **Windows** (Linux and macOS support coming soon)
- Basic understanding of HTML
- A terminal (Command Prompt, PowerShell, or any terminal app)

## 🔧 Step 1: Download ZIN Engine

1. Go to the [ZIN Releases](https://github.com/zin-engine/core/releases) page
2. Download the latest `zin-engine.zip` containing binary for Windows
3. (Optional) Add the `.exe` to your system PATH for easier access via command line

## 📁 Step 2: Create Your Project Folder

Set up a basic folder structure like this:

```

my-website/
│
├── index.html
├── about.html
├── template.html
├── .env
├── .zinignore
└── zin.config

````

This is where your code lives. You can expand it later with includes, data files, and more.

## ⚙️ Step 3: Configure Environment

Create a `.env` file in the root of your project:

```env
SITE_NAME="My Awesome Site"
CONTACT_FORM="https://api.example.com/contact"
GOOGLE_RECAPTCHA_SITE_KEY="your-public-key"
GOOGLE_RECAPTCHA_SITE_SECRET="your-secret-key"
````

These values are **never exposed to the browser**. You can access them in your HTML like:

```html
<h1>{{ process.env.SITE_NAME }}</h1>
```

## 🚫 Step 4: Ignore Files (Optional)

Use `.zinignore` to hide files/folders from:

* Public access
* Sitemap generation
* SEO indexing

Example:

```
/private
.env
draft.html
```

## 🔁 Step 5: URL Rewrites (Optional)

Use `zin.config` to define custom URL rewrites.

Example `zin.config`:

```xml
<zin-rewrite path="/github" to="https://github.com/cttricks" />
<zin-rewrite path="/hey" to="/hey/there.html" />
```


## 🚀 Step 6: Run ZIN

From your terminal:

```bash
zin.exe -p 3001 -r "/path/to/my-website"

# Or if system PATH is configired then just run
zin
```

Then open your browser to:

```
http://localhost:3001
```

You should see your site rendered with full zin-tag support and clean URLs (e.g. `/about` instead of `/about.html`).


## 👇 Next: Build Your First Page

Now that ZIN is running, let’s create your first page using ZIN’s templating and dynamic features.

➡️ [Continue to: First Webpage →](./MyWebPage.md)

