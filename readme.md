# Awesome Lab Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI agents that operate physical laboratories.

Almost every neighbouring list indexes software agents that read papers, write code and produce manuscripts. This list is only about agents whose actions move matter: an AI agent, driven by an LLM, VLM or foundation model with some planning or decision-making autonomy, connected to real laboratory hardware, with that connection demonstrated on actual hardware. That covers closed-loop design, execute, measure and redesign systems, agents whose protocols then run on real instruments even behind a human approval gate, instrument copilots that genuinely drive hardware, cloud-lab agents where execution is physical but offsite, and XR-mediated systems where the agent perceives and acts on the bench. Out of scope are dry-lab-only AI-scientist pipelines, in-silico chemistry agents with no hardware link, classical self-driving labs with no agentic decision layer, simulation-only embodied agents, and LIMS, ELNs and generic automation SDKs except as the substrate agents act through.

**Borderline rulings**, written down so the same argument does not recur in every pull request:

| Case | Ruling | Why |
|---|---|---|
| The Virtual Lab (AI agents designed SARS-CoV-2 nanobodies, Nature 646:716–723, 2025) | Out | Agents designed; humans ran the wet-lab validation. The agent never touched hardware. |
| LUMI-lab | In, with a note | Closed-loop and physical, but the decision layer is a pretrained foundation model plus active learning, not an agentic LLM. |
| ChemCrow | Background only | 18 expert tools, no hardware link. The single most common miscategorisation in neighbouring lists. |
| From Prompts to Protocols | In, marked ⚠️ | Real orchestration-system integration, but evaluated on three simulated labs. |
| A-Lab (2023) | Background only | ML plus active learning, no agentic decision layer. Always linked alongside its correction. |

**Not what you're looking for?**

- Agents that read papers, write code and run analyses: [Awesome-Agent-Scientists](https://github.com/AgenticScience/Awesome-Agent-Scientists#readme).
- LLM-driven self-driving labs graded on a five-level autonomy scale: [awesome-llm-self-driving-labs](https://github.com/Jianguo99/awesome-llm-self-driving-labs#readme).
- Physical AI for science more broadly, including robotics, lab automation and data tooling: [awesome-physical-ai-for-science](https://github.com/labclaw/awesome-physical-ai-for-science#readme).

## Contents

### Emoji Key

- 🔁 Closed-loop — the agent selects the next round of experiments across multiple rounds, without a human deciding between rounds.
- 📄 Peer-reviewed publication. Absence means preprint or technical report.
- 💻 Code publicly available. Partial availability is stated in the description.
- ⚠️ Hardware execution not fully demonstrated — simulation-only or partial.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighbouring rights to this work.
