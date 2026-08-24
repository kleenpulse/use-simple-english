# use-simple-english

Rewrite text into simple, honest English that sounds like a real person wrote it. Not impressive. Believable.

Built for non-native English speakers who need their writing to match their real voice: job application answers, employer questions, emails, messages. If you cannot say the sentence out loud in an interview, this skill will not let it ship.

## Install

```bash
npx skills add kleenpulse/use-simple-english
```

Works with Claude Code, Codex, Cursor, Copilot, and anything else that reads `SKILL.md`.

## Why this one

Most "improve my writing" prompts make text fancier. That is the opposite of what a non-native speaker filling out a job application needs. A voice that does not match its owner raises suspicion, and interviewers ask people to explain their own words live.

The core rule is the **believability test**: every sentence must be something the owner can say out loud, from memory, without stumbling. Simple and honest beats impressive and borrowed.

## What it does

- Rewrites text with short sentences, common words, and active voice
- Bans em-dashes and resume-bot vocabulary (consolidated, leverage, orchestrated, robust)
- Keeps the facts that prove the story is real: numbers, failure stories, tradeoff sentences
- Always delivers two labeled options: simplest, and slightly more technical
- Mirrors a form question's own structure (Context / Contribution / Why difficult / Learnings) so reviewers find every part instantly

## What it refuses to do

- Invent specifics to look concrete
- Delete numbers, tradeoffs, or contrast sentences while "simplifying"
- Apply itself to legal text, compliance docs, or marketing copy that wants polish

## Usage

- "Simplify this, my English isn't good enough to speak this well: ..."
- "Answer this question from an employer, keep it in my voice"
- "Make this email sound like me, not like an AI"
- "Rewrite my cover letter so I could defend every sentence in an interview"

## Attribution

Forked in spirit from [AminBlg/SimpleEnglish](https://github.com/aminblg/simpleenglish) (ASD-STE100, MIT). That skill writes like an aerospace manual so no one can misread it. This one writes like the person who owns the words so anyone can believe it.

## License

MIT
