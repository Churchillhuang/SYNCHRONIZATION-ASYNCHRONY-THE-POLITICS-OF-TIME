# AGENTS.md — Session Log

## Font
- **Body:** EBGaramond12-Regular (optical-size for 12pt)
- **Italic:** EBGaramond12-Italic
- **Bold:** EBGaramond-Bold (CTAN complete)
- **BoldItalic:** EBGaramond-BoldItalic (CTAN complete)
- **Sans:** DejaVu Sans
- **Mono:** DejaVu Sans Mono
- Source: CTAN (non-optical-size for bold), ~/.local/share/fonts/ for optical-size regular/italic

## Typography
- Body text: 12pt
- Line spacing: `\setstretch{1.15}`
- Alignment: justified (removed `\RaggedRight`)
- Indent: 2em (via `\setlength{\parindent}{2em}`)
- Hyphenation: `\hyphenpenalty=6000`, `\emergencystretch=3em`, `\righthyphenmin=4`, `\lefthyphenmin=4`
- Widow/orphan: `\widowpenalty=10000`, `\clubpenalty=10000`
- Microtype: protrusion only (`protrusion=true,factor=1100`)
- Lists: `\setlist[itemize]{topsep=4pt,itemsep=2pt,parsep=0pt,leftmargin=1.5em}`

## Page Layout (6"×9")
- top: 0.75", bottom: 1.0", inner: 0.85", outer: 0.55"
- `twoside`
- Paper: 6in × 9in (KDP standard)

## Headers
- Even: `\scshape Synchronization & Asynchrony`
- Odd: `\scshape\leftmark`
- `\headrulewidth{0.4pt}`

## TOC
- `\contentsname{}` cleared (with `\renewcommand` before `\tableofcontents` to bypass babel)
- `\cftchapfont{\normalfont}` (no bold for chapter entries)
- `\cftchappagefont{\normalfont}`
- `titletoc` package removed (conflict with tocloft)

## CTA
- Added before `\end{document}` in both templates
- Signature image: `signature-combined.png` at 0.8in height
- Text: `\large\emph{If you enjoyed this book, please consider leaving a review on Amazon...}`

## Mermaid Diagrams
All 5 ASCII diagrams converted to ` ```mermaid ` code blocks:
- `ch02.md:167` — Human Nature / Scarcity / Power 3-branch comparison (was `\includegraphics` placeholder)
- `ch02.md:999` — Multi-level causal hierarchy with edge labels
- `ch03.md:108` — Blueprint ontological chain (vertical cascade)
- `ch03.md:239` — Mathematical ratio (∞/F = ∞) calculus
- `ch04.md:94` — Principle ontological chain (vertical cascade)
Rendered via `build/mermaid-filter.lua` → mmdc → PDF vector graphics.

## Current Build Status (as of last audit)
- **Volume I PDF**: 205 pages, 6"×9", 0 overfull boxes
- **Volume II PDF**: 252 pages, 6"×9", 0 overfull boxes
- **Volume I EPUB**: 125KB, valid EPUB document
- **Volume II EPUB**: 164KB, valid EPUB document
- **Mermaid diagrams**: 5 rendered successfully in Volume I PDF pipeline

## Known Issues
- xelatex doesn't support microtype font expansion (protrusion only)
- Batch pandoc commands sometimes fail for Volume II (run separately)
- ch08.md contained a leftover placeholder `[To be continued with §8.2...]` — removed during audit

## Audit Summary (2026-06-22)
- All 14 source files present and complete
- Cross-references consistent: Part I-V headers match chapter content
- Placeholder in ch08 removed
- `.gitignore` updated for public repo readiness (adds *.epub, compiled manuscripts, backup dirs, node_modules)
- README updated with accurate build commands and Decoder Ring mention
- Volume I KU exclusive ends next month; Volume II has no KU restriction
- Repo remains private until Volume I KU expiry

## Unity Section (ch09 §9.4b)
- Inserted between §9.4 MAGA and §9.5 Pattern Recognition
- Structure: Unity as Synchronization Imperative → Moral Corruption of Promoting Unity → Internal Friction as Evolutionary Feature → Distinguishing Solidarity from Synchronization → Analytical Checklist
- Analytical tone preserved (no normative claims; readers draw own conclusions)
- Pattern Recognition updated: four → five cases throughout
  - Pattern One: added unity weaponization to insulation pattern
  - Pattern Two: added "divisive" to stigmatizing terminology
  - Pattern Three: added §9.4b Unity Weaponization as complementary mechanism (positive-concept capture)
  - Pattern Four: added "divisive/toxic" to cultural enforcement; circular logic for unity
  - Pattern Five: added manufactured unity to Blueprint examples; internal debate to Principle positions
  - Synthesis: added step 5 "Positive-concept capture" (reordered institutional reinforcement to step 6)
  - Conclusion: updated to five cases throughout; added "distinguishing organic solidarity from manufactured synchronization" to defense principles
- Volume II after update: **252 pages**, **0 overfull boxes**

## Volume II Preface Rewrite
- Replaced "Volume I is prerequisite" language with Decoder Ring (~2 pages)
- Decoder Ring: one question ("Does history have a finish line?") → two camps
  - Camp A (Blueprint): synchronize, crush buffers, expert vanguard, ends justify means
  - Camp B (Principle): async evolution, protect buffers, epistemic humility, deontological constraints
- Three instant-application examples (unity, neocon, DEI) bridge to Volume II content
- Volume I referenced as "academic foundation" at end of Decoder Ring (not prerequisite)
- "Navigating the Battlefield" section: "can be read independently" replaces "assumes readers have engaged Volume I"
- Removed duplicate H2 header in preface
- Volume II after update: **252 pages**, **0 overfull boxes**
