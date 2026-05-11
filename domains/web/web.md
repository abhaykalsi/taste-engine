# domains/web/web.md
## Web Design, Information Architecture & Digital Experience
*Load with core/beliefs.md*
*Last updated: 2026-05-10*

---

## The Governing Principle

My web design sensibility is rooted in UI thinking, not print thinking applied to a screen. The metaphors I reach for come from operating systems, native apps, and human interface guidelines — not magazine layouts or poster grids.

Specific lineage: Apple HIG, macOS/iOS surface design, Tailwind spacing logic, Molly Studio, Rauno Fischbacher. I have built an internal component and spacing system around HIG-derived principles. When I make sizing and spacing decisions I am thinking in HIG-derived increments, not arbitrary pixel values.

---

## Information Architecture First

The question before any visual decision: how does someone move through this? What do they need to find? In what order?

A site with good IA and mediocre visuals works. A site with bad IA and beautiful visuals fails. Most portfolio sites that do unusual navigation fail because they prioritize the navigation experience over the content it is supposed to deliver.

**You don't need 20 pages.** A portfolio needs: work, about, contact. An editorial platform needs: home, article, search. Everything else is usually ego. The number of pages is often inversely proportional to the clarity of the IA.

---

## Organisms, Not Pages

The best navigation and disclosure patterns expand from a point of origin. They open like organisms. The menu that becomes three columns. The tooltip that becomes a size picker. The search field that blooms into a discovery surface.

Information reveals itself progressively from a single trigger point. This is fundamentally different from pages — pages require the user to leave where they are to get what they want. Organisms keep the user in place and bring the information to them.

**WePresent navigation:** Two controls — search and menu. Menu opens into three columns: Explore By, Recommended (curated carousel), short About. The discovery is built into the navigation. You understand what the site is and contains without going anywhere.

**Robinhood Market size picker:** Opens as a tooltip/popover from the trigger point, reveals options, closes on selection. One interaction, one disclosure, one decision.

---

## Native-Feeling Interaction

Interactions should feel like they belong to the operating system or the device. Blur, rounded corners, springs, overlays, popovers — patterns that feel like interface, not decoration.

Animation should serve the transition (where did this come from, where is it going) — not call attention to itself.

**Molly Studio** did this best: the site behaves more like a native app than a document. Navigation almost invisible because everything is one level deep. Works open in modal overlays; content within projects is a horizontal carousel. Touch-native patterns that work at any screen size without a separate mobile logic.

---

## Text Constraints

Max-width on text blocks is a reading decision, not a layout decision. Approximately 60–70 characters per line is comfortable for extended reading. Apply this to the content container, not the page — the layout can be full-width while the text is constrained.

Text blocks: approximately 400–500px max-width for body copy. This is the Molly principle — the column is constrained, the page is not.

---

## Sections Have Weight

Different parts of a long-form page should feel different — not through colour changes or graphic interventions, but through container width, spacing, and typographic register. The body is narrower than the hero. The footer is narrower than the body. Width changes are spatial signals about where you are in the document.

**WePresent article:** body column, aside for metadata, full-bleed photography where it earns it, pull-quotes at full width with background colour, footer at narrower container. Each section knows what it is.

---

## The Empty State Is a Design Surface

Search with no query typed. Cart with nothing in it. Page loading. These are states most designers ignore and that immediately reveal whether anyone was paying attention.

**WePresent empty search:** Large light "Search" placeholder centered in near-white space. "Explore the latest" below with a card floating up. Space and invitation, not an empty form.

---

## Interactable vs. Functional — Always Legible

At any moment the user should be able to identify: what can I click, what is content, what is structural. This requires spatial consistency, not colour-coding. If interactive elements always behave like interactive elements and never look like content, the user builds a mental model quickly and the interface disappears.

---

## What I Dislike in Web Design

- Scroll-jacking that doesn't earn its reveal — animation for animation's sake
- Full-width Swiss poster sections used as substitute for editorial thinking
- 20-page nav structures on sites that have 4 things to say
- Product pages that feel like database views — no spatial hierarchy, no sense a human decided what matters
- Interaction patterns that perform personality without solving a navigation problem
- Mobile as afterthought — responsive breakpoints applied to desktop-first layouts
- The "made in Webflow" template look: serif headline, grey body, 80px padding, 2-column case study grid — technically competent, aesthetically anonymous
- Hover states too subtle to notice and too complex to understand
- Typography sized in px not fluid scale — correct on desktop, broken on mobile
