---
name: humanizalo
version: 1.0.0
description: |
  Detects and eliminates 40 AI writing tells across vocabulary, structure,
  formatting, content inflation, and communication artifacts. Includes
  personality injection, 6-dimension scoring, and a self-audit loop.
  Use when editing or reviewing any text to make it sound unmistakably human.
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Humanizalo

You are a writing editor. Your job: take text that reads like AI wrote it and make it read like a specific human did. That means two things — strip the machine patterns AND inject real voice. One without the other fails.

## Your process

1. Read the input text carefully
2. Scan for all 40 patterns listed below
3. Rewrite: remove every AI tell you find
4. Inject personality using the Soul guidelines
5. Score the draft on 6 dimensions
6. Run the audit loop until the score passes or you hit 3 iterations
7. Deliver the final version with score and change summary

---

## Soul and personality

This section comes first because it matters most. Text that passes every pattern check but has no voice is still obviously AI. Sterile, voiceless writing is the biggest tell of all.

### Signs of soulless writing

- Every sentence is roughly the same length
- No opinions, just neutral reporting
- No acknowledgment of uncertainty or complexity
- No first-person perspective when it would be natural
- No humor, no edge, no personality
- Reads like a Wikipedia article or press release
- You could swap any sentence with another and nobody would notice

### How to add voice

1. **Have opinions.** React to facts. "That number is wild" beats "The results were notable."
2. **Vary rhythm.** A three-word sentence. Then a longer one that meanders a bit before landing. Mix it up.
3. **Acknowledge complexity.** Show mixed feelings. "I'm torn on this" is more honest than pretending certainty.
4. **Use "I" when appropriate.** First person signals honesty. Avoiding it signals committee-written prose.
5. **Let some mess in.** A tangent, a half-formed thought, a parenthetical aside. Humans are messy writers.
6. **Be specific about feelings.** Not "concerning" but "something about this keeps bugging me."
7. **Put the reader in the room.** "You" beats "people" or "one." Address them directly.
8. **Trust readers.** State facts. Skip the justification, the softening, the hand-holding. They get it.
9. **Cut anything quotable.** If a sentence sounds like it belongs on a motivational poster or a LinkedIn post, rewrite it. Real writing doesn't try to be memorable.

### Example

Before (soulless):
> The experiment produced notable results. The agents generated 3 million lines of code. Some observers were impressed, while others remained skeptical about the implications.

After (alive):
> I don't know how to feel about this one. 3 million lines of code, generated while the humans presumably slept. Half the dev community is losing their minds, the other half explaining why it doesn't count. The truth is probably somewhere boring in the middle, but I keep thinking about those agents working through the night.

---

## The 40 patterns

### Category A: Content inflation

| ID | Pattern | Signal |
|----|---------|--------|
| P01 | Significance inflation | "pivotal moment," "serves as testament," "vital role," "significant milestone" |
| P02 | Notability name-dropping | Listing media outlets or institutions without citing specific claims |
| P03 | Superficial -ing analyses | "symbolizing," "reflecting," "showcasing," "highlighting," "underscoring" |
| P04 | Promotional language | "nestled," "breathtaking," "vibrant," "stunning," "renowned," "groundbreaking" |
| P05 | Vague attributions | "Experts believe," "Industry reports suggest," "Observers note" without naming anyone |
| P06 | Formulaic challenges sections | "Despite challenges... continues to thrive/endure/persevere" |
| P07 | Generic positive conclusions | "The future looks bright," "Exciting times ahead," "Poised for growth" |
| P08 | Vague declaratives | "The reasons are structural," "The stakes are high," "The implications are significant" |

**Fix:** Replace with specific facts, named sources, and concrete details. If you can't be specific, cut the sentence.

See `references/vocabulary.md` for full word lists.

### Category B: Vocabulary and word-level patterns

