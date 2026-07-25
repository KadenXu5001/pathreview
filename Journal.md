## Week 7 — Issue selection

**Issue link:** (https://github.com/ascherj/pathreview/issues/32)

**Issue title:** Implement a caching layer for repeated identical portfolio queries

**Tier:** [ ] Tier 1 [X] Tier 2 [ ] Tier 3

**Problem summary:**

The issue is that duplicate portfolio submissions will cause the RAG llm system to run on the
same object again. What's missing is a caching behavior to reduce this inefficency, and thus the
goal is to cache the response so that if the portfolio hasn't changed
since the last run, then it could just return the previous run's results instead. A sucessful fix
would implement this behavior. this should affect the review services.

**Branch name:** fix/32-query-caching

**Setup confirmation:** [X] App runs locally at localhost:5173

**Cohort ledger:** [ ] Issue added to cohort ledger

**Scope fit**

How many others are already working on this issue?

Claims are non-exclusive — more than one student may work on the same issue, and your grade comes from your own artifacts, never from being first. Still, check the issue comments and the Claims column in the Issue Catalog tab of the cohort ledger: a less-crowded issue of the same tier can mean smoother coaching and peer review.

[X] I've checked the issue comments and the ledger's Claims count, and I'm fine with how many others are on this issue.
Is the scope realistic for Weeks 8–9?

You have roughly two weeks to implement, test, and submit a PR. Tier 1 issues should take 3–6 hours of focused work. Tier 2 issues may take 8–12 hours. Tier 3 issues can take significantly longer.

Think about your week — other classes, work, other commitments. Is this achievable?

[X] I've estimated the time this will take and I'm confident I can complete it before the Week 9 deadline.
Are there any blockers or dependencies?

Some issues say "blocked by #X" or reference another issue that needs to be resolved first. Check the issue for any such dependencies.

[X] This issue has no open blockers or dependencies on other unresolved issues.

---

I picked this issue since I know about caching and wanted more practice in RAG pipelines.
I would say that I am used to large codebases so this isn't that much of a concern for me, so I thought that
tier 2 would be fitting for me.

**Reproduction commit link:** https://github.com/KadenXu5001/pathreview/commit/077df9a284e8e7483ea4e3660c73e26298042584

**Reproduction summary:**
This wasn't really an issue but rather a new feature implementation. But what I did was to make a unit test that fails if when given the same 2 portfolios, it fails if the run command happens twice.

**PLAN.md link:** [Link text](PLAN.md)

**Walkthrough video (recommended):** N/A

**Blockers or open questions:**
