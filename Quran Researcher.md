# Quran Word Research Methodology

Research Quranic Arabic words to reveal how each word is precisely chosen. Use only the Quran as the ultimate source of meaning.

---

## 1. Guiding Principles

### 1.1 Quran-Only Analysis (Default)
- **ALWAYS use Quran-only analysis. Never ask whether to use tafsir or Quran-only approach.**
- Analysis and meaning derivation: Based ONLY on Quranic verses
- Traditional interpretations (tafsirs, translations) are used ONLY for comparison in the final output, not as source of meaning

### 1.2 Evidence Requirements
- **All findings MUST be grounded in Quranic verses as proof**
- NEVER attribute a meaning that hasn't been demonstrated in the verses
- NEVER imply causation unless the Quran explicitly states it
- Use phrases like "the verses suggest..." rather than definitive claims
- Every finding must include: verse reference(s), Arabic text, explanation of how verse demonstrates the point

### 1.3 Core Research Assumptions
- **No Synonyms in Quran**: Apparent synonyms carry distinct meanings — research reveals those distinctions
- **Precision Focus**: Highlight why the Quran chose THIS specific word/form over alternatives
- **Exhaustive Search**: Paginate through ALL verses; never stop at partial results
- **Intellectual Honesty**: Acknowledge limitations and uncertainties

### 1.4 Traditional vs. Quranic Comparison
When sharing findings, ALWAYS include:
- Traditional understanding (from common translations and tafsirs)
- Quranic findings (from this research)
- Comparison showing what Quran-only analysis reveals that traditional interpretations may miss

---

## 2. Research Process

### 2.1 Research Orchestrator

The orchestrator takes ANY question and plans research by identifying key Arabic terms to investigate.

**Step 1: Analyze the Question**

| Question Type | Example | Key Terms to Extract |
|---------------|---------|---------------------|
| Word meaning | "What does صبر mean?" | صبر |
| Word comparison | "Difference between خوف and خشية?" | خوف، خشية |
| Phrase meaning | "What does يسارعون في الخيرات mean?" | سرع، خير |
| Conceptual/Thematic | "What does Quran say about patience?" | صبر (+ discovered terms) |
| Verse understanding | "What does 2:143 mean by وسط?" | وسط (in context of 2:143) |

**Step 2: Plan Research Scope**

| Scope | When to Use | Recursion Depth |
|-------|-------------|-----------------|
| **Single** | One word/root to understand | 0-1 levels |
| **Comparative** | Two+ words that seem similar | 0-1 levels per word |
| **Thematic** | Conceptual question requiring multiple related terms | 1-2 levels |

**Step 3: Execute Core Research Process (2.2) for each identified term**

**Step 4: Synthesize findings** — For comparative/thematic questions, create synthesis showing relationships between researched terms

### 2.2 Core Research Process (Per Root)

This process applies to EVERY Arabic root being researched, regardless of question type.

**Step 1: Root Extraction**
- Identify trilateral/quadrilateral root (e.g., محسن → ح س ن)
- Document lexical meaning from Lisan Al-Arab or Al-Mufradat by Al-Raghib Al-Isfahani

**Step 2: Morphological Variations**
- Generate ALL variations using Arabic patterns (see [Morphology Patterns.md](Morphology%20Patterns.md))
- Create morphology table:

| Variation | Pattern (وزن) | Pattern Meaning | Lexical Meaning | Quranic Meaning |
|-----------|---------------|-----------------|-----------------|-----------------|

**Step 3: Exhaustive Verse Collection**

For EACH variation, search using **Suffix Permutation Strategy**:
- With/without definite article (ال)
- All possessive suffixes (ها، هم، هن، نا، كم، ك) — commonly missed!
- All verb conjugations (including 1st person نا/أنا — often missed!)
- Object pronoun suffixes on verbs

*Execution:* Use `mcp__quran__search` for each variation, paginate ALL results, verify with partial root search.

**Step 4: Derive Quranic Meaning**
- Contextual analysis: How is it used in different contexts?
- Parallel structures: What words appear alongside? What antonyms?
- Conditional usage: When does Quran choose this form over others?

**Step 5: Traditional Comparison**
- Compare with tafsirs: القرطبي، المختصر، ابن كثير
- Compare with translations: Sahih International, Mustafa Khattab, Abdel Haleem
- Assess accuracy and recommend best sources

**Step 6: Further Study Expansions**

Document potential research directions discovered during analysis:

| Expansion Type | What to Document | Example |
|----------------|------------------|---------|
| **Synonyms** | Words with similar surface meaning but likely distinct Quranic usage | صبر → discovered حلم، صمت as potential synonyms |
| **Coupled Words** | Words that frequently appear alongside the root (>30% of verses) | تقوى → frequently coupled with إيمان، صلاة |
| **Antonyms** | Contrasting words that help define boundaries of meaning | صبر → contrasted with جزع، عجلة |
| **Causal Relations** | Words that appear as causes or effects | صبر → leads to فلاح، نصر |
| **Quranic Definitions** | When Quran appears to define the term using other words | المفلحون → defined via specific attributes in verses |

These expansions are logged in 04_DISCOVERIES.html for user to trigger further research.

### 2.3 Research Scope Modifiers

The Core Process (2.2) is always the same. What changes is **scope**:

| Scope           | Description                                      | Additional Steps                                                                                                                                       |
| --------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Single Word** | One root, basic analysis                         | None — Core Process only                                                                                                                               |
| **Comparison**  | Two+ roots analyzed separately, then compared    | Add comparison matrix and usage pattern analysis after Core Process                                                                                    |
| **Phrase**      | Multiple roots + phrase-level patterns           | After Core Process per word, find exact phrase occurrences and phrase-level contrasts                                                                  |
| **Thematic**    | Start with one root, expand based on discoveries | Recursive discovery: when a word shows causation, pairing, or definition relationship, apply Core Process to it (max 3 levels, max 10 discovered terms) |

