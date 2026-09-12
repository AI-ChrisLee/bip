---
name: bip
description: Use this when the day is over and tonight's post is not written. The founder says "/bip", "write today's post", "today's post", or on Sunday "/bip sunday" or "write this week's post". They dump the day in one messy message and back comes one build-in-public post, "Day N of Execution Squad" last, with the hand-written notebook drawing that goes with it. Sunday is the same post about the week, "Week N of Execution Squad" last. It never posts anywhere; the founder puts the text and the drawing on the squad's Threads, then on the one platform they picked.
---

# bip

The first message of a fresh run opens with this line, once:

> This skill is a base. Once you have done it your way, tell your squad "update the skill to do it like this."

**One messy message about today goes in. One post comes out, and the notebook page drawn from it.** The founder reads both, changes any word, says yes. Their hand puts them on the squad's Threads and the one platform they picked.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance file every member-run skill reads first (founder name, voice sample, talk to me); g2 makes it, this skill adds the `term day 1` row. The drawing needs a fal key, `FAL_KEY` in the company folder's `.env`, the same key the Proven Package reads (c2).

## The outputs

1. `squad/posts/YYYY-MM-DD.md`: the post verbatim, nothing else.
2. `squad/posts/YYYY-MM-DD.png`: the drawing, 1024x1536.
3. `.claude/squad-roots.md`: the `term day 1` row, written on the first run and never again.
4. `.env` in the company folder: the `FAL_KEY=` line, written once when the founder pastes the key.

Nothing else gets written.

**Resuming.** Check the files, never what a session remembers. No `.claude/squad-roots.md`: the install (g2) did not finish, so say so in one line and stop. A bare `/bip` when `squad/posts/<the effective date>.md` already exists: print it (and the drawing's path when the png is there), then one line, "Tonight's post is saved. Type the day again to rewrite it." A message that carries the day runs again: beat 3 overwrites the png, the yes overwrites the .md.

`/bip sunday` and "write this week's post" name the week. A bare `/bip` whose effective date falls on a Sunday is `/bip sunday`, and its `Week N = Day N divided by 7, rounded up`.

## Beat 0 · The roots

`references/post-cage.md` and `references/image-cage.md`, next to this `SKILL.md`, must open. If either is missing, stop and tell the founder to finish the install: copy the whole skill folder, `references/` included.

Read `.claude/squad-roots.md`: `founder name`, `voice sample`, `talk to me`, `term day 1`. Look for a `FAL_KEY=` line in `.env` in the company folder.

No `term day 1` row means the first run. Ask in one message (the key only when `.env` has none), never again:

1. What date did you post your hello? (today, if you have not yet)
2. Paste your fal key and I draw the page every night (free account at fal.ai, the key at fal.ai/dashboard/keys, about 5 cents a drawing). Skip it and the post still comes.

The date becomes the `term day 1` row. The key goes into `.env` as `FAL_KEY=<key>` (create the file when it is not there), replacing any line already there, never adding a second. A key pasted later is written the same way, and the drawing is made that same run. When no message this run carried the day, add one line: "Now type the day, messy, any order: what I did, what happened, what I learned, what I would never do again, how it felt."

**The count**, from the laptop's own date: `Day N = today minus term day 1, plus 1` (the hello is Day 1). It does not stop at 180. A run started before 4 in the morning is the night before: yesterday's date is the effective date, used for the count and for the files, and say which date it used in one line.

Nothing else is read, on any day: not `squad/business.md`, not `squad/pipeline.md`, not earlier posts. The post is tonight's message and nothing more.

## Beat 1 · The dump

One message, any order, any language, messy: what I did, what happened, what I learned, what I would never do again, how it felt. Sort it yourself, never ask the founder to. Numbers only when they said them.

**The one gate.** It fires only when the message has nothing that happened in it: no thing done, no thing that broke, no thing learned. "Worked on stuff" fires it. "Sent nothing today, I froze at the ask" does not; that is a day, and the freeze is the post. One question:

> What did you actually do today, and what did it teach you?

Then write. Never a lecture, never a second question. A thin answer gets a short list.

**Sunday.** The same message about the week: what shipped, what worked, what did not, the one change for next week or the number you are holding for. Same gate in week form (`references/post-cage.md`, The one gate).

## Beat 2 · The post

Write the post on the form and the writing rules in `references/post-cage.md`, and nothing else: the hook, the re-hook, the turn line, the numbered list, the close, and `Day N of Execution Squad` last, always.

The voice is the founder's: their words from the message, the tone the roots file's `talk to me` row sets, their rhythm from the voice sample. The language is the language of tonight's message; "in English" said in the message is enough to switch.

**Sunday.** Week form, `Week N of Execution Squad` last (`references/post-cage.md`, Sunday).

## Beat 3 · The drawing

Build the prompt in `references/image-cage.md` off the post, make one call to fal's `openai/gpt-image-2` with the key loaded from `.env` first, and land the image at `squad/posts/YYYY-MM-DD.png`.

**No key** (no `FAL_KEY=` line in `.env`): no drawing, and nothing stops.

A call that comes back without an image is tried once more, then one line says the drawing did not come back tonight, and the run carries on to the yes.

## Beat 4 · The yes

Print the post once, plain, ready to copy. When beat 3 made a drawing, open it for the founder (`open`, `explorer` or `xdg-open` on the png) and name its path in one line; with none, the hand-off drops its attach clause. Under it:

> Say yes and I save it, or change any line. Then post it: aichrislee.com/threads, Accountability, the drawing attached from squad/posts/YYYY-MM-DD.png.

On a Sunday, and only then, one more line under it:

> The close's first line is your line for the week. Your 4-week plan takes it (g8).

The founder answers with one of 3 things.

- **A changed line.** Reprint that line alone. A changed hook or list title is on the page, so the drawing is remade with the new words.
- **"Again."** The drawing is remade once, the same words.
- **The yes.** Save `squad/posts/YYYY-MM-DD.md`, the post verbatim, nothing else, and say the path in one line.

Then it is their hand.

## Rules

- Never posts, never sends, never books, never opens a platform. The post leaves through the founder's hand.
- Never a name, a number or a need the founder did not say. Never a price: the post teaches, it does not pitch, and the price belongs to `squad/business.md`.
- No count is ever asked for. A day with no number in it is a full post.
- The signature is last, always. A line the founder quotes (a reply, a buyer's words) stays verbatim, in the post and in the file.
- The key is never printed back, never put in any file but `.env`, never sent anywhere but fal.
