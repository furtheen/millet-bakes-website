# 🌾 Millet Bakes — React + Vite Project

## Folder Structure

```
millet-bakes/
├── public/
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── Hero.jsx
│   │   ├── FeaturesStrip.jsx
│   │   ├── Products.jsx
│   │   ├── WhyUs.jsx
│   │   ├── Testimonials.jsx
│   │   ├── About.jsx
│   │   ├── CTA.jsx
│   │   └── Footer.jsx
│   ├── data/
│   │   ├── products.js       ← product list array
│   │   └── testimonials.js   ← reviews array
│   ├── hooks/
│   │   └── useScrollFade.js  ← IntersectionObserver hook
│   ├── utils/
│   │   └── whatsapp.js       ← waLink() helper
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css             ← Tailwind directives + custom CSS vars
├── index.html
├── tailwind.config.js
├── vite.config.js
└── package.json
```

## How to Run

```bash
# 1. Create project
npm create vite@latest millet-bakes -- --template react
cd millet-bakes

# 2. Install dependencies
npm install
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

# 3. Configure Tailwind (tailwind.config.js)
# content: ["./index.html", "./src/**/*.{js,jsx}"]

# 4. Add to src/index.css:
# @tailwind base;
# @tailwind components;
# @tailwind utilities;

# 5. Run dev server
npm run dev

# 6. Build for production
npm run build

# 7. Deploy to Vercel
npx vercel
```

## WhatsApp Number Setup

In `src/utils/whatsapp.js`, replace the number:
```js
export const WA_NUMBER = "91XXXXXXXXXX"; // Shivani's WhatsApp number with country code
export const waLink = (msg) =>
  `https://wa.me/${WA_NUMBER}?text=${encodeURIComponent(msg)}`;
```

## Vercel Deployment

```bash
# One-command deploy
npx vercel --prod

# Or connect GitHub repo at vercel.com for auto-deploy on push
```

## Adding Real Product Images

Replace emoji placeholders in `src/data/products.js`:
```js
{
  id: 1,
  image: "/images/ragi-brownie.jpg",  // place in public/images/
  // ...
}
```
