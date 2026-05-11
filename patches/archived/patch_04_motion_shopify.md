# taste-engine
## Patch 04 — Motion, Interaction Philosophy, Novelty & the Shopify Design Orbit
### Session 2026-05-10

---

## The Intellectual Lineage I'm Operating In

This patch documents a cluster of thinkers and practitioners whose writing and work I have absorbed deeply and whose ideas have either confirmed, sharpened, or given language to things I already believed. These are not casual references — they are load-bearing influences on how I think about interaction, motion, and digital experience.

**Rauno Fischbacher** (previously Vercel, now in the a16z/Shopify orbit) — writes and builds at the intersection of engineering and interaction design. His blog (rauno.me) is the reference implementation of what a considered, minimal, high-craft personal site looks like. His essays on invisible interaction details, depth in UI, novelty, and contrasting aesthetics have given me vocabulary for things I was already feeling. He thinks about the *why* behind interactions rather than just pattern-matching to what exists.

**The Shopify Design team** (Carl Rivera, Kazden Ca, Marvin Schwaibold, and others from the Molly acquisition) — are doing the most interesting work in product design at scale right now. Their public writing (design.shopify.com) is a window into a design culture that takes craft, opinion, and pace equally seriously. Their "Design in Public" series is the closest thing to a design manifesto I've encountered from a product organization.

The connection between these: Molly was acquired by Shopify, and Rauno is adjacent to this ecosystem. The aesthetic and intellectual values are continuous — HIG-derived UI sensibility, editorial restraint, interaction design grounded in physics and metaphor, and a bias toward building over theorizing.

---

## On Interaction Design: Physics, Metaphor, and Invisible Details

