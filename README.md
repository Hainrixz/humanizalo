# Humanizalo

**[Leer en Espanol](README.es.md)**

Make AI text sound like a real person wrote it.

---

## The problem

AI writes in a way that's easy to spot. It uses the same fancy words over and over ("delve," "landscape," "tapestry"). It loves em dashes. It starts sentences with "Here's the thing:" and ends with "The future looks bright." It sounds like a robot trying to sound smart.

Humanizalo fixes that.

## How it works (the simple version)

You give it text that sounds like AI wrote it. It gives you back text that sounds like you wrote it.

**Before:**
> In today's rapidly evolving landscape, it is crucial to leverage cross-functional synergies and foster a culture of innovation. The implications are significant. The future looks bright.

**After:**
> Move faster. Your competition is.

That's it. Paste in robot text, get back human text.

---

## Set it up (2 minutes)

You need [Claude Code](https://claude.ai/code) installed on your computer.

### Step 1: Open your terminal

On Mac, open the Terminal app. On Windows, open Command Prompt or PowerShell.

### Step 2: Copy and paste this command

```bash
git clone https://github.com/Hainrixz/humanizalo.git ~/.claude/skills/humanizalo
```

Press Enter. Wait for it to finish. Done.

### If that didn't work

You can also do it manually:
1. Download this project (green "Code" button on GitHub, then "Download ZIP")
2. Unzip it
3. Put the folder at this path on your computer: `~/.claude/skills/humanizalo/`

The important files are `SKILL.md` and the `references/` folder. Those need to be inside that path.

---

## Use it

### Option 1: The slash command

In Claude Code, type:

```
/humanizalo
```

Then paste the text you want to humanize.

### Option 2: Just ask

Type something like:

```
Please humanize this text: [paste your text here]
```

### Option 3: Point it at a file

```
Humanize the text in my-draft.md
```

---

## What does it actually do?

Humanizalo looks for 40 specific patterns that give away AI writing. Here are the five categories:

### 1. Puffed-up content

AI loves making things sound more important than they are. "A pivotal milestone" when it could just say "a turning point." "Experts believe" without naming any expert.

### 2. Robot vocabulary

AI has favorite words. You've probably noticed them: "delve," "crucial," "enhance," "landscape," "foster," "underscore." Humanizalo swaps these for normal words.

### 3. Predictable structures

AI loves patterns like "Not X. Y." or giving human actions to things that aren't human ("the data tells us" instead of "we looked at the data and found"). It also forces everything into groups of three.

### 4. Formatting giveaways

Em dashes everywhere (those long dashes). Bold text on everything. Title Case On Every Heading. Humanizalo strips these out.

### 5. Chatbot habits

"I hope this helps!" "Great question!" "As of my last update..." "It's worth noting that..." These scream "a chatbot wrote this." Gone.

---

## The secret sauce: it checks its own work

Most tools rewrite once and call it done. Humanizalo rewrites, then asks itself "does this still sound like AI?" and fixes what it finds. It does this up to 3 times.

It also scores the result on 6 qualities (directness, rhythm, trust, authenticity, density, and soul) on a scale of 1-10 each. If the total is below 42 out of 60, it keeps going.

---

## What you get back

When Humanizalo finishes, you get:

1. **Your humanized text** - the final version
2. **A score** - how human it sounds (out of 60)
3. **What changed** - a short summary of what it fixed

---

## The full pattern list

For the curious, here are all 40 patterns it catches:

| # | What it catches | Type |
|---|----------------|------|
| P01 | Making things sound more important than they are | Content |
| P02 | Dropping famous names without real citations | Content |
| P03 | Fake-deep "-ing" words (showcasing, highlighting) | Content |
| P04 | Sales-y language (stunning, groundbreaking, vibrant) | Content |
| P05 | "Experts say" without naming experts | Content |
| P06 | "Despite challenges... continues to thrive" | Content |
| P07 | "The future looks bright" type endings | Content |
| P08 | Vague big statements ("The stakes are high") | Content |
| P09 | AI-favorite words (delve, landscape, tapestry, etc.) | Vocabulary |
| P10 | "Serves as" instead of "is" | Vocabulary |
| P11 | Too many adverbs (really, genuinely, fundamentally) | Vocabulary |
| P12 | Business buzzwords (synergy, deep dive, lean into) | Vocabulary |
| P13 | "Every," "always," "never" (sweeping claims) | Vocabulary |
| P14 | Too many hyphenated pairs (cross-functional, data-driven) | Vocabulary |
| P15 | "Not X. Y." dramatic contrasts | Structure |
| P16 | "Not a... Not a... A..." build-ups | Structure |
| P17 | "Speed. That's it. That's the thing." fragments | Structure |
| P18 | "What if I told you..." setups | Structure |
| P19 | Things doing human actions ("the data tells us") | Structure |
| P20 | Floating narrator voice ("People tend to...") | Structure |
| P21 | Passive voice ("Mistakes were made") | Structure |
| P22 | "Not just X, it's Y" constructions | Structure |
| P23 | Forcing everything into groups of three | Structure |
| P24 | Using different words for the same thing to avoid repeating | Structure |
| P25 | "From X to Y" fake ranges | Structure |
| P26 | Every sentence the same length | Structure |
| P27 | Em dashes everywhere (those long dashes) | Formatting |
| P28 | Bold text on everything | Formatting |
| P29 | Random emojis in serious text | Formatting |
| P30 | Fancy curly quote marks | Formatting |
| P31 | Title Case On Every Heading | Formatting |
| P32 | "I hope this helps!" chatbot phrases | Communication |
| P33 | "As of my last update..." disclaimers | Communication |
| P34 | Over-the-top niceness and agreement | Communication |
| P35 | "Here's the thing:" throat-clearing | Communication |
| P36 | "Let that sink in." emphasis tricks | Communication |
| P37 | "In this section, we'll..." narrating the structure | Communication |
| P38 | "I promise" and "this is genuinely hard" | Communication |
| P39 | "In order to" instead of just "to" | Communication |
| P40 | Stacking hedges ("could potentially possibly maybe") | Communication |

---

## Files in this project

```
humanizalo/
├── SKILL.md              # The brain (Claude reads this)
├── README.md             # You are here
├── README.es.md          # This file in Spanish
├── LICENSE               # MIT (use it however you want)
└── references/
    ├── vocabulary.md     # Lists of AI words and their replacements
    ├── structures.md     # Structural patterns to avoid
    ├── formatting.md     # Formatting rules
    ├── communication.md  # Chatbot habits to remove
    └── examples.md       # 5 before/after examples
```

---

## License

MIT. Use it, modify it, share it.
