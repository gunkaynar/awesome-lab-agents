# Contributing to Awesome Lab Agents

Thanks for helping curate this list! This guide explains how to add, edit or report entries.

The list covers AI agents that plan or run experiments on physical laboratory hardware, plus the benchmarks, simulators, tooling and surveys around them.

## Quick start

1. Fork the repo and create a branch off `main`.
2. Edit `readme.md` to add or update an entry.
3. Open a pull request. `awesome-lint` runs automatically.

If you only want to suggest a paper, open an issue using the **Paper Submission** template. Leads that still need their details checked are collected in [backlog.md](backlog.md).

## Entry format

Every entry is a single list item:

```markdown
- \[YYYY-MM\] ![tag1] ![tag2] "Title." Authors. Venue YYYY. [paper](url) | [code](url) | [project](url)
```

Rules:

- **Date**: `\[YYYY-MM\]` for the first public release (preprint date is fine). Use the first public code release for code-only entries. The brackets are escaped so the date is not read as a link.
- **Tags**: 1–3 shields.io badges from the taxonomy below, type tags first.
- **Title**: in double quotes, ending with a period inside the quotes. If the title does not name the system, add the name in parentheses, e.g. `"Augmenting large language models with chemistry tools (ChemCrow)."`
- **Authors**: `First Last et al.` for more than three authors.
- **Venue**: journal or conference plus year (e.g. `Nature 2023`). For preprints use `arXiv YYYY` or `bioRxiv YYYY`.
- **Links**: `[paper]` is required when a paper exists. Add `[code]`, `[project]`, `[blog]` or `[package]` as available, separated by ` | `. Code-only entries use `"Name" (code-only release).`

Example:

```markdown
- \[2023-12\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Autonomous chemical research with large language models (Coscientist)." Daniil A. Boiko et al. Nature 2023. [paper](https://doi.org/10.1038/s41586-023-06792-0) | [code](https://github.com/gomesgroup/coscientist)
```

## Tag taxonomy

Type tags (blue, `1f6feb`):

- `Multi-Agent` — system coordinates several agents
- `LLM-Agent` — a single language or vision-language model agent with tools
- `Closed-Loop` — the agent chooses the next round of experiments across several rounds
- `Benchmark` — evaluation suite, dataset or comparative study
- `Simulator` — simulated laboratory or digital twin
- `Framework` — reusable codebase, SDK or protocol language
- `MCP` — Model Context Protocol server for instruments
- `Survey` — review, survey or perspective
- `Platform` — lab operating system or hosted platform

Domain tags (green, `2da44e`) — pick when relevant:

- `Chemistry`, `Materials`, `Biology`, `Liquid-Handling`, `Microscopy`, `Synchrotron`, `Quantum`, `Optics`, `Safety`

Company tags (purple, `8250df`): `Cloud-Lab`, `Company`.

Badge URL format: `https://img.shields.io/badge/<TAG>-<COLOR>` (use `--` to escape literal hyphens, e.g. `Multi--Agent`).

## Sorting

Within each section, entries are sorted **reverse-chronologically by `YYYY-MM`**.

## Section choice

| Section | What goes here |
| --- | --- |
| 🧪 Chemistry & Materials | Robotic synthesis, electrochemistry, materials discovery |
| 🧬 Life Science | Cell culture, protein production, liquid handling, wet-lab biology |
| 🔬 Instruments & Facilities | Microscopes, beamlines, quantum hardware, optical setups |
| 📊 Benchmarks & Simulation | Benchmarks, simulators, digital twins |
| 🛠️ Lab Tooling | Protocol languages, lab operating systems, SDKs, MCP servers |
| 📚 Surveys & Perspectives | Reviews and perspectives |
| 🏛️ Foundations | Earlier autonomous laboratories and tool-using chemistry agents |
| 🏢 Companies & Cloud Labs | Companies and cloud laboratories |

If unsure, suggest a section in your pull request and a maintainer will help.

## PR checklist

- [ ] Entry follows the format template above
- [ ] Date is correct (`YYYY-MM`, first public release)
- [ ] Tags chosen from the taxonomy
- [ ] Placed in the correct section, in chronological order
- [ ] All links resolve (try them in a private window)
- [ ] No duplicate of an existing entry
- [ ] `awesome-lint` passes (run `npx awesome-lint` locally if possible)

## Reporting broken links

Open an issue using the **Broken Link** template. Pull requests that fix dead links are welcome.

## Code of conduct

Be respectful. We follow the [Contributor Covenant](https://www.contributor-covenant.org/).
