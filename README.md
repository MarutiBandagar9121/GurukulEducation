# Gurukul Education — Marketing Website

A freelance client project: a marketing and information website for **Gurukul Education**, a Pune-based academy (Panshet) offering defense-career coaching, school adventure camps, and life-skills training programs. Built end-to-end — design-to-code, content structuring, and production deployment — as a solo freelance engagement.

> **Status:** The client's contract ended and the site is no longer live. This repository is kept as a portfolio reference for the code and approach.

## About the Client

Gurukul Education trains students for government defense-force recruitment and runs adventure/life-skills camps for school-age children, led by ex-military instructors. The site needed to present the academy's programs, leadership team, achievements, and a large volume of photo/video evidence of past camps to prospective parents and students.

## Why Astro

The client's brief was a content-driven, mostly static marketing site: a handful of pages (home, about, services, gallery, testimonials, FAQ, contact), heavy on images, with no need for a client-side app or a database-backed backend. The priorities were fast page loads, good SEO out of the box, and low, predictable hosting costs.

Astro was the right fit for that brief:

- **Ships zero/minimal JS by default** — pages render to static HTML, which keeps load times low on a small VPS and helps organic search ranking.
- **Component-based authoring** without the runtime overhead of a full SPA framework — ideal for a content site that's really a set of related pages, not an application.
- **Cheap, simple hosting** — no need for a managed Node platform or serverless functions; a small VPS with Node running in standalone mode is enough.

## Tech Stack

| Layer | Choice |
|---|---|
| Framework | [Astro 5](https://astro.build) |
| Styling | [Tailwind CSS 3](https://tailwindcss.com) |
| Server adapter | `@astrojs/node` (standalone mode) |
| Language | TypeScript / Astro components |
| Hosting | Self-managed VPS (Hostinger) |

## Site Structure

- **Home** — hero banner and mission snapshot
- **About Us** — mission & vision, achievements/stats, and a full leadership & instructor team roster
- **Services** — Adventure Camp, School Training, and Defence Training program breakdowns
- **Image Gallery** — curated photo grid from past camps
- **Videos Gallery** — embedded YouTube highlights
- **Testimonials** — parent and student feedback
- **FAQ** — common questions for prospective families
- **Contact Us** — embedded Google Map, phone, address, and email, sourced from reusable SVG-icon cards

Shared layout, navbar, and footer components (with social links to WhatsApp, Facebook, Instagram, and YouTube) are reused across every page via a single `Layout.astro`.

## Freelance Scope

As the sole developer on this engagement, responsibilities covered the full delivery pipeline:

- Translating the client's brand assets and content (photos, program descriptions, staff bios) into a structured, componentized site
- Building a responsive layout (mobile nav, responsive image grids) with Tailwind, with no design system handed off in advance
- Setting up and hardening a VPS on Hostinger, configuring the Node server, domain, and SSL
- Handling change requests iteratively over the site's ~year-long life (see commit history), including content and personnel updates as the client's team changed

## Project Status

This was a live production site for a paying client for roughly a year. It was taken offline after the client discontinued the engagement (non-payment); the codebase here reflects its last deployed state and is preserved to demonstrate the build.

## Running Locally

```bash
npm install
npm run dev       # http://localhost:4321
```

| Command | Action |
|---|---|
| `npm install` | Install dependencies |
| `npm run dev` | Start local dev server |
| `npm run build` | Build production site (Node server output) |
| `npm run preview` | Preview the production build locally |
| `npm run astro ...` | Run Astro CLI commands (e.g. `astro check`) |
