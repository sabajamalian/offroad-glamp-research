# Decision: HTML Design System for Business Documents

**Date:** March 1, 2025  
**Decision Maker:** Wash (Frontend Dev)  
**Status:** Implemented  

## Context

Need to convert two business strategy documents (competitive analysis and business plan) from Markdown to standalone HTML files that work offline and look professional on all devices.

## Decision

Implement a single-file, mobile-first HTML design system with the following characteristics:

### Design System Choices

1. **Color Palette: "Outdoorsy Professional"**
   - Forest Green (#2d5016) - primary brand color
   - Sage (#7a9b76) - secondary/accent
   - Earth Brown (#8b7355) - tertiary
   - Warm Gray (#4a4a4a) - body text
   - Cream (#faf8f3) - page background
   - Accent Orange (#d97941) - highlights/callouts
   
   **Rationale:** Evokes nature, adventure, and outdoor recreation (the business domain) while maintaining professionalism for a business document. Colors are muted enough for extended reading, not garish.

2. **Typography: System Font Stack**
   ```css
   font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
   ```
   - 16px minimum body text (mobile)
   - 1.7 line-height for comfortable reading
   - Generous heading sizes with clear hierarchy
   
   **Rationale:** System fonts load instantly (no web font download), look native on each platform, excellent readability. Line-height of 1.7 is optimal for extended reading of business prose.

3. **Layout: Sidebar + Main Content**
   - Desktop: Sticky sidebar TOC (260px) + main content (max 800px)
   - Mobile: Fixed overlay hamburger menu + full-width content
   
   **Rationale:** Sidebar navigation is standard for long documents on desktop. Mobile overlay preserves screen real estate while maintaining navigation access.

4. **Responsive Strategy: Mobile-First**
   - Base styles for 375px (mobile)
   - Enhancements at 768px (tablet)
   - Enhancements at 1024px (desktop)
   
   **Rationale:** Forces consideration of constraints first, then enhancement. Ensures mobile experience is first-class, not an afterthought.

5. **Table Handling: Horizontal Scroll**
   - All tables wrapped in `.table-wrapper` with `overflow-x: auto`
   - Tables maintain minimum width (600px) for structure
   - Mobile users swipe horizontally
   
   **Rationale:** Alternatives (hiding columns, stacking rows) destroy data relationships. Horizontal scroll preserves table integrity while fitting mobile viewports.

6. **Single-File Architecture: Inline CSS + Minimal JS**
   - All CSS in `<style>` tag (~8KB)
   - Vanilla JavaScript only (~50 lines) for navigation
   - No external dependencies
   
   **Rationale:** Documents must work via file:// protocol (double-click to open). No network requests, no build process, no frameworks. Pure HTML works everywhere.

### Component Design Patterns

1. **Callout Boxes** - colored left border + background tint for highlighting
2. **SWOT Grid** - 2×2 grid (desktop) → 1-column (mobile), color-coded by quadrant
3. **Financial Highlights** - stat boxes with large numbers for scanning
4. **Phase Cards** - timeline visualization with consistent structure
5. **Tables** - striped rows, hover states, header row styling

### Rejected Alternatives

- **Custom Web Fonts:** Adds 100KB+ download, delays render, unnecessary for business doc
- **CSS Framework (Bootstrap/Tailwind):** Bloats file size, requires external CSS or massive inline bloat
- **React/Vue Components:** Requires build process, defeats single-file requirement
- **Dark Mode:** Not requested, adds significant CSS complexity
- **Collapsible Sections:** Long documents benefit from being fully visible for Ctrl+F
- **External Stylesheets:** Breaks file:// protocol offline requirement

## Consequences

### Positive

- Documents work offline indefinitely (no external dependencies)
- Load instantly (no network requests, fonts are instant)
- Print perfectly (custom @media print styles)
- Mobile-friendly without compromises
- Clean, professional aesthetic appropriate for business context
- Easy to maintain (edit HTML directly, no build step)
- Accessible (semantic HTML, good contrast, keyboard navigation)

### Negative

- CSS duplication across files (~8KB per file) - not DRY
- Manual updates required (no templating/build system)
- Limited interactivity (no frameworks means manual DOM manipulation)
- File size larger than plain markdown (but still tiny: <100KB each)

### Neutral

- Single-file approach means content and presentation are coupled (acceptable for static docs)
- Visual design locked in (can't swap themes without editing inline styles)

## Implementation Notes

- Competitive Analysis: 72KB HTML (from 27KB markdown)
- Business Plan: 96KB HTML (from 59KB markdown)
- Both include identical CSS and JavaScript structure for consistency
- Print styles ensure clean PDF export
- All tables, lists, headings, and emphasis from markdown preserved

## Success Criteria

✅ Works on mobile (375px+), tablet (768px+), desktop (1024px+)  
✅ No external dependencies (works offline)  
✅ Professional appearance (appropriate for business use)  
✅ All content from markdown preserved  
✅ Tables handle mobile without breaking layout  
✅ Prints cleanly (page breaks, hidden nav)  
✅ Accessible (semantic HTML, ARIA labels, good contrast)  

## Related Documents

- `/competitive-analysis.html` - Implementation
- `/business-plan.html` - Implementation
- `/.squad/agents/wash/history.md` - Technical details

---

**Next Steps:** None. Design system complete and implemented. Future documents can reuse this CSS/structure with minimal modifications.
