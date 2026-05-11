# taste-engine
## Patch 03 — Web Design: What Good Digital Work Feels Like
### Session 2026-05-10

---

## The Governing Principle: UI as Design Language

My web design sensibility is rooted in UI thinking, not print thinking applied to a screen. This is not a rejection of editorial design — WePresent is proof that editorial thinking translates beautifully to digital — but it means the metaphors I reach for when designing a website come from operating systems, native apps, and human interface guidelines rather than from magazine layouts or poster grids.

The specific lineage I work within and am influenced by: Apple HIG, macOS/iOS surface design, the Tailwind design system (spacing logic, sizing increments), and the emergent product design aesthetic of studios like Molly and engineers like Rauno Fischbacher. This is a world of blur, rounded corners, restrained drop shadows, surfaces that feel like they have material weight without being skeuomorphic. Depth without decoration.

I have built an internal component and spacing system around these principles. When I make sizing and spacing decisions, I am thinking in HIG-derived increments, not arbitrary pixel values.

---

## Molly Studio (now Shopify internal)

One of my primary references for how a studio website can think about itself. Molly has been acquired by Shopify (August 2025) and now functions as an internal design team, which is a loss for the public reference pool.

**What they got right:**

The entire site operates through a single-page modal/carousel system. There are no pages in the traditional sense. Work opens in a modal overlay; content within each project is a native-feeling horizontal carousel. This is not a gimmick — it is a considered architectural decision. The site behaves more like a native app than a document. Navigation is almost invisible because it doesn't need to exist: everything is reachable from one place, one level deep.

Text blocks are constrained to approximately 400–500px max-width. This is a reading-width decision, not a layout decision. On any screen size, the text remains comfortable to read because the constraint is on the content, not the container. This is the correct approach and it's surprising how rarely designers apply it — they think about the column, not the line length.

The modal system means the site works identically across device sizes without a separate mobile logic. The carousel is already a touch-native pattern. The overlay is already a spatial metaphor that works at any scale. Good mobile web design is not responsive layout — it is device-agnostic information architecture.

**The design register:** Low cognitive load. Every element is immediately identifiable — this is content, this is navigation, this is an action. Blur, rounded corners, tasteful drop shadows, surfaces that feel like they have physical material. This is the antithesis of a tech startup website. Tech startup websites perform complexity. Molly performed clarity.

**The UI-editorial tension:** There is a category of studio website that tries to be a design object — full-bleed images, scroll-jacking, aggressive typography. Molly refused that. The website understood that its job was to get you to the work, not to be the work. This restraint is harder than it looks.

---

## WePresent (by WeTransfer) — Molly's Project

The best example I have of editorial design done correctly for a digital context, without falling into the trap of making everything a full-width Swiss poster.

**Navigation as organism:** The nav has two controls — search and menu. When menu opens, it expands into a three-column structure: Explore By (site sections), Recommended (a curated article carousel with image), and a short About paragraph. It functions like an organism opening — it reveals depth that was latent, not depth that was hidden. The discovery is built into the navigation itself. You don't need to go anywhere to understand what the site is and what it contains. This is navigation designed around content discovery, not around site structure.

**The reading experience:** Body text at a comfortable column width, aside for metadata (date, author, share/bookmark), clean heading hierarchy, full-bleed photography where the image earns it. Pull-quotes animate on scroll — large-scale serif type on a tinted background section, full width. This is not a gimmick; it is the digital equivalent of a magazine pull-quote that breaks the column grid to give the reader a breath and an anchor.

**What it avoids:** It does not make every section a poster. The structure breathes — sections have weight, wider containers give space, the footer is a narrower container that signals closure. The typographic register shifts appropriately between contexts: display at headline, editorial serif at body, small utility sans at metadata. Three registers, all consistent, none fighting each other.

**The search state:** Empty search field centered on a near-white page with "Search" as a very large, very light placeholder. Below it, "Explore the latest" with a card floating up. This is the kind of decision that requires someone to ask: what does the user feel when they open search and have typed nothing yet? The answer here is: space and invitation, not an empty form.

**The insight:** A lot of things on a website are self-understood. You do not need 20 pages. A site like this works because it trusts that users understand what a navigation, a search, an article, a card, and a footer are. It does not over-explain its own structure. The design gets out of the way of the content.

---

## Robinhood Market — E-commerce as UI System

