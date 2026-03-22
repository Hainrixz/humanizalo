# Before and after examples

These examples demonstrate the full audit loop: original text, draft rewrite, self-interrogation, and final version.

---

## Example 1: Encyclopedic article

### Original
> Founded in 1987, the Springfield Community Center has served as a vital hub for local residents, offering a diverse tapestry of programs and services. The center has garnered significant recognition for its innovative approach to community engagement, earning accolades from numerous organizations. Nestled in the heart of downtown Springfield, the facility boasts state-of-the-art amenities that cater to individuals of all ages. Despite facing challenges related to funding and infrastructure, the center continues to thrive, underscoring its enduring commitment to fostering community well-being. Experts highlight the center's pivotal role in enhancing the social fabric of the region, serving as a testament to the power of collective action.

### Draft rewrite
> The Springfield Community Center opened in 1987. It runs after-school programs, senior fitness classes, and a food bank that feeds about 200 families a week. The building got a new gym and computer lab in 2019 after a bond measure passed. Funding is tight. The city cut its allocation by 15% last year, and the roof needs replacing. People keep showing up anyway.

### Self-interrogation
- "People keep showing up anyway" is slightly punchy-ending (P26) but acceptable here since the rest varies.
- No remaining AI patterns detected.

### Score
| Dimension | Score |
|-----------|-------|
| Directness | 9 |
| Rhythm | 8 |
| Trust | 9 |
| Authenticity | 8 |
| Density | 9 |
| Soul | 7 |
| **Total** | **50/60** |

### Changes made
Removed: significance inflation (P01), promotional language (P04, "nestled," "state-of-the-art"), vague attributions (P05, "experts highlight"), copula avoidance (P10, "served as," "boasts"), formulaic challenges section (P06), AI vocabulary (P09, "garnered," "pivotal," "fostering," "testament," "underscore," "enduring," "tapestry"). Replaced with specific facts (200 families, 15% cut, 2019 renovation).

---

## Example 2: Blog post / essay

### Original
> Here's the thing: building products is hard. Not because the technology is complex — though it often is — but because people are complex. Let that sink in. In today's fast-paced landscape, we need to lean into discomfort and navigate uncertainty with clarity. The uncomfortable truth is that nobody wants to admit they're confused. And that's okay. What if I told you that the best teams don't optimize for productivity? Here's what I mean: they optimize for learning. Think about it. The implications are significant.

### Draft rewrite
> Building products is hard because people are hard to predict. Technology, you can debug. People, not so much. Most teams I've worked with avoid admitting confusion. They optimize dashboards and sprint velocity instead of asking "do we even understand the problem?" The teams that ship good work tend to treat confusion as information, not failure.

### Self-interrogation
- Clean. No binary contrasts, no throat-clearing, no em dashes.
- "not so much" is conversational and human.
- Good rhythm variation.

### Score
| Dimension | Score |
|-----------|-------|
| Directness | 9 |
| Rhythm | 8 |
| Trust | 9 |
| Authenticity | 8 |
| Density | 9 |
| Soul | 8 |
| **Total** | **51/60** |

### Changes made
Removed: throat-clearing opener (P35, "Here's the thing:"), binary contrast (P15), em dashes (P27), emphasis crutch (P36, "Let that sink in"), business jargon (P12, "landscape," "lean into," "navigate"), rhetorical setup (P18, "What if I told you," "Think about it"), vague declarative (P08, "The implications are significant"), unnecessary permission (P18, "And that's okay"). Compressed from 89 words to 63 while adding specific detail.

---

## Example 3: Business communication

### Original
> I wanted to take a step back and provide a comprehensive overview of our Q3 performance. The team has done a commendable job navigating the challenges of the current market landscape. Moving forward, it is crucial that we double down on our core competencies and leverage our cross-functional capabilities to drive impactful results. Additionally, I'd like to highlight the importance of aligning our strategic objectives with the evolving needs of our stakeholders. In order to ensure seamless execution, we need to foster a culture of accountability and continuous improvement. The future looks bright, and I'm genuinely excited about what lies ahead.

### Draft rewrite
> Q3 numbers: revenue up 12%, churn down to 3.2%. Two things to focus on next quarter. First, the enterprise pipeline is thin. We need three more qualified deals by mid-November or Q4 misses target. Second, the handoff between sales and onboarding is still dropping customers. Sarah's team is mapping that process this week. I'll share the updated plan Friday.

### Self-interrogation
- Clean. Specific numbers, named person, concrete deadline.
- No jargon, no filler, no hedging.

### Score
| Dimension | Score |
|-----------|-------|
| Directness | 10 |
| Rhythm | 8 |
| Trust | 10 |
| Authenticity | 8 |
| Density | 10 |
| Soul | 7 |
| **Total** | **53/60** |