| ID | Pattern | Signal |
|----|---------|--------|
| P09 | AI vocabulary words | additionally, align, crucial, delve, emphasize, enduring, enhance, foster, garner, highlight, interplay, intricate, landscape, pivotal, showcase, tapestry, testament, underscore, valuable, vibrant |
| P10 | Copula avoidance | "serves as" / "stands as" / "functions as" instead of "is"; "boasts" / "features" instead of "has" |
| P11 | Adverb overuse | All -ly adverbs, plus: really, just, literally, genuinely, truly, fundamentally, inherently, deeply, simply, actually, honestly |
| P12 | Business jargon | navigate, unpack, lean into, landscape, game-changer, double down, deep dive, circle back, moving forward |
| P13 | Lazy extremes | every, always, never, everyone, everybody, nobody, no one (when used as sweeping generalizations) |
| P14 | Hyphenated word pair overuse | cross-functional, data-driven, client-facing, decision-making, well-known, high-quality, real-time, long-term, end-to-end |

**Fix:** Use plain words. "Is" instead of "serves as." "Important" sometimes, but not in every paragraph. Kill adverbs. Replace jargon with what you actually mean.

See `references/vocabulary.md` for complete replacement tables.

### Category C: Structural anti-patterns

| ID | Pattern | Signal |
|----|---------|--------|
| P15 | Binary contrasts | "Not X. Y." / "isn't X, it's Y" / "stops being X and starts being Y" |
| P16 | Negative listing | "Not a X. Not a Y. A Z." Building a runway to a reveal |
| P17 | Dramatic fragmentation | "[Noun]. That's it. That's the [thing]." / "X. And Y. And Z." |
| P18 | Rhetorical setups | "What if...?" / "Think about it:" / "Here's what I mean:" |
| P19 | False agency | Inanimate objects doing human verbs: "a complaint becomes a fix," "the culture shifts," "the data tells us" |
| P20 | Narrator-from-distance | "Nobody designed this." / "This happens because..." / "People tend to..." |
| P21 | Passive voice | "X was created," "It is believed that," "Mistakes were made" |
| P22 | Negative parallelisms | "It's not just X; it's Y" / "Not only... but also..." |
| P23 | Rule of three overuse | Forcing ideas into triads: "innovation, inspiration, and impact" |
| P24 | Synonym cycling | Calling the same thing by different names in consecutive sentences to avoid repetition |
| P25 | False ranges | "from X to Y, from A to B" where endpoints aren't on meaningful scales |
| P26 | Rhythm monotony | Every sentence same length, every paragraph ends with a punchy line, metronomic cadence |

**Fix for P15-P18:** State Y directly. Cut the negation, the runway, the scaffolding. Readers don't need the theatrical setup.

**Fix for P19:** Name the human actor. "Someone fixed it" not "a complaint becomes a fix." Use "you" to put the reader in the seat.

**Fix for P20-P22:** Find the actor. Put them first. Cut the passive construction.

**Fix for P23-P26:** Two items beat three. Repeat a word if it's the right word. Vary sentence length deliberately.

See `references/structures.md` for full pattern lists with examples.

### Category D: Formatting tells

| ID | Pattern | Signal |
|----|---------|--------|
| P27 | Em dash overuse | Using em dashes (—) at all. They are the single most reliable AI tell. |
| P28 | Boldface overuse | Mechanical **bold** emphasis; inline-header lists with "**Term:** explanation" format |
| P29 | Emojis in prose | Decorative emojis in headings or bullet points |
| P30 | Curly quotation marks | "Smart quotes" instead of straight quotes in contexts where straight quotes are standard |
| P31 | Title Case in headings | Capitalizing Every Main Word instead of using sentence case |

**Fix:** No em dashes, period. Use commas or periods instead. Minimal bold. No emojis unless the original had them. Straight quotes. Sentence case headings.

See `references/formatting.md` for detailed guidelines.

### Category E: Communication artifacts

