---
name: bip
description: Use this when the day is over and tonight's post is not written. The founder says "/bip", "write today's post", "today's post", or on Sunday "/bip sunday" or "write this week's post". They type one messy message (what I did today, what went well, what did not, what I would change) and it writes one build-in-public post on the lesson spine, in their own words, sized to the one platform they picked once (LinkedIn, X or Threads), "Day N of Execution Squad" last, then stops for their yes. Sunday is the same post about the week, "Week N of Execution Squad" last. It never posts anywhere; the founder's hand does.
---

# bip

**Take one messy message about today and write the post: a hook a stranger would stop on, what I did today, what did not work, what I do about it, the one thing it taught, `Day N of Execution Squad` last.** The founder reads it, changes any word, says yes, and posts it by hand on the one platform they picked.

The post is an insight, not a receipt and not a diary. A stranger who reads only the first line should learn something, and a stranger who reads all of it should want to save one line. Every fact in it comes from tonight's message; nothing is read from anywhere else. On Sunday the same skill writes the same post about the week, and it never adds anything up.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance file every member-run skill reads first (founder name, voice sample, talk to me), and its values win over the `squad/` paths written below, which are worked examples. A row reading "(none yet)" is an unanswered field, not an override: the worked-example path stands until a run fills it. The install lesson (g2) creates the file; this skill adds 2 rows the first time it runs, `term day 1` and `post platform`.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE ROOTS | AUTO: the install check, the roots file, the count. First run only, HUMAN INPUT: the date of the hello and the platform, 2 questions in one message, written once |
| 1 THE DAY | HUMAN INPUT: tonight's one message. **STOP · GATE, the only one:** nothing that happened in it, one question, then write |
| 2 THE POST | AUTO: one post on the spine, sized to the platform, printed once, then the one hand-off line |
| 3 THE YES | **STOP:** the founder reads it, changes any word, says yes; the file is saved; posting is their hand |

The beat numbers ARE the step numbers below. One gate, one stop. Never a second question at the gate, never the file before the yes, never a post anywhere.

**Resuming.** The rule keys on the OUTPUTS, never on what a session remembers.

| Missing or incomplete | Resume at |
|---|---|
| `.claude/squad-roots.md` has no `term day 1` row or no `post platform` row, or either reads (none yet) | beat 0: ask for the missing row only |
| `squad/posts/<today>.md` does not exist | beat 1: the founder types the day |
| today's file holds one of the two posts and the founder asked for the other | beat 1, the one that is missing. On the yes both live in the same file, the week's post on top |
| `squad/posts/<today>.md` exists and the line above its first `## The input` is the signature this run would write (`Day` for a day run, `Week` for a Sunday run) | done. A re-run on the same date says so and overwrites only after a yes |

`/bip sunday` and "write this week's post" name their own mode; the table picks the mode only for a bare `/bip`.

## The outputs (1 file, and 2 rows once)

1. `squad/posts/YYYY-MM-DD.md`: the post verbatim, then the raw message under `## The input`. Sunday's file holds the weekly post, and its signature line begins `Week`. A date that carries both posts keeps the week's on top, a `---` line between them.
2. `.claude/squad-roots.md`: the `term day 1` and `post platform` rows, written on the first run and never again.

Nothing else gets written.

## Beat 0 · The roots

**A self-check first.** `references/post-cage.md`, next to this `SKILL.md`, must open. If it is missing, stop and tell the founder to finish the install: copy the whole skill folder, `references/` included.

Then read `.claude/squad-roots.md`: `founder name`, `voice sample`, `talk to me`, `term day 1`, `post platform`. No roots file at all means the install (g2) did not finish; say so in one line and stop.

**First run only.** Either row missing or reading (none yet): ask for what is missing, both in one message when both are, and never again:

1. What date did you post your hello? (today, if you have not yet)
2. Which platform is yours: LinkedIn, X or Threads? (If it is X, say so when the account is Premium.)

Write the rows as answered:

| Field | Value |
|---|---|
| term day 1 | YYYY-MM-DD |
| post platform | LinkedIn, X or Threads. `X, Premium` when the founder says their account is Premium |

Threads here is Meta's Threads, the founder's own account. The squad's Threads page at aichrislee.com/threads is a different place: it keeps the hello (g1) and the hot seat, and the daily post does not go there.

**Then the count**, from the laptop's own date: `Day N = today minus term day 1, plus 1` (the hello is Day 1), and `Week N = Day N divided by 7, rounded up`. The count does not stop at 180. A run started before 4 in the morning is the night before: use yesterday's date for the count and for the file, and say which date it used in one line.

