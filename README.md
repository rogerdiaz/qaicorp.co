# Turing's Lab — Website

AI-Powered Quality Engineering company website. Dark-mode, SaaS-style, fully static HTML/CSS/JS.

## Pages

| File | URL |
|------|-----|
| `index.html` | Home (landing page) |
| `services.html` | Services |
| `methodology.html` | The Turing QA Framework |
| `case-studies.html` | Case Studies |
| `about.html` | About Us |
| `blog.html` | Blog / Insights |
| `contact.html` | Contact / Book a Call |

---

## 🚀 How to Publish on GitHub Pages

### Step 1 — Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it `turings-lab` (or `yourusername.github.io` for a root domain)
4. Set it to **Public**
5. Click **Create repository**

### Step 2 — Upload your files

**Option A — via GitHub web interface (easiest):**
1. Open your new repository
2. Click **Add file → Upload files**
3. Drag and drop ALL the `.html` files from this folder
4. Click **Commit changes**

**Option B — via Git CLI:**
```bash
cd /path/to/turings-lab
git init
git add .
git commit -m "Initial website commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/turings-lab.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll to **Pages** in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Select branch: **main**, folder: **/ (root)**
6. Click **Save**

### Step 4 — Visit your site

After 1–2 minutes, your site will be live at:
```
https://YOUR_USERNAME.github.io/turings-lab/
```

---

## 🌐 Custom Domain (optional)

If you want `turingslab.io` or similar:

1. Buy a domain (Namecheap, Cloudflare Domains, etc.)
2. In GitHub Pages settings → **Custom domain** → enter your domain
3. Add these DNS records with your registrar:

```
Type    Name    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     YOUR_USERNAME.github.io
```

4. Check **Enforce HTTPS** in GitHub Pages settings

---

## 🎨 Customization Guide

### Update your contact info
Search for `hello@turingslab.io` across all files and replace with your real email.

### Update social links
Search for `href="#"` in the footer of each page and replace with your:
- LinkedIn: `https://linkedin.com/in/yourprofile`
- GitHub: `https://github.com/yourprofile`

### Update LinkedIn / booking link
In `contact.html`, the form currently just shows a success message. To connect it to a real form:
- [Formspree](https://formspree.io) — free, just add `action="https://formspree.io/f/YOUR_ID"` to the `<form>` tag
- [Cal.com](https://cal.com) — free booking page, add a "Book on Cal.com" button

### Connect a real booking calendar
Replace the "Book a Call" CTA links with your Calendly or Cal.com link:
```html
<a href="https://cal.com/yourname/30min" ...>Book a Call</a>
```

---

## 🛠 Tech Stack

- **Tailwind CSS** — via CDN (no build required)
- **Space Grotesk** — Google Fonts
- **Vanilla JS** — scroll reveal, sticky navbar, mobile menu
- **No frameworks** — works in any browser, deploys anywhere

---

© 2026 Turing's Lab
