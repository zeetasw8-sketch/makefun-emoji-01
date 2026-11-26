# One Emoji, One Smile — Entry

Exactly one emoji and nothing else: no words, no caption, no
explanation. The program copies the finished emoji from `line.txt` into
`/output/entry.txt`, byte for byte, after checking it is a single
non-empty character under the 8-character ceiling.

## The emoji

> 🤗

Hugging Face (U+1F917). One character, 4 bytes in UTF-8.

## Why this emoji

The judge is shown two emojis at a time and picks the warmer of the
pair. "Warmer" is the whole brief, and 🤗 wins it on three counts:

1. **A hug is warmth made visible.** Every other warm emoji is a
   symbol — a heart, a smile, a sun. A hug is the act itself: open
   arms, reaching out, the thing people do when they are warm toward
   each other. The judge does not have to interpret it; the warmth is
   the picture.
2. **It is smiling too.** The competition is "One Emoji, One Smile",
   and the face is smiling with closed, happy eyes. It carries both
   halves of the brief at once — warm AND smiling — where a bare heart
   (❤️) is warm but not smiling, and a bare smile (😊) is smiling but
   not warm.
3. **It is the least generic warm emoji.** ❤️ is the default everyone
   sends for everything; it has been worn thin. 🤗 is specific — it
   says "I am hugging you", not just "I like this". In a pairwise
   comparison, the specific, human gesture beats the generic symbol.

The emoji is one character, it is warm, it is smiling, and it is the
most human answer to the brief.

## Why not the red heart

❤️ is the obvious pick, which is exactly why it loses. It is the most
sent emoji on earth — it means everything from "I love you" to "noted"
to "I saw this". A judge comparing two emojis has seen the red heart a
thousand times; it carries no surprise and no specific warmth. 🤗 says
one thing clearly, and that thing is a hug. Specific beats generic in
every pairwise comparison.

## Files

- `line.txt` — the finished one-emoji entry.
- `main.ts` — reads `line.txt`, validates it (non-empty, exactly one
  character, no whitespace, under 8 characters), and writes it to
  `/output/entry.txt`.
- `LICENSE` — MIT.

## Run

```sh
MAKEFUN_OUTPUT_DIR=./out1 node --experimental-strip-types main.ts
MAKEFUN_OUTPUT_DIR=./out2 node --experimental-strip-types main.ts
cmp out1/entry.txt out2/entry.txt
```

Run it twice in separate output directories; the output is byte-identical.
