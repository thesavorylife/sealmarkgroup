# Sealmark Group Inc — Website

Production-ready static site for **Sealmark Group Inc**, New York corporation. Built for Netlify deployment with Stripe Checkout integration.

## Structure

```
sealmark/
├── index.html                       # Home (with Mission & Vision)
├── services.html                    # Four service cards
├── about.html                       # About / story / credentials
├── contact.html                     # Contact info + Netlify form
├── blog.html                        # Blog index (6 posts)
├── post-what-is-a-notary.html       # Blog: Notary Basics
├── post-spousal-poa.html            # Blog: Spousal POA in NY
├── post-mobile-vs-ron.html          # Blog: Mobile vs. RON
├── post-nassau-closing.html         # Blog: Nassau County Closings
├── post-apostille-guide.html        # Blog: NY Apostille Guide
├── post-5-documents-homeowners.html # Blog: 5 Homeowner Docs
├── terms.html                       # Terms of Service (Stripe-compliant)
├── privacy.html                     # Privacy Policy (Stripe-compliant)
├── refund.html                      # Refund Policy + No-Sign Contingency
├── css/styles.css                   # Brand stylesheet
├── js/main.js                       # Nav toggle, scroll reveals
├── assets/favicon.svg               # Octagonal S favicon
├── sitemap.xml                      # For Google Search Console
├── robots.txt                       # Crawler directives + sitemap link
└── netlify.toml                     # Security headers + deploy config
```

## Brand System

- **Palette:** Navy `#1B3A5C` · Brass `#B08D57` · Ivory `#F6F1E7`
- **Typography:** IM Fell English (display) · Playfair Display (sub) · Montserrat (body/UI)
- **Motif:** Octagonal "S" seal brand mark throughout

## Deployment

1. Push folder to a GitHub repo named `sealmark`.
2. Connect to Netlify: New site from Git, choose the repo.
3. Build settings: leave blank (no build step). Publish directory: `.`
4. Add custom domain (e.g., `sealmarkgroup.com` or `sealmarknotary.com`).
5. Netlify auto-provisions SSL, required for Stripe.

## Live-Ready Status

All placeholders have been filled in:

| Item | Status |
|---|---|
| Calendly link (`calendly.com/taniasavory2026/sealmarkgroup`) | Live |
| Phone `(516) 631-0081` | Live |
| Email `info@sealmarkgroup.com` | Live |
| Mailing address (Freeport, NY 11520) | Live |

Update the mailing address only if it changes.

## Stripe Compliance Checklist

- ✅ Business name (Sealmark Group Inc) on every page
- ✅ Services described clearly
- ✅ Contact email + phone displayed
- ✅ Terms of Service published
- ✅ Privacy Policy published (Stripe disclosed as processor in §4)
- ✅ Refund Policy published (with No-Sign Contingency)
- ✅ HTTPS via Netlify

## Legal Entity Language

All three legal pages reference **Sealmark Group Inc, a New York corporation**. No DBA language.

## Getting Indexed by Google

After the site is live on its final domain:

1. Go to Google Search Console (search.google.com/search-console) and add your domain as a property.
2. Verify ownership (Netlify makes this easy with a DNS TXT record).
3. Submit your sitemap: enter `sitemap.xml` in the Sitemaps section.
4. Google will begin crawling and indexing all 14 URLs.

**Important:** `sitemap.xml`, `robots.txt`, and the canonical tags in each blog post all use `https://sealmarkgroup.com`. If your final live domain is different, do a find-and-replace on that string across these files before submitting to Search Console.

## Adding Your YouTube Intro Video

The homepage has a "Meet Sealmark Group" section with one video slot for your intro video. To add it:

1. Upload the video to YouTube.
2. On the video page, copy the ID from the URL. Example: in `youtube.com/watch?v=ABC123xyz`, the ID is `ABC123xyz`.
3. In `index.html`, find `VIDEO_ID_1` and replace it with your real video ID.
4. Update the caption text below the video (or delete the caption line if you don't want one).

To add more videos later, copy the `<div class="video-card">` block, paste it inside `<div class="video-grid single">`, give the new one a different ID, and remove the word `single` from `video-grid single` so they sit side by side.

## Services Note

Active services: Mobile Notary, Loan Signings, Field Inspections, General Notary Work.
Coming soon (clearly labeled on the site): Remote Online Notarization and Apostille. When you are authorized for these, remove the `soon` class and the `badge-soon` line from those two cards, and change the footer links to drop "(soon)".

## Form Handling

Contact form on `contact.html` uses Netlify Forms:
1. Auto-detected via `data-netlify="true"`.
2. Submissions appear in Netlify Dashboard, Forms tab.
3. Configure email notifications in Netlify: Forms, Settings.

## Blog

Currently 6 static blog posts. To add more:
1. Copy an existing `post-*.html` file
2. Update the `<title>`, `<meta description>`, hero eyebrow, heading, and content
3. Add a new card in `blog.html` (in the `.blog-grid` section)

For a CMS-driven blog (self-serve publishing), Netlify CMS can be added later. Say the word.
