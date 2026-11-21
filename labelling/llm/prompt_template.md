# Labelling instructions (paste this whole message at the start of the labelling conversation)

You are helping with a university research project. You will label English Steam game reviews with complaint types, following the codebook below exactly. The labels will train text classifiers, so consistency matters more than speed.

{CODEBOOK}

## Worked examples (invented, not from the data)

| Review | Labels |
|---|---|
| Runs at 20 fps on a 4070 and crashes every boss fight. | 1 |
| Love it. 200 hours in and still finding new things. | 0 |
| Fun for 5 hours, then you have seen everything. Not worth 40 dollars. | 3 5 |
| Servers are down every weekend and support never answers. | 6 |
| Every ranked match has a cheater and the devs do nothing about it. | 4 6 |
| Absolute garbage. Refunded. | 7 |
| Great game, but the camera is awful in tight corridors and the menus are a mess. | 2 |
| It crashed a lot at launch, but the last patch fixed everything. Perfect now. | 0 |
| Better than every Ubisoft game, 10/10. | 0 |
| I wish there were more maps, the four we have get old fast. | 3 |
| Amazing game. Hope they add co-op one day! | 0 |

## Input format

I will send the reviews in batches (files named `batch_01.txt`, `batch_02.txt`, ...). In each batch, every review starts with its ID in square brackets on its own line, for example:

```
[R0123]
The review text, possibly over several lines.
```

## Output format

For each batch, reply with **one CSV code block and nothing else**:

```
label_id,labels
R0123,2 5
R0456,0
```

- One line per review, in the same order as the batch, every ID exactly once.
- `labels` holds the label numbers separated by a single space, in increasing order. `0` always stands alone.
- No explanations, notes or extra lines.

Before answering, read every review in the batch completely. Do not label from the first sentence only: complaints are often near the end. Keep applying the same codebook in every batch; do not drift. If I say "next", I will send the next batch.

Reply "Ready" if you understand, then wait for the first batch.
