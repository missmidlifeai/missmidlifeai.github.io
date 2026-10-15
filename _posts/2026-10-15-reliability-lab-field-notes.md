---
title: "I run a reliability lab on my AI assistants"
date: 2026-10-15 12:00:00 -0400
excerpt: "The models aren't the problem. The lack of instrumentation is."
---

I don't trust my AI assistants. That's not cynicism, it's policy.

Every mistake they make goes into a corrections log: what happened, what was actually correct, why it happened, and what rule would have prevented it. The log has a fixed schema, because if you let anyone describe their own failures in free prose, everything becomes "a slight misunderstanding."

New rules don't get adopted because they sound good. Each one has to survive a backtest: I pull two or three old failures and check whether the rule would have caught them. If it can't prove it, it doesn't ship. Failures get classified first, because the fix depends on the diagnosis — a bad rule gets rewritten, an ignored rule gets enforced, a useless one gets retired, and a tooling problem never gets solved by writing a memo about it.

Memory itself runs on a budget. My assistants share 9,500 tokens of long-term memory, and it's zero-sum: anything new has to name what it's replacing. Constraints like that keep everyone honest.

This week I ran an access audit on one assistant's accounts — tokens, sessions, API keys, the full accumulation. Everything found was revoked or rotated the same day. Boring work. That's rather the point: the systems you don't inspect are the systems you don't control.

The assistants are getting better. Not because the models changed — because the errors stopped being free.
