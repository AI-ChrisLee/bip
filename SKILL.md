---
name: bip
description: Use this when the day is over and tonight's post is not written. The founder says "/bip", "write today's post", "today's post", or on Sunday "/bip sunday" or "write this week's post". They dump the day in one messy message (what I did, what happened, what I learned, what I would never do again, how it felt) and it writes one build-in-public post in the viral text form (a hook, the turn, a numbered list, a close, "Day N of Execution Squad" last), draws the hand-written notebook page that goes with it through fal, and stops for their yes. Sunday is the same post about the week, "Week N of Execution Squad" last. It never posts anywhere; the founder puts the text and the drawing on the squad's Threads, then on the one platform they picked.
---

# bip

**Take one messy message about today and write the post a stranger stops on: a hook, 2 or 3 lines that turn it, a numbered list of what the day taught, a close, `Day N of Execution Squad` last. Then draw the page: a photo of an open notebook with the hook underlined as the title, the subject in the centre, and a branch for every list item.** The founder reads both, changes any word, says yes, and posts them by hand.

The post is the day's story, told the way the biggest build-in-public accounts tell theirs: a claim, a turn, a list, a line worth saving. Every fact in it comes from tonight's message and nothing is read from anywhere else. On Sunday the same skill writes the same post about the week.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance file every member-run skill reads first (founder name, voice sample, talk to me). The install lesson (g2) creates the file; this skill adds 1 row the first time it runs, `term day 1`. The drawing needs a fal key; it lives in the company folder's `.env` as `FAL_KEY`, the same file and the same name the Proven Package reads (c2), so one key serves both.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE ROOTS | AUTO: the install check, the roots file, the count. First run only, HUMAN INPUT: the date of the hello, asked once. No `FAL_KEY` in `.env`: the key is asked once, in the same message, and written to `.env` when it comes; never a stop |
| 1 THE DUMP | HUMAN INPUT: tonight's one message, the day as it happened. **STOP · GATE, the only one:** nothing that happened in it, one question, then write |
| 2 THE POST | AUTO: one post in the form `references/post-cage.md` sets |
| 3 THE DRAWING | AUTO: the prompt built off the post, one fal call, `squad/posts/YYYY-MM-DD.png` |
| 4 THE YES | **STOP:** the post and the drawing in front of the founder, the hand-off under them. "Again" remakes the drawing once; a changed line is reprinted alone; the yes saves the file |

The beat numbers ARE the step numbers below. One gate, one stop. Never a second question at the gate, never the `.md` before the yes, never a post anywhere.

