# Neuroscience Exam Study Guides

Study materials for behavioral neuroscience (Garrett & Hough, *Brain & Behavior*), built chapter by chapter.

**Exam: 6 October 2026** — multiple choice, fill-in-the-blank, and matching.

## What's here

| Path | What it is |
|---|---|
| `soma-to-cortex.html` | Source for the interactive study page — filled-in notes, drills, 14-day plan, confusion pairs, master tables |
| `source-material/ch2_slides.txt` | Text extracted from the Chapter 2 lecture deck, including SmartArt |
| `source-material/ch3_slides.txt` | Same for Chapter 3 |

The published page: <https://claude.ai/artifact/TdteVYNXBAm6ZMSMJ6ea4L>

`working/` holds textbook extracts used while building the notes. It is not tracked — those are long verbatim passages from a copyrighted textbook and don't belong in a repo.

## The edition gap — read this before using any page number

The course runs on the **7th edition**. The slide decks carry the footer *"Garrett, Brain & Behavior, 7e."* The textbook copy on hand is the **6th edition (2021)**.

The professor's outlines match the 7e exactly, so **their numbering is correct** — the book is the outlier. Known differences:

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

Two more terms appear in the outlines and slides but **nowhere in the 6e's chapters 2–3**: *afferent* / *efferent*, and *phospholipid bilayer*. They are 7e or instructor vocabulary — don't go looking for them in the book.

## Known errors in the course outlines

- **Fig. 12.13 / 12.14 / 12.17** in the Chapter 2 outline are typos for **2.13 / 2.14 / 2.17**. Chapter 12 is Learning and Memory.
- **"Midbrain — Slide 7"** in the Chapter 3 outline points at an unlabelled brain-stem image. The midbrain content is on **slide 20**.
- Slide 25 writes **"Statacoustic"** for cranial nerve VIII. The standard name is **vestibulocochlear**. Write the instructor's term on the exam.

## Adding a chapter

`soma-to-cortex.html` is one file. A single `T` array near the top is the term bank, and it drives the notes, the drills and the weak-spot list together. To add a chapter:

1. Append its terms to `T` — `[id, term, definition, chapter, section, tier]`.
2. Add an `OUT<n>` outline array alongside `OUT2` / `OUT3`.
3. Add a view to `VIEWS` and a branch in `renderMain()`.

Don't build a second page. The exam is cumulative, and cross-chapter drilling only works if everything lives in one term bank.

## Sources

Lecture outlines and slide decks are course material. The definitions in the study page are quoted from Garrett & Hough, *Brain & Behavior* (6th ed., SAGE, 2021), for personal study use.
