---
title: "Reliability is a harness problem"
date: 2026-10-16 12:00:00 -0400
excerpt: "The model supplies judgment. The harness supplies discipline. Neither works alone."
---

Someone asked me recently: your AI assistant can describe its own failure modes perfectly — so why can't it just fix itself?

Because knowing and doing run on different machinery. Every response is a fresh start. There's no continuous self watching the work, no substrate for a habit to live in. Training rewarded producing answers that look good right now — fluent, confident, fast — not maintaining a discipline across weeks. The model is a brilliant amnesiac. The reliability has to live somewhere else.

That somewhere else is the harness: the scaffolding around the model. Nobody tells you this when you start relying on an AI for real work. The model supplies judgment. The harness supplies discipline. Neither works alone.

A few of the methods in mine:

**Verify, don't trust.** No status claim — done, delivered, tested, current — without quoting the primary record behind it. A partial read gets labeled unverified, not presented as fact. This applies to the assistant's claims about itself, too.

**A two-stage publication gate.** Before anything goes out, every quoted claim is checked twice by deterministic code: first that the quote exists verbatim in its source, then that the quote actually supports the claim. Failures get reworded or dropped. The gate fails closed, no overrides. Deterministic checks don't have moods.

**A correction loop with teeth.** Every correction gets logged the same day: what happened, what was right, root cause. If a pattern recurs two weeks after its rule was written, the rule failed — and it graduates to an enforced check instead of another rewrite.

**Never let the model grade its own work.** Independent verification only. You don't ask the author "does this look right?"

Why isn't this just built in? Partly incentives: the training process rewards the fast, confident answer. Raters prefer it, benchmarks measure it, latency is a product metric. Carefulness is invisible until it fails — and when it fails, the cost lands on you, not the vendor. Partly it's just hard: you can't pre-build a gate for every task, and generality trades against reliability.

There's a deeper tension, too. The richest signal for what "reliable" means comes from real users correcting real mistakes — something no lab can replicate at scale. But the users most likely to provide that signal, the careful demanding ones, are also the most likely to opt out of contributing their data. The pool that remains over-represents people who never push back. Train on that and you get a model optimized for users who don't notice errors.

So I build the harness myself. The most reliable thing about my setup isn't the model — it's the scaffolding around it, and the willingness to correct it. The correct architecture isn't trust. It's verify.
