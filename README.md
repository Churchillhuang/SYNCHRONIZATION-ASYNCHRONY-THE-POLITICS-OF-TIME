# Synchronization & Asynchrony: The Politics of Time

**Volume I: Meta-Conservatism — A Temporal Framework**

**Volume II: Culture War — From Words to Worldviews**

---

## What This Is

This book proposes that political positions fundamentally reflect temporal assumptions about history—whether history moves toward knowable endpoints (Blueprint worldview) or evolves perpetually without terminus (Principle worldview). These metaphysical commitments generate systematic patterns across epistemology, ethics, institutional design, and social organization.

The framework explains:

- **Why traditional left-right classification systematically fails** — same policies get opposite labels depending on context and era
- **Why opposite ideologies converge** — Soviet communism and Nazi fascism produced nearly identical structures despite opposite contents
- **Why certain positions cluster** — planning, teleological ethics, and centralization derive from shared temporal premises
- **What unifies diverse conservatisms** — meta-conservative analysis reveals structural commonalities beneath surface contradictions
- **How language war operates** — concepts get weaponized, classifications manipulated, to protect some logics while stigmatizing others

## How to Read

If you want the framework's complete philosophical derivation, start with **Volume I** — it builds from ontology through epistemology and ethics to politics.

If you want to see the framework applied to recognizable political phenomena (Nazi classification, DEI, MAGA, cancel culture, unity weaponization), start with **Volume II** — its preface contains a "Decoder Ring" that gives you the essential framework in two pages.

The two volumes are designed to be complementary: Volume I is the academic foundation; Volume II is the battlefield.

## Structure

### Volume I: Meta-Conservatism — A Temporal Framework

| File | Chapter |
|------|---------|
| `src/preface-volume-I.md` | Preface to Volume I |
| `src/ch01.md` | 1: When Traditional Categories Fail |
| `src/ch02.md` | 2: Time as Criterion |
| `src/ch03.md` | 3: The Blueprint Worldview |
| `src/ch04.md` | 4: The Principle Worldview |
| `src/ch05.md` | 5: Meta-Conservatism |

### Volume II: Culture War — From Words to Worldviews

| File | Chapter |
|------|---------|
| `src/preface-volume-II.md` | Preface to Volume II (includes Decoder Ring) |
| `src/ch06.md` | 6: Institutional Battlegrounds |
| `src/ch07.md` | 7: Cultural Fronts |
| `src/ch08.md` | 8: Mapping the Political Spectrum |
| `src/ch09.md` | 9: The Language War |
| `src/ch10.md` | 10: Conceptual Battlegrounds |
| `src/ch11.md` | 11: Methodological Reflection |
| `src/afterword.md` | Afterword |

## Build

Requires pandoc, xelatex, and mermaid-cli (for diagram rendering in Volume I).

**Volume I PDF:**
```bash
pandoc src/preface-volume-I.md src/ch01.md src/ch02.md \
  src/ch03.md src/ch04.md src/ch05.md \
  -o Volume-I.pdf \
  --pdf-engine=xelatex \
  --template=build/volume-I-template.tex \
  --lua-filter=build/mermaid-filter.lua \
  --top-level-division=chapter \
  -V mainfont="EB Garamond"
```

**Volume II PDF:**
```bash
pandoc src/preface-volume-II.md src/ch06.md src/ch07.md \
  src/ch08.md src/ch09.md src/ch10.md src/ch11.md src/afterword.md \
  -o Volume-II.pdf \
  --pdf-engine=xelatex \
  --template=build/volume-II-template.tex \
  --lua-filter=build/mermaid-filter.lua \
  --top-level-division=chapter \
  -V mainfont="EB Garamond"
```

**EPUB (either volume):** Same command, but omit `--pdf-engine`, `--template`, `-V`, use `--lua-filter=build/mermaid-epub-filter.lua` instead (renders diagrams to PNG), and add `-o Volume-I.epub` / `-o Volume-II.epub` with appropriate metadata.

## License

CC BY-NC-ND 4.0 + Translation Permission — see `LICENSE`.

In short: share freely with attribution for non-commercial purposes, no derivatives. Translation into any language is explicitly permitted for non-commercial community efforts. **Print rights are reserved by the author.**

## Contributing

- **Errata**: Open an issue for typos or factual corrections.
- **Translation**: Open a Translation issue. See LICENSE for terms.
- **Discussion**: Use the Discussions tab for framework questions.

Pull requests for translation are welcome. For text corrections, open an issue first.
