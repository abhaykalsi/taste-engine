# domains/motion/motion.md
## Motion, Interaction Physics & Animation Philosophy
*Load with core/beliefs.md + domains/web/web.md*
*Last updated: 2026-05-10*

---

## The Foundation: Physics, Metaphor, Interruptibility

The best interaction design is invisible because it has done enough thinking to disappear. It is modeled on the physics and metaphors of the real world.

**Metaphors as learnability.** When iOS teaches you to swipe up to unlock, it teaches a spatial metaphor: the interface is composed of stacked layers, each dismissable by sliding in the direction it came from. You learn this once. Every surface that obeys this metaphor is learned for free. Every exception costs the user effort.

**Interruptibility as trust.** Animations that can be interrupted mid-play communicate: I am responding to you, not running a script. Non-interruptible animations feel like loading states even when they aren't. Interruptibility is one of the clearest signals that an interface is actually responsive vs. performing responsiveness.

**Kinetic physics as trust.** When you dismiss an app and it morphs into the Dynamic Island retaining the angle and momentum of the throw, the interface is saying: I am an extension of your body, not a tool you control. The distinction matters. Products that feel like extensions are used differently from products you operate.

---

## When to Trigger

Trigger timing encodes the weight of an action.

**During the gesture (lightweight, exploratory):** Revealing overlays, peeking at screens, progressive disclosure. The feedback should be immediate. Waiting for gesture end before showing anything feels broken. The user is exploring — let them.

**On gesture end (heavy, committed, destructive):** Dismissing an app, deleting content, submitting a form. The action requires explicit intent. Triggering mid-gesture risks an accidental committed action the user cannot undo. The delay is communicating: I want to be sure you meant this.

**The rule:** Lightweight actions trigger during gesture after arbitrary distance. Destructive actions trigger on gesture end regardless of distance.

---

## Choreography as Narrative

When multiple things need to move, the sequence is the design. Almost never "all at once."

**The iOS search gesture example:** Home screen blurs first (lowering it on z-axis) before Siri suggestions appear. If they appeared simultaneously the layering would be visually incoherent — two things in the same space with no spatial relationship established. Each step clears the stage for the next.

**The principle:** Choreography is about preventing two things from competing for visual attention simultaneously. Time and delay used narratively, not decoratively.

In animation our instruments are time and artificial delays to be leveraged in a way that feels true to motion in nature — you rarely see all the leaves of a tree moving in jarring concert.

---

## Staggering as Dimension

When sibling elements animate with slight timing offsets, they read as three-dimensional — occupying different positions in depth rather than being a flat grid that switches on. 

**Examples:**
- iOS unlock staggered app icon translation — a primitive swipe becomes three-dimensional, exaggerated, satisfying
- iOS Control Centre — each row has slightly different spring configuration. Organic rubber banding
- OpenAI grid content fade-in — new content arrives rather than switches on
- Staggered text hover animations — character-by-character delay makes type feel alive

A school of fish swimming: very slight differences in movement and timing, visually indistinguishable from each other. The effect is mesmerising. Use this for sibling items that look similar.

---

## Depth as Spatial Argument

Blur, offset, parallax, and stagger are not decorative tools — they are arguments that the interface occupies three-dimensional space.

**Blur as z-axis:** When an overlay appears and the background blurs, the interface is saying: that layer is now behind this one. Without the blur, both layers read as coplanar and the modal feels arbitrary.

**Blurred backdrop in overlays:** Dimming/blurring the backdrop when launching a modal is not just visual hierarchy — it signals that the backdrop is no longer interactive. Only the foreground is actionable. Tapping the backdrop closes it because the blur told you it was behind the thing you're looking at.

**Layered composition:** Offset browser frames, out-of-focus objects in periphery — used in marketing visuals to suggest depth and abundance. The objects are not arbitrary decoration; they are primary subjects appearing in quantity, which is itself the message.

---

## Novelty in Motion — The 10% Rule

The more frequently an interaction is performed, the less appropriate any extravagant treatment of it is.

**Onboarding:** Maximum novelty budget. You experience it once. It creates a first impression. Dial it up.

**Daily interactions:** Almost no novelty budget. An elaborate animation on a button you click 50 times a day becomes friction. The brain stops registering it and it starts feeling like lag.

**The correct implementation:** Gate novelty animations. Fire them once (on first login, first unlock). After that: standard behavior. The novelty is preserved because it is rare. Paco Coursey's site does this — stagger plays on first load, not on every return.

**Novelty tax:** Every novel interaction pattern is a tax on the user — they must learn it before it becomes useful. Arc (The Browser Company) built a saxophone but couldn't convert it into a piano. The novelty tax was too high for non-novelty-seeking users. Know your audience's novelty tolerance before you spend the budget.

---

## Spring Physics Over Easing Curves

Springs are the correct model for UI motion. They are:
- Defined by physical properties (stiffness, damping, mass) rather than time
- Naturally interruptible — a spring can be redirected mid-motion without a discontinuity
- Contextually appropriate — different spring configurations feel lighter or heavier, which communicates the weight of the element

Standard CSS easing curves (ease-in, ease-out, cubic-bezier) are time-based. They cannot be interrupted cleanly. They feel mechanical next to spring-based motion.

**Apple HIG timing:** The reference for spring configuration. Study the iOS unlock, the Dynamic Island morph, the Control Centre reveal. These are calibrated by people who have thought about nothing else for years.

---

## Fidgetability

Some interactions are worth designing not because they are functional but because they are satisfying to repeat. The AirPods case. The Apple Pencil tip. These are probably not accidents.

Digital equivalent: an interaction that rewards repeated use with a feeling that the system is responsive and alive. Related to game-feel — the sense that the interface is communicating back to you with every gesture.

Not every interaction needs this. But the ones that get it are remembered.