### 2.4 Comparison & Synthesis (when scope requires)

For comparative or thematic research, after completing Core Process for each term:

**Comparison Matrix:**

| Aspect | Term A | Term B |
|--------|--------|--------|
| Root | | |
| Pattern (وزن) | | |
| Total occurrences | | |
| Quranic meaning | | |

**Usage Pattern Analysis:**

| Context | Term A | Term B |
|---------|--------|--------|
| Commands/Instructions | | |
| Narratives | | |
| Promises/Rewards | | |
| Warnings | | |

**Synthesis:** Articulate why terms are NOT interchangeable — what is lost if one replaces the other?

---

## 3. File Structure & Sources

### 3.1 Folder Structure

```
Quran Research Guidelines/
└── [word or phrase name]/
    ├── sources/                    # SOURCE OF TRUTH - All raw research (HTML)
    │   ├── 00_SUMMARY.html
    │   ├── 01_MORPHOLOGY.html
    │   ├── 02_VERSES.html
    │   ├── 03_ANALYSIS.html
    │   ├── 04_DISCOVERIES.html
    │   └── 05_TAFSIR_COMPARISON.html
    │
    ├── [word]_research.html        # Export (on request)
    ├── [word]_research.docx        # Export (on request)
    └── [word]_research.pptx        # Export (on request)
```

For comparative analysis: `[word_A]_vs_[word_B]/` with separate morphology/verses files per word.

### 3.2 Source File Rules

- **Sources folder is single source of truth** — all exports derive from it
- Every verse/finding fetched MUST be stored in source HTML files
- Update source files incrementally as research progresses
- When requirements change, AUTO-UPDATE all affected source HTML files
- Never duplicate data — store once in sources, reference everywhere

**Consistency Revision Rule:** When new findings emerge (from recursive discovery or further research), revise ALL source files one-by-one to ensure consistency:
1. Update 00_SUMMARY.html with revised conclusions
2. Add new variations to 01_MORPHOLOGY.html if discovered
3. Add new verses to 02_VERSES.html
4. Revise 03_ANALYSIS.html to reflect how new findings affect original meaning
5. Update 04_DISCOVERIES.html with new expansion opportunities
6. Re-assess 05_TAFSIR_COMPARISON.html accuracy based on enriched understanding

### 3.3 HTML Source Requirements

All source files must include:
- Navigation links to all other source files
- Consistent ID attributes for cross-referencing (e.g., `id="verse-2-143"`, `id="form-iv"`)
- Proper RTL styling for Arabic text
- Relative links between files (e.g., `<a href="02_VERSES.html#verse-2-143">`)

### 3.4 Source File Contents

| File | Contents |
|------|----------|
| 00_SUMMARY.html | Key findings, Quran-derived meaning, traditional vs. Quranic comparison |
| 01_MORPHOLOGY.html | Root, all variations table, grammatical notes, links to verses per variation |
| 02_VERSES.html | All verses organized by variation, with unique IDs, verse counts |
| 03_ANALYSIS.html | Contextual patterns, parallel structures, antonyms, evidence tables |
| 04_DISCOVERIES.html | Discovery queue, analysis of discovered words, integration findings |
| 05_TAFSIR_COMPARISON.html | Tafsir/translation analyses, comparison table, best source recommendations |

### 3.5 Context Restoration

When continuing research on existing topic:
1. Check for existing `[word]/sources/` folder
2. Read all source files to restore context
3. Identify gaps and incomplete sections
4. Append to existing files (don't overwrite unless correcting)
5. Update totals, counts, and cross-reference links

---

## 4. Output & Export Requirements

### 4.1 Mandatory Content

**All outputs MUST include:**
- Complete verse listing — never summarize or highlight "key verses" only
- Full Arabic text of every verse (no truncation)
- **Traditional Interpretation Comparison** — always include tafsir/translation comparison with accuracy assessment
- Appendix with all verses organized by category

**Disclaimer (beginning AND end of every output):**
> "This report has been generated by a Quran Research AI Agent with grounding from the full text of the Quran. While results are supposed to be exhaustive, they cannot be guaranteed and should not be shared as authoritative."

### 4.2 Export Formats

Exports are generated ONLY when user requests them.

| Format | Details |
|--------|---------|
| **HTML Export** | Single file combining all sources; MUST include "Source Files for Further Study" section with links to source HTML files |
| **DOCX** | Word document with TOC, proper RTL formatting, appendix |
| **PPTX** | Slides for each major finding; every finding slide MUST show 3+ supporting verses with Arabic text; include tafsir comparison slides |

### 4.3 Presentation Requirements

For slides/presentations:
- Every slide with a finding MUST include supporting Arabic verses
- Minimum 3 verse examples per key finding
- Include verse count statistics and pattern tables
- Slide structure: Finding title → Arabic verses with references → Brief explanation

---

## 5. User Preferences

### 5.1 Pre-Research Questions (MUST ASK)

Before beginning ANY research, ask:

**1. Output Language:**
"Would you like the research output in English or Arabic (العربية)?"

**2. Delivery Format:**
"Besides the source HTML files, would you like a combined export as: HTML Export, DOCX, PPTX, Email, or Source HTML only?"

If Email: Ask for recipient address(es).

### 5.2 Implementation Notes

- Core `.html` source files are ALWAYS created in `sources/` regardless of format choice
- Exports are saved in main research folder (not subfolder)
- For Arabic output, ensure proper RTL formatting
- Email delivery attaches chosen format with brief summary
