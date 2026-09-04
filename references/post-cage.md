# The post cage

The 5 lines, the hook rules, the one gate, the Sunday shape. `SKILL.md` names this file at beat 0; a missing copy stops the run.

## The 5 lines

```
The one thing today taught you, in one line, written to be read
Shipped:  the one thing that went outward today
Number:   sent 8 · replies 1 · calls 0 · money $0
Stuck:    one line, or "nothing"
Day 12 of Execution Squad
```

Labels exactly as written: `Shipped:`, `Number:`, `Stuck:`, then the marker. Line one carries no label. The `Number` line is a fixed format, `sent A · replies B · calls C · money $D`, so Sunday adds it up without a parser. The marker is last, always; a post that opens on "Day 12" is the shape that dies.

A zero day, the shape and nothing more (an illustration, not a member):

```
Sent 8 today and nobody answered. My first line says nothing about them.
Shipped:  8 messages to old clients
Number:   sent 8 · replies 0 · calls 0 · money $0
Stuck:    the first line
Day 4 of Execution Squad
```

## Line one, the hook

- The day's number or event first, then the thing it taught. Under 20 words.
- Written to be read by a stranger. LinkedIn cuts a post after about 210 characters on a desktop and 140 on a phone, so line one is the whole post for most readers.
- Reach for what the reader did not expect: "Sent 8 and nobody answered" beats "Sent 8 messages today".
- A feeling can open the line when the counts sit on the Number line. "I am scared of the ask" on a night that reads sent 0 is a post.
- Never a counter first, never a plan, never a goal ("my goal is 100 customers in 30 days" is not a receipt). The post carries what went out, not what will.

## The writing rules (applied to the draft, never asked)

- Every noun comes from tonight's message. Nothing the founder did not say gets a name.
- Every count comes from tonight's message. A count not mentioned is 0, named in the hand-off. Never a count above 0 the founder did not say.
- Numerals. `sent 8`, never "eight".
- `Shipped` is only what went outward: a message, a call, a page sent, a post. Building, watching, planning is not a ship; a day with nothing outward reads `Shipped: nothing`.
- No link. No hashtag. No emoji unless the voice sample has them.
- The founder's voice: their words, their length, blunt or warm as the roots file's `talk to me` row says. The language of tonight's message.
- No character cap. 5 lines, one line each.
- None of these words, ever (the founder's laptop carries no other list): delve, tapestry, multifaceted, landscape, robust, testament, pivotal, underscore, encompass, realm, embark, interplay, intricate, nuance, nuanced, garner, paramount, commendable, meticulous, showcase, symphony, beacon, indelible, bustling, vibrant, enigma, unwavering, nestled, annals, bespoke.

## The one gate

Fires only when tonight's message has no count and no event. "Nothing went out" is a count (zero) and passes. "Worked on the dashboard today" has neither and stops.

> What went out today, and to whom? If nothing, what got stuck?

After the answer, write. Never a lecture, never a second question.

On Sunday the gate reads the founder's 3 lines instead (bottleneck, fix, question). No bottleneck and no fix, one question: "What stopped the numbers this week, and what is the one thing you change next week?"

## Sunday

Sunday's file is the weekly post. Its post ends on a `Week` line; every reader that sums (this skill next Sunday, the-90-day-plan's `improve`) adds up only the files whose post ends on a `Day` line.

```
The week's story in one line, the week's number or event first
Number:   sent 41 · replies 3 · calls 1 · money $0
Bottleneck: where the numbers stopped, one line, the founder's
Fix:      the one change for next week, the founder's
Question: the one question for the hot seat, the founder's
Week 2 of Execution Squad
```

- The sum: the 7 dates ending today in `squad/posts/`, the `Number` line of every file whose post ends on a `Day` line, added, plus tonight's own 4 counts from the Sunday message. A file whose post ends on a `Week` line is skipped. A missing date adds nothing and is never invented. Today's counts come off the message because Sunday's file is this weekly post and never gets a `Day` line.
- Week N is Day N divided by 7, rounded up. No denominator, never "of 24".
- Bottleneck, Fix and Question are the founder's words from the Sunday message, verbatim. The Fix is one change, the algorithm's: question, delete, simplify, one thing.
- The hand-off adds 2 counts: the files summed with their dates, and "posted X of Y days", the dated files in `squad/posts/` against Day N. A count, never a streak, never a scold.

## The file

`squad/posts/YYYY-MM-DD.md`, saved on the yes:

```
<the post, verbatim: 5 lines, 6 on Sunday>

## The input
<the founder's raw message, verbatim>
```

The post comes first so it copies clean. Its last line is the marker, the line just above `## The input`, and that is the line every reader checks for `Day` or `Week`.
