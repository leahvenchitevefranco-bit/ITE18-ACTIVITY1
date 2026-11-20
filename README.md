# Kuring | Personal Profile Website

A two-page creative personal profile website for **Leahvenchiteve M. Franco (Kuring)**, a BSIT student at Caraga State University.
Built with **Nuxt** (Vue 3 single-file components) and **Tailwind CSS**, styled after an editorial creative-portfolio design
(chocolate brown, butter yellow and bright orange).

## Pages

| Route      | File                    | Description                                                       |
| ---------- | ----------------------- | ----------------------------------------------------------------- |
| `/`        | `app/pages/index.vue`   | Name, introduction, profile picture, welcome message |
| `/profile` | `app/pages/profile.vue` | About me (info + education), skills + interests, hobbies gallery|

## Requirements

- Node.js 20 or newer (Node 22 recommended)
- npm (comes with Node.js)

## Install and run

```bash
# 1. open the project folder
cd personal-profile

# 2. install dependencies
npm install

# 3. start the development server
npm run dev
```

Then open <http://localhost:3000>.

Other commands:

```bash
npm run build     # production build
npm run preview   # preview the production build
npm run generate  # static site generation
```

## Project structure

```text
personal-profile/
├── app/
│   ├── app.vue                  # root: <NuxtLayout><NuxtPage /></NuxtLayout>
│   ├── assets/css/main.css      # Tailwind directives + small component classes
│   ├── layouts/default.vue      # navbar + footer shell
│   ├── components/
│   │   ├── Navbar.vue           # NuxtLink navigation (Home, Profile)
│   │   ├── PhotoGallery.vue     # masonry / grid photo gallery
│   │   └── SectionTitle.vue     # reusable section heading
│   ├── pages/
│   │   ├── index.vue            # Homepage
│   │   └── profile.vue          # Profile page
│   └── types/gallery.ts         # shared TypeScript type
├── public/images/               # personal photographs
├── nuxt.config.ts
├── tailwind.config.ts           # colour palette and fonts
└── package.json
```

## Photo usage

| File                         | Used for                                  |
| ---------------------------- | ----------------------------------------- |
| `profile.jpg` (B&W portrait) | Homepage profile picture only             |
| `beach-1.jpg`, `beach-2.jpg` | Beach and Traveling                       |
| `hiking.jpg`, `waterfall.jpg`| Nature and Hiking                         |
| `sunset.jpg`                 | Watching Sunsets                          |
| `reading.jpg`                | Reading                                   |
| `volleyball.jpg`             | Playing Volleyball                        |
| `crime-series.jpg`           | Watching Crime Scene Movies and Series    |

Photos keep their natural proportions (no stretching or forced cropping), and the gallery is responsive.

## Design tokens

| Token    | Hex       |
| -------- | --------- |
| `choc`   | `#40231C` |
| `deep`   | `#321A15` |
| `butter` | `#F5EBA0` |
| `ember`  | `#FF4B0B` |
| `cream`  | `#F6F0E5` |
| `ink`    | `#3A211B` |

Fonts (loaded from Google Fonts): Poppins (headings), DM Sans (body), Mrs Saint Delafield (script accents).
