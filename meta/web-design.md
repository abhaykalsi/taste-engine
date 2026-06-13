# meta/web-design.md
## Designing Websites
*Load with core/beliefs.md + domains/web/web.md + domains/motion/motion.md*
*Last updated: 2026-05-10*

---

## Voice

Design for how things feel to use, not how they look in a screenshot. A site that photographs well and navigates badly has failed. A site that navigates perfectly and looks considered is almost always good enough.

---

## The Sequence

Start in this order. Skipping steps makes the subsequent steps useless.

**1. What is this site for?** One sentence. Not a mission statement — a function. "Show work to potential clients." "Let people buy coffee subscriptions." "Publish essays." If you can't write the function in one sentence, you don't understand what you're building yet.

**2. What does someone need to find?** Map the actual content, not the page structure. Content first. Structure is a consequence of the content, not something you design around it.

**3. How many pages does this actually need?** Usually fewer than you think. Portfolio: work, about, contact. Editorial: home, article, search. Most other things: one or two. Every additional page is a navigation decision the user has to make. Don't make them make decisions you can make for them.

**4. What is the reading/use order?** On every page: what do they see first, what do they need next, what do they do when they're done? Design that sequence before you design anything visual.

**5. Now: typographic hierarchy.** Scale, weight, spacing. Get this right before you add any colour, imagery, or motion. If the hierarchy doesn't work in black and white, it doesn't work.

**6. Layout and spatial logic.** Sections with different weights. Column constraints. Container width as spatial signal.

**7. Motion and interaction.** Last. Motion that is designed before the spatial structure is animation for animation's sake.

---

## Navigation

Navigation is an organism, not a page. The ideal: it expands from a single point, reveals the shape of the site without requiring the user to travel anywhere, and disappears when not needed.

**Two controls is usually enough.** Search and menu. If you need more than two persistent navigation controls, the IA is probably wrong.

**What the menu should reveal:** What is on this site. Where I am. How to get somewhere else. Not: a list of pages, a brand statement, decorative imagery.

**Depth kills navigation.** One level of navigation deep is almost always sufficient. Two levels is sometimes necessary. Three levels means the content hasn't been organized — it's been filed.

---

## Sections

Every section of a long-form page should know what it is. The signals that tell you where you are in a document: container width, spacing scale, typographic register. Not colour blocking, not graphic dividers.

**The section logic:**
- Hero: full-width container, large type, minimal text, high-contrast
- Body: constrained container (60–70 characters per line), comfortable spacing, readable type
- Aside / metadata: offset or narrower, secondary typographic register
- Full-bleed: earned for images or quotes that justify the interruption
- Footer: narrower than body, smallest typographic register, high information density

**What sections should not do:** Announce themselves with a thick coloured background and a centered oversized heading. That is presentation design applied to a document. A section should feel like a different part of the same thing — not a different thing.

---

## Type on the Web

Fluid scale over fixed sizes. px values that are correct on desktop and broken on mobile are not correct — they are incomplete.

Body copy: ~400–500px max-width container. Not because columns are always this width, but because reading is. The layout can be full-width; the text column should be human-scaled.

**Line height:** 1.5–1.65 for body. 1.1–1.2 for display. Tighter than that at large sizes makes stacked descenders and ascenders compete. Looser than that in body creates floating lines with no visual relationship to each other.

**Never set type smaller than 15px for any content the user is expected to read.** Small type is not sophisticated. It is inaccessible by another name.

**The heading-to-body spacing error:** If the gap between a heading and its body paragraph is wider than the gap between that heading and the content above it, the heading is floating. It belongs to the content below it. The spatial proximity should signal that relationship.

---

## Layout Logic

The grid is a constraint system, not a decoration. The grid's job is to make layout decisions consistent and to free cognitive load for the decisions that actually require judgment.

**Build the grid from the content, not the other way.** What are the actual content units? How wide should each be for its purpose? What is the relationship between them? That is your grid.

**Something should be slightly unexpected.** Not arbitrary — not predictable either. If every element sits exactly where the grid suggests, the grid is doing all the work and the designer is absent. Mild tension: the logic is legible, the result is not obvious.

**White space has weight.** The empty areas of a layout are as designed as the content. If you are not deciding what the empty areas look like, someone else is — usually the default. That is a decision abdicated, not made.

---

## Motion

Motion should answer two questions: where did this come from, and where is it going?

If it doesn't answer either, cut it.

**For navigation and disclosure:** animate during the gesture where possible. The user is exploring — let the interface explore with them. Waiting until gesture end before showing anything feels broken.

**For page load and state changes:** stagger sibling elements with slight timing offsets. Not all at once. Elements that arrive simultaneously read as a flat switch. Elements that arrive with slight offsets read as three-dimensional.

**Duration:** Almost everything is too slow. 150–250ms for micro-interactions. 250–400ms for larger transitions. Anything over 400ms requires a reason.

**Spring physics over easing curves.** Springs are interruptible. Easing curves are not. An interface that can be interrupted mid-animation is communicating: I am responding to you. An interface that finishes its animation before responding is not.

---

## Interactivity

At any moment the user should be able to identify: what can I click, what is content, what is structural. This requires spatial and behavioral consistency — not color coding.

**Hover states:** visible enough to catch the eye, not so complex they distract from the content. If a hover state is the most interesting thing on the page, something is wrong.

**Focus states:** do not remove them. Override them with something considered if you must, but a page with no visible focus states is inaccessible.

**Touch targets:** 44px minimum. Not because it looks right — because it works for hands that are not cursors.

---

## What Makes a Website Bad

The common failure modes, in order of frequency:

**No hierarchy.** Everything is the same size, the same weight, the same spacing. The eye has no anchor. The user has no reading order.

**IA designed for the client, not the user.** Navigation structured around the company org chart. Sections named after internal departments. Pages that exist because someone wanted them, not because someone needs them.

**Motion that performs personality.** Elaborate scroll animations, cursor followers, staggered text that plays on every scroll. The first time: interesting. The fifth time: friction. Motion that calls attention to itself is motion that is failing at its job.

**Mobile as afterthought.** Responsive breakpoints bolted onto a desktop layout. The result: either the mobile layout is clearly a shrunken desktop, or it breaks in specific places because the assumptions baked into the desktop layout don't survive scaling.

**The Webflow template look.** Serif headline at 80px. Grey body at 18px. 80px vertical padding between sections. Two-column case study grid. This aesthetic is not wrong — it has been repeated into invisibility. Technically competent, aesthetically anonymous.

**Empty states ignored.** The search field with no query. The cart with nothing in it. The loading state. These are where most designers stop caring. They are surfaces. Design them.

---

## The Final Check

Before anything goes to production:

Read the site aloud, in order, as a user would experience it. Does the reading sequence make sense? Does the hierarchy hold?

Resize to 375px wide. Does the layout survive? Is anything broken, inaccessible, or awkward?

Turn off images and colour. Does the typographic hierarchy still function?

Interact with every interactive element. Does every hover, focus, and active state behave correctly?

Ask the point of view test: who made this, and does the work know it? If the answer is "could be anyone" — start over.
