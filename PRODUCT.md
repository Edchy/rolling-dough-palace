# Product

## Register

brand

## Users

People and companies in Sweden planning events, parties, weddings, workshops, or workplace gatherings who need a memorable mobile pizza catering experience.

## Product Purpose

The site presents Pedalling Pizza Palace as a mobile wood-fired pizza catering business and turns visitor interest into booking enquiries. Success means visitors quickly understand what can be booked, where the service is available, and how to get in touch.

## Brand Personality

Bohemian, avant-garde, novel, untraditional. Warm and handmade underneath, but expressed as an artsy statement rather than a catering service. This is not a traditional pizza place; it reads more like a creative studio, a gallery, or an artsy brewery's merch drop (reference: omnipollo.com, ahumanfuture.co, wondermake.xyz). Confident and a little irreverent. Easy to navigate, but never polished into a generic restaurant template or a tidy corporate SaaS layout.

## Anti-references

Avoid overloaded Wix-style navigation, generic beige restaurant templates, stocky corporate catering language, and top-level city links that make the main menu harder to scan.

## Design Principles

- Put booking intent first.
- Keep the primary navigation short enough to scan in one glance.
- Preserve city pages for SEO, but group them under the relevant service.
- Use food and event imagery as the main emotional proof once real assets are available.
- Let the tone feel handmade and direct rather than corporate.

## Information Architecture

The original Wix site sprawled across ~16 pages that mostly repeat one pitch (mobile wood-fired oven, comes to you, three pizzas, made from scratch), with cities duplicated under multiple slugs, three overlapping booking/contact paths, an empty events section, and Wix scaffolding (blank-sida, members, feedback). The redesign collapses this to a small, scannable structure.

**Foodtruck, catering, and företag are the same service** (one mobile wood-fired oven that comes to you and bakes on-site). They were separate, near-duplicate pages on the original site. They collapse into ONE page; the former audiences (public/festival, private parties, company events) plus workshops become use-case sections within it, not separate pages. The page is framed around booking/event intent and lives at `/event`. (The bike-oven "foodtruck" stays the visual brand identity in the logo and hero copy; it is just no longer the page name.)

Pages:
- `/` Home: leads with the foodtruck identity; orients rather than repeating the full pitch.
- `/event` The one service page: the offering plus all use-cases (festival/public, privat fest, företag, workshops) as sections. City pages nest under it for SEO: `/event/stockholm`, `/event/uppsala`, `/event/goteborg`.
- `/om-oss` The story: how it began (2021), the self-built bike-ovens, the cykel identity, and the people behind the vagn. This is where the bohemian, handmade brand voice lives.
- `/kontakt` Contact and booking (merges the old /boka, /bokafoodtruck, /contact paths).

Nav (short): Event, Om oss, Kontakt, plus a "Boka oss" CTA. No "Artiklar" item; no separate Catering/Företag.

Workshops were a real offering on the original site; they live as a section on `/event`, not a separate page, to keep the nav short.

Articles are external press mentions, not a blog. They appear as a card grid section ("omskrivna i" / press), each card linking out to the outlet. Lives on the home page, never as a top-nav page.

Dropped entirely: separate catering/företag pages, the original empty events + event-details Wix pages (the new `/event` service page is a fresh, populated page, not those), blank-sida, members, feedback, and all duplicate city slugs.

Home page sections (foodtruck-led): hero, the concept (core pitch told once), the three pizzas, one bold "what we do" block (trucks photo + single CTA to /event), press card grid, a cities strip, closing booking CTA.

## Accessibility & Inclusion

Aim for WCAG AA contrast, keyboard-accessible navigation, visible focus states, reduced-motion-safe interaction, and clear Swedish labels for the public-facing site.
