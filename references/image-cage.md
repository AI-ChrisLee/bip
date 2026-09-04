# The image cage

The drawing that goes with every post: what is on the page, the prompt, the fal call, where the file lands, the "again" rule, the no-key line, the cost, and one worked prompt. `SKILL.md` names this file at beat 0; a missing copy stops the run.

## What is on the page

A photo taken from directly above of an open lined notebook lying on a plain dark wooden desk, in soft natural daylight. The page is filled in by hand: a black fine-tip pen, casual handwriting a stranger can read at phone size, and a yellow highlighter marker on some of the words. Nothing else in the frame: no logo, no person, no hands, no mug, no laptop.

The page is the post drawn as a mind map:

| On the page | From the post | Size |
|---|---|---|
| the title at the top, underlined once | the hook, as it stands | 1 line |
| the centre, highlighted in yellow | the post's subject, in the founder's words (the hook's noun) | 2 to 4 words |
| the branches, each label highlighted in yellow, each joined to the centre by a hand-drawn arrow | the list titles, in order, one branch per list item | 2 to 4 words a label |
| 2 short unhighlighted lines under each label | that item's own lines, cut to their nouns | 2 or 3 words a line |
| a small page number at the bottom centre | `1` | 1 character |

One branch per list item, up to 10. The words stay short because handwriting is the hardest text a model renders, and 2 to 4 words a label is where it lands clean. Nothing the post does not say goes on the page: every satellite word is lifted out of that item's own lines, never invented to fill the space.

**The script.** The page's words are the post's words. When the post is not in a Latin script, write the title, the centre, the labels and the satellites in English (the same meaning, the founder's words translated) and say so in one line under the drawing, because handwritten non-Latin script does not come back clean.

## The prompt

One paragraph, the words in straight double quotes exactly as the post has them, the numbers as numerals, and the last sentence always the spelling line:

```
A photo taken from directly above of an open lined notebook lying on a plain dark wooden desk, in soft natural daylight. The page is filled in by hand with a black fine-tip pen in casual, legible handwriting, with a yellow highlighter marker used on some words. At the top of the page, written as a title and underlined once with a single hand-drawn line: "<the hook>". In the middle of the page, one short phrase highlighted in yellow marker: "<the subject>". <N> hand-drawn arrows go outward from that centre phrase to <N> labels around it, each label highlighted in yellow marker: "<title 1>", "<title 2>", "<title 3>", "<title 4>", "<title 5>". Under each label, two short lines of small plain handwriting with no highlight: under "<title 1>" it reads "<a>" then "<b>"; under "<title 2>" it reads "<a>" then "<b>"; <one clause per label>. At the bottom centre of the page, a small handwritten page number: "1". Nothing else in the frame: no logo, no person, no hands, no other objects. Every word spelled exactly as written here.
```

The label list and the satellite clauses grow and shrink with the list: 3 items, 3 labels and 3 clauses; 8 items, 8 of each. Nothing else is added to the prompt: no style names, no artist, no colour beyond black ink, yellow marker and the paper.

## The call

The endpoint is fal's `openai/gpt-image-2`. The key is `FAL_KEY` in the company folder's `.env`, the same line the Proven Package reads (c2), loaded first because the terminal does not read `.env` on its own. The prompt goes in as JSON on standard input, so nothing is written to disk except the image:

```
[ -f .env ] && { set -a; . ./.env; set +a; }
curl -s -X POST https://fal.run/openai/gpt-image-2 \
  -H "Authorization: Key $FAL_KEY" -H "Content-Type: application/json" \
  --data-binary @- <<'JSON'
{"prompt": "<the prompt, on one line, its inner quotes escaped as \">",
 "image_size": {"width": 1024, "height": 1536},
 "quality": "medium",
 "output_format": "png",
 "num_images": 1}
JSON
```

`image_size` is the custom object, not a preset: fal's presets have no 1024x1536, and a custom size only needs both sides to be multiples of 16. `quality` stays `medium`: `low` is a tenth of the price and the handwriting comes back rough. The response is `{"images": [{"url": "...", "content_type": "image/png", ...}]}`. Take `images[0].url` and download it:

```
curl -s -o squad/posts/YYYY-MM-DD.png "<images[0].url>"
```

(`grep -o '"url":"[^"]*"' | head -1 | cut -d'"' -f4` pulls the url out of the response without any other tool.) A response with no `images` entry, or a status other than 200, is tried once more; a second miss prints one line, "the drawing did not come back tonight", and the run carries on to the yes. A `401` is a bad key: say so in one line, and the founder pastes a fresh one when they want to.

## The file

`squad/posts/YYYY-MM-DD.png`, 1024x1536, next to the post's `.md`. One drawing per date. A remake overwrites it.

## Again

"Again" from the founder at beat 4 remakes the drawing once with the same words and the same prompt; the pen draws differently each time, and a typo in the handwriting is the reason to say it. A second "again" gets one line: the words are right, the pen is the pen; post it or change a line. A changed hook or list title changes the page's words, so that remake is a new prompt, not the "again".

## No key

`FAL_KEY` empty after the load: the post prints as it would have, then this one line, and nothing stops:

> No drawing tonight. Paste your fal key for the image (fal.ai/dashboard/keys) and I make it.

A key pasted after that line is written to `.env` as `FAL_KEY=<key>` (once, never printed back) and the drawing is made in the same run, off the post as it stands.

## Cost

About 4 cents a drawing (1024x1536 at quality medium is $0.042 on fal). "Again" is another 4 cents. A month of nightly posts is under $2.

## The worked prompt

For a post whose hook is "My first 10 videos. 1 went viral, 9 did not." and whose 5 list titles are Hook first, One idea, Show the screen, Cut the intro, Post anyway. The centre is the hook's subject in the founder's words, "My first 10 videos", and every satellite is lifted out of that item's own lines:

```
A photo taken from directly above of an open lined notebook lying on a plain dark wooden desk, in soft natural daylight. The page is filled in by hand with a black fine-tip pen in casual, legible handwriting, with a yellow highlighter marker used on some words. At the top of the page, written as a title and underlined once with a single hand-drawn line: "My first 10 videos. 1 went viral, 9 did not.". In the middle of the page, one short phrase highlighted in yellow marker: "My first 10 videos". Five hand-drawn arrows go outward from that centre phrase to five labels around it, each label highlighted in yellow marker: "Hook first", "One idea", "Show the screen", "Cut the intro", "Post anyway". Under each label, two short lines of small plain handwriting with no highlight: under "Hook first" it reads "finished result" then "not hello"; under "One idea" it reads "3 things" then "left at 2"; under "Show the screen" it reads "80% screen" then "not my face"; under "Cut the intro" it reads "40 sec" then "nobody waited"; under "Post anyway" it reads "almost deleted" then "at midnight". At the bottom centre of the page, a small handwritten page number: "1". Nothing else in the frame: no logo, no person, no hands, no other objects. Every word spelled exactly as written here.
```

That prompt was rendered on 2026-09-04 through the call above: every word came back spelled right, the five labels sat highlighted around the centre with an arrow into each, the satellites stayed small and plain, and the page number sat at the bottom. It is the drawing G3 shows.