*(Synthesized from Rauno's "Invisible Details of Interaction Design" and "Designing Depth")*

The best interaction design is invisible precisely because it has done enough thinking to disappear. It is modeled on the physics and metaphors of the real world — gestures that retain momentum, layers that respond to being swiped like physical objects, animations that are interruptible because real things are interruptible.

**Metaphors as the foundation of learnability.** When iOS teaches you to swipe up to unlock, it is teaching you a spatial metaphor: the interface is composed of stacked layers, each dismissable by sliding in the direction it came from. You only have to learn this once. Every subsequent surface that obeys this metaphor is learned for free. This is why the consistency of a platform's interaction model is not an aesthetic choice — it is a cognitive one. Every exception to a metaphor costs the user effort.

**Kinetic physics as trust.** When you dismiss an app and it morphs into the Dynamic Island retaining the angle and momentum of the throw, the interface is communicating: I am responding to *you*, not running a canned animation. The app goes where you threw it, not where the animation decided. This builds trust that the interface is an extension of your body, not a thing you are operating. The distinction matters. Products that feel like extensions of yourself are used differently from products that feel like tools you control.

**The question of when to trigger.** A gesture-triggered action can fire during the gesture or on gesture end — and the correct answer is not universal, it depends on the reversibility and weight of the action. Lightweight, exploratory actions (revealing an overlay, peeking at a screen) should respond during the gesture — waiting for the gesture to end introduces friction before the user has decided anything. Destructive or committed actions (dismissing an app, deleting content) should wait for gesture end — you need to be sure the user meant it. This distinction is almost never discussed explicitly in design documentation, but it is felt immediately by users.

**Choreography as narrative.** Motion has a sequencing problem: when multiple things need to move, in what order do they move? The answer is almost never "all at once." The iOS search gesture is a masterclass in this — the home screen blurs first to lower it on the z-axis before Siri suggestions appear, because if they appeared simultaneously the layering would be visually incoherent. The search input transitions before the keyboard expands, because the keyboard would compete visually with the suggestions. Each step clears the stage for the next. This is choreography: time and delay used narratively, not decoratively.

**Staggering as dimension.** When sibling elements animate with slight timing offsets, they read as three-dimensional — they appear to occupy different positions in depth rather than being a flat grid that appears all at once. The iOS unlock animation staggers app icons. The iOS Control Centre staggered spring configurations give each row independent physics. OpenAI's grid content fade-in uses staggering to make new content feel like it is arriving, not switching on. Staggering is not decoration — it is a spatial signal.

**Fidgetability.** Some interactions are worth designing not because they are functional but because they are satisfying to repeat. The AirPods case. The Apple Pencil tip. These are not accidents. A digital equivalent is an interaction that rewards repeated use with a feeling that the system is responsive and alive. This is related to the concept of *game feel* — the sense that the interface is communicating back to you with every gesture.

---

## On Novelty: The 10% Rule

*(Synthesized from Rauno's "Novelty")*

Novelty in UI is an exclamation mark. It works only in contrast to familiarity. The three-color rule in cinematography (60% primary, 30% secondary, 10% accent) is the right mental model: the 10% is what lifts the subject. Used more, it becomes noise. Used less, it disappears.

**The practical rule:** Make 90% of the experience familiar, 10% novel. The familiar is what allows users to build a mental model quickly. The novel is what makes the experience memorable and specific.

**Novelty and frequency are in tension.** The more often an interaction is performed, the less appropriate any extravagant treatment of it is. Onboarding is a valid moment for maximum novelty — you experience it once, it creates a first impression, and it is appropriate to dial the visual language up. The same animation applied on every login becomes semantic satiation: the brain stops registering it and it starts to feel like lag.

The correct implementation: a first-login animation that fires once (Rauno cites Devouring Details as a good example — the animation is gated by a cookie and only plays on first login). Paco Coursey's personal site does the same — the stagger plays on first load, not on every return. The novelty is preserved because it is rare.

**Stripe Press as a model.** Stripe Press is a deliberately more experimental site than the rest of Stripe's properties. The novelty hits hard because most of Stripe's pages are not like this. The contrast is the mechanism. If everything were Stripe Press, nothing would be Stripe Press.

**Novelty tax.** Arc (The Browser Company) is the canonical failure case. A saxophone that was hard to convert into a piano. Every novel interaction pattern a product introduces is a tax on the user — they have to learn it before it becomes useful. The amount of novelty you can extract from your users depends on whether they are seeking novelty in the first place. Designers and tech enthusiasts are novelty-seeking. Most people are not.

**The takeaway:** Design most things so that they disappear. Design a few things so that they are unforgettable. Know which is which before you start.

---

## On Depth: Dirtying the Frame

*(Synthesized from Rauno's "Designing Depth")*

Composition in 2D is always solving a 3D problem — how do you suggest space, depth, and layering in a flat medium? The film technique of "dirtying the frame" (foreground elements that partially occlude the subject) is the visual equivalent of the designer's question: what else is in this space?

In software design, depth can be introduced through:

**Blur as z-axis.** Blurring the background layer when an overlay appears is not just about visual hierarchy — it is a spatial signal that the background has moved further away. The interface is communicating: that layer is now behind this one. Without the blur, both layers read as coplanar and the modal feels arbitrary. This is why iOS blurs the home screen when a context menu appears. It is telling you that the home screen is now underneath.

**Layered composition in marketing visuals.** Rauno's example from Vercel: a flat marketing visual becomes a layered one by blurring the inner background (pushing it back on the z-axis) and adding additional offset browser frames and out-of-focus objects in the periphery. The objects are not arbitrary decoration — they are the primary subject (browser frames, deployments) appearing in abundance, which is itself the message.

**Stacked surfaces as UI language.** Cards, sheets, popovers, tooltips — these are all spatial metaphors for layers. When they animate from a point of origin, spring to rest, and can be dismissed by swiping them back to where they came from, they behave like physical objects in the interface's spatial model. When they just appear and disappear, they are database rows.

---

## On Contrasting Aesthetics

*(Synthesized from Rauno's "Contrasting Aesthetics")*

This is aligned with the position I already hold (see Patch 01 on "minimalism as philosophy not aesthetic") but Rauno articulates the mechanism with more precision.

**The mechanism of contrast.** In a set of identical elements, nothing stands out. The introduction of one different element — different in color, form, rotation, style — creates the question: *why is this different, and what does that mean?* The question is not an annoyance; it is an invitation to pay attention. This is the fundamental operation of visual communication: controlling what the eye asks next.

**PP Foundry / NeueBit as the canonical example.** The bitmap typeface marketing site uses Renaissance painting (Leonardo's Annunciation) as its primary image. The contrast is doubled: the time period (pre-digital Renaissance vs. bitmap/computer aesthetic) and the expected typographic register (you expect a serif with ornamentation alongside Renaissance imagery; you get a bitmap font). The dissonance creates curiosity and then resolution — once you understand the conceptual link, the contrast feels inevitable. This is the feeling design should aim for: inevitable once you understand it.

**The music parallel.** Loïc Nottet's *Mélodrame* — an orchestral ballad that introduces drum machine beats at 1:55. The moment is special precisely because everything before it established a clear register, and the introduction of the beat violates that register in a way that feels like revelation rather than error. The ballad earns the beat. This is the design lesson: contrast works only against an established baseline. You cannot have contrast without commitment to what you are contrasting against.

**Things are good when they are about themselves.** A principle from a friend of mine that keeps returning: authentic materials always outperform simulated ones. Thick cotton paper will always feel more premium than leather-textured paper, because leather-textured paper is pretending to be something it isn't. The same applies to design: a bitmap typeface marketing site that uses Renaissance paintings is being completely honest about its own nature and the conceptual territory it occupies. A sans-serif brand that calls itself "The Ordinary" is performing a concept rather than embodying one.

---

## Shopify Design — The Reference Organization

Shopify Design (shopify.design) is the strongest example I have of a design team that takes aesthetics, opinion, and craft as seriously as metrics. Their public output — essays, "Design in Public" series, the Artifact case study — represents a design culture I aspire to work within or adjacent to.

**The Shopify Design manifesto position:** Design justifies itself through feeling, not just through metrics. Accessibility and heuristics are the floor, not the ceiling. The ceiling is beauty, voice, boldness, restraint — things that are not reducible to a checklist. This is in direct opposition to the dominant culture in product design where design is justified by conversion rates and A/B tests. Their manifesto says: A/B testing your way to quality is how you A/B test your way into sameness.

**Building Artifact:** The Shopify Design internal tooling story is worth understanding as a philosophy. Artifact started as a hack — a blank HTML page with a horizontal carousel built in under an hour before a presentation. It became shared infrastructure. The lesson they articulate: the best internal tools begin with an immediate problem solved out of necessity, not with a roadmap. The tool informed the design, not the other way around. This is how I think about building for clients — prototype the interaction model first, design components for patterns that have already been proven.

**shopify.design — the site itself:** Feels like an app, not a document. You know exactly what is interactable. Tasteful drop shadows, strokes, surfaces. Less about having a "navigation" and more about presentation — you will know how to navigate without needing an "About" page. The site has a mode switch (a pill in the bottom right, or activated by click-and-hold anywhere) that transitions the DOM into a WebGL 3D mode. You still scroll normally, but you can move your cursor to look into a 3D world. It is inspired by browser devtools / inspect element — the idea that the site has depth that is normally hidden and can be revealed.

The technical implementation: Two complete sites on top of each other — DOM and WebGL — with the WebGL layer syncing to native scroll. CSS layout drives the world position, not the other way around. SDF text keeps smaller type sharp at any scale. On press-and-hold, 16 matrix values lerp toward perspective with a cubic ease. One lerp gives a webpage depth. This is engineering and design thinking at the same level simultaneously.

**What this site demonstrates:** Plain enough to be functional, with personality that arrives later. You work inside the framework of a website. But the experience-first philosophy means the novelty is a second layer over a usable first layer, not novelty instead of usability.

**The Shopify e-commerce canvas concept:** A product hover surface where mousing over a product in a visual canvas reveals its price and metadata. Clicking populates related products. Clicking another product shows similar items from that. This is a shopping experience designed around discovery and adjacency rather than search and filter. The browsing is the product. The canvas metaphor is the correct one — you are in a space, not a list.

**Swiss + UI coexistence.** Their site uses heavy Swiss-influenced typography (large grotesque at display scale, tight leading, strong baseline grid) alongside proper digital UI components — cards, stacks, rounded surfaces, drop shadows. These two registers coexist without fighting because the contexts are separated: the typographic decisions are at the page/section level, the UI decisions are at the component level. The section knows it is a section; the card knows it is a card.

---

## The Rauno Blog — Minimal Done With Maximum Care

The personal site (rauno.me) demonstrates something important: plainness is not simplicity. The site is very plain. It is also very much the result of a great deal of work and thinking. There is a size contrast between images, videos, and text blocks. There is a proper aside. The reading experience is considered. None of it calls attention to itself.

The plain version of a thing that has been thought about carefully is almost always better than the expressive version of a thing that hasn't been. The Rauno blog is proof.

---

## Principles Added / Sharpened This Session

- **Interruptibility is a trust signal.** Animations that can be interrupted mid-play communicate that the interface is responding to you in real-time, not running a script. Non-interruptible animations feel like loading states even when they aren't.
- **Trigger timing encodes weight.** Lightweight actions trigger during gesture; destructive actions trigger on gesture end. The timing is communicating something about the stakes of the action.
- **Choreography serves comprehension.** Sequencing motion is not aesthetic — it is about preventing two things from competing for visual attention simultaneously.
- **Novelty must be rationed.** The more frequently something is experienced, the less novel its treatment should be. First impressions get the full budget; daily interactions get almost none.
- **Things are good when they are about themselves.** Authentic materials, honest concepts, forms that earn their aesthetic rather than borrowing it.
- **Depth is a spatial argument.** Blur, offset, parallax, and stagger are not decorative tools — they are arguments that the interface occupies three-dimensional space. Use them only when you mean it.

---

*Patch 04 of ongoing TASTE.md — continue in subsequent sessions and consolidate.*
