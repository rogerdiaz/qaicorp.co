# QAI Corp. — Website

Boutique QA/QE company website. Cream/navy/gold, editorial-style, fully static HTML/CSS/JS — no build step, no framework.

## Pages

| File | URL |
|------|-----|
| `index.html` | Home (landing page) |
| `services.html` | Services |
| `methodology.html` | The QAI Framework |
| `case-studies.html` | Case Studies (⚠️ placeholder content — see below) |
| `about.html` | About Us |
| `blog.html` | Blog / Insights |
| `contact.html` | Contact / Book a Call |

---

## 🚀 How to Publish on GitHub Pages

This repo (`rogerdiaz/qaicorp.co`) already includes a `CNAME` file pointing at `qaicorp.co`, so publishing is just:

### Step 1 — Push your changes

```bash
cd /path/to/qaicorp.co
git add .
git commit -m "Update site"
git push
```

### Step 2 — Enable GitHub Pages (one-time)

1. Go to the repository on GitHub → **Settings** tab
2. Scroll to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Select branch: **main**, folder: **/ (root)**
5. Click **Save**

### Step 3 — Custom domain (already configured)

The `CNAME` file already points to `qaicorp.co`. In GitHub Pages settings, confirm the domain field shows `qaicorp.co` and that **Enforce HTTPS** is checked. DNS should already have these records with your registrar:

```
Type    Name    Value
A       @       185.199.108.153
A       @       185.199.109.153
A       @       185.199.110.153
A       @       185.199.111.153
CNAME   www     rogerdiaz.github.io
```

After a push, the live site updates at `https://qaicorp.co` within a minute or two.

---

## ⚠️ Before going live: replace the case studies

`case-studies.html` still has a visible warning banner and a `TODO(Roger)` comment in the source. The two case studies on that page are generic, anonymized placeholders carried over from the original template — replace them with QAI Corp.'s own real, attributable client results (for example, the TotalWine/Kibo ERP Playwright migration or the Promérica QE engagement) before publishing, then remove the banner and the TODO comment.

---

## 📬 Contact form & newsletter

Both currently use `mailto:hello@qaicorp.co` — the contact form builds a pre-filled email from the form fields client-side (no backend), and the blog's newsletter button does the same. This was a deliberate choice to avoid standing up a backend or a third-party form service for now. If you want a real inbox/CRM integration or a newsletter list later, swap in something like:
- [Formspree](https://formspree.io) — add `action="https://formspree.io/f/YOUR_ID"` to the `<form>` tag in `contact.html`
- A real ESP (Mailchimp, ConvertKit, etc.) for the blog newsletter form

## 📅 Booking

"Get your free audit" / "Book a Call" CTAs embed or link to a real Calendly link (`https://calendly.com/dia12176/free-qa-audit-qai-corp`) — update it in `index.html`, `services.html`, and any other page's CTA if the Calendly URL changes.

### Update social links
Search for `href="#"` in the footer of each page (if any remain) and replace with your real LinkedIn/GitHub links.

---

## 🛠 Tech Stack

- **Custom CSS design system** — no framework, no build step (cream/navy/gold palette, CSS variables in each page's `<style>` block)
- **Playfair Display** (headings) + **Epilogue** (body) — Google Fonts
- **Vanilla JS** — scroll reveal, sticky navbar, mobile hamburger menu
- **No frameworks** — works in any browser, deploys anywhere

---

© 2026 QAI Corp.