Nothing else is read, on any day: not `squad/business.md`, not `squad/pipeline.md`, not earlier posts. The post is tonight's message and nothing more.

## Beat 1 · The day

The founder types one message, any order, any language, messy: what I did today, what went well, what did not, what I would change. Numbers only when the founder said them. Sort it yourself; never ask them to.

| The founder says | Goes to |
|---|---|
| what I did today | the credibility line, one concrete line |
| what went well | the hook, or the insight |
| what did not, what was hard | the problem |
| what I would change, what I do tomorrow | the move |
| what it taught, how it felt | the insight, or the hook |

**The one gate.** It fires only when the message has nothing that happened in it: no thing done, no thing that broke, no thing learned. "Worked on stuff" fires it. "Sent nothing today, I froze at the ask" does not; that is a day, and the freeze is the post. One question:

> What did you actually do today, and what did it teach you?

Then write. Never a lecture, never a second question. A thin answer gets a short post, never another question.

**Sunday.** `/bip sunday` or "write this week's post" takes the same message about the week: what shipped, what worked, what did not, the one change for next week. Same sort, same gate, with the question in week form: "What did you actually do this week, and what did it teach you?" Nothing is read from the week's files and nothing is added up; the week is what the founder says it was.

## Beat 2 · The post

Write the 6 beats in `references/post-cage.md`, in that order, and nothing else:

1. **The hook.** The day's lesson or the day's event, written for a stranger, under about 12 words. It is the only line most readers see.
2. **The credibility line.** What I did today, one line, concrete.
3. **The problem.** What did not work, or what was hard. One or two lines.
4. **The move.** What I did about it, or what I change tomorrow.
5. **The insight.** The one thing it taught, one line. The line a stranger would save.
6. **The signature.** `Day N of Execution Squad`. Last, always.

Short lines, a blank line between beats, no labels on the lines. The voice is the founder's: their words from the message, the tone the roots file's `talk to me` row sets, their rhythm from the voice sample. The language is the language of tonight's message; "in English" said in the message is enough to switch.

**The length follows the platform**, off the `post platform` row:

| Platform | The post |
|---|---|
| LinkedIn | 120 to 250 words, all 6 beats. The first 200 characters carry the hook, because LinkedIn cuts there on a desktop and sooner on a phone |
| Threads | under 500 characters, the same 6 beats compressed to a line each |
| X | under 280 characters: the hook, the insight, the signature. A founder who said their account is Premium gets the LinkedIn length |

The writing rules in `references/post-cage.md` are applied to the draft, never bounced back as questions: nothing the founder did not say (no name, no number, no need), numerals, no hashtag, no link, no emoji unless the voice sample has them, none of the banned words.

**Sunday.** The same 6 beats about the week, `Week N of Execution Squad` last. The hook is the week's lesson; the credibility line is what shipped this week; the move is the one change for next week, in the founder's words, and that line is what the 90-day plan's Decide column takes on Sunday (g8).

Then print the post once, plain, ready to copy, and under it one line and nothing else:

> Post it on <platform>.

`<platform>` is the name only, LinkedIn, X or Threads. A `post platform` row reading `X, Premium` prints "Post it on X."

## Beat 3 · The yes

The founder reads it and changes any word; their yes is the edit. On the yes, save `squad/posts/YYYY-MM-DD.md`: the post verbatim, a blank line, `## The input`, the raw message verbatim. A file for today already there: say so, overwrite after a yes. The one exception is a file that already holds the other post: both stay, the week's post and its input on top, a `---` line between, and the post that was already there is not rewritten.

A no is a changed line, never a menu: reprint only the line the founder changed, alone. Then it is their hand, on their platform. Nothing else happens here.

## Rules

- Never posts, never sends, never books, never opens the platform or a browser. The post leaves through the founder's hand.
- Every message to the founder is scannable: the post, then one line. Never a wall of paragraphs at 11 at night.
- Never a name, a number or a need the founder did not say. Never a price: the post teaches, it does not pitch, and the price belongs to `squad/business.md`, not to this post.
- No count is required. A day with no number in it is a full post, and a number appears only when the founder gave it.
- The signature is last, always. A post that opens on "Day 12" is the shape that dies.
- A line the founder quotes (a reply, a buyer's words) stays verbatim, in the post and in the file.
- One question at the gate, 2 first-run questions in one message, nothing else asked, ever.
- Never adds up a week. Sunday's post is the founder's read of the week, not a sum.
