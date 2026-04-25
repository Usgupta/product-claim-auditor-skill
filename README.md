# Product Claim Auditor

An Agent Skill for cutting through tech marketing fog and finding what buyers actually get.

Tech companies are very good at making small, conditional, or configuration-specific improvements sound huge. Product pages mix "up to" numbers, invented terms, peak-only metrics, hidden footnotes, and specs from different variants until even a careful buyer can lose track of what is actually included.

This portable skill turns a web-search agent into a skeptical product researcher. It captures the exact claim, finds the qualifier, decodes the term, verifies the purchasable configuration, and translates the result into plain buyer truth.

## Built For

- Researchers comparing tech products through noisy launch claims.
- Buyers trying to understand what a device actually includes.
- Reviewers and writers checking whether a headline spec is meaningful.
- Agents that need a repeatable workflow for product-claim verification.

## Inspiration And Credit

This skill was inspired by the video [How Tech Companies Lie to You](https://www.youtube.com/watch?v=JstGCPsj9wg) by [Mrwhosetheboss](https://www.youtube.com/@Mrwhosetheboss), made with [Marques Brownlee / MKBHD](https://www.youtube.com/@mkbhd).

The video breaks down patterns that shaped this skill, including "up to" claims, imaginary specs, invented display and camera terminology, software-feature padding, cherry-picked comparisons, premium-material wording, misleading peak brightness numbers, digital zoom claims, and "shot on" demo caveats.

## What It Catches

- "Up to 2x faster" claims with missing workload, baseline, or configuration.
- Imaginary specs where the best performance number is shown beside the lowest starting price.
- Branded terms that sound like standards but are really vendor-defined marketing language.
- Peak brightness, digital zoom, megapixel, range, and battery claims that do not represent normal use.
- Software features marketed as new-device advantages even when they come from third parties, older models, or future updates.
- Demo claims like "shot on phone" that omit rigs, lenses, lighting, post-production, or disabled default features.

## Why It Matters

Marketing language is often technically defensible while still being practically confusing. A claim can be true only under a specific workload, on a specific trim, with a specific accessory, for a few seconds, in a peak mode, or compared against a much older product.

This skill teaches an agent to search for the missing context:

- What does the term actually mean outside the vendor's page?
- Which SKU or configuration gets the headline number?
- Is the feature exclusive, or is it coming to older devices and competitors?
- Is the metric peak, typical, sustained, optical, digital, physical, or software-generated?
- What do independent measurements show in the user's real use case?

The output should not be a generic product summary. It should be a claim ledger that separates buyer-relevant facts from technically true but misleading framing.

## Output Style

The skill pushes the agent toward a structured audit:

- Buyer truth first.
- Claim-by-claim evidence ledger.
- Loopholes and ambiguity called out directly.
- Remaining unknowns listed before someone buys.

## Install

Install from GitHub with the `skills` CLI:

```bash
npx skills add Usgupta/product-claim-auditor-skill
```

Install globally:

```bash
npx skills add -g Usgupta/product-claim-auditor-skill
```

Install only this skill from the package:

```bash
npx skills add Usgupta/product-claim-auditor-skill --skill product-claim-auditor
```

Preview available skills before installing:

```bash
npx skills add Usgupta/product-claim-auditor-skill --list
```

Then invoke the skill in your agent:

```text
Use $product-claim-auditor to audit this product claim and explain what a buyer actually gets.
```

## Package Layout

This repository is packaged for the open Agent Skills standard: a skill package repo containing a skill folder with a required `SKILL.md`.

```text
product-claim-auditor-skill/
├── README.md
└── product-claim-auditor/
    ├── SKILL.md
    └── references/
        ├── marketing-ambiguity-patterns.md
        └── web-search-playbook.md
```

## Contents

- `product-claim-auditor/SKILL.md`: Core workflow and output format.
- `product-claim-auditor/references/web-search-playbook.md`: Query tactics and source-priority rules.
- `product-claim-auditor/references/marketing-ambiguity-patterns.md`: Common marketing loopholes and research questions.

## Safety Notes

This is a Markdown-only skill package. It does not include executable scripts or tool integrations.
