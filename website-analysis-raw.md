# Website Development Options for the Off-Road + Rooftop Tent Experience

## 1. Build-From-Scratch Analysis
### Recommended Tech Stack
- **Frontend:** Next.js or Remix with React, TypeScript, Tailwind CSS, and a component kit (e.g., Radix + Framer Motion) for highly branded storytelling pages.
- **Backend:** Node.js (NestJS) or a lightweight serverless API (AWS Lambda / Vercel Functions) to handle booking logic, waivers, and integrations with Stripe/Square.
- **CMS + Content:** Headless CMS such as Sanity or Contentful so non-technical teammates can update itineraries, packing lists, and blog content without redeploying code.
- **Infrastructure:** Vercel or Netlify for hosting + CI/CD, Cloudflare for caching/edge rules, AWS S3 for media assets, and a managed database (Supabase/Postgres) for bookings/waitlists.

### Cost & Timeline Estimates (CAD)
| Approach | Upfront Build | Timeline | Notes |
| --- | --- | --- | --- |
| DIY (owner builds with templates/components) | $300–$1,000 (domain, premium components, SaaS) | 4–8 weeks of part-time effort | Lowest cash cost but highest learning curve and maintenance burden. |
| Freelance developer | $1,500–$5,000 for brochure site; $5,000–$8,000 if booking flows/custom API needed | 2–6 weeks for a small site; 6–10 weeks if custom booking integrations are included | Rates of $30–$75/hr are common in Canada for independent devs/designers.[SpaceO](https://www.spaceo.ca/blog/website-development-cost/) |
| Boutique agency | $5,000–$20,000+ depending on depth of UX, branding, and complex integrations | 6–12+ weeks due to discovery, design, development, QA | Agencies charge $100–$175/hr and bring specialists (UX, brand, SEO) at higher cost.[DigitalWebPort](https://digitalwebport.com/best-web-design-companies-toronto-vs-freelance-designers-cost-comparison/) |

### Pros
- Full control over performance, custom booking flows, custom React components to showcase off-road shots, and unique brand storytelling.
- Own your stack (no vendor lock-in, data stays in your DB) and avoid escalating SaaS fees once volume grows.
- Easier to integrate novel experiences later (e.g., telemetry dashboards, route planners, custom waiver flows).

### Cons
- Requires upfront capital or significant founder time. Build + maintenance + DevOps will compete with running trips.
- You must manage security patches, dependency upgrades, uptime, and analytics instrumentation.
- Booking, CRM, and marketing tooling must be integrated manually (vs. turn-key tools on Squarespace/Wix).

### When It Makes Sense
- You have validated demand, need advanced workflows (dynamic pricing, real-time fleet availability, complex upsells), or plan to raise capital and scale beyond a regional operator.
- You want a premium brand experience (immersive storytelling, hero video, 3D route map) that standard templates cannot deliver.
- You have in-house technical talent or a long-term agency partner budgeted for maintenance.

---

## 2. Off-the-Shelf Platform Comparison
### Snapshot
| Platform | Monthly Cost (CAD, annual billing) | Booking Options | Payments | Mobile/SEO | Ease of Updates |
| --- | --- | --- | --- | --- | --- |
| **Squarespace** | $30.95 Business / $45 Basic Commerce | Native Acuity Scheduling ($20–$61 CAD/mo) for real-time booking, group slots, reminders.[Forbes Advisor CA](https://www.forbes.com/advisor/ca/business/software/squarespace-pricing/) | Stripe, PayPal via Acuity; taxes + deposits configurable.[Squarespace Support](https://support.squarespace.com/hc/en-us/articles/360034944391-Acuity-Scheduling-pricing-billing-and-invoices) | Responsive templates, built-in SEO metadata controls, OpenGraph settings. | Visual editor, sections, and campaign tools make changes simple for non-devs. |
| **WordPress.org + Plugins** | Hosting $3–$35+; premium booking plugins $59–$249 USD/year | WooCommerce Bookings, Travel Tour Booking, WP Travel Engine for capacity, tiered pricing, deposits.[WooCommerce](https://woocommerce.com/products/travel-tour-booking/) | Depends on gateway (Stripe, Square, PayPal). Full control over payment mix. | SEO powerhouse (Yoast/RankMath), mobile responsive themes for adventure tourism.[WordPress Themes](https://wordpress.org/themes/adventure-tourism/) | Requires maintenance (updates/backups). Page builders (Elementor, Gutenberg) simplify editing once set up. |
| **Wix** | Core $29.77 / Business $39.77 CAD with Wix Bookings included.[Wix Pricing](https://www.wix.com/plans) | Built-in Wix Bookings handles classes, group trips, deposits, staff calendars.[Wix Bookings](https://www.wix.com/website/templates/html/travel-tourism/travel-services) | Wix Payments, Stripe, PayPal; POS add-ons. | Strong mobile editor, SEO Wiz for structured data. | Drag-and-drop editor, AI text assistant, app market add-ons. |
| **Shopify** | Basic $49 CAD/mo ($37 CAD if annual).[Shopify Pricing](https://www.shopify.com/ca/pricing) | Booking apps such as Experiences ($9–$129/mo + %), BookThatApp, Sesami for tours with reminders & POS.[Shopify App Store](https://apps.shopify.com/experiences) | Shopify Payments (2.8% + $0.30 online, 2.6% POS) or 3rd-party (extra 2%).[AVADA](https://avada.io/blog/shopify-pricing-canada/) | Mobile-first themes, robust SEO settings, fast CDN. | Familiar admin, easy product/experience duplication, but booking UX relies on app. |
| **Webflow** | CMS $23 USD/mo; Ecommerce Standard $29 USD/mo (annual).[Webflow Pricing](https://webflow.com/pricing) | Requires embed/integration with booking tools (Calendly, Acuity, Checkfront). No native booking. | Stripe for ecommerce; 2% fee on Standard until upgrading to Plus ($74 USD/mo) for 0% fee.[Tech.co](https://tech.co/website-builders/webflow-pricing) | Pixel-perfect control, fast hosting, CMS for itineraries/blog, clean SEO controls. | Designer has a learning curve; Editor mode makes copy updates easy once built. |

### Platform Deep Dives
- **Squarespace:** Fluid Engine layouts + tourism templates showcase rigs, itineraries, and testimonials fast. Acuity Scheduling (free to $61 CAD/mo) plugs in for group bookings, intake forms, and automated reminders with Stripe/PayPal payments.[Squarespace Support](https://support.squarespace.com/hc/en-us/articles/360034944391-Acuity-Scheduling-pricing-billing-and-invoices) Upgrading to Commerce removes the 3% transaction fee on Business plans.
- **WordPress + Plugins:** Pair managed hosting (SiteGround promo $2.99 CAD/mo, renews $17.99; WP Engine $34 CAD/mo steady)[SiteGround](https://www.siteground.com/wordpress-hosting.htm)[WP Engine](https://wpengine.com/ca/plans/) with adventure tourism themes (Adventure Tourism, Adventure Tour) that already include galleries, FAQs, and CTA blocks.[WordPress Themes](https://wordpress.org/themes/adventure-tourism/) WooCommerce Bookings ($249 USD/yr), Travel Tour Booking ($59 USD/yr), or WpTravelly ($69 USD/yr) add per-person pricing, deposits, and automated emails.[WooCommerce](https://woocommerce.com/products/travel-tour-booking/)[MagePeople](https://mage-people.com/product/woocommerce-tour-and-travel-booking-manager-pro/)
- **Wix:** Core/Business plans ($29.77–$39.77 CAD/mo) include Wix Bookings for capacity caps, deposits, staff calendars, SMS reminders, and membership packs.[Wix Pricing](https://www.wix.com/plans) Huge template marketplace (Adventure Tour Company, Outdoor Rentals) lets you personalize quickly.[Wix Templates](https://www.wix.com/website/templates/html/travel-tourism/travel-services)
- **Shopify:** Choose Basic ($49 CAD/mo) and add a booking app (Experiences $9–$129/mo + % or BookThatApp). These apps pump bookings into Shopify orders, support POS check-in, SMS/email reminders, Zapier workflows, and calendar sync.[Shopify App Store](https://apps.shopify.com/experiences) Shopify Payments fees apply (2.8% + $0.30 CAD online; 2.6% POS; +2% if you use PayPal externally).[AVADA](https://avada.io/blog/shopify-pricing-canada/)
- **Webflow:** CMS ($23 USD/mo) or Ecommerce ($29–$74 USD/mo) plans give total design control, CMS collections for itineraries/blogs, and fast AWS hosting.[Webflow Pricing](https://webflow.com/pricing) There’s no native booking, so embed Checkfront, FareHarbor, Calendly, or Acuity via HTML/CMS, or connect to Zapier/Make for automation.

### Integrated vs. Standalone Booking Approaches
- **Integrated (Squarespace + Acuity, Wix Bookings, Shopify apps, WordPress plugins):** Best when you want everything under one login. Ideal for one-to-two tour offerings because pricing is predictable and setup is wizard-driven. Limitation: if you later need OTA distribution, multi-day manifesting, or wholesale partners, these tools cap out quickly.
- **Standalone (Checkfront, FareHarbor, Peek Pro, Bookeo, Rezdy):** Purpose-built for tours/activities with robust manifests, reseller networks, reseller accounts, waivers, and channel management. They embed into any site and connect to POS/payment processors. Costs are higher (monthly fee or booking commission), but they future-proof scaling.

## 3. Booking System Analysis
| System | Pricing Model | Features for Off-Road Tours | Integrations & Fit |
| --- | --- | --- | --- |
| **Checkfront** | $149/month + 3% online booking fee (pass to guest or absorb). No setup/OTA fees.[Checkfront](https://www.checkfront.com/pricing/) | Custom packages, automated waivers, dynamic availability, multi-day inventory, flexible payments, Apple/Google Pay support. Strong automation keeps waivers + reminders tight. | Embeds on any site, Zapier/Make, deep WordPress plugin, partner APIs. Great long-term option if you outgrow Acuity/Wix because data portability is solid. |
| **FareHarbor** | No subscription; up to ~6% booking fee (usually passed to customer) + ~1.9% + $0.30 processing fee absorbed by operator.[Bokun](https://www.bokun.io/fareharbor-pricing) | Extensive OTA distribution, resource management, guide scheduling, waivers, multilingual checkouts. | Works via embeddable widgets + hosted checkout. Ideal when you want marketing reach and don’t mind visible service fees to guests. |
| **Peek Pro** | 6–8% per booking + ~2.3% + $0.30 card fee; negotiable but opaque.[Peek](https://www.bokun.io/peek-pro-pricing) | Slick mobile UI, resource calendars, upsells, Zapier, text reminders, tipping, kiosk mode. | Embeds into any site + branded checkout links. Good if aesthetics + upsells matter, but fees are among the highest. |
| **Bookeo (Tours & Activities)** | Flat $39.95 / $79.95 / $119.95 USD per month tiers, 30-day trial, optional waivers add-on from $9/mo.[Bookeo](https://www.bookeo.com/tours/pricing/) | Up to 60 guides/vehicles, 3,000 bookings/mo, vouchers, packages, recurring trips, SMS reminders. | Embed widgets, integrates with WordPress, Squarespace (code block), Shopify (app), Zapier. Predictable cost for small operators. |
| **Rezdy** | $49 / $99 / $249 USD per month + 3% booking fee + $1-$0.70 offline booking fee.[Rezdy](https://rezdy.com/pricing/) | Channel manager to 40k+ resellers, packages/extras, API/webhooks, advanced reporting, waivers, manifesting. | Embeds anywhere, syncs with Google Things To Do, OTAs, and payment gateways. Strong choice for scaling + B2B wholesale. |

**Feature Gaps to Watch:** Checkfront + Rezdy handle multi-day trips and multi-vehicle inventory best. FareHarbor/Peek help with OTA sales but add customer-visible fees. Bookeo is cost-effective but lighter on automation + reseller channels.

## 4. Payment Processing & Booking Policy Considerations
| Processor | Standard Canadian Fees | Why/H when to use | Deposit vs Full Payment | Cancellation & Refund Handling |
| --- | --- | --- | --- | --- |
| **Stripe** | 2.9% + $0.30 CAD online; +0.8% for international cards; 2.7% + $0.05 in-person; 0.5% extra for keyed transactions.[Stripe](https://stripe.com/en-ca/pricing) | Pairs with Squarespace/Acuity, WordPress, Shopify apps, Checkfront, Rezdy. Offers Payment Links, subscriptions, BNPL, and Tap to Pay. | Acuity, WooCommerce, and Checkfront let you capture deposits (e.g., 30%) and auto-charge balances via Stripe. | Dashboard supports partial refunds, automated cancellation emails, and dispute workflows (CA$15 fee if customer files a chargeback). |
| **Square** | 2.5% tap/chip credit, 0.75% + $0.07 Interac debit, 2.8% + $0.30 online, 3.3% + $0.15 keyed, +1.5% for international cards.[Square](https://squareup.com/ca/en/payments/our-fees) | Strong if you want Square POS for merch or on-site add-ons; integrates with Wix (native), Squarespace (via Acuity), and WordPress through plugins. | Square Online Checkout + Square Appointments support deposits or pay-in-full toggles. | Offers instant refunds to cards, cancellation automation through Square Appointments, and easy export for GST/HST accounting. |
| **PayPal** | 2.9% + $0.30 CAD domestic commercial; +0.8% (US) or +1% (other countries) cross-border; 3–4% FX spread.[PayPal](https://www.paypalobjects.com/marketing/ua/pdf/CA/en/ca-en-merchant-fees-15-oct-2024.pdf) | Needed if your audience prefers PayPal or buys from overseas; embeds on Squarespace, Shopify, WordPress, Wix. | PayPal buttons can request deposits but management is clunkier vs. Stripe/Square. | Partial refunds cost nothing; instant bank withdrawals cost 1.75%. Make sure cancellation windows are spelled out to avoid disputes. |

**Policy Tips:**
- Use deposits (25–50%) to secure bookings while keeping flexibility for weather; capture balances 7 days before departure via Stripe/Square automation.
- Publish cancellation tiers (e.g., full refund >14 days, 50% refund 7–13 days, no refund <7 days) and sync them with booking software so refunds trigger automatically.
- Automate reminder + prep emails (what to pack, meeting point GPS, waiver link) 48 hours in advance.

## 5. Essential Website Features for This Business
1. **Hero media + gallery** – High-resolution shots of Toyota rigs, rooftop tents, night skies, recovery gear, and happy guests to build trust.
2. **Availability calendar + booking CTA** – Show open weekends/months with live inventory embedded above the fold; allow group selection up to five seats.
3. **Experience breakdowns** – Detail itinerary, driving difficulty, camp amenities, menu, what’s included / optional add-ons, and min/max skill level.
4. **Safety & prep section** – Gear checklist, licensing requirements, waivers, insurance coverage, weather considerations, and guide credentials.
5. **Testimonials & social proof** – Embed Google/TripAdvisor reviews, Instagram reels, and UGC featuring the vehicles.
6. **FAQ + policies** – Answer top concerns (bathrooms, weather cancellations, dietary needs, alcohol, wildlife) and list cancellation/deposit rules.
7. **Blog / field notes** – Publish trip recaps, trail spotlights, maintenance tips, and seasonal planning to drive SEO for “off-road tours Vancouver,” etc.
8. **Contact + inquiry form** – Offer WhatsApp/text CTA for quick questions plus email form with dropdown for private group requests.
9. **Mobile-first UX** – Optimize for social traffic (Instagram, TikTok) with sticky book button and quick-dial link.

## 6. Cost Comparison Table (CAD unless noted)
Assumptions: Prices use annual billing when available and USD amounts converted at 1 USD ≈ 1.35 CAD for comparison. Payment processing fees are per-transaction (variable) but noted for awareness.

| Option | Year 1 Fixed Cost | Year 2+ Fixed Cost | Booking Stack | Payment Fees | Owner Time | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| **Custom DIY (Next.js + headless)** | ~$600 (domain, Vercel pro, headless CMS seats, design assets) + sweat equity | ~$600 | Stripe or Square via custom integration | Stripe 2.9% + $0.30 | 120–160 hrs build + maintenance | Highest control, but opportunity cost is high while business is pre-launch. |
| **Custom via Freelancer** | $3,000–$8,000 upfront + ~$600 hosting/tooling | $600–$1,200 maintenance retainers | Same as above | Stripe/Square negotiated | 20–30 hrs for approvals/content | Pay once for bespoke UX; budget for ongoing bug fixes + updates.[SpaceO](https://www.spaceo.ca/blog/website-development-cost/) |
| **Custom via Agency** | $10,000–$25,000+ including strategy + content + QA | $2,000–$5,000/yr support | Enterprise booking (Checkfront/Rezdy) layered on | Stripe/Square enterprise rates | 30–50 hrs stakeholder time | Best for funded phase or national expansion.[DigitalWebPort](https://digitalwebport.com/best-web-design-companies-toronto-vs-freelance-designers-cost-comparison/) |
| **Squarespace Business + Acuity Growing** | $30.95×12 + ~$36×12 ≈ **$804** | Same | Acuity Scheduling | Stripe/PayPal 2.9% + $0.30 | 20–30 hrs setup & copy | Fastest to market, includes email + analytics. Transaction fee 3% on Business unless you upgrade to Commerce plan. |
| **Squarespace Commerce Basic + Acuity Growing** | ($45×12) + ($36×12) ≈ **$972** | Same | Acuity Scheduling | Stripe/PayPal | 20–30 hrs | Removes 3% transaction fee, worth it once bookings ramp. |
| **WordPress (SiteGround year 1) + WooCommerce Bookings** | Hosting promo ($2.99×12 ≈ $36) + plugin $249 USD (~$336 CAD) + premium theme ~$100 CAD ⇒ **~$472** | Renewal hosting $216 + plugin renewal $336 + theme renewals (~$100) ⇒ **~$652** | WooCommerce Bookings / Travel Tour Booking | Stripe/Square/PayPal | 40–60 hrs setup + plugin tuning | Low cash but higher time. Switch to WP Engine ($34/mo) for better uptime once traffic grows.[SiteGround](https://www.siteground.com/wordpress-hosting.htm)[WooCommerce](https://woocommerce.com/products/travel-tour-booking/) |
| **Wix Business** | $39.77×12 ≈ **$477** | Same | Wix Bookings (included) | Wix Payments / Stripe 2.9% + $0.30 | 15–20 hrs | No hidden booking fees; app market add-ons optional.[Wix Pricing](https://www.wix.com/plans) |
| **Shopify Basic + Experiences app** | $49×12 = **$588** + Experiences Premium $39×12 ≈ $468 + rev share (0.75%–1%) | Same | Experiences / BookThatApp / Sesami | Shopify Payments 2.8% + $0.30 (+2% if external gateway) | 25–35 hrs | Factor extra % fee on every booking. Strong path if you also sell merch. |
| **Webflow CMS + Checkfront** | ($23 USD×12 ≈ $372 CAD) + Checkfront ($149×12 = $1,788) + 3% booking fee | Same | Checkfront embedded | Stripe/Square via Checkfront | 40–60 hrs (designer + setup) | Premium look + enterprise-grade booking. Fees higher but scalable. |
| **Bookeo + existing site** | Bookeo Standard $39.95 USD/mo (~$54 CAD) ⇒ **$648** | Same | Bookeo embed | Stripe/Square/PayPal | 10–15 hrs to embed | Predictable SaaS; pair with Squarespace/Wix if you need more automation than native booking. |
| **Rezdy + existing site** | $49 USD/mo (~$66 CAD) + 3% fee + offline per-booking fee | Same | Rezdy embed | Stripe/Square etc. | 20–30 hrs to configure | Adds OTA distribution + reseller network when you’re ready for scale. |

*Time cost is estimated owner effort for copy, media, and QA; it excludes photography/video shoots.*

## 7. Recommendation & Phased Approach
**Recommendation:** Launch on **Squarespace Commerce Basic + Acuity Growing** now, then graduate to **WordPress or Webflow + Checkfront/Rezdy** once demand and partnerships justify higher investment.

### Why Squarespace + Acuity first?
- Fastest build: you can repurpose brand photography, drop in itinerary blocks, and enable bookings without code.
- Canadian-friendly payments via Stripe/PayPal with CAD pricing and tax collection.
- Acuity handles up to five guests per outing, automated reminders, waiver/intake forms, coupon codes, packages, and deposits—all critical for weather-dependent tours.
- Built-in email campaigns + blog + analytics keep marketing simple while you validate pricing and operations.

### Phase Plan
1. **Phase 0 (Week 1–2)** – Gather assets, finalize itinerary copy, choose Squarespace template, configure Commerce Basic plan, hook up Stripe + PayPal, and embed Acuity offerings (public + private group). Publish essential pages (Home, Trips, About/Guides, Safety, FAQ, Blog intro, Contact). Enable Google Analytics + Search Console.
2. **Phase 1 (Month 1–2)** – Add blog posts (trail spotlights), publish a packing checklist download, integrate social proof (Google reviews, Instagram feed), and launch paid ads / partnerships. Use Acuity packages for multi-day trips and enable 30% deposits with balance auto-charge.
3. **Phase 2 (Month 3–6)** – Introduce Bookeo or Checkfront if you need richer manifests, reseller logins, or OTA distribution. Embed the widget on Squarespace or build a lightweight WordPress landing hub while keeping Squarespace live for content.
4. **Phase 3 (Year 2)** – Once bookings exceed ~400/year or you expand to multi-vehicle fleets, migrate to a custom WordPress or Webflow build backed by Checkfront/Rezdy. Use headless CMS content migration tools or Webflow’s CSV importer to bring over itineraries/blog posts. Keep Acuity as a waitlist/consultation scheduler even after adopting a dedicated booking engine.

### Migration Path Considerations
- Maintain all copy + assets in a shared CMS (Notion, headless) so moving platforms is mostly a front-end rebuild.
- Choose a booking system (Checkfront or Rezdy) that offers embed codes + API; you can swap website platforms without touching customer history.
- Continue using Stripe or Square across platforms to avoid re-onboarding and to keep historical payout data intact.
- When moving to WordPress/Webflow, start with a subdomain pilot (e.g., beta.offroadglamp.ca) to ensure SEO + tracking survive cutover.

### When to Reconsider
- If you plan to wholesale through OTAs quickly (e.g., TripAdvisor, GetYourGuide), consider going straight to WordPress/Webflow + Rezdy/Checkfront so you don’t rebuild twice.
- If merchandise/gear becomes a major revenue stream, Shopify + Experiences might be better despite stacking app fees because its inventory + POS story is strongest.

With this path you get a branded, mobile-first, SEO-friendly site live in weeks, validate packages/pricing, and retain the option to graduate to a more complex stack once revenue supports it.
