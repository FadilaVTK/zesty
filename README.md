# 🍕 Zesty - Food Delivery & Restaurant Discovery

> *"Skip the Wait, Start the Plate"*

**Zesty** is a modern food ordering and restaurant exploration web application built with **Next.js 16 (App Router)**, **React 19**, and **Tailwind CSS**. It provides a clean, responsive interface for users to discover local restaurants, browse popular culinary categories, compare food prices across different eateries, and explore full menus.

---

## 📌 Project Overview & Suggested Name

- **Recommended Project Name:** **Zesty** (or **Zesty Food Delivery**)
  - *Why this name?* The application already carries the "Zesty" branding in its navigation bar alongside the tagline *"Skip the Wait, Start the Plate"*, evoking fresh, appetizing flavors and fast service.
- **Alternative Name Ideas:**
  - *Craver / CraveCart*
  - *BiteSwift*
  - *PlateHop*
  - *FeastFinder*

---

## ✨ Features

- 🔐 **Authentication & Protected Routes**
  - Context-powered authentication (`AuthContext`) with session persistence in `localStorage`.
  - Route guard (`Protected` component) ensuring secured pages are accessible only after logging in.
  - Dedicated login screen with input validation and error feedback.

- 🏠 **Interactive Home Dashboard**
  - Personalized welcome greeting for authenticated users.
  - Featured promotional banner with appetizing visuals.
  - **Top Restaurants** showcase grid linking directly to individual restaurant pages.
  - **Popular Foods** circular category browser for one-click filtering.

- 🍽️ **Restaurant Profiles (`/restaurant/[id]`)**
  - Dedicated pages for individual eateries (e.g., *Grill House*, *Pepper Palace*, *Pizza Villa*).
  - Displays restaurant imagery and a tailored menu of dishes served at that location.

- 🏷️ **Category-Based Filtering (`/category/[category]`)**
  - Dynamic route to explore foods by category (e.g., *Pizza*, *Biriyani*, *Shawarma*, *Al-faham*, *Drinks*, *Pasta*).

- 🔍 **Food Details & Cross-Restaurant Price Comparison (`/food/[id]`)**
  - Detailed food view with high-resolution imagery and pricing.
  - **"Available At"** feature: Lists all restaurants preparing that dish so users can compare prices and select their preferred outlet.

- 📜 **Full Menu Listing (`/menu`)**
  - Complete catalog of available food items across all partner restaurants.
  - Responsive food cards equipped with pricing, restaurant attribution, and "Add to Cart" triggers.

---

## 🔑 Demo Credentials

To test the application, log in with the following preset credentials:

| Field | Value |
| :--- | :--- |
| **Email** | `admin@gmail.com` |
| **Password** | `12345` |
| **User Name** | *James* |

---

## 🛠️ Tech Stack

- **Framework:** [Next.js 16](https://nextjs.org/) (App Router)
- **Library:** [React 19](https://react.dev/)
- **Styling:** [Tailwind CSS v4](https://tailwindcss.com/)
- **State Management:** React Context API (`AuthContext`)
- **Icons / Assets:** SVG icons & high-quality food photography from Unsplash and iStock
- **Tooling:** ESLint 9, TypeScript types configured

---

## 📂 Project Structure

```text
project2/
├── app/
│   ├── category/
│   │   └── [category]/
│   │       └── page.jsx        # Category-filtered food listing
│   ├── food/
│   │   └── [id]/
│   │       └── page.jsx        # Food item details & restaurant price comparison
│   ├── login/
│   │   └── page.jsx            # User login page
│   ├── menu/
│   │   └── page.jsx            # All-items menu catalog
│   ├── restaurant/
│   │   └── [id]/
│   │       └── page.jsx        # Individual restaurant profile & dishes
│   ├── favicon.ico             # App favicon
│   ├── globals.css             # Tailwind CSS imports & global styles
│   ├── layout.jsx              # Root layout with AuthProvider & dynamic Navbar
│   ├── page.jsx                # Home page (Top Restaurants & Categories)
│   └── protected.jsx           # Client-side authentication guard
├── components/
│   ├── Banner.jsx              # Promotional hero banner
│   ├── FoodCard.jsx            # Reusable food card with price and CTA
│   └── Navbar.jsx              # Navigation header with branding & auth actions
├── context/
│   └── AuthContext.jsx         # React Context for login/logout state & localStorage
├── data/
│   ├── categoryImages.js       # Category metadata & thumbnail URLs
│   ├── foods.js                # Food items dataset with restaurant associations
│   └── restaurants.js          # Partner restaurants dataset
├── public/                     # Static SVG icons and assets
├── eslint.config.mjs           # ESLint configuration
├── next.config.ts              # Next.js configuration
├── package.json                # Project dependencies and scripts
└── tsconfig.json               # TypeScript configuration
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) (v18.18.0 or newer recommended) and `npm` installed.

### 1. Installation

Clone or open the repository directory and install dependencies:

```bash
npm install
```

### 2. Run the Development Server

Start the local development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### 3. Build for Production

To create an optimized production build:

```bash
npm run build
npm run start
```

### 4. Linting

Run code linting:

```bash
npm run lint
```

---

## 🗺️ Roadmap & Future Enhancements

- [ ] Cart state management (persisted cart drawer & item counter in Navbar)
- [ ] Checkout page & mock payment gateway integration
- [ ] Search bar for instant dish & restaurant filtering
- [ ] User order history and delivery status tracker
- [ ] Backend database integration (e.g., PostgreSQL, MongoDB, or Supabase)