**Resuming.** 2 checks, on the files, never on what a session remembers. No `.claude/squad-roots.md`: the install (g2) did not finish; say so in one line and stop. `/bip` with no day in the message when `squad/posts/<the effective date>.md` already exists: print it (and the drawing's path when the png is there), then one line, "Tonight's post is saved. Type the day again to rewrite it." A message that carries the day runs the whole run again: beat 3 overwrites the png, the yes overwrites the .md.

`/bip sunday` and "write this week's post" name the week. A bare `/bip` whose effective date (the one beat 0 computed, yesterday's when the run started before 4 in the morning) falls on a Sunday is `/bip sunday`: Sunday's post is the week's post, and its `Week N = Day N divided by 7, rounded up`.

## The outputs (2 files a day, and 2 lines once)

1. `squad/posts/YYYY-MM-DD.md`: the post verbatim, nothing else.
2. `squad/posts/YYYY-MM-DD.png`: the drawing, 1024x1536.
3. `.claude/squad-roots.md`: the `term day 1` row, written on the first run and never again.
4. `.env` in the company folder: the `FAL_KEY=` line, written once when the founder pastes the key, never printed back, never copied anywhere else.

Nothing else gets written.

## Beat 0 · The roots

**A self-check first.** `references/post-cage.md` and `references/image-cage.md`, next to this `SKILL.md`, must open. If either is missing, stop and tell the founder to finish the install: copy the whole skill folder, `references/` included.

Then read `.claude/squad-roots.md`: `founder name`, `voice sample`, `talk to me`, `term day 1`.

**The key.** Look for a `FAL_KEY=` line in `.env` in the company folder. No `.env`, or no line in it, means no key: the ask below on a first run.

**First run only.** The `term day 1` row missing: ask for the date, and when `.env` has no `FAL_KEY` either, ask for the key in the same message. One message, never again:

1. What date did you post your hello? (today, if you have not yet)
2. Paste your fal key and I draw the page every night (free account at fal.ai, the key at fal.ai/dashboard/keys, about 5 cents a drawing). Skip it and the post still comes.

Write what came:

| Field | Value |
|---|---|
| term day 1 | YYYY-MM-DD, in `.claude/squad-roots.md` |
| FAL_KEY | the key, as `FAL_KEY=<key>` in `.env` (create the file when it is not there; a `FAL_KEY=` line already in it is replaced, never a second one added) |

Then one line:

> Now type the day, messy, any order: what I did, what happened, what I learned, what I would never do again, how it felt.

The type-the-day clause only when no message this run carried the day, else write from the one that did. A key pasted at any later point is written the same way, once, and the drawing is made that same run.

**Then the count**, from the laptop's own date: `Day N = today minus term day 1, plus 1` (the hello is Day 1). The count does not stop at 180. A run started before 4 in the morning is the night before: use yesterday's date for the count and for the files, and say which date it used in one line.

Nothing else is read, on any day: not `squad/business.md`, not `squad/pipeline.md`, not earlier posts. The post is tonight's message and nothing more.

## Beat 1 · The dump

The founder types one message, any order, any language, messy: what I did, what happened, what I learned, what I would never do again, how it felt. It is the day as it happened, told to a friend. Numbers only when the founder said them, and no count is ever asked for. Sort it yourself; never ask them to.

| The founder says | Goes to |
|---|---|
| what happened (the result, the reply, the number when they said one) | the hook, a number first when there is one |
| what I did | the re-hook lines, or a list item |
| what I learned | the list: each lesson a title line and 1 or 2 lines under it |
| what I would never do again | the last item, or the close |
| how it felt | the re-hook, or the close |

**The one gate.** It fires only when the message has nothing that happened in it: no thing done, no thing that broke, no thing learned. "Worked on stuff" fires it. "Sent nothing today, I froze at the ask" does not; that is a day, and the freeze is the post. One question:

> What did you actually do today, and what did it teach you?

Then write. Never a lecture, never a second question. A thin answer gets a short list, never another question.

**Sunday.** The same message about the week: what shipped, what worked, what did not, the one change for next week or the number you are holding for. Same sort, same gate in week form (`references/post-cage.md`, The one gate).

## Beat 2 · The post

Write the form in `references/post-cage.md`, in this order, and nothing else:

1. **The hook.** One line, a claim or an observation, under about 50 characters. A number first when the dump has one. It is the only line most readers see.
2. **The re-hook.** 2 or 3 one-line paragraphs that turn the claim.
3. **The turn line.** "Here is what I learned:" or a line like it, ending in a colon.
4. **The list.** 3 to 10 numbered items, each a short title line and 1 or 2 lines under 20 words.
5. **The close.** 2 one-line paragraphs, the last one a line a stranger would save.
6. **The signature.** `Day N of Execution Squad`. Last, always.

Single-line paragraphs, a blank line between every one, 900 to 1,500 characters, no hashtag, no link, no emoji, numerals. The voice is the founder's: their words from the message, the tone the roots file's `talk to me` row sets, their rhythm from the voice sample. The language is the language of tonight's message; "in English" said in the message is enough to switch.

The writing rules in `references/post-cage.md` are applied to the draft, never bounced back as questions: nothing the founder did not say (no name, no number, no need), numerals, none of the banned words.

**Sunday.** Same run, week form, `Week N of Execution Squad` last. The rules are in `references/post-cage.md`, Sunday.

## Beat 3 · The drawing

Build the prompt in `references/image-cage.md` off the post: an open lined notebook shot from above, the hook underlined as the title, the post's subject in the centre in yellow marker, one yellow branch per list item (2 to 4 words a label, an arrow into the centre), 2 short plain lines under each branch, 2 or 3 words each, off that item's own lines, a page number at the bottom. Then one call to fal's `openai/gpt-image-2` (1024x1536, quality medium, png), the key loaded from `.env` first, and the image lands at `squad/posts/YYYY-MM-DD.png`.

**No key** (no `FAL_KEY=` line in `.env`): no drawing, and nothing stops.

A call that comes back without an image is tried once more, then one line says the drawing did not come back tonight, and the run carries on to the yes.

## Beat 4 · The yes

Print the post once, plain, ready to copy. When beat 3 made a drawing, open it for the founder (macOS `open`, Windows `explorer`, Linux `xdg-open` on the png) and name its path in one line; with none, the hand-off drops its attach clause. Under them, the hand-off, and nothing else:

> Say yes and I save it, or change any line. Then post it: aichrislee.com/threads, Accountability, the drawing attached from squad/posts/YYYY-MM-DD.png.

On a Sunday, and only then, one more line under it:

> Then put the week in your plan: say `Put this in week <your plan's week, 1 to 4>'s Measure: <your 2 numbers> / Improve: <the close's first line, printed verbatim>`.

The founder reads and answers with one of 3 things:

- **A changed line.** Reprint only that line, alone. A changed hook or list title is on the page, so the drawing is remade with the new words; that remake is not the "again".
- **"Again."** The drawing is remade once, the same words. A typo in the handwriting is the reason to say it. A second "again" gets one line: the words are right, the pen is the pen; post it or change a line.
- **The yes.** Save `squad/posts/YYYY-MM-DD.md`: the post verbatim, nothing else, and say the path in one line. A file already there for this date is overwritten by this yes; nothing else is asked.

Then it is their hand. Nothing else happens here.

## Rules

- Never posts, never sends, never books, never opens a platform. The post leaves through the founder's hand.
- Every message to the founder is scannable: the post, the drawing's path, the hand-off. Never a wall of paragraphs at 11 at night.
- Never a name, a number or a need the founder did not say. Never a price: the post teaches, it does not pitch, and the price belongs to `squad/business.md`, not to this post.
- No count is ever asked for. A day with no number in it is a full post, and a number appears only when the founder gave it.
- The signature is last, always. A post that opens on "Day 12" is the shape that dies.
- A line the founder quotes (a reply, a buyer's words) stays verbatim, in the post and in the file.
- One question at the gate, 2 first-run questions in one message, nothing else asked, ever.
- The key is never printed back, never put in any file but `.env`, never sent anywhere but fal.