### Changes made
Removed: filler phrases (P39, "In order to," "I wanted to take a step back"), business jargon (P12, "navigate," "landscape," "double down," "leverage," "cross-functional," "impactful," "moving forward," "stakeholders," "seamless"), AI vocabulary (P09, "comprehensive," "commendable," "crucial," "highlight," "aligning," "foster"), generic positive conclusion (P07, "The future looks bright"), performative emphasis (P38, "genuinely excited"), adverb (P11, "genuinely"). Replaced with specific metrics, names, and deadlines.

---

## Example 4: Technical writing

### Original
> The authentication module serves as a crucial component of the system architecture, providing a robust and seamless login experience for end users. It leverages industry-leading encryption standards to ensure the security and integrity of user data. The module encompasses a multifaceted approach to identity verification, including multi-factor authentication, biometric scanning, and token-based session management. Additionally, the framework has been meticulously designed to foster interoperability with third-party identity providers, showcasing the system's commitment to flexibility and scalability.

### Draft rewrite
> The auth module handles login. It encrypts passwords with bcrypt, verifies identity through MFA or biometrics, and manages sessions with JWTs that expire after 24 hours. It also connects to third-party identity providers (Google, Okta, SAML) through a standard OAuth2 flow. Config lives in auth.config.yaml.

### Self-interrogation
- Clean. Specific technical details replace every vague claim.
- No AI vocabulary, no jargon, no copula avoidance.

### Score
| Dimension | Score |
|-----------|-------|
| Directness | 10 |
| Rhythm | 7 |
| Trust | 10 |
| Authenticity | 8 |
| Density | 10 |
| Soul | 6 |
| **Total** | **51/60** |

### Changes made
Removed: copula avoidance (P10, "serves as"), AI vocabulary (P09, "crucial," "robust," "seamless," "encompasses," "multifaceted," "meticulous," "foster," "showcasing," "leverage"), hyphenated word pair (P14, "industry-leading"), business jargon (P12, "scalability"), promotional language (P04). Replaced with specific technologies (bcrypt, JWT, OAuth2, SAML), concrete config (24-hour expiry, auth.config.yaml), and named providers.

---

## Example 5: Full audit loop demonstration

### Original
> In today's rapidly evolving technological landscape, artificial intelligence stands as a transformative force that is fundamentally reshaping how we approach creative work. Not only does AI enhance productivity, but it also fosters new forms of artistic expression — from generative art to AI-assisted music composition. However, it is important to note that this transformation is not without its challenges. Artists and creators have raised concerns about issues of authenticity, copyright, and the potential displacement of human creativity. Despite these challenges, the creative industry continues to embrace AI, underscoring the technology's enduring appeal. Experts highlight that the key lies in finding the right balance between human intuition and machine capability. The future of creative AI looks bright, promising a vibrant tapestry of human-machine collaboration.

### Pass 1: Draft rewrite
> AI is changing creative work. Tools like Midjourney and Suno let people generate images and music in minutes that used to take hours or days. Some artists use these as starting points, feeding outputs back into their own process. Others see them as a threat. The copyright questions are real and unresolved. When an AI trains on millions of images and produces something that looks like a specific artist's style, who owns what? Courts are still figuring this out. The tech isn't going away, but the rules around it haven't caught up.

### Pass 2: Self-interrogation
- "The tech isn't going away" (P19, slight false agency, but borderline acceptable as colloquial)
- "but the rules around it haven't caught up" (P19 again, rules don't literally catch up)
- Otherwise clean. Good specificity, human voice, varied rhythm.

### Pass 3: Final rewrite
> AI is changing creative work. Midjourney and Suno let people generate images and music in minutes. Some artists feed these outputs back into their own process as starting material. Others see the whole thing as a threat to their livelihood. The copyright questions are real. When someone trains an AI on millions of images and it produces something in a specific artist's style, who owns that? Courts are still working through it. People will keep using these tools. Lawmakers and judges haven't figured out the boundaries yet.

### Final score
| Dimension | Score |
|-----------|-------|
| Directness | 9 |
| Rhythm | 9 |
| Trust | 9 |
| Authenticity | 8 |
| Density | 9 |
| Soul | 8 |
| **Total** | **52/60** |

### Changes made across all passes
**Pass 1 removed:** AI vocabulary (P09, "landscape," "transformative," "foster," "underscore," "enduring," "vibrant," "tapestry"), copula avoidance (P10, "stands as"), negative parallelism (P22, "Not only... but also"), em dash (P27), filler (P39, "it is important to note"), vague attribution (P05, "experts highlight"), formulaic challenges section (P06), generic positive conclusion (P07).

**Pass 3 fixed:** False agency (P19, "tech isn't going away" -> "People will keep using these tools," "rules haven't caught up" -> "Lawmakers and judges haven't figured out the boundaries"). Added human actors to every sentence.
