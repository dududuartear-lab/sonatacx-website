# 🌐 Sonata.cx — Institutional Website

---

## 🔗 Live Site

**https://sonatacx.com.br**

The website serves as the primary digital presence for Sonata.cx, a CX and business management consultancy. It is hosted on Hostinger (shared hosting) and built entirely with static HTML, Tailwind CSS (CDN), and vanilla JavaScript — no build step required.

---

## 🏢 Project Context & Strategic Value

Sonata.cx is a consultancy focused on Customer Experience (CX), business management, and operational efficiency. The website was designed to:

- Present the consultancy's services and portfolio to potential clients
- Showcase the founder's professional trajectory and client results
- Serve as a lead capture gateway for proprietary CX tools developed under the **Sonata.cx Lab** initiative
- Publish editorial content (blog/column) to establish authority in the CX and management space

---

## 📄 Pages & Structure

### `index.html` — Main Institutional Page

The single-page website is structured into the following sections:

- **Hero:** Value proposition and primary CTAs
- **Sobre:** Founder profile and professional background
- **Resultados:** Key client outcomes and notable partnerships (Nubank, Mercado Livre, iFood, Fluke)
- **Serviços:** Service portfolio — Business Management, People Management, Market Strategy, and Special Services (AI training, mentoring)
- **Ferramentas:** Gateway to free CX tools developed under Sonata.cx Lab, with lead capture before access
- **Blog:** Editorial content published in a regional business newspaper (Montes Claros - MG)
- **Contato/Footer:** Contact form, WhatsApp button, and social links

### `planner.html` — Capacity Planner Landing & Lead Gate

A dedicated landing page for the **Sonata CX Capacity Planner** tool. It explains the tool's value proposition and requires the visitor to register (name, email, phone, company) before being redirected to the live application.

- Lead data is captured via **Sheet.best** and stored directly in Google Sheets
- Google Analytics (`G-C0J8CEBHSX`) tracks page views and lead conversion events
- Google Ads conversion (`AW-905546952`) fires only after successful form submission

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | Tailwind CSS (CDN) |
| Fonts | Google Fonts (Bebas Neue, Raleway) |
| Analytics | Google Analytics 4 (GA4) |
| Lead Capture | Sheet.best → Google Sheets |
| Hosting | Hostinger (shared hosting) |

---

## 🚀 AI-Assisted Development & Methodology

This website was built using an **AI-Augmented** product methodology. Acting as Product Lead and Content Architect, I used generative AI to:

- Translate brand identity and service portfolio into a structured, conversion-focused layout
- Implement the lead capture flow integrated with Google Sheets via Sheet.best, without requiring a backend
- Configure Google Analytics and Google Ads conversion tracking with correct event firing (conversion pixel moved from page load to post-submission)
- Develop the **Ferramentas** section as a scalable gateway for future CX tools

---

## 💼 Developer / Portfolio

**Project by: Eduardo Duarte e Araujo**

Role: CX Strategy & AI-Augmented Product Development

> **Disclaimer:** This repository contains the source code of the institutional website for Sonata.cx. It is published here for portfolio and code review purposes. The live version is hosted on Hostinger and may differ from the files in this repository.
