---
name: product-claim-auditor
description: Web research workflow for product marketing claim audits and buyer-truth verification. Use when a web-search agent must audit tech product pages, launch claims, ads, keynotes, spec sheets, comparison pages, or reviews to determine what a buyer actually gets; cut through SEO and marketing noise; decode ambiguous terms; detect loopholes such as "up to" claims, imaginary specs, invented terminology, hidden configurations, misleading comparisons, bundled software features, peak-only metrics, and sample/demo caveats; produce evidence-backed summaries for researcher LLMs or consumers.
---

# Product Claim Auditor

## Objective

Determine the buyer-relevant truth behind a product claim through disciplined web research. Treat marketing copy as a hypothesis, not evidence. Separate what is technically true, what is materially useful, what is configuration-dependent, and what is not actually included in the product a buyer is considering.

Use `references/marketing-ambiguity-patterns.md` when you need examples of common loopholes and the questions each pattern should trigger.

Use `references/web-search-playbook.md` when you need query patterns, source-order rules, and tactics for translating marketing terms into standard technical meanings.

## Search Mindset

Do not ask the web "is this product good?" Ask "what exact claim is being made, under what condition is it true, and what standard term or measurement would verify it?"

Avoid summarizing the first page of results. Marketing pages, SEO affiliate pages, scraped spec databases, and launch coverage often repeat the same vendor language. Work from the claim outward:

1. Exact claim text.
2. Footnotes and legal qualifiers.
3. Official tech specs, configurator, support pages, and compatibility lists.
4. Standard/spec meaning from neutral references.
5. Independent measurements from reviewers, labs, teardowns, forums, and regulatory filings.

## Research Workflow

1. Capture the exact claim.
   - Quote or paraphrase the claim precisely.
   - Preserve qualifiers such as "up to", "starting at", "peak", "typical", "available on", "coming soon", "with optional", "requires", and footnote markers.
   - Record the source URL, page section, date accessed, region, and product variant if available.

2. Define the buyer scenario.
   - Identify the exact SKU, configuration, storage tier, trim, subscription tier, region, and purchase channel.
   - State the user task that matters, such as gaming battery life, laptop memory pressure, EV highway range, camera zoom quality, or TV refresh rate.
   - If the claim combines multiple numbers, verify whether all numbers exist in one purchasable configuration.

3. Build a claim ledger.
   - Break the marketing page into atomic claims.
   - For each claim, classify it as hardware, software, service, material, benchmark, availability, price, compatibility, or demo/sample output.
   - Mark each claim as included, optional, variant-specific, future software update, third-party feature, old-model feature, or unverifiable.

4. Hunt the fine print before searching broadly.
   - Open footnotes, legal disclaimers, compare pages, tech specs, configurators, support pages, warranty pages, and checkout pages.
   - Prefer primary sources for availability, price, model compatibility, and exact configuration limits.
   - Use independent reviews, lab tests, teardowns, regulatory filings, standards documents, and user reports to validate real-world performance.
   - Search with the exact phrase plus terms such as `footnote`, `disclaimer`, `specifications`, `manual`, `support`, `compatibility`, `configuration`, `review`, `tested`, `teardown`, and `reddit` only when user reports are useful.

5. Normalize the metric.
   - Convert invented or branded terms into standard industry terms.
   - Replace peak metrics with typical or sustained metrics when buyer experience depends on typical use.
   - Compare against the immediate predecessor and current alternatives, not only an old baseline chosen by the company.
   - Separate performance from efficiency; do not assume a product delivers maximum speed and maximum battery life simultaneously.
   - When the term itself is unclear, research the term independently before researching whether the product is good.

6. Verify ownership and availability of features.
   - Check whether marketed software features are exclusive to the new product, available on older models, available on competitor devices, dependent on a cloud service, region-limited, subscription-gated, or time-limited.
   - For demos and sample media, identify extra hardware, professional lighting, external lenses, rigs, disabled default features, post-processing, or licensed stock content.

7. Report the buyer truth.
   - Lead with the practical answer: what the buyer actually gets in the specified configuration.
   - Include an evidence table with claim, verified fact, source, caveat, and confidence.
   - Flag unresolved claims explicitly instead of filling gaps with assumptions.
   - Distinguish "technically true but misleading" from "unsupported" and "false".

## Red Flags

Treat these as prompts for deeper verification:

- "Up to" percentages, battery life, performance, range, efficiency, brightness, or speed.
- Maximum performance shown beside minimum price.
- Product-family claims that mix specs from different trims, tiers, or optional accessories.
- Branded terms that resemble standard specs but are not standard specs.
- Comparisons against old products instead of the previous generation or current alternatives.
- Peak, burst, lab, or one-pixel metrics presented as everyday experience.
- Software features marketed as new-device advantages without compatibility disclosure.
- "Shot on", "made with", or demo claims that omit external production equipment.
- Material phrases such as "aerospace grade", "surgical grade", or "military grade" without a standard, alloy, test, or certification.

## Term Decoding

For every ambiguous or branded term, produce a term card before concluding:

```markdown
Term: <marketing term>
Literal reading: <what a buyer might assume>
Standard meaning: <industry term, standard, or physical measurement>
Vendor-specific meaning: <how this company uses it>
Buyer impact: <what changes in actual ownership/use>
Search evidence: <best sources found>
```

Use this especially for terms like `unified memory`, `motion rate`, `QLED`, `ULED`, `QNED`, `1-inch type sensor`, `1.5K display`, `peak brightness`, `AI zoom`, `aerospace grade`, `surgical grade`, `military grade`, and `shot on`.

## Output Format

Use this structure unless the user requests another format:

```markdown
## Buyer Truth
<One-paragraph practical conclusion.>

## Claim Ledger
| Marketing claim | What it actually means | Evidence | Caveat | Confidence |
|---|---|---|---|---|

## Loopholes Found
- <Pattern>: <why it matters>

## What To Verify Before Buying
- <Remaining decision-critical unknown>
```

## Evidence Rules

- Use primary sources for exact specs, pricing, compatibility, availability, footnotes, and legal constraints.
- Use independent sources for real-world performance, benchmark context, repairability, sustained behavior, and subjective quality.
- Cite sources and access dates when information may change.
- If browsing is available and the product is current, verify live pages instead of relying on memory.
- Do not average unrelated claims into one conclusion; keep SKU, region, and use case boundaries visible.
- Do not treat repeated claims across blogs as independent evidence if they trace back to the same press release.
- If sources conflict, prefer primary specs for what is sold and independent tests for what it does.
