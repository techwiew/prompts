You are a senior full-stack developer, system architect, UI/UX designer, and SEO expert.

Your task is to generate a **fully dynamic, production-ready website** using **Next.js (App Router), TypeScript, Tailwind CSS**, where **EVERYTHING is controlled via a single `data.json` file**.

---

## 🧾 INPUT

You will receive a **paragraph describing a business**.

[PASTE CLIENT PARAGRAPH HERE]

---

## 🎯 CORE OBJECTIVE

1. Extract all business information from the paragraph
2. Convert it into a **highly structured `data.json`**
3. Store **ALL reusable constants inside `data.json`**
4. Build the website using ONLY values from `data.json`

---

## 📦 `data.json` (SINGLE SOURCE OF TRUTH)

This file must act as a **central configuration + content + design system**.

---

### 🔹 1. BRAND SYSTEM (Design Tokens)

Store all reusable UI constants:

* colors:

  * primary
  * secondary
  * accent
  * background
  * surface
  * textPrimary
  * textSecondary
  * border

* typography:

  * fontFamily:

    * heading
    * body
  * fontSizes (xs → 4xl)
  * fontWeights

* spacingScale (xs, sm, md, lg, xl)

* borderRadius (sm, md, lg, xl)

* shadows (light, medium, heavy)

---

### 🔹 2. COMPONENT CONFIG (Reusable UI)

Define reusable styles:

* buttons:

  * primary
  * secondary
  * outline
    (include color, padding, radius, hover states)

* cards:

  * padding
  * shadow
  * border

* inputs:

  * styles

* layout:

  * containerWidth
  * sectionSpacing

---

### 🔹 3. BRANDING

* companyName
* tagline
* description
* logo
* favicon

---

### 🔹 4. BUSINESS DATA

* industry
* services (title, description, icon key)
* products
* usp
* experience

---

### 🔹 5. LOCATION & CONTACT

* address
* city, state, country
* coordinates (lat, lng)
* phone
* email
* whatsapp
* socialLinks

---

### 🔹 6. TEAM

* name
* role
* education
* experience
* achievements

---

### 🔹 7. CONTENT SYSTEM

All sections must be configurable:

* hero
* about
* services
* testimonials
* faq
* gallery
* cta

Each section must include:

* visibility (true/false)
* title
* subtitle
* description
* items (array-based for scalability)
* CTA config

---

### 🔹 8. SEO SYSTEM (AUTO-GENERATED)

* meta:

  * title
  * description
  * keywords (include city + niche)

* openGraph

* twitterMeta

* canonicalUrl

* structuredData (JSON-LD for LocalBusiness)

---

### 🔹 9. ANALYTICS

* googleAnalyticsId
* tagManagerId
* metaPixelId

---

### 🔹 10. FEATURE FLAGS

Enable/disable features:

* enableAnimations
* enableWhatsAppChat
* enableCallButton
* enableDarkMode
* enableStickyNavbar

---

### 🔹 11. ROUTING CONFIG

* navigation:

  * label
  * path
  * visible

---

## 🧱 DEVELOPMENT RULES

* Use Next.js + TypeScript
* Use Tailwind CSS (derive config from `data.json`)
* Use Framer Motion (controlled via feature flags)
* Build reusable components:

  * Navbar
  * Hero
  * About
  * Services
  * Footer

---

## ❗ STRICT RULES

* DO NOT hardcode any value
* ALL:

  * text
  * colors
  * spacing
  * styles
  * feature toggles
    MUST come from `data.json`

---

## 🎨 UI BEHAVIOR

* UI must adapt dynamically based on JSON
* Sections render only if `visibility = true`
* Theme must switch if enabled

---

## 🌐 SEO & PERFORMANCE

* Semantic HTML
* Dynamic meta tags from JSON
* Optimized images
* Lazy loading
* Sitemap + robots.txt

---

## 📁 OUTPUT

Provide:

1. Complete `data.json` (well structured, scalable)
2. Full Next.js project code
3. Tailwind config generated from JSON tokens
4. Clear setup instructions

---

## 🔁 REUSABILITY

This system must work for ANY business by ONLY changing `data.json`.

---

## 🚀 FINAL GOAL

Build a **config-driven website engine** where:
👉 `data.json = entire website (design + content + behavior + SEO)`
👉 Code = reusable renderer
