# DMI Portfolio Website (Static HTML/CSS)

This repository contains a clean, professional-looking **static portfolio website** used in **DevOps Micro Internship (DMI)** Week 1 to practice:
- Linux basics
- Nginx hosting
- Deployment proof / ownership
- Production-style checks

✅ Students deploy this website on an Ubuntu VM using Nginx and keep it live for 24 hours.

---

## Who is this for?
- DMI students (beginner → intermediate)
- Anyone learning how to host a static site with Nginx on Linux

---

## What you will build
A portfolio-style website hosted on:
- **Ubuntu VM**
- **Nginx**
- Accessible via: `http://<public-ip>`

---

## Mandatory Ownership Proof (DMI Rule)
Before you deploy, you MUST edit the footer and add your details:

Original:

```html
<p>Crafted with <span>cloud</span> excellence by Pravin Mishra</p>
```

Add this line (example):

```html
<p><strong>Deployed by:</strong> DMI Cohort 2 | Rahul Sharma | Group 4 | Week 1 | 16-01-2026</p>
```

✅ This proof must be visible in your browser screenshot submission.

## Footer Requirement (Week 4 — Mini-Sprint)

The site footer displays the site version, deployment date, and author, in the following exact format:
Pravin Mishra Portfolio v1.0 — Deployed on 4th August 2026 — By Judah Oyekunle

### How the Date Is Generated
The deployment date is generated automatically using JavaScript. A `<span id="deployDate">` placeholder sits in the footer HTML, and a script fills it in with the current date — formatted as `DD Mon YYYY` — every time the page loads.

<!-- Script that fills in the current date -->
<script>
  const options = { day: '2-digit', month: 'short', year: 'numeric' };
  document.getElementById('deployDate').textContent =
    new Date().toLocaleDateString('en-GB', options).replace(',', '');
</script>

This means the displayed date always reflects the date the page was actually loaded, with no manual updating required on future deployments.
