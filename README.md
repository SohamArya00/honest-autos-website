# Honest Autos Website

A 7 page static site built from your Stitch export, wired together into one working site.

## Pages
- index.html (Home)
- services.html (Our Services)
- ceramic-coating.html (Ceramic Coating detail)
- pricing.html (Pricing Packages)
- gallery.html (Project Gallery)
- about.html (Our Story)
- book.html (Book Your Service)

All nav links (desktop top nav, mobile bottom nav, and in-page "Learn More" / CTA buttons) now point to the real pages instead of "#".

## Deploying to Cloudflare Pages
1. Push this folder to a GitHub repo (or use Cloudflare's "Direct Upload").
2. In Cloudflare dashboard: Workers & Pages > Create > Pages > connect the repo (or drag-and-drop the folder for direct upload).
3. Build settings: no build command needed, this is plain static HTML. Set the output directory to the repo root (or wherever this folder sits).
4. Deploy. The `_redirects` file gives you clean URLs like `/book` instead of `/book.html`.

## Booking form
The form currently posts to `https://formspree.io/f/YOUR_FORMSPREE_ID`. To make bookings actually land in your inbox:
1. Create a free account at formspree.io and make a new form.
2. Replace `YOUR_FORMSPREE_ID` in `book.html` with the ID they give you.
That's it, no backend server needed, works fine on Cloudflare Pages as a static site.

## About the "NZTA API to find vehicle size" idea
I looked into this before building, and wanted to be upfront rather than build something that won't actually work:

- NZTA (Waka Kotahi) does not offer a free public API where you type in a number plate and get back the vehicle's size or dimensions. Their open data (the Motor Vehicle Register dataset) is a bulk anonymised snapshot for research, not a plate lookup service.
- Real plate to vehicle-details lookups in NZ (make, model, body type, dimensions) come from commercial resellers of NZTA data, e.g. MotorWeb, Checka, Carjam. These require signing up as a paying business customer and agreeing to their terms, they're not something you can just call for free from a public website.
- Even if you got access, most of these products are priced per lookup, which adds an ongoing cost to every booking form submission, including from people who never actually book.

**What I built instead:** a "Vehicle Size" dropdown on the booking form (Small / Medium / Large-SUV / XL-Van-Ute / Not sure) with example models in each option, plus an optional number plate field so your team has it on hand when they call to confirm. This gets you accurate-enough sizing for quoting without any ongoing per-lookup cost, and it's how most detailing and mobile mechanic sites in NZ actually handle this.

If down the track you want automatic plate-to-vehicle lookups (useful once you're doing higher volume), the practical path is:
1. Sign up with MotorWeb or Checka as a business.
2. Add a Cloudflare Pages Function (a small serverless endpoint that lives alongside this site) that calls their API server-side, so your API key never sits in the public HTML/JS.
3. Have that function return size/body-type info back to the booking form to auto-fill the dropdown.

Happy to build that integration once you've picked and signed up with a provider, just send me the API docs they give you.
