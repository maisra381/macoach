# MA COACH — Personal Sport Coaching Services · Downtown Dubai

A cinematic, single-page brand site for MA Coach (personal trainer, Burj Khalifa,
Downtown Dubai). Built with **React 19 + Vite + Tailwind CSS v4 + GSAP ScrollTrigger**.

## Run

```bash
npm install
npm run dev      # local development
npm run build    # production build → dist/
npm run preview  # preview the production build
```

## Structure

- `src/lib/data.ts` — all business facts (phone, maps link, hours, rating) and
  image URLs. **Edit copy, descriptions and imagery here and in the section
  components** — no credentials, prices or testimonials are invented anywhere.
- `src/lib/motion.ts` — GSAP setup, scoped `useGsap` hook with automatic cleanup,
  reveal helpers. All animation respects `prefers-reduced-motion` and pins are
  desktop-only; mobile gets purpose-built stacked / swipe layouts.
- `src/components/` — one component per section (Hero, Philosophy, Experience,
  Coaching, Journey, Gallery, Trust, Location, Booking, Footer, Nav, KineticBand,
  Monogram).

## Booking form

The appointment enquiry form validates the visitor's details and hands the
enquiry to the coach over **WhatsApp** (`wa.me` link, pre-filled with name,
contact, format, time and notes). Nothing is stored on the site. The WhatsApp
number is set in `BUSINESS.whatsapp` in `src/lib/data.ts`. Confirm it is a
WhatsApp-enabled number before launch.

## Verified business details used

- 5.0 / 5 rating · 99 Google reviews (linked to the supplied Maps listing)
- Daily 7 AM – 10 PM · appointments required
- On-site, outdoor and online services · child care & restroom
- Wheelchair-accessible seating & toilet · credit / debit cards
- Phone: +971 56 666 2243

Photography is served from the Pexels CDN (licence-free stock, cinematic
treatment applied in CSS). Swap in the coach's own photography via `IMG` in
`src/lib/data.ts` when available.