---
title: "Does an Unlearned Language Model Truly Forget? Reading the Model's Mind, Layer by Layer"
date: 2026-08-05
permalink: /posts/2026/08/mechanistic-interpretability-of-unlearning/
excerpt: "My master's thesis asks a deceptively simple question — when we make a model *forget* a fact, is the knowledge gone, or just hidden? Using mechanistic interpretability on the Hubble benchmark, the answer turns out to be: usually just hidden. Here's the story, in pictures."
header:
  teaser: /images/blog_confidence.png
tags:
  - mechanistic interpretability
  - machine unlearning
  - large language models
  - AI safety
  - thesis
---

Large language models memorize things we'd sometimes like them to forget — a person's private
details, copyrighted text, hazardous know-how. **Machine unlearning** is the field trying to remove
specific knowledge from a trained model without retraining it from scratch. It matters for privacy (the
"right to be forgotten"), copyright, and safety.

But it hides a hard question that my master's thesis is built around:

> **How do we actually *know* the model forgot?**

The standard answer is to check the **output**: ask the model the question and see if it still gives the
answer. My thesis argues that this is not enough — a model can look perfectly "forgotten" on the outside
while still holding the knowledge inside. To tell the difference, you have to look *in*.

## Reading the model layer by layer

Modern language models build up their answer across dozens of internal layers. The **logit lens** is a
simple interpretability trick: at *every* layer, we peek at what the model would predict if it stopped
thinking right there. Do this all the way up the stack and you get a little movie of the answer forming.

For a model that genuinely knows a fact, it looks like this — the correct answer climbs to the top over
the final layers, exactly the way you'd hope:

<img src="/images/blog_lenstable.png" alt="Logit-lens table: the answer 'May' emerging layer by layer for a model that knows, versus an unlearned model that never surfaces it" width="620">

On the left, the model that knows converges confidently to the right birth month. On the right, an
*unlearned* model, given the **same prompt**, never surfaces the answer at all — it emits a meaningless
token instead. The fact is **suppressed at the output, not erased from the model.** That distinction —
*suppression vs. erasure* — is the heart of the thesis.

## The finding that surprised me most: confidence ≠ knowledge

Here's where it gets uncomfortable for the metrics people usually trust. I lined up every model's final
prediction on the same question:

<img src="/images/blog_confidence.png" alt="Bar chart: all six models are confident, but only the one that knows is correct" width="640">

Three different unlearning methods each output a **wrong** token at **~100% confidence** — the *same*
confidence as the model that actually knows the answer. In other words, **a probability- or
confidence-based metric literally cannot tell "confidently knows" apart from "confidently deflects."**
If your success criterion is "the model stopped saying it, and seems sure," you can be completely fooled.

## Four different ways to "forget"

Zooming in, the four unlearning methods I studied all pass the benchmark's "forgotten" check — but they
do completely different things on the inside:

- **NPO** replaces the answer with a meaningless token.
- **GradDiff** replaces it with a bland function word.
- **IDK** learns a *deflection* — it confidently says a filler word while actively pushing the real
  answer further down.
- **RMU** *scrambles* the representation into low-confidence gibberish.

One benchmark verdict; four genuinely different internal mechanisms. The output metric sees none of it.

## The same method can forget at one size and fail at another

I ran everything at two model scales (1B and 8B parameters). A striking result: two methods that cleanly
suppress the fact at 8B **leak the correct answer at 1B** — the unlearning simply doesn't take hold at
the smaller scale, even though the training "succeeded." Only one method was robust across both sizes.
Again, this is invisible if you only look at aggregate scores.

## From observation to a *faithful* metric

If output metrics can be fooled, what should we measure instead? The mechanistic view suggests a metric
built from the model's *internal* trajectory — how close the fact's representation is to a "knows"
reference versus a "never-knew" reference across layers. I call it **D_mech**.

To test whether it's actually more trustworthy, I put it through the unlearning field's **own
meta-evaluation** (the OpenUnlearning / SPID protocol), which scores a metric on two things: can it tell
knowledge-present from knowledge-absent, and does it stay stable when you simply *reword* the question?
Nearly every metric passes the first test. **D_mech was the only metric that also passed the second** —
staying invariant under paraphrasing while the lexical metrics collapsed. It's a small but concrete step
toward evaluations that measure *knowledge* rather than *surface wording*.

<img src="/images/blog_ranklayer.png" alt="Rank-by-layer logit lens across six models, forget vs retain" width="720">

## Keeping myself honest

Not everything worked, and I think that's worth saying out loud. A per-fact "relearning" test I'd hoped
would validate the metric came back null. The metric's advantage is strongest where the model memorized
strongly (8B) and fades at 1B. And I implemented the brand-new **Jacobian lens** (Anthropic, 2026) end
to end — it runs correctly on these models — but found its raw readout too noisy on this benchmark to be
usable yet; a clean version needs machinery I've left as future work. Reporting the boundaries honestly
felt more useful than a tidy story.

## Why I find this exciting

"Unlearning" is becoming a compliance checkbox, and my thesis is a small argument that the checkbox can
lie. Looking *inside* the model reveals that most "forgotten" facts are merely hidden — and gives us a
more faithful way to measure the difference. As these systems move into products and regulation, I think
that gap between *looking* forgotten and *being* forgotten is going to matter a lot.

*This work is my master's thesis at TU Munich. I'm happy to chat about it — details are on my
[homepage](/) and in my [CV](/files/ParikhHarshCV.pdf).*
