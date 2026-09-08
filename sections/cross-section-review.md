## Cross-Section Review

**Task:** Verify every state-of-the-art claim (method or performance figure) has a specific, checkable primary/official source. Flag unsupported claims and secondary-summary-only citations.

**Scope audited:** general.md, intellectual-contributions.md, education-and-teaching.md, eureka-labs.md, views-on-ai-future.md, key-relationships-and-collaborations.md, key-relationships.md — cross-checked against sources.md.

**Method:** No web search performed (per instructions). Each numeric/methods/SOTA-type claim was traced to its cited source ID and checked against the tier and description recorded in sources.md. Findings below are additions to the document's own self-flagged uncertainties — items the document had not already surfaced.

---

### 1. Findings requiring correction or confidence downgrade

**1.1 Tesla data-engine figures rest entirely on a Tier 3 source, under a HIGH-confidence section header**
- **Location:** intellectual-contributions.md, "The Tesla Data Engine" (Tesla Autopilot section, badged Confidence: HIGH | Depth: HIGH)
- **Claim:** 1.5 petabytes, 6 billion labeled objects, 1 million 10-second videos, 221 manually-implemented triggers, 7 complete training cycles.
- **Issue:** All five figures cite only [70] (Dynamically Typed — ML newsletter, Tier 3). No Tier 1 (official Tesla/CVPR slides) or Tier 2 (mainstream press) source independently confirms any of these numbers. The section's Uncertainty block discusses the fleet-size discrepancy (1M vs 1.5M) but does not flag that the entire data-engine paragraph's quantitative content is single-sourced from a Tier 3 newsletter.
- **Recommendation:** Downgrade this specific paragraph's confidence to MEDIUM (the section-wide badge should not cover it at HIGH), or add an explicit caveat that these figures are Tier-3-only and unverified against Tesla's own CVPR 2021 slides.

**1.2 HydraNet architecture details are Tier 3-only, same pattern**
- **Location:** intellectual-contributions.md, "Tesla AI Day 2021" paragraph.
- **Claim:** RegNet+BiFPN backbone, ~50 engineers working in parallel, 8 cameras at 1280×960/12-bit/36Hz.
- **Issue:** Sole source is [24], a WordPress fan-blog transcript (Tier 3). The Uncertainty block already flags this ("should be verified against the official Tesla YouTube recording") — good — but the section-level Confidence: HIGH badge still nominally covers this paragraph. Same recommendation as 1.1: either exempt this paragraph from the HIGH badge or explicitly mark it MEDIUM.

**1.3 "Match or exceed radar-fused systems" is a stronger claim than the cited source supports**
- **Location:** intellectual-contributions.md, "The vision-only strategic bet."
- **Claim:** "The CVPR talk demonstrated that vision-only neural networks could match or exceed radar-fused systems for depth, velocity, and acceleration estimation... at fleet scale [69][72]."
- **Issue:** [69] is Karpathy's own tweet, which states only the *goal* ("to estimate very accurate depth, velocity, acceleration with neural nets from vision") — it does not claim a head-to-head benchmark result against radar-fusion systems. [72] is Tier 2 press coverage of the same keynote and, per its own sources.md description, documents "Tesla's vision-only strategy" generally, not a specific quantitative comparison. As written, the document asserts a comparative performance result ("match or exceed") that neither cited source actually states.
- **Recommendation:** Either soften to "Karpathy characterized the vision-only approach as sufficient to replace radar-fused sensing" (matching what the sources actually say) or find a source that states an explicit vision-vs-radar performance comparison.

**1.4 GPT-4.5 "10x more pretraining compute" figure sourced only via Tier 3 tweet aggregator**
- **Location:** views-on-ai-future.md, "Post-o1: Cognitive Deficits Persist" paragraph.
- **Claim:** GPT-4.5 was "released with roughly 10× more pretraining compute than GPT-4."
- **Issue:** Source [125] is a Karpathy tweet thread recovered via a Tier 3 secondary aggregator (threadreaderapp), not OpenAI's own model card/announcement, which would be the authoritative source for a compute-scaling figure about OpenAI's own model. This is a specific, checkable technical claim attributed to the wrong kind of source — it should be corroborated by (or re-attributed to) OpenAI's official GPT-4.5 documentation if that figure is to be retained with confidence.
- **Recommendation:** Flag for follow-up research to locate an OpenAI-official compute figure; until then, this specific figure should carry a MEDIUM/unverified caveat, not be stated as flat fact.

