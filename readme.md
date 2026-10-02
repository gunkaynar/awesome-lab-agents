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

- [Agents](#agents)
  - [Chemistry and Materials](#chemistry-and-materials)
  - [Biology and Life Sciences](#biology-and-life-sciences)
  - [Instruments and Facilities](#instruments-and-facilities)

### Emoji Key

- 🔁 Closed-loop — the agent selects the next round of experiments across multiple rounds, without a human deciding between rounds.
- 📄 Peer-reviewed publication. Absence means preprint or technical report.
- 💻 Code publicly available. Partial availability is stated in the description.
- ⚠️ Hardware execution not fully demonstrated — simulation-only or partial.

## Agents

### Chemistry and Materials

- 🔁 📄 💻 [Coscientist](https://doi.org/10.1038/s41586-023-06792-0) - GPT-4 planner that searches documentation, writes controller code, and runs palladium-catalysed cross-couplings on cloud-lab hardware. ([code](https://github.com/gomesgroup/coscientist) — simplified implementation and analysis outputs only; Apache-2.0 with Commons Clause, commercial use restricted)
- 🔁 📄 💻 [ChemAgents](https://doi.org/10.1021/jacs.4c17738) - Hierarchical multi-agent robotic chemist on an on-board Llama-3.1-70B, with a task manager coordinating literature, design, computation and robot-operator agents. ([code](https://github.com/pic-ai-robotic-chemistry/ChemAgents))
- 📄 💻 [ORGANA](https://doi.org/10.1016/j.matt.2024.10.015) - Chemistry robot that derives goals through dialogue and schedules parallel work, including a 19-step electrochemistry characterisation of quinone derivatives. ([code](https://github.com/ac-rad/organa))
- 📄 [CLAIRify](https://doi.org/10.1007/s10514-023-10136-2) - Translates natural language into the XDL protocol language behind a syntactic verifier, then executes it through a task-and-motion planner. ([project](https://ac-rad.github.io/clairify/))
- 📄 [LLM-RDF](https://doi.org/10.1038/s41467-024-54457-x) - Six GPT-4 agents, including a hardware executor, covering end-to-end development of a copper/TEMPO aerobic alcohol oxidation.
- 📄 💻 [AutoLabs](https://doi.org/10.1038/s41598-026-45593-z) - Self-correcting multi-agent system turning natural-language instructions into executable protocols for a high-throughput liquid handler. ([code](https://github.com/pnnl/autolabs))
- 🔁 📄 💻 [CRESt](https://doi.org/10.1038/s41586-025-09640-5) - Multimodal models over compositions, text and microstructural images driving robotic electrochemistry, exploring over 900 catalyst chemistries in three months. ([code](https://github.com/zhang21mit/CRESt))
- 🔁 📄 [MARS](https://doi.org/10.1016/j.matt.2025.102577) - Hierarchical system of 19 LLM agents and 16 domain tools that optimised perovskite nanocrystal synthesis within ten iterations.
- 🔁 [A-Lab GPSS](https://arxiv.org/abs/2604.11957) - Glovebox solid-state synthesis of air-sensitive materials, with agents reasoning abductively about anomalies and inductively across 352 synthesised samples.
- 🔁 [SynAgent](https://arxiv.org/abs/2609.18598) - Runs an automated deposition system while maintaining an explicit, revisable written account of the synthesis process as the campaign's main output.
- [AgentChemist](https://arxiv.org/abs/2603.23886) - Multi-agent robotic platform pairing task decomposition with chemical perception for real-time reaction monitoring and feedback-driven execution.
- 🔁 [La Agente Óptima](https://arxiv.org/abs/2609.04564) - Builds and supervises Bayesian-optimisation campaigns with auditable state, catching a mid-run measurement failure and inferring that a contact-angle target was unreachable.

### Biology and Life Sciences

- 🔁 [BioMARS](https://arxiv.org/abs/2507.01485) - Dual-arm platform with biologist, technician and inspector agents performing autonomous cell passaging and retinal pigment epithelial differentiation.
- 🔁 [GPT-5 autonomous lab](https://doi.org/10.64898/2026.02.05.703998) - Six closed-loop rounds across 36,000 cell-free protein synthesis conditions in a cloud lab, cutting benchmark protein cost from $698/g to $422/g. Preprint. ([summary](https://openai.com/index/gpt-5-lowers-protein-synthesis-cost/))
- [LabscriptAI](https://doi.org/10.1101/2025.09.30.679666) - Generates and self-corrects executable Python for heterogeneous liquid handlers, characterising 318 GFP variants across a biofoundry and a fume-hood robot. ([project](https://labscriptai.cn/))
- 💻 [LabOS](https://arxiv.org/abs/2510.14861) - Couples a self-evolving multi-agent dry-lab core to wet-lab execution through AR/XR smart glasses and robots. ([code](https://github.com/zaixizhang/LabOS) — dry-lab core only; hardware kit not yet released)
- 🔁 📄 [LUMI-lab](https://doi.org/10.1016/j.cell.2026.01.012) - Foundation-model-driven closed loop that synthesised and screened over 1,700 lipid nanoparticles and found brominated tails to improve mRNA delivery. Decision layer is a foundation model with active learning rather than an agentic LLM.

### Instruments and Facilities

- 📄 💻 [AILA](https://doi.org/10.1038/s41467-025-64105-7) - Runs atomic force microscopy end to end across calibration, imaging and analysis, and documents "sleepwalking" where agents execute unrequested steps on real instruments. ([code](https://github.com/M3RG-IITD/AILA))
- 📄 💻 [VISION](https://doi.org/10.1088/2632-2153/add9e4) - Modular assembly of LLM-scaffolded cognitive blocks that ran the first voice-controlled experiment at an X-ray scattering beamline. ([code](https://github.com/CFN-softbio/VISION))
- 📄 💻 [CALMS](https://doi.org/10.1038/s41524-024-01423-2) - Retrieval- and tool-augmented assistant that positioned a diffractometer at the Advanced Photon Source by resolving lattice constants into motor positions. ([code](https://github.com/mcherukara/CALMS) — repository inactive)
- 📄 💻 [Learn-on-the-job instrument agents](https://doi.org/10.1038/s41524-026-02005-0) - Operates an X-ray nanoprobe beamline and a robotic materials station, embedding spoken operator corrections as memories retrievable in later sessions. ([code](https://github.com/AdvancedPhotonSource/CALMS/tree/sdl_agents))
- [EAA](https://arxiv.org/abs/2602.15294) - Vision-language-model agents automating microscopy workflows, with instrument-control tools both consumed and served over the Model Context Protocol.
- 🔁 📄 💻 [k-agents](https://doi.org/10.1016/j.patter.2025.101372) - Decomposes experimental procedures into agent-based state machines and autonomously calibrated a superconducting quantum processor for hours. ([code](https://github.com/ShuxiangCao/LeeQ) — the orchestration substrate, not the agent layer)
- 📄 [Accelerator Assistant](https://doi.org/10.1103/jtqy-9jz1) - Executes multistage physics experiments on a production synchrotron through plan-first orchestration over EPICS, cutting preparation time by two orders of magnitude.
- 📄 💻 [AI X-ray Scientist](https://doi.org/10.1038/s42256-026-01261-5) - Aligns single crystals on a synchrotron beamline, transferring from a virtual diffractometer to real hardware with no retraining. ([code](https://doi.org/10.5281/zenodo.20017991))
- 🔁 [AIMS](https://arxiv.org/abs/2607.16544) - Operates cryogenic microwave impedance microscopy through three nested loops that convert perceptual, sampling and interpretive uncertainty into the next measurement.
- [Quailbot](https://arxiv.org/abs/2609.27302) - Agent harness delivering end-to-end LLM tip conditioning on a low-temperature scanning tunnelling microscope, focused on what to do when an experiment misbehaves.
- ⚠️ [OPERA](https://arxiv.org/abs/2608.05990) - Frames optical experiments as typed operators with physically interpretable residuals, cutting score-improvement-without-physical-improvement from 23.6–39.0% to 0.9–1.9%. Decisions in digital twins, protocols transferred to three real instruments.
- [Owl·AuraID](https://arxiv.org/abs/2603.29828) - GUI-native agent that drives instrument software directly rather than through APIs, for hardware that exposes no programmatic interface.
- ⚠️ [From Prompts to Protocols](https://arxiv.org/abs/2605.16552) - Agent embedded in a laboratory orchestration system over MCP, reporting 97% first-attempt protocol generation across three simulated labs.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighbouring rights to this work.
