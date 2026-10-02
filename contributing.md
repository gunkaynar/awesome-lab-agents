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
- \[YYYY-MM\] `tag1` `tag2` [Name](paper-url) - One-sentence description. Surname et al., "Title," Venue YYYY. [code](url)
```

Rules:

- **Date**: `\[YYYY-MM\]` is the date the linked version was first published online (the posting date of version 1 for preprints). Code-only entries use the month the repository was created. If the date cannot be confirmed from a primary source, leave it out; undated entries go at the end of their section.
- **Tags**: inline code spans from the taxonomy below: 1–3 type and domain tags, then any evidence tags that apply.
- **Name**: the system's short name, linked to the primary paper (or to the repository for code-only entries).
- **Description**: one sentence, starting with a capital letter and ending with a dot. Say what the system does, with at most one number and no marketing language. Keep factual caveats, such as simulation-only evaluation or partial code release.
- **Citation**: first author's surname (`et al.` for more than three authors), title in quotes, venue and year. For preprints use `arXiv YYYY` or `bioRxiv YYYY`.
- **Links**: add `[code]`, `[project]`, `[blog]`, `[package]` or `[correction]` after the citation as available. Code-only entries have no citation.
- **Sources**: take authors, dates, venues and numbers from the paper, the publisher's page or the repository itself, not from secondary lists.

Example:

```markdown
- \[2023-12\] `llm-agent` `chemistry` [Coscientist](https://doi.org/10.1038/s41586-023-06792-0) - GPT-4 system that reads hardware documentation and writes code to run experiments, performing Suzuki and Sonogashira couplings on a liquid handler and HPLC runs in the Emerald Cloud Lab. Boiko et al., "Autonomous chemical research with large language models," Nature 2023. [code](https://github.com/gomesgroup/coscientist)
```

## Tag taxonomy

Type:

- `multi-agent` — system coordinates several agents
- `llm-agent` — a single language or vision-language model agent with tools
- `closed-loop` — the agent chooses the next round of experiments across several rounds
- `benchmark` — evaluation suite or dataset
- `simulator` — simulated laboratory or digital twin
- `framework` — reusable codebase, SDK or protocol language
- `mcp` — Model Context Protocol server for instruments
- `survey` — review, survey or perspective
- `platform` — lab operating system or hosted platform

Domain (pick when relevant): `chemistry`, `materials`, `biology`, `liquid-handling`, `microscopy`, `synchrotron`, `quantum`, `optics`, `safety`.

Company: `cloud-lab`, `company`.

Evidence:

- `preprint` — the linked version has not appeared at a confirmed venue
- `simulation-only` — evaluated on simulated laboratories rather than real hardware
- `partial-hardware` — decisions made in simulation or digital twins, with only part of the work run on real hardware

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
