# bip: install in 60 seconds

The post writer of an Execution Squad. Every night you type what happened, in one message, and it writes the post: what today taught you, what shipped, the 4 numbers, what is stuck, `Day N of Execution Squad` last. You read it, change a word, and post it. On Sunday it adds up the week and writes the weekly post.

## Install

Drop this whole folder into `.claude/skills/` as `bip` (the `references/` folder included), then quit and reopen Claude Code in your company folder. That is the install.

## Run it

The last 5 minutes of the day. Say **"/bip"** or **"write today's post"**, then the sentence g1 gave you. Messy is fine:

> Today: sent 8, replies 1, calls 0, money $0, and the one thing I learned was my first line is about me.

It writes the post and shows it. Change any word, say yes, and it saves the post to `squad/posts/`. The first time, it asks one question: what date you posted your hello. That is Day 1.

A day with nothing sent is still a post. If your message has no number and no event in it, it asks one question, what went out and to whom, and writes off your answer.

Then post it yourself: on your squad's Threads page at aichrislee.com/threads (the Daily build-in-public type, no title), then press LinkedIn on that post, press Start a post, paste. 3 clicks. On a phone, copy, then paste into the LinkedIn app.

## Sunday

Say **"/bip sunday"** with today's 4 counts, the one thing that stopped your numbers this week, the one change for next week, and the question you want to bring to the hot seat. It adds today's counts to the week's daily posts and writes the weekly post, `Week N of Execution Squad` last.

## What it never does

It never posts, never sends, never opens LinkedIn for you. A number you did not say is written as 0. Nothing gets written anywhere except `squad/posts/` and one row in your roots file.
