# Contributing to Awesome Lab Agents

Thanks for helping curate this list! This guide explains how to add, edit or report entries.

The list covers AI agents that plan or run experiments on physical laboratory hardware, plus the benchmarks, simulators, tooling and surveys around them.

## Quick start

1. Fork the repo and create a branch off `main`.
2. Edit `readme.md` to add or update an entry.
3. Open a pull request. `awesome-lint` runs automatically.

If you only want to suggest a paper, open an issue using the **Paper Submission** template. Leads that still need their details checked are collected in [backlog.md](backlog.md).

## Entry format

Every entry is a single list item: date, tags, short name linked to the primary paper, a one-sentence description, then the citation.

```markdown
- \[YYYY-MM\] ![Tag1](badge-url) ![Tag2](badge-url) [Name](paper-url) - One-sentence description. Surname et al., "Title," Venue YYYY. [code](url)
```

Rules:

- **Date**: `\[YYYY-MM\]` is the date the linked version was first published online (the posting date of version 1 for preprints). Code-only entries use the month the repository was created. Specifications use the publication date of their current version, as recorded by the standards body. If the date cannot be confirmed from a primary source, leave it out; undated entries go at the end of their section.
- **Tags**: shields.io badges from the taxonomy below: 1–3 type and domain tags, then any evidence tags that apply.
- **Name**: the system's short name, linked to the primary paper (or to the repository for code-only entries).
- **Description**: one sentence, starting with a capital letter and ending with a dot. Say what the system does, with at most one number and no marketing language. Keep factual caveats, such as simulation-only evaluation or partial code release.
- **Citation**: first author's surname (`et al.` for more than three authors), title in quotes, venue and year. For preprints use `arXiv YYYY` or `bioRxiv YYYY`.
- **Links**: add `[code]`, `[project]`, `[blog]`, `[package]` or `[correction]` after the citation as available. Code-only entries have no citation.
- **Sources**: take authors, dates, venues and numbers from the paper, the publisher's page or the repository itself, not from secondary lists.

Example:

```markdown
- \[2023-12\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) [Coscientist](https://doi.org/10.1038/s41586-023-06792-0) - GPT-4 system that reads hardware documentation and writes code to run experiments, performing Suzuki and Sonogashira couplings on a liquid handler and HPLC runs in the Emerald Cloud Lab, with reaction optimisation benchmarked on previously collected condition-space datasets. Boiko et al., "Autonomous chemical research with large language models," Nature 2023. [code](https://github.com/gomesgroup/coscientist)
```

## Tag taxonomy

Type (blue, `1f6feb`):

- `Multi-Agent` — system coordinates several agents
- `LLM-Agent` — a single language or vision-language model agent with tools
- `Closed-Loop` — see the test below
- `Benchmark` — evaluation suite or dataset
- `Simulator` — simulated laboratory or digital twin
- `Framework` — reusable codebase, SDK or protocol language
- `MCP` — Model Context Protocol server for instruments
- `Survey` — review, survey or perspective
- `Platform` — lab operating system or hosted platform

Domain (green, `2da44e`), pick when relevant: `Chemistry`, `Materials`, `Biology`, `Liquid-Handling`, `Microscopy`, `Synchrotron`, `Quantum`, `Optics`, `Safety`.

Company (purple, `8250df`): `Cloud-Lab`, `Company`.

Evidence (orange, `bc4c00`):

- `Preprint` — the linked version has not appeared at a confirmed venue
- `Vendor-Reported` — the only source for the system's capability claims is the vendor's own announcement or its launch partners' statements, with no paper, preprint or independent verification. It ranks below `Preprint` on the evidence ladder (peer-reviewed, then `Preprint`, then `Vendor-Reported`), and comes off only when a paper or independent verification appears; releasing code alone does not remove it.
- `Simulation-Only` — evaluated on simulated laboratories rather than real hardware
- `Partial-Hardware` — decisions made in simulation or digital twins, with only part of the work run on real hardware

Badge URL format: `https://img.shields.io/badge/<TAG>-<COLOR>` (use `--` to escape literal hyphens, e.g. `Multi--Agent`).

### The Closed-Loop test

All three must hold:

1. The system selected its next experiments itself. The agent layer must be inside the selection loop: it performs the selection, or it configures and runs the optimiser that does. An agent that only offers a natural-language front end to an optimisation loop that would run without it does not count. Delegating the arithmetic to a Bayesian optimiser that the agent builds and runs is fine.
2. The selection used results from physical experiments it had just run.
3. This happened across several rounds, with no human choosing between rounds.

It does not cover optimisation over previously collected datasets, a single multi-step workflow run on hardware, iterating toward a goal within one task such as aligning a crystal or conditioning a tip, or process control that adjusts operating conditions rather than choosing experiments.

Apply the tag when the best available evidence establishes all three, at whatever level of the paper supplies it (title, abstract, figure legends, methods or results), and say in your pull request which level that was. Read beyond the abstract when an abstract sentence is ambiguous about whether the optimisation was physical. Leave the tag off when the accessible evidence does not establish it.

Boundary case for reference: k-agents carries the tag. Humans write its natural-language transition rules, but the agents judge each experiment's result and choose the next stage across hours of unattended operation, which sits closer to in than out.

## Sorting

Within each section, entries are sorted **reverse-chronologically by `YYYY-MM`**, with undated entries last.

## Section choice

| Section | What goes here |
| --- | --- |
| 🧪 Chemistry & Materials | Robotic synthesis, electrochemistry, materials discovery |
| 🧬 Life Science | Cell culture, protein production, liquid handling, wet-lab biology |
| 🔬 Instruments & Facilities | Microscopes, beamlines, quantum hardware, optical setups |
| 📊 Benchmarks & Simulation | Benchmarks, simulators, digital twins |
| 🛠️ Lab Tooling | Protocol languages, lab operating systems, SDKs, MCP servers |
| 📚 Surveys & Perspectives | Reviews and perspectives |
| 🏛️ Foundations | Earlier autonomous laboratories that this work builds on |
| 🏢 Companies & Cloud Labs | Companies and cloud laboratories |

If unsure, suggest a section in your pull request and a maintainer will help.

## PR checklist

- [ ] Entry follows the format template above
- [ ] Date is correct (`YYYY-MM`, first public release)
- [ ] Tags chosen from the taxonomy, including evidence tags
- [ ] Authors, date, venue and any numbers checked against the primary source
- [ ] Placed in the correct section, in chronological order
- [ ] All links resolve (try them in a private window)
- [ ] No duplicate of an existing entry
- [ ] `awesome-lint` passes (run `npx awesome-lint` locally if possible)

## Reporting broken links

Open an issue using the **Broken Link** template. Pull requests that fix dead links are welcome.

## Code of conduct

Be respectful. We follow the [Contributor Covenant](https://www.contributor-covenant.org/).
