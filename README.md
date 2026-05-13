# Olympic Paints — Staff Portal

The front door for internal staff tools. Single landing page that links out to walkthroughs, dashboards, forms, and other resources as they come online.

**Live site:** https://flomaticauto.github.io/olympic-paints-staff-portal/

## What's on it (v1)

- **Odoo Walkthroughs** — step-by-step guides for Sales Order, Customer Collection, Vehicle Scheduling. Links to the [walkthroughs site](https://flomaticauto.github.io/olympic-paints-odoo-walkthroughs/).
- Placeholder tiles for Forms & Requests and Contacts & Help — to be filled in as those tools are built.

## Design

- **Light theme by default** — readable on cheap warehouse monitors, sunny offices, and direct-sun phone screens. Dark / Navy / Brand themes are available via the top-right toggle; selection persists per device.
- **Mobile-first** — tiles reflow to a single column on phones, with large finger-friendly touch targets.
- **Olympic Paints design system** — Barlow Condensed (display) + Barlow (body), official Clickpaint logo, navy / yellow / teal palette. No frameworks — vanilla HTML/CSS/JS.

## Adding a new tile

In `index.html`, copy any existing tile block and update:

```html
<a class="portal-tile" href="https://your-tool-url" target="_blank" rel="noopener">
  <div class="portal-tile-icon">🎨</div>
  <h2>Tile Title</h2>
  <p>Short, friendly description in plain English.</p>
  <span class="portal-tile-cta">Open Tool</span>
</a>
```

For a "coming soon" placeholder, replace the `<a>` with `<div class="portal-tile coming-soon" aria-hidden="true">` and use `Coming Soon` as the CTA text — the dashed border styling kicks in automatically.

## Structure

```
olympic-paints-staff-portal/
├── index.html              # the landing page
├── assets/
│   ├── logo.jpg            # official Clickpaint digital badge
│   └── oly-theme.css       # shared 4-theme token system
└── README.md
```

## Deployment

Pushed to `main` → published automatically via GitHub Pages from the repo root. There is no build step.

## License

Internal Olympic Paints property.
