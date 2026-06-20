# Synchronization & Asynchrony: The Politics of Time

**Volume I: Meta-Conservatism: A Temporal Framework**

**Volume II: Culture War: From Words to Worldviews**

---

## What This Is

This book proposes that political positions fundamentally reflect temporal assumptions about history—whether history moves toward knowable endpoints (Blueprint worldview) or evolves perpetually without terminus (Principle worldview). These metaphysical commitments generate systematic patterns across epistemology, ethics, institutional design, and social organization.

The framework explains:

- **Why traditional left-right classification systematically fails** — same policies get opposite labels depending on context and era
- **Why opposite ideologies converge** — Soviet communism and Nazi fascism produced nearly identical structures despite opposite contents
- **Why certain positions cluster** — planning, teleological ethics, and centralization derive from shared temporal premises
- **What unifies diverse conservatisms** — meta-conservative analysis reveals structural commonalities beneath surface contradictions

## Open Source Notice

Volume I of this work spent six months on Amazon Kindle Unlimited and sold zero copies. Volume II was completed shortly after. The market rewards political categories that flatter existing prejudices, not ones that cut through them. Rather than let the framework gather dust, it's released here for anyone who finds it useful.

This work is licensed under **CC BY-NC-ND 4.0** — see the `LICENSE` file for the full legal text. In short: you may share it freely with attribution, but not for commercial purposes, and not in modified form. **Print rights are reserved by the author** — this license grants digital access, not the right to produce and sell physical copies.

If you find the framework valuable and would like to support the author's work, the most helpful thing you can do is **leave an honest review on Amazon** — whether positive or critical, your genuine response helps other readers decide whether this book is for them. I am sincerely grateful to anyone who takes the time, and the help means more than I can say.

## Localization

Translations into other languages are welcome — please use the **Translation** issue template. The LICENSE file includes an additional permission specifically allowing non-commercial community translations. Translators will be formally credited both in the work and in this repository. Commercial translation rights remain reserved by the author.

## Contributing

Found an error or a typo? Open an **Errata** issue. For framework discussion, use the **Discussion** template. Pull requests for translation are welcome; for text corrections, please open an issue first.

## Structure

### Volume I: Meta-Conservatism: A Temporal Framework
| File | Chapter | Words |
|------|---------|-------|
| `src/preface-volume-I.md` | Preface to Volume I | ~1,350 |
| `src/ch01.md` | 1: When Traditional Categories Fail | ~3,900 |
| `src/ch02.md` | 2: Time as Criterion | ~6,500 |
| `src/ch03.md` | 3: The Blueprint Worldview | ~12,800 |
| `src/ch04.md` | 4: The Principle Worldview | ~10,600 |
| `src/ch05.md` | 5: Meta-Conservatism | ~7,200 |

### Volume II: Culture War: From Words to Worldviews
| File | Chapter | Words |
|------|---------|-------|
| `src/preface-volume-II.md` | Preface to Volume II | ~1,350 |
| `src/ch06.md` | 6: Institutional Battlegrounds | ~7,050 |
| `src/ch07.md` | 7: Cultural Fronts | — |
| `src/ch08.md` | 8: Mapping the Political Spectrum | — |
| `src/ch09.md` | 9: The Language War | — |
| `src/ch10.md` | 10: Conceptual Battlegrounds | — |
| `src/ch11.md` | 11: Methodological Reflection | ~6,500 |
| `src/afterword.md` | Afterword | ~580 |

## How to Read

All chapters are in Markdown. The complete book is `COMPLETE_BOOK_Chapters_1-11.md`; individual chapters are in `src/`.

To rebuild the complete book from sources:

```bash
cat src/00-frontmatter.md src/preface-volume-I.md \
    src/ch01.md src/ch02.md src/ch03.md src/ch04.md src/ch05.md \
    src/preface-volume-II.md src/ch06.md src/ch07.md src/ch08.md src/ch09.md \
    src/ch10.md src/ch11.md src/afterword.md > COMPLETE_BOOK.md
```

For PDF output, use pandoc:

```bash
pandoc COMPLETE_BOOK.md -o Synchronization_Asynchrony.pdf \
  --pdf-engine=xelatex \
  --toc \
  --metadata title="Synchronization & Asynchrony" \
  --metadata author="Churchill Húnn"
```


