# How to run the LLM labelling (2,720 reviews, 38 batches)

1. Start a new conversation. Paste the whole of `prompt.md` and wait for "Ready".
2. Upload or paste `batches/batch_01.txt`. The answer is one CSV code block.
3. Copy the CSV into `answers/batch_01.csv` (same number as the batch), including the header `label_id,labels`.
4. Repeat for the next batch.
5. Start a fresh conversation (and paste `prompt.md` again) about every 5 batches. Long conversations get compressed and the codebook may be applied less consistently.

Do not edit the batch files. Partial answers are fine; the merge notebook will report missing or invalid IDs, and those batches can be redone.
