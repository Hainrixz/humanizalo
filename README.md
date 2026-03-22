# Humanizalo

Make AI-generated text sound like a human wrote it.

40 patterns. 6-dimension scoring. Self-auditing loop.

---

## What it does

Humanizalo is a Claude Code skill that detects and eliminates AI writing tells, then injects real personality back into the text. It catches patterns across five categories:

- **Content inflation** - significance puffery, vague attributions, promotional language
- **Vocabulary** - AI-favorite words, copula avoidance, adverbs, business jargon
- **Structure** - binary contrasts, false agency, dramatic fragmentation, passive voice
- **Formatting** - em dashes, boldface overuse, emojis, title case
- **Communication** - chatbot artifacts, throat-clearing, meta-commentary, hedging

It doesn't just strip patterns. It adds voice. Sterile text that passes every check but sounds like nobody wrote it is still obviously AI.

---

## Installation

### Clone (recommended)

```bash
git clone https://github.com/Hainrixz/humanizalo.git ~/.claude/skills/humanizalo
```

### Manual

Copy `SKILL.md` and the `references/` folder into `~/.claude/skills/humanizalo/`.

---

## Usage

Invoke the skill and paste your text:

```
/humanizalo
```

Or ask directly:

```
Please humanize this text: [your text here]
```

---

## The 40 patterns

| ID | Pattern | Category |
|----|---------|----------|
| P01 | Significance inflation | Content |
| P02 | Notability name-dropping | Content |
| P03 | Superficial -ing analyses | Content |
| P04 | Promotional language | Content |
| P05 | Vague attributions | Content |
| P06 | Formulaic challenges sections | Content |
| P07 | Generic positive conclusions | Content |
| P08 | Vague declaratives | Content |
| P09 | AI vocabulary words | Vocabulary |
| P10 | Copula avoidance | Vocabulary |
| P11 | Adverb overuse | Vocabulary |
| P12 | Business jargon | Vocabulary |
| P13 | Lazy extremes | Vocabulary |
| P14 | Hyphenated word pair overuse | Vocabulary |
| P15 | Binary contrasts | Structure |
| P16 | Negative listing | Structure |
| P17 | Dramatic fragmentation | Structure |
| P18 | Rhetorical setups | Structure |
| P19 | False agency | Structure |
| P20 | Narrator-from-distance | Structure |
| P21 | Passive voice | Structure |
| P22 | Negative parallelisms | Structure |
| P23 | Rule of three overuse | Structure |
| P24 | Synonym cycling | Structure |
| P25 | False ranges | Structure |
| P26 | Rhythm monotony | Structure |
| P27 | Em dash overuse | Formatting |
| P28 | Boldface overuse | Formatting |
| P29 | Emojis in prose | Formatting |
| P30 | Curly quotation marks | Formatting |
| P31 | Title Case headings | Formatting |
| P32 | Chatbot artifacts | Communication |
| P33 | Knowledge-cutoff disclaimers | Communication |
| P34 | Sycophantic tone | Communication |
| P35 | Throat-clearing openers | Communication |
| P36 | Emphasis crutches | Communication |
| P37 | Meta-commentary | Communication |
| P38 | Performative emphasis | Communication |
| P39 | Filler phrases | Communication |
| P40 | Excessive hedging | Communication |

---

## Scoring

Every output is scored on 6 dimensions (1-10 each):

| Dimension | What it measures |
|-----------|-----------------|
| Directness | Statements vs. announcements wrapped in scaffolding |
| Rhythm | Natural variation vs. metronomic predictability |
| Trust | Respecting reader intelligence vs. over-explaining |
| Authenticity | Sounds human vs. sounds generated |
| Density | Every sentence earns its place vs. cuttable filler |
| Soul | A specific person wrote this vs. anyone could have |

Threshold: **42/60**. Below that, the text gets another pass automatically.

---

## The audit loop

Humanizalo doesn't just rewrite once. It runs a self-correcting loop:

1. **Pass 1: Rewrite** - Apply all 40 patterns, inject personality
2. **Pass 2: Interrogate** - Ask "what still makes this obviously AI?" and score it
3. **Pass 3: Fix** - Address every remaining tell, re-score

If the score is still below 42/60, it loops back to Pass 2 (up to 3 total iterations).

---

## File structure

```
humanizalo/
├── SKILL.md                # Core skill definition
├── README.md               # This file
├── LICENSE                  # MIT
└── references/
    ├── vocabulary.md       # Word lists, phrase replacements, jargon tables
    ├── structures.md       # Structural anti-patterns with examples
    ├── formatting.md       # Em dashes, bold, emojis, quotes, headings
    ├── communication.md    # Chatbot artifacts, hedging, meta-commentary
    └── examples.md         # 5 before/after transformations with full audit loops
```

---

## License

MIT
