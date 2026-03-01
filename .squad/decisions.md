# Team Decisions

> Canonical record of all team decisions. Merged from `.squad/decisions/inbox/` by Scribe.

---

## Zoe — Competitive Findings (Vancouver BC Off‑Road / Adventure)

### Key Findings
- **Direct competitor pricing bands:** Day‑tour off‑road experiences cluster at **$199–$339 per rider/buggy** with premium private day trips at **$800 per group**; overland rentals run **$175–$305/day** and **$225/night** for equipped Jeep rentals.
- **Direct competitor set (Vancouver/Sea‑to‑Sky):** Vancouver Outdoor Adventures, Canadian Wilderness Adventures, Squamish Adventure, Maple Overland, FarOut Wilderness, Western Red Adventures (Vancouver Island).
- **Market size anchor:** Vancouver overnight visitors **~10.95M (2023)** and **~11.27M (2024)** with **C$8.4B–C$9.6B** annual visitor spend; BC adventure tourism revenue **~C$10.7B** (2023).
- **Seasonality:** Peak spring‑to‑fall operations (e.g., rafting runs **April–September**).
- **Channel insights:** Heavy reliance on **TripAdvisor/Viator/GetYourGuide** listings; strong social media presence (Instagram/Facebook/TikTok); tourism‑board partnerships.
- **Strategic gap/opportunity:** No clear **guided overnight off‑road + camping** product near Vancouver; current options are day‑only tours or self‑drive rentals, leaving a gap for a turnkey overnight experience with transport + camp setup.

---

## Inara — Marketing Strategy

**Date:** 2026-03-01  
**Topic:** Launch Marketing Strategy

### Decisions Made
1. **Visual-First Approach:** Instagram and TikTok prioritized over text-heavy platforms. The "product" is the visual envy of the experience.
2. **Local SEO Priority:** Focus on long-tail keywords ("off road camping Vancouver") to compete with larger generic tour operators.
3. **Influencer Barter Model:** Trade experiences for content/distribution rather than cash payments to influencers during launch phase.
4. **Google Business Profile as MVP:** Critical "MVP" for appearing in local search maps before complex website SEO strategy.

### Rationale
- Customers "shop with their eyes" for adventure experiences
- Organic social and barter partnerships have high effort but low cash cost, suitable for startup phase
- Reviews and UGC are primary trust signals for adventure activities (safety concerns)

---

## Kaylee — Website Platform Recommendation

**Date:** 2026-03-01  
**Topic:** Platform Selection & Migration Strategy

### Decision
- **Immediate build:** Launch on Squarespace Commerce Basic with Acuity Growing to get booking-ready pages, CAD payments, and automated reminders live within weeks.
- **Booking roadmap:** Stay on Acuity until manifests/OTAs become complex, then embed Checkfront (preferred) or Rezdy for deeper automation while keeping the front end intact.
- **Migration trigger:** When annual bookings exceed ~400 or wholesale partners require channel management, migrate content to WordPress/Webflow backed by Checkfront/Rezdy without changing Stripe/Square processors.

---

## Mal — Strategic Synthesis & Positioning

**Author:** Mal (Lead / Strategist)  
**Date:** 2026-03-01  

### Decision: Market Positioning
**Choice:** Position as a premium guided adventure experience, not a budget tour or rental.  
**Rationale:** White space exists between day-trip ATV tours and self-drive overlanding rentals. Premium positioning justifies higher pricing and avoids competing on cost with established ATV operators.

### Decision: Pricing at $399/person
**Choice:** $399/person for 2-day/1-night experience; $1,595 for private group (up to 5).  
**Rationale:** Sits above day tours ($199–$339) and above rental rates ($175–$305/night). Justifies premium through all-inclusive guided experience. Group rate incentivizes full-capacity bookings. 30% deposit at booking with balance auto-charged 7 days before departure.

### Decision: Squarespace + Acuity for Launch Platform
**Choice:** Squarespace Commerce Basic ($45/mo) + Acuity Scheduling Growing ($36/mo) for launch.  
**Rationale:** ~$972/year vs. $3,000–$8,000+ for custom build. Gets live in 2 weeks. Handles group bookings, deposits, waivers, reminders. Migrate to Checkfront/Rezdy + WordPress/Webflow only at 400+ bookings/year or when OTA distribution needed.

### Decision: Top 3 Launch Channels
**Choice:** Instagram Reels (organic), Google Business Profile, micro-influencer seeding.  
**Rationale:** Product is inherently visual — Instagram is the storefront. GBP is free trust + local SEO. Influencer barter trips cost only fuel + food but generate social proof and audience reach. SEO and paid ads layer on in months 2–3.

### Decision: Phased Growth Strategy
**Choice:** Three-phase roadmap — Foundation (months 1–3), Growth (months 3–6), Scale (months 6–12).  
**Rationale:** Launch lean with one itinerary and one vehicle. Add second itinerary and hotel partnerships in Phase 2. Add second vehicle and hire guide only when turning away 5+ bookings/month.

### Decision: Regulatory Compliance is Pre-Launch Blocker
**Choice:** BC commercial recreation tenure and ICBC commercial vehicle insurance must be secured before accepting paid bookings.  
**Rationale:** Operating on Crown land without tenure can result in fines and shutdown. Carrying paying passengers without commercial insurance is illegal and creates catastrophic liability exposure.

---

## Book — Document Structure & Format

**Decision Maker:** Book (Business Writer)  
**Date:** 2026-03-01  
**Context:** Creating final deliverables (Competitive Analysis + Business Plan) for off-road glamping venture

### Competitive Analysis (`competitive-analysis.md`)
**11 chapters, 27,000 words**

1. Executive Summary
2. Market Overview (Vancouver/BC tourism data)
3. Direct Competitors (detailed profiles with tables)
4. Indirect Competitors (adjacent experiences)
5. Competitive Positioning Map (text-based price vs. experience matrix)
6. Customer Acquisition Channels Analysis
7. Pricing Landscape (with recommended strategy)
8. SWOT Analysis
9. Gaps & Opportunities (market white space)
10. Competitive Advantages
11. Key Takeaways & Recommendations

### Business Plan (`business-plan.md`)
**12 chapters, 59,000 words**

1. Executive Summary (business concept, market, financials)
2. Company Overview (mission, vision, legal structure)
3. The Experience (detailed trip description)
4. Market Analysis (target customers, market size)
5. Competitive Analysis (summary with reference to full doc)
6. Marketing Strategy (multi-channel with budget allocation)
7. Website & Technology (build vs. buy, phased approach)
8. Operations Plan (vehicles, gear, permits, insurance, workflow)
9. Financial Projections (3 scenarios, break-even analysis)
10. Risk Analysis (10 key risks with mitigation)
11. Implementation Timeline (3 phases with milestones)
12. Appendices (references, assumptions, metrics)

### Rationale
- **Executive-friendly:** Each document starts with standalone summary for quick decision-making
- **Action-oriented:** Every major section ends with recommendations or "suggested path"
- **Data-driven:** Used real competitor data, actual pricing, verified market statistics
- **Comprehensive but scannable:** Tables, bullet points, bold key numbers for easy navigation
- **Phased implementation:** Timeline broken into manageable chunks with clear triggers
- **Risk-balanced:** SWOT and risk analysis provide realistic view, not just optimism
