# My Portfolio

My personal portfolio site, built with [Nuxt](https://nuxt.com), [Nuxt UI](https://ui.nuxt.com), and [Tailwind CSS](https://tailwindcss.com).

## Getting started

### Requirements

- [Node.js](https://nodejs.org) (current LTS version)
- npm (comes with Node.js), or yarn, or pnpm

### Setup

1. Clone the repository

   ```bash
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```

2. Install the dependencies

   ```bash
   npm install
   ```

3. Start the development server

   ```bash
   npm run dev
   ```

4. Open http://localhost:3000 in your browser. The page updates automatically when you save a file.

Using yarn or pnpm? Replace `npm install` with `yarn` or `pnpm install`, and `npm run dev` with `yarn dev` or `pnpm dev`.

## Scripts

| Command            | What it does                                 |
| ------------------ | -------------------------------------------- |
| `npm run dev`      | Start the development server                 |
| `npm run build`    | Build the site for production                |
| `npm run generate` | Build a static version of the site           |
| `npm run preview`  | Preview the production build locally         |
| `npm run lint`     | Check the code for problems and formatting   |
| `npm run lint:fix` | Automatically fix formatting and lint issues |

## Project structure

```
app/
  app.vue          Root of the site (page title, layout wrapper)
  pages/           Each file here becomes a page (index.vue is the home page)
  layouts/         Shared page structure, such as header and footer
  components/      Reusable pieces
  assets/css/      Global styles
public/            Images and files served as-is (favicon, photos, resume)
nuxt.config.ts     Nuxt settings
```

## Customizing

- **Your content:** edit the text and lists at the top of `app/pages/index.vue`.
- **Site title:** change `"Your Name"` in `app/app.vue`.
- **Favicon:** replace `public/favicon.ico`.
- **Images:** put them in `public/` and reference them like `/my-photo.jpg`.
- **New page:** create `app/pages/about.vue` and it will be available at `/about`.

## Deploying

Run `npm run generate`. This creates a static site in `.output/public` that you can host for free on Netlify, Vercel, Cloudflare Pages, or GitHub Pages.