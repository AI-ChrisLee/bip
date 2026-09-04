---
name: bip
description: Use this when the day is over and tonight's post is not written. The founder says "/bip", "write today's post", "today's post", or on Sunday "/bip sunday" for the weekly post. They type one messy message (what went out, sent / replies / calls / money, what it taught or how it felt) and it writes the 5-line build-in-public post in their own words, "Day N of Execution Squad" last, then stops for their yes. On Sunday it adds up the week's numbers and writes the weekly post. It never posts anywhere; the founder's hand does.
---

# bip

**Take one messy message about today and write the post: what today taught in one line, what shipped, the 4 numbers, what is stuck, `Day N of Execution Squad` last.** The founder reads it, changes any word, says yes, and posts it by hand.

The post is a receipt, not a diary. Every noun and every count in it comes from tonight's message, and nothing is read from anywhere else on a weekday. A zero day is a post. On Sunday the same skill adds up the week and writes the weekly post, the one place the week's numbers get summed.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance file every member-run skill reads first (founder name, voice sample, talk to me), and its values win over the `squad/` paths written below, which are worked examples. A row reading "(none yet)" is an unanswered field, not an override: the worked-example path stands until a run fills it. The install lesson (g2) creates the file; this skill adds one row, `term day 1`, the first time it runs.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE ROOTS | AUTO. First run only, one question: the date of the hello |
| 1 THE DAY | HUMAN INPUT: tonight's one message. **STOP · GATE, the only one:** no count and no event in it, one question, then write |
| 2 THE POST | AUTO: the 5 lines, printed once, ready to copy |
| 3 THE YES | **STOP:** the founder reads it, changes any word, says yes; the file is saved; posting is their hand |

The beat numbers ARE the step numbers below. One gate, one stop. Never ask a second question at the gate, never save the file before the yes, never post.

**Resuming.** The rule keys on the OUTPUTS, never on what a session remembers.

| Missing or incomplete | Resume at |
|---|---|
| `.claude/squad-roots.md` has no `term day 1` row | beat 0 |
| `squad/posts/<today>.md` does not exist | beat 1: the founder types the day again |
| `squad/posts/<today>.md` exists | done. A re-run on the same date says so and overwrites only after a yes |

## The outputs (2 files; the second gets one row, once)

1. `squad/posts/YYYY-MM-DD.md`: the post verbatim, then the raw message under `## The input`. Sunday's file is the weekly post, and the post's last line begins `Week`.
2. `.claude/squad-roots.md`: the `term day 1` row, written on the first run and never again.

Nothing else gets written.

## Beat 0 · The roots

**A self-check first.** `references/post-cage.md`, next to this `SKILL.md`, must open. If it is missing, stop and tell the founder to finish the install: copy the whole skill folder, `references/` included.

Then read `.claude/squad-roots.md`: `founder name`, `voice sample`, `talk to me`, `term day 1`. No roots file at all means the install (g2) did not finish; say so in one line and stop.

`term day 1` missing: ask once, "What date did you post your hello? (today, if you have not yet)". Write the row and never ask again:

| Field | Value |
|---|---|
| term day 1 | YYYY-MM-DD |

Then the count, from the laptop's own date: `Day N = today minus term day 1, plus 1` (the hello is Day 1), and `Week N = Day N divided by 7, rounded up`. The count does not stop at 180.

Nothing else is read on a weekday: not `squad/business.md`, not `squad/pipeline.md`, not earlier posts. On Sunday, beat 2 reads the week's files in `squad/posts/` and nothing more.

## Beat 1 · The day

The founder types one message, any order, messy: what went out, what came back, what it taught or how it felt, and the 4 counts. g1 gave them the sentence: "Write today's post. Today: sent __, replies __, calls __, money $__, and the one thing I learned was __." Sort it yourself; never ask them to.

| The founder says | Goes to |
|---|---|
| what they did | `Shipped`, only when it went outward. A plan, a lesson watched, a file built is not a ship |
| the result | `Number`, and the noun in line one |
| how it felt, what it taught | line one, or `Stuck`, whichever it is |
| sent, replies, calls, money | `Number`, numerals, zero written as zero |

**The one gate.** It fires only when the message has no count (an explicit "nothing went out" IS a count, zero) and no event (nothing left the laptop, no name). One question:

> What went out today, and to whom? If nothing, what got stuck?

Then write. Never a lecture, never a second question. A count the founder did not mention prints as zero and gets named in beat 2's hand-off; it is never asked.

**Sunday.** `/bip sunday` takes the same message plus the 3 lines only the founder can say: the bottleneck, the one change for next week, the question for the hot seat. Tonight's 4 counts come off the message like any other night; the rest of the week comes off the files, so the gate reads the 3 lines instead. No bottleneck and no fix, one question: "What stopped the numbers this week, and what is the one thing you change next week?" Then write.

## Beat 2 · The post

Write the 5 lines in `references/post-cage.md`, in that order, with those labels, and nothing else. Line one is the day's number or event, under 20 words, written for a stranger. The voice is the founder's: their words from the message, the length and the tone the roots file sets. The language is the language of tonight's message; "in English" said in the message is enough to switch.

The writing rules in `references/post-cage.md` are applied to the draft, never bounced back as questions: no noun the founder did not say, no count above zero the founder did not say, no link, no hashtag, no emoji unless the voice sample has them, none of the banned words. No character cap: 5 lines, one line each, and the shape limits itself.

**Sunday.** Read the 7 dates ending today in `squad/posts/`. Add up the `Number` lines of every file whose post ends on a `Day` line; skip any file whose post ends on a `Week` line; a missing date adds nothing. Add tonight's own 4 counts, from the Sunday message, to that sum: Sunday's file is this weekly post, so today never gets a `Day` file of its own. Write the 6 Sunday lines from the reference: the week's story, the summed counts, the bottleneck, the fix, the question, `Week N of Execution Squad`.

Then print the post once, plain, ready to copy, and under it the hand-off:

- **Post it by hand.** On your squad's Threads page at aichrislee.com/threads, the Daily build-in-public type, no title. Then press LinkedIn on that post: it copies the text and opens LinkedIn; press Start a post and paste. On a phone, copy, then paste into the LinkedIn app. This skill never posts.
- **Defaults, when any:** "calls and money read zero; change them if not."
- **Sunday only:** how many files were summed and their dates, and "posted X of Y days" (the dated files in `squad/posts/`, tonight's counted, against Day N), said as a count, never a streak.

## Beat 3 · The yes

The founder reads it and changes any word; their yes is the edit. On the yes, save `squad/posts/YYYY-MM-DD.md`: the post verbatim, a blank line, `## The input`, the raw message verbatim. A file for today already there: say so, overwrite after a yes.

A no is a changed line, never a menu: re-print only the lines the founder changed. Then it is their hand: Threads, then LinkedIn. Nothing else happens here.

## Rules

- Never posts, never sends, never opens the platform or a browser. The post leaves through the founder's hand and the platform's LinkedIn button on their own Threads post.
- Every message to the founder is scannable: the post, then a short list. Never a wall of paragraphs at 11 at night.
- Never a count above zero the founder did not say. Zero is written as zero; the days that read zero are the ones that matter.
- Never a noun, a name or a need the founder did not say. Never a price: the post is a receipt, not a pitch, and `money $X` is a count.
- A line the founder quotes (a reply, a buyer's words) stays verbatim, in the post and in the file, where the date sits on the filename.
- One question at the gate, one first-run question, nothing else asked, ever.
