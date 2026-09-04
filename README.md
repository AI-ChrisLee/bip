# bip: install in 60 seconds

The post writer of an Execution Squad. Every night you dump the day in one messy message: what you did, what happened, what you learned, what you would never do again, how it felt. It writes your build-in-public post in the form the posts that travel are written in (a hook, 2 or 3 lines that turn it, a numbered list of what the day taught, a close, `Day N of Execution Squad` last) and draws the page that goes with it: a photo of an open notebook with your hook underlined at the top, your subject in the middle, and a branch for every item on your list, made through fal for about 5 cents. You read both, change a word, and post them. On Sunday it writes the same post about the week.

## Install

Drop this whole folder into `.claude/skills/` as `bip` (the `references/` folder included), then quit and reopen Claude Code in your company folder. That is the install.

## Run it

The last 5 minutes of the day. Say **"/bip"** or **"write today's post"**, then tell it the day. Messy is fine:

> video 10 went up today, 10 in 10 days. 9 did nothing, 40 views. number 7 did 6,000 overnight and I think it's because I said the point in the first sentence. spent 2 hours on the intro of number 3, nobody got there. almost quit after 5. never again a video where the first sentence isn't the point.

It writes the post, draws the page, opens the drawing, and shows you both. Change any word, say "again" if the handwriting has a typo, say yes, and it saves the post to `squad/posts/` next to the drawing. The first time, it asks 2 things in one message: what date you posted your hello (that is Day 1), and your fal key for the drawings (free account at fal.ai, the key at fal.ai/dashboard/keys). Skip the key and the post still comes; paste it any night and the drawings start.

Then post it: the text and the drawing on aichrislee.com/threads, in Accountability, no title. Under your post are 3 share buttons, X, LinkedIn and Threads, and a Copy button beside them. X opens with your hook and your signature in the box, Threads with the post cut to fit; LinkedIn copies it and opens the composer. Attach the drawing by hand on each.

A day where nothing went out is still a post; the freeze is the post. If your message has nothing that happened in it, it asks one question, what you actually did and what it taught you, and writes off your answer. It never asks you for a count.

## Sunday

Say **"/bip sunday"** with the week: what shipped, what worked, what did not, the one change for next week or the number you are holding for. It writes the weekly post, `Week N of Execution Squad` last, and the close carries your Improve line: one named change, or the hold. Most weeks the honest line is the hold, and a week that names no change is a week working. Then put it in the plan: say `Put this in week <N>'s Measure: <your 2 numbers> / Improve: <that line>`. It never adds anything up; the week is what you say it was.

## What it never does

It never posts, never sends, never opens a platform for you. It never puts in a name, a number or a need you did not say. Nothing gets written anywhere except `squad/posts/` (the post and the drawing), 1 row in your roots file, and your fal key in `.env`.
