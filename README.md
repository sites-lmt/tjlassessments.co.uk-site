# TJL Assessments — static site

tjlassessments.co.uk rebuilt as a static HTML/CSS/JS site, deployed on GitHub Pages.

**This site has no affiliation with TJL Contractors.** No links, references or shared
branding — verified by the link audit (see below).

**Brand:** slate periwinkle `#66669B`, sampled from the TJL monogram.
**Type:** Lora (headings) + Source Sans 3 (body).

The identity is deliberately different from the other sites in this workspace. The
logo is a high-contrast serif, so the site is set in serif throughout and kept
restrained — small corner radii, hairline rules, a cream ground and no gradient
panels. It should read as letterhead, not as a marketing site.

## Structure

- `index.html` — homepage
- `css/style.css` — the whole design system; every colour is a token in `:root`
- `js/site.js` — nav toggle, FAQ accordion, scroll reveal, footer year
- `images/tjla-monogram.png` — the logo (transparent background)

## Pages

`/` · `/about/` · `/contact/` · `/faq/` · `/free-consultation/` · `/self-assessment/` ·
`/privacy-policy/` · `/terms-conditions/` · `/cookie-policy/`

Slugs are preserved from the WordPress site. The old plugin paths
(`/wpautoterms/privacy-policy/`, `/wpautoterms/terms-and-conditions/`) and the
leftover `/welcome-to-cloudways/` placeholder now redirect to their equivalents.

## Content corrections made in this build

Three problems on the previous site were fixed rather than carried over:

1. **A live FAQ answer was placeholder text.** "What are the required documents
   required to file my tax return?" read *"I am item content. Click edit button to
   change this text. Lorem ipsum dolor sit amet…"*. Replaced with a real list of the
   documents needed.
2. **The About page linked to `tjlcontractors.co.uk`.** A direct cross-link to the
   other company, which contradicts the no-affiliation requirement. Removed.
3. **The promotion had expired.** The site advertised "£125 until end of August"
   against a standard fee of £185. Presenting an expired promotion is misleading, so
   the site now states the standard £185 flat fee throughout. **If the promotion is
   still running, the fee appears in `index.html`, the template, `_body/about.html`,
   `_body/free.html` and `_body/selfassessment.html` — tell me and I will reinstate it
   with a current date.**

## Conventions

- Pages one level deep use `../` prefixes for assets and links.
- The pages were generated from a template; the generator lives in
  `~/Desktop/Repo/tmp/tjla/` (`template.html`, `build.ps1`, `body/`). Re-run `build.ps1`
  after editing anything in `body/`.
- The header is cream and the footer is white. The logo has a transparent background,
  so it needs no special treatment on either.

## Still to confirm with the client

- **Whether the £125 promotion is still running.** See above.
- **The email address is on `iflmanagement.co.uk`**, not this domain. If the site is
  meant to look fully independent, a `@tjlassessments.co.uk` address would read better.
- **No company registration or VAT number anywhere.** An accountancy service normally
  shows these; the £185 fee is quoted "including VAT", which implies VAT registration.
- **Google Fonts** load from Google's CDN, so visitor IPs reach Google. Self-hosting the
  fonts would remove that; the privacy policy currently discloses it honestly.
- **No analytics.** If any is added, the cookie policy must change and a consent
  banner becomes necessary — the current policy states there are no cookies.
