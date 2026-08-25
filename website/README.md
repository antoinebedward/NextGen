# Fallingbrook Health and Wellness — Website

Static, framework-free source for the Fallingbrook Health and Wellness site
(Acupuncture, Cosmetic Acupuncture, and Registered Massage Therapy — Orléans,
ON). Plain HTML/CSS/JS, no build step required.

## Structure

```
website/
  index.html      Home
  services.html   Services & pricing
  about.html      About the practitioner
  policies.html   Cancellation / booking policies
  contact.html    Contact info + booking form
  css/style.css   Shared stylesheet (palette, layout, components)
  js/main.js      Mobile nav toggle, active-nav highlighting, footer year,
                  contact form validation
  assets/images/  Site images
```

Each page is self-contained (its own `<head>`, header, and footer) so the
site can be opened directly from disk or hosted on any static file host
(GitHub Pages, Netlify, etc.) with no server-side includes or build tooling.

## Content status — placeholders to fill in

This was rebuilt from the practitioner's own account of the business plus
publicly available details, since the live pages weren't directly
accessible while generating this code. Search the files for `TODO` comments
and replace before publishing:

- Exact street address (unit/number), phone number, and email
- Hours of operation
- Real service prices and durations on `services.html`
- Real social media links
- Practitioner photo (`assets/images/placeholder-practitioner.svg` is a
  placeholder — swap in a real image)
- Exact wording for the late-arrival and insurance/receipt policies on
  `policies.html`
- Wire up `contact.html`'s form to an actual backend/email service
  (e.g. Formspree, Netlify Forms) — it currently only validates client-side

Verified facts already reflected in the copy: in-home clinic on Princess
Louise Drive, Orléans, ON; services are Registered Acupuncture, Cosmetic
Acupuncture, Registered Massage Therapy, Cupping, Tui Na, Moxibustion, and
Gua Sha; practitioner holds a Massage Therapy diploma from Centennial
College and Acupuncture diplomas from the Shiatsu School of Canada and the
SSC Acupuncture Institute, with 16+ years in health care; cancellations
within 24 hours are billed 25% of the service price (patient responsibility,
not billable to insurance).

## Local preview

No build step — open `index.html` in a browser, or serve the folder:

```
cd website
python3 -m http.server 8000
```