Robinhood Market (the Robinhood financial brand's merch/product store, not the trading app) is a product page designed like a presentation deck — and it works.

**The layout:** Vertical thumbnail carousel on the right edge of the viewport — all products, small, rounded, with a rounded pill indicator marking the currently active product. Center viewport: the product image, large, with space around it — treated like a keynote slide. Left side: product name, price, quantity selector, add-to-bag CTA — persistent, doesn't move, is always the action panel. The nav centroid is just the wordmark and a category label. Nothing else.

**Interaction logic:** Every interactive element is immediately identifiable. The distinction between "this is functional" and "this is content" is never ambiguous. The size selector opens as a tooltip/popover — it expands like an organism from the trigger point, reveals size options as pill buttons, greyed-out for unavailable sizes. One interaction, one disclosure, one decision. Then it closes.

The details panel at the bottom opens like an accordion with clipping mask animation — only one section can be open at a time, and the opening feels physical, like a fold. This is the correct restraint for a product details section: the information is available but it doesn't compete with the product image for attention.

**The insight:** When you strip an e-commerce product page to its minimum viable information surface — image, name, price, CTA, specs — and give each element its correct spatial weight, the result feels like design. Most e-commerce product pages feel like spreadsheets formatted by a committee. This one feels like someone sat down and thought: what do you actually need to decide to buy something?

---

## Rauno Fischbacher — rauno.me

A personal portfolio site by a developer/designer (former Vercel, now at a16z-backed companies). The site is navigated horizontally. Each project is a "frame" — the visual metaphor is explicitly Figma-like, the projects displayed as canvas frames rather than as list items or grid cells. There is a minimap at the top of the viewport — a tiny abstracted representation of the full horizontal canvas, with a viewport indicator showing where you are. Parallax of oversized text as you scroll: the project title is large enough that it extends beyond the frame, and it moves at a different speed from the frame container, so you can read the full title even when the frame is cropped.

**Why it works:** It earns its cleverness. The Figma-frame metaphor is not arbitrary — Rauno is a developer who thinks in design tools, and his portfolio is structured the way he thinks. The minimap is functional, not decorative — it tells you how much content there is and where you are in it. The parallax is functional — it makes cropped text readable. Every unusual interaction decision is solving a real problem, not performing personality.

**The contrast with bad interaction design:** Most portfolio sites that do unusual navigation (scroll-jacking, custom cursors, elaborate entrances) are performing the interaction at the expense of the content. You remember the animation, not the work. Rauno's site is memorable because the interaction logic is inseparable from the content logic. You navigate it the way you'd navigate a Figma file because the content is structured like a Figma file.

---

## Principles Distilled — Web Design

**1. Information architecture first, visual design second.**
The question before any visual decision: how does someone move through this? What do they need to find? In what order? A site with good IA and mediocre visuals works. A site with bad IA and beautiful visuals fails.

**2. Native-feeling interaction over performed animation.**
Interactions should feel like they belong to the operating system or the device. Blur, rounded corners, springs, overlays, popovers — these are patterns that feel like interface, not decoration. Animation should serve the transition (where did this come from, where is it going) not call attention to itself.

**3. Organisms, not pages.**
The best navigation and disclosure patterns expand from a point of origin — they open like organisms. The menu that becomes three columns. The tooltip that becomes a size picker. The search field that blooms into a discovery surface. Information reveals itself progressively from a single trigger point. This is fundamentally different from pages, which require the user to leave where they are to get what they want.

**4. Constrain the text, not the layout.**
Max-width on text blocks is a reading decision. Approximately 60–70 characters per line is comfortable for extended reading. Apply this to the content, not to the page — the layout can be full-width while the text is constrained. This is the difference between a page that reads well and one that forces you to track across the full viewport.

**5. Sections have weight.**
Different parts of a long-form page should feel different — not through color changes or graphic interventions, but through container width, spacing, and typographic register. The body is narrower than the hero. The footer is narrower than the body. These width changes are not decoration; they are spatial signals about where you are in the document.

**6. You don't need 20 pages.**
A website that trusts its users understands that most navigation categories are self-evident. A portfolio needs: work, about, contact. An editorial platform needs: home, article view, search. Everything else is probably ego. The number of pages a site has is often inversely proportional to the clarity of its IA.

**7. The empty state is a design surface.**
Search with no query typed. Cart with nothing in it. A page loading. These are states that most designers ignore and that immediately reveal whether anyone was paying attention. WePresent's empty search state — large light "Search" placeholder, space, invitation — is a design decision. Most empty states are an afterthought.

**8. Interactable vs. functional — always legible.**
At any moment, the user should be able to identify what they can click, what is content, and what is structural. This doesn't require colour-coding or obvious button shapes — it requires spatial consistency. If interactive elements always behave like interactive elements and never look like content, the user builds a mental model quickly and the interface disappears.

---

## What I Dislike in Web Design

- Scroll-jacking that doesn't earn its reveal — animation for animation's sake
- Full-width Swiss poster sections used as a substitute for editorial thinking
- 20-page nav structures on sites that have 4 things to say
- Product pages that feel like database views — no spatial hierarchy, no sense that a human decided what matters
- Interaction patterns that perform personality ("look how we scroll!") without solving a navigation problem
- Mobile as an afterthought — responsive breakpoints applied to a desktop-first layout rather than IA decisions that work at any size
- Hover states that are too subtle to notice and too complex to understand
- Typography that looks correct on desktop and collapses on mobile because it was sized in px not in a fluid scale
- The "made in Webflow" template look — everything flush left, serif headline, grey body, 80px padding everywhere, case studies in a 2-column grid — technically competent, aesthetically anonymous

---

*Patch 03 of ongoing TASTE.md — continue in subsequent sessions and consolidate.*