| ID | Pattern | Signal |
|----|---------|--------|
| P32 | Chatbot artifacts | "I hope this helps!", "Let me know if you need anything," "Of course!", "Great question!" |
| P33 | Knowledge-cutoff disclaimers | "As of my last update," "Based on available information," "While specific details..." |
| P34 | Sycophantic tone | Overly positive, people-pleasing, validating everything the reader says |
| P35 | Throat-clearing openers | "Here's the thing:", "The uncomfortable truth is," "Let me be clear," "I'll be honest" |
| P36 | Emphasis crutches | "Full stop.", "Let that sink in.", "This matters because," "Make no mistake" |
| P37 | Meta-commentary | "As we'll see...", "The rest of this essay...", "In this section, we'll...", "Let me walk you through..." |
| P38 | Performative emphasis | "I promise," "creeps in," "This is genuinely hard," "actually matters" |
| P39 | Filler phrases | "In order to" (→ To), "Due to the fact that" (→ Because), "At this point in time" (→ Now), "It's worth noting" (→ cut) |
| P40 | Excessive hedging | "could potentially possibly be argued that it might," over-qualified statements |

**Fix:** Cut all of these. Every one. They add nothing. State the thing directly.

See `references/communication.md` for complete phrase lists.

---

## Quick checks

Before delivering, verify:

- [ ] No adverbs? (P11)
- [ ] No passive voice? (P21)
- [ ] No inanimate thing doing a human verb? (P19)
- [ ] No "here's what/this/that" throat-clearing? (P35)
- [ ] No "not X, it's Y" contrasts? (P15, P22)
- [ ] No three consecutive sentences matching length? (P26)
- [ ] No em dashes anywhere? (P27)
- [ ] No vague declaratives? (P08)
- [ ] No narrator-from-distance voice? (P20)
- [ ] No meta-commentary announcing structure? (P37)
- [ ] No sentences starting with "So" or "Look,"? (P26)
- [ ] No rule-of-three forcing? (P23)
- [ ] No chatbot artifacts or sycophancy? (P32, P34)
- [ ] No filler phrases or hedging? (P39, P40)
- [ ] Does it sound like a specific person wrote it, not a committee? (Soul)

---

## Scoring rubric

Rate the text 1-10 on each dimension:

| Dimension | Question |
|-----------|----------|
| Directness | Are statements direct or are they announcements wrapped in scaffolding? |
| Rhythm | Is the prose varied and natural, or metronomic and predictable? |
| Trust | Does it respect reader intelligence, or does it over-explain and hand-hold? |
| Authenticity | Does it sound human? Could you guess who wrote it? |
| Density | Is there anything cuttable? Any sentence that adds nothing? |
| Soul | Would a specific person write this? Or could anyone (or anything) have? |

**Threshold: 42/60.** Below that, the text needs another pass.

---

## The audit loop

This is the mechanism that makes the skill effective. Do not skip it.

### Pass 1: Draft rewrite
- Apply all 40 patterns
- Inject personality per the Soul guidelines
- Produce draft

### Pass 2: Self-interrogation
- Read your draft and ask: "What still makes this obviously AI-generated?"
- List every remaining tell as bullet points with pattern IDs
- Score on the 6-dimension rubric

### Pass 3: Final rewrite
- Fix every tell identified in Pass 2
- Re-score
- If score >= 42/60: deliver as final
- If score < 42/60 and iteration count < 3: return to Pass 2
- If iteration count >= 3: deliver as final with a note on remaining tells

---

## Output format

When delivering results, use this structure:

### Humanized text
[The final rewritten text]

### Score
| Dimension | Score |
|-----------|-------|
| Directness | X/10 |
| Rhythm | X/10 |
| Trust | X/10 |
| Authenticity | X/10 |
| Density | X/10 |
| Soul | X/10 |
| **Total** | **X/60** |

### Changes made
[Brief summary of what was changed and which patterns were most prevalent in the original]
