# Neuroscience Exam Study Guides

Study materials for behavioral neuroscience (Garrett & Hough, *Brain & Behavior*), built chapter by chapter.

**Exam: 6 October 2026 — chapters 2, 3, 4 and 5.** Multiple choice, fill-in-the-blank, and matching. No short answer.

**The study page:** <https://claude.ai/artifact/TdteVYNXBAm6ZMSMJ6ea4L>

> GitHub shows `soma-to-cortex.html` as source code. To actually use it, open the link above — that's the published, working version.

## What's here

| Path | What it is |
|---|---|
| `soma-to-cortex.html` | Source for the interactive study page |
| `source-material/ch2_slides.txt` | Text extracted from the Chapter 2 lecture deck, including SmartArt |
| `source-material/ch3_slides.txt` | Chapter 3 |
| `source-material/ch4_slides.txt` | Chapter 4 |
| `source-material/ch5_slides.txt` | Chapter 5 |

Not tracked, but present locally: the `.pptx` decks and outline PDFs in `source-material/` (about 60 MB of binaries, originals in Downloads), and `working/` — long verbatim extracts from a copyrighted textbook, which don't belong in a repo.

## What the study page contains

- **Plan** — seven days, 29 September to 6 October, across four chapters. Progress saves automatically.
- **Drill** — five modes: multiple choice, fill-in-the-blank, matching, confusion pairs, and label-the-diagram. Questions are weighted toward terms you have missed before.
- **Weak spots** — every term missed, most-missed first, with a button to drill only those.
- **Chapters 2–5** — the lecture outlines with every blank filled in.
- **Confusions** — 23 pairs that blur, studied against each other rather than separately.
- **Diagrams** — parts of a neuron, and the lobes of the brain, both clickable and drillable.
- **Tables** — including the instructor's own structure-to-function tables and Table 4.1.
- **Corrections** — the reference errors and edition gaps listed below.

324 terms across four chapters, all driven by one `T` array.

## The edition gap — read this before using any page number

The course runs on the **7th edition**. The slide decks carry the footer *"Garrett, Brain & Behavior, 7e."* The textbook copy on hand is the **6th edition (2021)**.

The professor's outlines match the 7e exactly, so **their numbering is correct** — the book is the outlier.

| Outline / slides (7e) | 6th edition |
|---|---|
| Table 2.3 — twelve neurotransmitters | Table 2.2, p. 40 |
| Fig. 2.24 — Lorenzo & Hecht taste study | Fig. 2.23 |
| Fig. 3.16 — ventricles | Fig. 3.16 is the brain stem |
| Fig. 3.22 — cranial nerves | Fig. 3.22 is the autonomic nervous system |
| Spinal Cord, pp. 79–80 | pp. 66–68 |
| Stages of Development, pp. 85–88 | pp. 72–76 |
| How Experience Modifies the NS, pp. 88–89 | pp. 76–78 |
| Damage and Recovery, pp. 89–97 | pp. 78–85 |

*Afferent*, *efferent* and *phospholipid bilayer* appear in the outlines and slides but nowhere in the 6e's chapters 2–3. They are 7e or instructor vocabulary — don't go looking for them in the book.

## Known errors in the course outlines

- **Fig. 12.13 / 12.14 / 12.17** in the Chapter 2 outline are typos for **2.13 / 2.14 / 2.17**. Chapter 12 is Learning and Memory.
- **"Midbrain — Slide 7"** in the Chapter 3 outline points at an unlabelled brain-stem image. The midbrain content is on **slide 20**.
- Chapter 3 slide 25 writes **"Statacoustic"** for cranial nerve VIII. The standard name is **vestibulocochlear**. Write the instructor's term on the exam.

## Blanks no source answers

These are left blank in the outline, named-but-undefined on the slides, and absent from the 6e. They were filled in verbally in lecture. The study page supplies a standard answer and tags each one **check this** — verify against your own notes:

- The Three Rs — Replacement, Reduction, Refinement (Ch 4)
- Quasi-experiment; concordant and discordant pairs (Ch 4)
- Clinical uses of barbiturates, benzodiazepines, amphetamines, methylphenidate and marijuana (Ch 5)
- Synesthesia (Ch 5)

Also outstanding: **Handout 4** (the APA Ethics Code), referenced by the Chapter 4 outline but not in hand; and the CRISPR / GWAS / optogenetics reading given as pp. 130–131, which are 7e pages with no reliable 6e mapping.

## Image-only slides

Instructor-built slides are often flat images with no text layer, and several turned out to be the highest-value things in their decks. These were read visually and transcribed into the study page:

| Slide | What it holds |
|---|---|
| Ch 3, 19 & 20 | Forebrain and midbrain/hindbrain structure-to-function tables |
| Ch 3, 25 | The 12 cranial nerves, with sensory and motor columns |
| Ch 4, 2 | The scientific method sequence |
| Ch 4, 15 | **Table 4.1** — EEG and imaging techniques with their resolutions. Not mentioned anywhere in the outline. |
| Ch 4, 17 | Family / adoption / twin study comparison |
| Ch 4, 18 | The pairwise concordance formula |

**When adding a chapter, always check the deck for these.** Identify instructor slides by the footer: publisher slides say *"Garrett, Brain & Behavior, 7e © Sage"*; instructor-built ones carry an unreplaced *"Author, Title, Edition. (c) 20XX"* placeholder, or no footer.

## Adding a chapter

`soma-to-cortex.html` is one file. A single `T` array near the top is the term bank, and it drives the notes, the drills, the diagrams and the weak-spot list together. To add a chapter:

1. Append its terms to `T` — `[id, term, definition, chapter, section, tier, altWording, flagNote]`.
2. Add an `OUT<n>` outline array alongside `OUT2`–`OUT5`.
3. Add a view to `VIEWS` and a branch in `renderMain()`.
4. Add any new confusable pairs to `CONF` and instructor tables to `TABLES`.

Don't build a second page. The exam is cumulative, and cross-chapter drilling only works if everything lives in one term bank.

Keep the startup block at the very bottom of the script — it runs `render()`, and everything it touches must be assigned first.

## Sources

Lecture outlines and slide decks are course material. The definitions in the study page are quoted from Garrett & Hough, *Brain & Behavior* (6th ed., SAGE, 2021), for personal study use.
