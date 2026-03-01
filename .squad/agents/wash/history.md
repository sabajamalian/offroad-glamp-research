# Wash — Frontend Dev History

## Session: March 1, 2025

### Task: Convert business documents to mobile-first HTML

Created two standalone, mobile-friendly HTML documents from markdown sources:
- `competitive-analysis.html` (~72KB, 12 sections)
- `business-plan.html` (~96KB, 13 sections)

### Learnings

**Design Decisions:**
- **Color Palette:** Used earth tones (forest green #2d5016, sage #7a9b76, earth brown #8b7355) to evoke outdoorsy/adventure feel while maintaining professional business document aesthetic
- **Typography:** System font stack for performance; 16px minimum body text on mobile; generous 1.7 line-height for readability
- **Single-file approach:** All CSS inline in `<style>` tag, minimal vanilla JavaScript only for navigation - ensures documents work offline via file:// protocol
- **Reading width:** Max 800px for main content, centered on desktop for optimal line length and reading comfort

**Responsive Approach:**
- **Mobile-first breakpoints:** 375px base → 768px tablet → 1024px desktop
- **Navigation pattern:** Sticky sidebar on desktop (260px width), collapsible hamburger menu on mobile (fixed overlay, 80% viewport width)
- **Table handling:** Wrapped all tables in `.table-wrapper` divs with `overflow-x: auto` to enable horizontal scrolling on mobile without breaking layout
- **Touch targets:** 50px circular buttons for menu toggle and back-to-top; adequate padding on all interactive elements
- **Grid layouts:** Used CSS Grid with `repeat(auto-fit, minmax(280px, 1fr))` for flexible responsive cards (SWOT boxes, phase cards, financial highlights)

**Component Patterns:**
- **Callout boxes:** `.callout` class with left border accent (4px) for highlighting key findings, recommendations, and takeaways
- **SWOT grid:** 2×2 CSS Grid layout with color-coded borders (strengths=green, weaknesses=orange, opportunities=sage, threats=brown)
- **Financial highlights:** Grid of stat boxes with large numbers (1.8rem) for quick scanning
- **Phase cards:** Used for timeline visualization with consistent structure and visual hierarchy
- **Tables:** Alternating row colors, hover states, sticky headers considered but skipped for simplicity
- **Print styles:** `@media print` rules hide navigation, adjust page breaks, ensure clean output

**JavaScript (minimal):**
- Mobile menu toggle (hamburger)
- Back-to-top button with scroll threshold (300px)
- Active section highlighting in TOC based on scroll position
- Smooth scrolling via CSS `scroll-behavior: smooth`
- All vanilla JS, no frameworks, ~50 lines total

**Performance & Accessibility:**
- Zero external dependencies (no CDN calls)
- System fonts load instantly
- Semantic HTML5 structure (`<nav>`, `<main>`, `<section>`, `<header>`)
- ARIA labels on icon buttons
- Color contrast meets WCAG AA standards
- Focus states preserved for keyboard navigation

**Content Structure:**
- Maintained all markdown content without summarizing
- Converted lists, tables, code blocks, and emphasis appropriately
- Preserved document hierarchy with proper heading levels (h1→h6)
- Added visual formatting for specific data types (pricing tables, financial projections, timelines)

**File Sizes:**
- `competitive-analysis.html`: 72KB (from 27KB markdown)
- `business-plan.html`: 96KB (from 59KB markdown)
- Size increase due to inline CSS (~8KB) + complete HTML structure + enhanced formatting

**Browser Compatibility:**
- CSS Grid, Flexbox (IE11+ but targeting modern browsers)
- System fonts work across macOS, Windows, Linux, iOS, Android
- Tested file:// protocol compatibility (no server required)

**Future Enhancements Considered But Skipped:**
- Table of contents auto-generation from headings (kept manual for control)
- Search functionality (adds significant JS, not needed for ~100KB documents)
- Dark mode (not requested, would add CSS complexity)
- Collapsible sections (unnecessary for document reading flow)
- External stylesheet (requirement was inline CSS)
- Progressive web app features (overkill for static documents)

**Key Takeaway:** Mobile-first means designing for 375px width FIRST, then progressively enhancing. Not desktop-first with mobile afterthoughts. The sticky sidebar becoming a hamburger menu, tables becoming horizontally scrollable, and the two-column SWOT grid becoming single-column on mobile are all examples of this approach working correctly.
