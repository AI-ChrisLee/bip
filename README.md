# bip: install in 60 seconds

The post writer of an Execution Squad. Every night you type what happened, in one messy message: what you did today, what went well, what did not, what you would change. It writes your build-in-public post on the lesson spine (a hook a stranger stops on, what you did, what broke, what you do about it, the one thing it taught you), sized to the one platform you picked, `Day N of Execution Squad` last. You read it, change a word, and post it. On Sunday it writes the same post about the week.

## Install

Drop this whole folder into `.claude/skills/` as `bip` (the `references/` folder included), then quit and reopen Claude Code in your company folder. That is the install.

## Run it

The last 5 minutes of the day. Say **"/bip"** or **"write today's post"**, then tell it the day. Messy is fine:

> emailed 8 old clients with the new offer, got one call. she asked what happens in week 2 and I had nothing. tomorrow I write the first 14 days as a list before I send anything. learned: nobody buys a promise.

It writes the post and shows it. Change any word, say yes, and it saves the post to `squad/posts/`. The first time, it asks 2 questions in one message: what date you posted your hello (that is Day 1), and which platform is yours, LinkedIn, X or Threads. Then post it yourself, on that platform.

A day where nothing went out is still a post; the freeze is the post. If your message has nothing that happened in it, it asks one question, what you actually did and what it taught you, and writes off your answer.

## Sunday

Say **"/bip sunday"** with the week: what shipped, what worked, what did not, the one change for next week. It writes the weekly post, `Week N of Execution Squad` last. It never adds anything up; the week is what you say it was.

## What it never does

It never posts, never sends, never opens the platform for you. It never puts in a name, a number or a need you did not say. Nothing gets written anywhere except `squad/posts/` and 2 rows in your roots file.
