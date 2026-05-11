# taste-engine
## A structured design knowledge base / digital ego

---

## What This Is

Not a style guide. Not a system prompt. A second brain — calibration material that tells an AI (or a collaborator) how to *think and judge* the way I do, not what outputs to produce. The AI already knows how to design. This tells it how I evaluate design.

**The core distinction:** opinions and judgment, not instructions and rules.

---

## Folder Structure

```
taste-engine/
│
├── README.md                          ← this file. architecture + usage
│
├── core/
│   ├── beliefs.md                     ← 10-15 high-level positions. always load this.
│   ├── philosophy.md                  ← extended reasoning behind the beliefs
│   └── influences.md                  ← formative intellectual/cultural context
│
├── domains/
│   ├── brand/
│   │   └── brand.md                   ← identity, systems, positioning
│   ├── web/
│   │   └── web.md                     ← web design, IA, interaction philosophy
│   ├── typography/
│   │   └── typography.md              ← type decisions, hierarchy, alignment
│   ├── motion/
│   │   └── motion.md                  ← animation, interaction physics, choreography
│   └── editorial/
│       └── editorial.md               ← layout, print, publication systems
│
├── references/
│   ├── studios.md                     ← studio positions — brief, scannable
│   ├── designers.md                   ← individual designer positions
│   └── works.md                       ← specific works — what they exemplify
│
├── tensions.md                        ← where my positions conflict + how to resolve
│
├── meta/
│   └── presentations.md               ← how i structure and present work
│
└── patches/
    ├── PATCH_TEMPLATE.md              ← template for new patches
    └── archived/                      ← raw session patches (source material)
        ├── patch_01_brand_good.md
        ├── patch_02_bad_work.md
        ├── patch_03_web.md
        ├── patch_04_motion_shopify.md
        ├── patch_05_han_gao_antidesign.md
        └── patch_06_typography_minimal.md
```

---

## How to Use This

### For AI prompting
Load files based on task. Always load `core/beliefs.md`. Then load the relevant domain file. Reference files are optional — load them when specific studios/designers are relevant.

When the AI is *using* this material to evaluate work, answer questions, or critique: it should **not** mention which files it loaded or quote filenames in the reply. The content is silent context; responses should read as natural judgment, not “per beliefs.md” or “the web domain says.”

**Minimal context (quick tasks):**
```
core/beliefs.md
```

**Brand/identity work:**
```
core/beliefs.md + domains/brand/brand.md + references/studios.md
```

**Web/digital work:**
```
core/beliefs.md + domains/web/web.md + domains/motion/motion.md
```

**Typography/layout:**
```
core/beliefs.md + domains/typography/typography.md + domains/editorial/editorial.md
```

**Hiring/critique:**
```
core/beliefs.md + tensions.md + references/studios.md
```

**Presentations:**
```
core/beliefs.md + meta/presentations.md
```

### For adding new patches
1. Write raw session notes into `patches/PATCH_TEMPLATE.md`
2. Extract relevant content into the appropriate domain/reference/tension files
3. Archive the raw patch in `patches/archived/`
4. Update `tensions.md` if any new contradictions emerge
5. Update `core/beliefs.md` only if a genuinely new high-level position crystallizes

### Management principle
The core files should change rarely and deliberately. Domain files grow with new knowledge. References grow freely. Tensions grow when contradictions are noticed. The patches folder is the raw input layer — never delete from it.

---

## Versioning
No formal versioning yet. Date-stamp major changes in file headers.
Last updated: 2026-05-10
