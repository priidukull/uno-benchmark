# uno-benchmark

The repo and benchmark are named after my grandfather Uno Kivik (1929-2016). 
The benchmark uses pages from Uno's work diary to test how accurately LLMs transcribe handwritten Estonian.

## Structure of the repo
- `images/` — the first 10 diary pages with a typed ground truth (`<date>.jpeg`, named for the
  first date on the page), as sent to the model. 1985-12-25 is the original photograph, not the
  2026-09-19 reshoot.
- `ground_truth/` — the typed reference transcript of each page (`<date>.txt`), to score against.
- `system_prompt.txt` — the system prompt.
- `user_prompt.txt` — the user message, sent with one page image per request.

## Attribution
Both prompts are from Crosilla, Klic and Colavizza. The user prompt is theirs unchanged; the
system prompt adds guideline 7 on times:

> Giorgia Crosilla, Lukas Klic and Giovanni Colavizza. *Benchmarking Large Language Models for
> Handwritten Text Recognition.* arXiv:2503.15195, 2025. https://arxiv.org/abs/2503.15195