**1.5 Unsupported superlative: "most-cited works in computer vision history"**
- **Location:** intellectual-contributions.md, Stanford PhD section, end of paragraph on the ILSVRC survey paper.
- **Claim:** "The paper is among the most-cited works in computer vision history."
- **Issue:** No citation count or comparative benchmark is given for this specific claim (unlike the dissertation-era papers, which all carry precise Semantic Scholar figures). This is an uncited superlative dropped into an otherwise rigorously quantified section.
- **Recommendation:** Either supply a citation count for the ILSVRC survey paper (would be straightforward via the same Semantic Scholar Graph API method used elsewhere in the document) or remove the superlative.

### 2. Date/figure consistency check

**2.1 "Under 3 minutes" speedrun milestone — date attribution slightly loose**
- **Location:** education-and-teaching.md ("reducing GPT-2 training time from ~45 minutes (June 2024) to under 3 minutes (May 2025)") and general.md Section Highlights (same claim, "in one year").
- **Issue:** The cited source [47] is dated June 2025, not May 2025, and intellectual-contributions.md's own more granular timeline doesn't include a checkpoint at exactly "under 3 minutes" in May 2025 — it jumps from the Oct 2024 Muon record (24.9 min) to the March 2026 record (1.435 min) without an intermediate data point. The "under 3 minutes / May 2025" figure appears to be inferred from [47]'s publication rather than quoted from a specific leaderboard entry.
- **Recommendation:** Either locate the specific modded-nanogpt leaderboard entry that hit sub-3-minute wall-clock time around May 2025, or soften the date to "by mid-2025" and note it's inferred from the paper's publication timing rather than a directly cited leaderboard record.

**2.2 No new contradictions found beyond those already logged.** The Feb 13 vs Feb 14, 2024 OpenAI-departure date conflict and the 1M vs 1.5M Tesla fleet-size discrepancy are already correctly self-flagged in their respective sections and in open-questions.md; no action needed beyond what's already tracked there.

### 3. Structural/coverage gap (not a sourcing issue, but affects reliability of any cross-section consistency check)

**3.1 Two divergent files both titled "Key Relationships and Collaborations"**
- `sections/key-relationships-and-collaborations.md` (linked from general.md's Sections list) covers Justin Johnson, Percy Liang, Ilya Sutskever, and a "Formal AI Safety Research Community" subsection.
- `sections/key-relationships.md` (not linked from general.md at all) independently covers the AI-safety-community non-engagement finding a second time (in more detail) plus the Musk relationship, which does not appear in the linked file at all.
- No factual contradictions were found between the two on overlapping claims (CAIS non-signature, no Concrete Problems co-authorship, no Olah engagement — consistent across both). But the Musk relationship — a substantial, well-sourced subsection — is currently only reachable via the unlinked file. This is a coverage/navigation gap: a reader following general.md's Sections list would never see the Musk material.
- **Recommendation:** Not a citation-quality issue per se, but flagged to open-questions.md since it risks future drift (edits to one file not propagating to the other) and currently orphans sourced content.

### 4. What's working well (no action needed)

- All citation-count claims (nanoGPT stars, micrograd stars, cs231n notes stars, the six dissertation-paper citation counts, Show/Show-and-Tell counts) are Tier 1/Tier 2 GitHub- or Semantic-Scholar-API-sourced with explicit "as of March 2026, live counts may differ" caveats — this is the right pattern and should be the template for 1.1/1.2/1.4 above.
- The Muon optimizer and Moonlight scaling claims (1.35× sample efficiency, ~2× compute efficiency vs AdamW, 5.7T tokens) are all traced to Tier 1 primary sources (Jordan's blog, the Moonshot arXiv paper) with precise figures — no issue.
- The human-vs-ConvNet ImageNet experiment (5.1% vs 6.8%, p=0.022) is Tier 1 primary-sourced and precisely quantified — no issue.
- The document's own Uncertainty subsections already do substantial self-policing (tier flags, verbatim-vs-paraphrase distinctions, live-count caveats) — the gaps found here are the residual cases that self-review missed, not a systemic absence of self-review.

### 5. Confidence badge recommendations

| Section / subsection | Current badge | Recommendation |
|---|---|---|
| Tesla Autopilot — "The Tesla Data Engine" paragraph specifically | HIGH / HIGH (inherited from section) | MEDIUM for this paragraph's quantitative figures (Tier 3-only sourcing) |
| Tesla Autopilot — HydraNet architecture paragraph specifically | HIGH / HIGH (inherited) | MEDIUM for this paragraph (Tier 3-only sourcing) |
| Views on AI Future — GPT-4.5 compute figure | (inherited MEDIUM) | Retain MEDIUM but add explicit "needs OpenAI-official corroboration" caveat |
| All other audited sections | as assigned | No change — badges are consistent with source tiers |
