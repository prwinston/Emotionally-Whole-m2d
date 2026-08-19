# Emotionally Whole — website (static, no forms)

A single-page marketing site. No comment form, no backend, no configuration —
just files. This makes deployment simple and removes every step that was
causing trouble before.

## What's in this folder

```
index.html          the whole site
images/
  cover.png         book cover (hero)
  author.png        author portrait
```
- seminar.html — standalone page for the 19 Oct 2026 teach-in (links back to index.html; uses images/cover.png)

The "Buy on Amazon" buttons link to:
https://www.amazon.com/dp/B0HDDK3DB3

The contact section lists the author's email:
thrivemindxmento@gmail.com

## Deploy to Cloudflare Pages (drag and drop — easiest)

Because there is no backend anymore, the simple drag-and-drop upload works
perfectly. You do NOT need Git, Wrangler, KV, or any binding.

1. Sign in at https://dash.cloudflare.com
2. Go to **Workers & Pages**.
3. Choose the option to **upload assets / deploy a site** (not "Create Worker").
   If the interface pushes you toward Workers, look specifically for the
   **"Upload"** or **"Drag and drop"** wording.
4. Drag in the **contents of this folder** — that means `index.html` and the
   `images` folder together. Do NOT drag the outer folder itself; the
   `index.html` file must sit at the top level of what you upload.
5. Give the project a name (e.g. `emotionally-whole`) and deploy.
6. Your site goes live at `https://emotionally-whole.pages.dev` (or similar).

## If Cloudflare keeps redirecting you to "Create Worker"

Cloudflare merged Workers and Pages in 2025 and the menus shifted. Two fallbacks:

- **Any static host works.** Because this is now pure static files, you can drop
  this same folder onto Netlify, GitHub Pages, Vercel, or Cloudflare — all of
  them accept a plain folder of HTML/images. Netlify's drag-and-drop
  (app.netlify.com/drop) is currently the least fussy: just drag the folder's
  contents onto the page and it deploys instantly.

## Custom domain

Once deployed, open the project's **Custom domains** tab and follow the prompt
to attach your own domain. If the domain is already on Cloudflare, it is one
click.

## Editing later

Everything is in `index.html`. To change the Amazon link, the email address,
or any text, open that one file in any text editor, edit, save, and re-upload
the folder. There is nothing else to keep in sync.
