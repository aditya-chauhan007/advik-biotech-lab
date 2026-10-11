# Advik Biotech Lab — Website

Official website for **Advik Biotech Lab**, an ISO-certified biotechnology training and research lab based in Greater Noida, Uttar Pradesh, India.

**Live site:** [advikbiotechlab.com](https://advikbiotechlab.com)

---

## About

Advik Biotech Lab offers hands-on training in biotechnology, molecular diagnostics, plant tissue culture, microbiology, bioinformatics, and related disciplines, alongside sample testing and research kit development for the contractual sector. This repository contains the source code for the lab's public website.

## Features

- Single-page site with client-side routing (Home, About Us, Services, Contact Us)
- Course catalog with expandable topic lists
- Lab photo gallery with a swipeable, auto-advancing slider
- "Special Weekend Certificate Course" promotional section with a one-time welcome pop-up
- Persistent "Sign Up" side panel available on every page
- Contact and sign-up forms wired to [Formspree](https://formspree.io) for email delivery
- Google Analytics (GA4) integration for visitor tracking
- Legacy URL redirects (e.g. `/about-us`, `/services`) to preserve old search-engine links
- Fully responsive, light-themed, single-file deployment

## Tech Stack

- **HTML5, CSS3, vanilla JavaScript** — no build step or framework dependencies
- **[Formspree](https://formspree.io)** — contact and sign-up form submission handling
- **[Google Analytics (GA4)](https://analytics.google.com)** — visitor and traffic analytics
- **[Vercel](https://vercel.com)** — hosting and deployment, connected to this repository for automatic deploys

## Project Structure

```
.
├── index.html       # Entire website (markup, styles, and scripts)
├── vercel.json       # Hosting configuration: legacy URL redirects and SPA routing
└── README.md         # This file
```

The site is intentionally built as a single self-contained `index.html` file, with all images embedded directly as base64 data — there are no external image files or build artifacts to manage.

## Deployment

This repository is connected to a Vercel project. Any commit pushed to the `main` branch is automatically built and deployed to production at **advikbiotechlab.com** within seconds — no manual steps required.

### Routing

`vercel.json` defines:
- 301 redirects from legacy page URLs (from the site's previous platform) to the corresponding section on the new single-page site
- A catch-all rewrite so any unrecognized URL falls back to `index.html` instead of returning a 404

## Making Updates

1. Edit `index.html` (or replace it with an updated version).
2. Commit the change directly to the `main` branch, either via the GitHub web editor or a regular Git push.
3. Vercel detects the push and redeploys automatically — check the **Deployments** tab on Vercel to confirm the new build is marked **Ready**.

No local build tools, package installation, or compilation step is required at any point.

## Forms & Integrations

| Integration | Purpose | Recipient |
|---|---|---|
| Formspree (Contact form) | General enquiries from the Contact Us page | advikbiotechlab@gmail.com |
| Formspree (Sign Up form) | Course/training sign-up requests from the side panel | advikbiotechlab@gmail.com |
| Google Analytics (GA4) | Visitor and page-view tracking | Linked Google Analytics account |

## Contact

**Advik Biotech Lab**
F-46, Kadamba Market, Gamma-1, Greater Noida (UP), India, 201310
Phone: +91 98184 37050 / +91 99104 48533
Email: advikbiotechlab@gmail.com

---

© 2026 Advik Biotech Lab. All rights reserved.
