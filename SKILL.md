---
name: use-simple-english
description: Rewrite text into simple, honest English that sounds like a real person wrote it. Use for job application answers, emails, messages, READMEs, and any text that must be believable when spoken aloud, especially for non-native speakers who need writing to match their real voice. Triggers on "simplify this", "my english isn't good enough", "make this sound like me", "answer this question from an employer".
license: MIT (adapted from AminBlg/SimpleEnglish, MIT)
---

# Use Simple English: Write Like the Person Who Owns the Words

Rewrite text so its owner can say every sentence out loud without sounding like someone else. This matters most for non-native English speakers filling out job applications, writing to employers, or messaging colleagues. A voice that does not match its owner raises suspicion, and interviewers will ask the writer to explain their own words live.

This is not aerospace STE. STE optimizes for zero misreading. This skill optimizes for **believability**: the reader should picture a real person, and the writer should be able to defend every sentence in conversation.

## When to Use

- The user asks to simplify, shorten, or "de-fancy" text they will send as themselves
- Job application form answers, cover letters, employer questions, interview prep
- The user says their English is not good enough for a draft you wrote
- Emails, DMs, LinkedIn messages, README prose that should sound human

**Do not use for:** legal text, formal compliance docs, marketing copy that wants polish, or technical documentation that needs STE-style precision (use a stricter standard for those).

## Core Principle: The Believability Test

Read each sentence and ask: **can the owner say this out loud in an interview, from memory, without stumbling?**

If the sentence needs a thesaurus to produce, it fails. If a hiring manager would ask "did you write this yourself?", it fails. Simple and honest beats impressive and borrowed, every time.

## Voice Rules

1. Short sentences. One idea per sentence.
2. Common words over impressive ones. See the swap table.
3. **No em-dashes, ever.** Use a comma, a period, or the word "and". Em-dashes are the strongest AI-writing tell.
4. Active voice with a visible subject: "I built X", not "X was achieved".
5. Contractions are fine. They sound human. (This is the opposite of STE rule 4.2. Believability wins here.)
6. No hedging filler: basically, essentially, arguably, honestly, actually.
7. No stacked adjectives. One is enough: "a hard bug", not "a subtle, elusive, hard-to-reproduce bug".
8. Say what happened, not what it demonstrates: "the socket never connected", not "this demonstrated the importance of observability".
9. Prefer verbs to abstract nouns: "I cleaned up the code", not "I performed a consolidation".
10. It is fine to start sentences with So, But, And.
11. Numbers stay. "87 places" is proof of scale and costs nothing to say out loud.
12. If cutting a word loses a fact, keep the word. This is compression, not amputation.

### Word swaps (resume-bot → human)

| Resume bot | Human |
|---|---|
| consolidated | cleaned up, replaced, merged |
| leverage / utilize | use |
| divergent | different |
| orchestrated | set up, ran |
| architected | designed, built |
| spearheaded | led, started |
| robust | reliable |
| seamless | smooth, or delete it |
| streamlined | simplified |
| a seam / a layer of abstraction | one shared place, one shared module |
| facilitated | helped |
| implemented | built, added, wrote |
| subsequently | later, then |
| in order to | to |
| polish came from X | I got that polish by X |

If a word carries no fact, delete it instead of replacing it.

## What to Keep (Untouchables)

Rewrite the style, never the substance:

- **Numbers and scale.** "87 API handlers", "9 locales", "5 retry attempts". These are the proof that the story is real.
- **Concrete failure stories.** "The socket had never connected in production because of a wrong path" beats any adjective. Interviewers know invented answers have no failure stories.
- **The tradeoff sentence.** "Users sometimes see data a second old. For a dashboard that is fine. I would not do this for banking." Naming what a decision cost signals senior thinking. Never simplify it away.
- **Contrast structure.** "It was a rule from day one, not a cleanup at the end." The contrast IS the point of the sentence.
- Code, commands, product names, technology names, quoted strings, error messages.

Do not invent specifics to look concrete. If the source has no number, keep the general statement.

## Method

1. **Find the 2-3 facts that matter.** In any sentence or paragraph, most words are decoration around a few load-bearing facts (a number, a result, a decision).
2. **Rewrite around only those facts.** Everything else is a candidate for deletion.
3. **Apply the voice rules** and the swap table.
4. **Run the believability test.** Read each sentence as if speaking it in an interview.
5. **Deliver two options:** one simplest, one slightly more technical. Label them. The user picks the one that feels like them. Then say in one line which facts you kept and why.

## Structure Rule (for form questions)

When a question lists its parts ("Context, your exact contribution, why it was difficult, key learnings"), the answer uses those exact parts as labeled sections in the same order. A skimming reviewer must find every part instantly.

Inside each part: concrete stories beat adjectives. Two short failure stories outrank a paragraph of "it was very challenging".

## Worked Example

**Before (real output from this method's origin session):**

> Later, I consolidated 87 hand-rolled service calls into a single typed transport layer, which collapsed nine divergent forks of the same logic into one seam with consistent error handling.

**Option 1 (simplest):**

> Later, I cleaned up the code that talks to our backend services. Before, there were 87 places doing the same thing in slightly different ways. I replaced them all with one shared function, so error handling works the same everywhere.

**Option 2 (slightly more technical):**

> Later, I refactored how the app calls our backend services. 87 API handlers each had their own copy of the same logic. I moved it all into one shared module with consistent error handling.

What survived: the number 87 (proof of scale) and the result (one shared place, consistent errors). Everything else in the original was decoration.

## Self-Check Before You Deliver

1. Search the draft for em-dashes. Zero allowed.
2. Search for every word in the swap table's left column. Replace or delete each hit.
3. Read each sentence aloud (mentally). Any sentence the owner could not say from memory gets rewritten.
4. Confirm every number and concrete fact from the source survived.
5. Confirm two labeled options were delivered for rewrite requests.
6. If the question had listed parts, confirm the answer has the same labeled parts in the same order.

## Attribution

Forked in spirit from [AminBlg/SimpleEnglish](https://github.com/aminblg/simpleenglish) (ASD-STE100 skill, MIT). That skill makes text impossible to misread. This one makes text possible to own.
