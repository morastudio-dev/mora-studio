# itzmenorah.com: End-to-End GitHub Pages Guide

## Purpose
This document is a stage-gated, research-first implementation plan for creating and publishing a safe, lightweight portfolio website for a 14-year-old creator at `itzmenorah.com`.

The recommended architecture is:
1- Domain registration: Hostinger
2- Email: Hostinger Email- Norahs email or pappas email
3- Static website hosting: GitHub Pages
- Website files: HTML, CSS and JavaScript
- Cost of website hosting: zero additional hosting cost
- Domain cost: the existing domain registration and future renewal remain separate

---

## Safety and responsibility rules

### Audience
The creator is 14 years old. A parent or guardian should supervise account creation, domain changes, publishing and public content.

### Never publish
- Home address
- School name
- Personal phone number
- Daily routine
- Exact location
- Private email address
- Passwords or recovery codes
- Private photographs
- Unapproved social-media accounts
- API keys, tokens or secret files

### DNS safety rule
Do not delete or replace email records while connecting the website. The existing Hostinger Email service depends on its MX, SPF and DKIM records.
Do not use a wildcard DNS record such as `*.itzmenorah.com`.

---

## Website Files Included in Package

- `index.html` — Homepage ("Small ideas, thoughtfully made.")
- `work.html` — Projects & experiments ("Quiet Room", "Folded Object", "Little Web Home")
- `journal.html` — Stories ("The House That Collected Light", "The Chair by the Window")
- `about.html` — Studio philosophy & calm Norwegian design principles
- `style.css` — Responsive design system with Norwegian minimalist palette
- `script.js` — Accessible navigation controls
- `CNAME` — Preconfigured apex custom domain (`itzmenorah.com`)
- `images/` — Visual assets for studies

---

## Hostinger DNS Configuration

When pointing `itzmenorah.com` to GitHub Pages:
1. Preserve all existing MX records (`mx1.hostinger.com`, `mx2.hostinger.com`) and SPF TXT record.
2. Add four `A` records for `@`:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. Point `CNAME` for `www` to `<github-username>.github.io` (or `itzmenorah.com`).

