# Safiullah — Portfolio Website

A premium, black-and-gold personal portfolio built with **React 19**, **Vite**, **Tailwind CSS v4**, **Framer Motion**, **GSAP**, and **Lenis** smooth scroll.

Live sections: Loading Screen · Navigation · Hero · About · Skills · Services · Experience Timeline · Education · Certifications · Volunteer Work · Projects · Achievements · Contact · Footer · 404 Page.

---

## ✨ Features

- Premium black & gold, glassmorphism design system
- Animated loading screen, custom cursor, scroll progress bar
- Canvas particle background with mouse glow effect
- Typing animation in the hero (role rotator)
- Scroll-triggered reveal animations (Framer Motion + GSAP)
- Animated skill progress bars and stat counters
- Filterable project cards, 3D tilt hover on service cards
- Light / dark theme switcher
- Fully responsive: desktop, laptop, tablet, mobile
- SEO meta tags, Open Graph & Twitter cards, `robots.txt`
- Accessible: visible focus states, `prefers-reduced-motion` respected

---

## 🧰 Tech Stack

| Purpose            | Library              |
|---------------------|-----------------------|
| UI Framework         | React 19              |
| Build Tool           | Vite 6                |
| Styling              | Tailwind CSS v4        |
| Animation            | Framer Motion, GSAP    |
| Smooth Scroll        | Lenis                  |
| Routing              | React Router DOM       |
| Icons                | Lucide React, React Icons |

---

## 📦 Project Structure

```
├── public/
│   ├── favicon.svg
│   └── robots.txt
├── src/
│   ├── components/       # All UI building blocks (Navbar, Hero, About, ...)
│   ├── pages/             # Route-level pages (Home, NotFound)
│   ├── hooks/              # useTheme, useLenis, useScrollProgress, ...
│   ├── utils/               # data.js (all content), motionVariants.js
│   ├── styles/               # index.css (Tailwind + design tokens)
│   ├── App.jsx
│   └── main.jsx
├── index.html
├── vite.config.js
├── tailwind.config.js
└── package.json
```

All editable content (name, bio, skills, projects, contact links, etc.) lives in a single file: **`src/utils/data.js`**. Edit that file to personalize the site — no need to touch any component.

---

## 🚀 Getting Started

### 1. Install dependencies

```bash
npm install
```

### 2. Run the development server

```bash
npm run dev
```

The site will be available at `http://localhost:5173`.

### 3. Build for production

```bash
npm run build
```

Output is generated in the `dist/` folder.

### 4. Preview the production build locally

```bash
npm run preview
```

---

## 🛠️ Personalizing the Site

1. Open `src/utils/data.js` and update:
   - `profile` — name, roles, country, summary, CV link
   - `contact` — email, LinkedIn, GitHub, WhatsApp
   - `skills`, `services`, `experience`, `education`, `certifications`, `volunteer`, `projects`, `achievements`
2. Replace `public/favicon.svg` with your own icon if desired.
3. Add an `og-image.png` (1200×630) to `public/` for social share previews, referenced in `index.html`.
4. Wire the contact form in `src/components/Contact.jsx` to a backend of your choice (e.g. Formspree, EmailJS, Resend).

---

## ☁️ Deployment

### Vercel

1. Push this project to a GitHub repository.
2. Go to [vercel.com/new](https://vercel.com/new) and import the repository.
3. Framework preset: **Vite**. Build command: `npm run build`. Output directory: `dist`.
4. Click **Deploy**.

### Netlify

1. Push this project to a GitHub repository.
2. Go to [app.netlify.com](https://app.netlify.com) → **Add new site** → **Import an existing project**.
3. Build command: `npm run build`. Publish directory: `dist`.
4. Click **Deploy site**.

### GitHub Pages

1. Install the GitHub Pages helper:
   ```bash
   npm install --save-dev gh-pages
   ```
2. In `package.json`, add:
   ```json
   "homepage": "https://<your-username>.github.io/<repo-name>",
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d dist"
   }
   ```
3. In `vite.config.js`, set `base: '/<repo-name>/'` inside `defineConfig`.
4. Deploy:
   ```bash
   npm run deploy
   ```

---

## ♿ Accessibility & Performance

- Respects `prefers-reduced-motion` (disables custom cursor, smooth scroll, and heavy animation for users who request it).
- Keyboard-visible focus rings on all interactive elements.
- Semantic headings and landmark sections throughout.
- Lightweight canvas particle system with no external animation dependency.

---

## 📄 License

This project is free to use and modify for personal portfolio purposes.
