# Awesome Lab Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI agents that operate physical laboratories.

Almost every neighbouring list indexes software agents that read papers, write code and produce manuscripts. This list is only about agents whose actions move matter: an AI agent, driven by an LLM, VLM or foundation model with some planning or decision-making autonomy, connected to real laboratory hardware, with that connection demonstrated on actual hardware. That covers closed-loop design, execute, measure and redesign systems, agents whose protocols then run on real instruments even behind a human approval gate, instrument copilots that genuinely drive hardware, cloud-lab agents where execution is physical but offsite, and XR-mediated systems where the agent perceives and acts on the bench. Out of scope are dry-lab-only AI-scientist pipelines, in-silico chemistry agents with no hardware link, classical self-driving labs with no agentic decision layer, simulation-only embodied agents, and LIMS, ELNs and generic automation SDKs except as the substrate agents act through.

**Borderline rulings**, written down so the same argument does not recur in every pull request:

- **The Virtual Lab** (AI agents designed SARS-CoV-2 nanobodies, Nature 646:716–723, 2025): out. Agents designed; humans ran the wet-lab validation. The agent never touched hardware.
- **LUMI-lab**: in, with a note. Closed-loop and physical, but the decision layer is a pretrained foundation model plus active learning, not an agentic LLM.
- **ChemCrow**: Background only. 18 expert tools, no hardware link. The single most common miscategorisation in neighbouring lists.
- **From Prompts to Protocols**: in, marked ⚠️. Real orchestration-system integration, but evaluated on three simulated labs.
- **A-Lab** (2023): Background only. ML plus active learning, no agentic decision layer. Always linked alongside its correction.

**Not what you're looking for?**

<!--lint disable double-link-->

- Agents that read papers, write code and run analyses: [Awesome-Agent-Scientists](https://github.com/AgenticScience/Awesome-Agent-Scientists#readme).
- LLM-driven self-driving labs graded on a five-level autonomy scale: [awesome-llm-self-driving-labs](https://github.com/Jianguo99/awesome-llm-self-driving-labs#readme).
- Physical AI for science more broadly, including robotics, lab automation and data tooling: [awesome-physical-ai-for-science](https://github.com/labclaw/awesome-physical-ai-for-science#readme).

<!--lint enable double-link-->

## Contents

- [Emoji Key](#emoji-key)
- [Agents](#agents)
  - [Chemistry and Materials](#chemistry-and-materials)
  - [Biology and Life Sciences](#biology-and-life-sciences)
  - [Instruments and Facilities](#instruments-and-facilities)
- [Benchmarks, Simulators and Digital Twins](#benchmarks-simulators-and-digital-twins)
- [Tooling](#tooling)
- [Critical Reading](#critical-reading)
- [Surveys](#surveys)
- [Background](#background)
- [Organizations](#organizations)

## Emoji Key

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
  <!--lint disable double-link-->
- 💻 [LabOS](https://arxiv.org/abs/2510.14861) - Couples a self-evolving multi-agent dry-lab core to wet-lab execution through AR/XR smart glasses and robots. ([code](https://github.com/zaixizhang/LabOS) — dry-lab core only; hardware kit not yet released)
  <!--lint enable double-link-->
- 🔁 📄 [LUMI-lab](https://doi.org/10.1016/j.cell.2026.01.012) - Foundation-model-driven closed loop that synthesised and screened over 1,700 lipid nanoparticles and found brominated tails to improve mRNA delivery. Decision layer is a foundation model with active learning rather than an agentic LLM.

### Instruments and Facilities

<!--lint disable double-link-->

- 📄 💻 [AILA](https://doi.org/10.1038/s41467-025-64105-7) - Runs atomic force microscopy end to end across calibration, imaging and analysis, and documents "sleepwalking" where agents execute unrequested steps on real instruments. ([code](https://github.com/M3RG-IITD/AILA))
  <!--lint enable double-link-->
- 📄 💻 [VISION](https://doi.org/10.1088/2632-2153/add9e4) - Modular assembly of LLM-scaffolded cognitive blocks that ran the first voice-controlled experiment at an X-ray scattering beamline. ([code](https://github.com/CFN-softbio/VISION))
- 📄 💻 [CALMS](https://doi.org/10.1038/s41524-024-01423-2) - Retrieval- and tool-augmented assistant that positioned a diffractometer at the Advanced Photon Source by resolving lattice constants into motor positions. ([code](https://github.com/mcherukara/CALMS) — repository inactive)
- 📄 💻 [Learn-on-the-job instrument agents](https://doi.org/10.1038/s41524-026-02005-0) - Operates an X-ray nanoprobe beamline and a robotic materials station, embedding spoken operator corrections as memories retrievable in later sessions. ([code](https://github.com/AdvancedPhotonSource/CALMS/tree/sdl_agents))
- [EAA](https://arxiv.org/abs/2602.15294) - Vision-language-model agents automating microscopy workflows, with instrument-control tools both consumed and served over the Model Context Protocol.
- 🔁 📄 💻 [k-agents](https://doi.org/10.1016/j.patter.2025.101372) - Decomposes experimental procedures into agent-based state machines and autonomously calibrated a superconducting quantum processor for hours. ([code](https://github.com/ShuxiangCao/LeeQ) — the orchestration substrate, not the agent layer)
- 📄 [Accelerator Assistant](https://doi.org/10.1103/jtqy-9jz1) - Executes multistage physics experiments on a production synchrotron through plan-first orchestration over EPICS, cutting preparation time by two orders of magnitude.
- 📄 💻 [AI X-ray Scientist](https://doi.org/10.1038/s42256-026-01261-5) - Aligns single crystals on a synchrotron beamline, transferring from a virtual diffractometer to real hardware with no retraining. ([code](https://doi.org/10.5281/zenodo.20017991))
- 🔁 [AIMS](https://arxiv.org/abs/2607.16544) - Operates cryogenic microwave impedance microscopy through three nested loops that convert perceptual, sampling and interpretive uncertainty into the next measurement.
- [Quailbot](https://arxiv.org/abs/2609.27302) - Agent harness delivering end-to-end LLM tip conditioning on a low-temperature scanning tunnelling microscope, focused on what to do when an experiment misbehaves.
  <!--lint disable double-link-->
- ⚠️ [OPERA](https://arxiv.org/abs/2608.05990) - Frames optical experiments as typed operators with physically interpretable residuals, cutting score-improvement-without-physical-improvement from 23.6–39.0% to 0.9–1.9%. Decisions in digital twins, protocols transferred to three real instruments.
  <!--lint enable double-link-->
- [Owl·AuraID](https://arxiv.org/abs/2603.29828) - GUI-native agent that drives instrument software directly rather than through APIs, for hardware that exposes no programmatic interface.
- ⚠️ [From Prompts to Protocols](https://arxiv.org/abs/2605.16552) - Agent embedded in a laboratory orchestration system over MCP, reporting 97% first-attempt protocol generation across three simulated labs.

## Benchmarks, Simulators and Digital Twins

- 📄 💻 [AFMBench](https://github.com/M3RG-IITD/AILA) - 100 curated atomic force microscopy tasks that require physical execution on hardware rather than simulated scoring.
- 💻 [LabUtopia](https://github.com/Rui-li023/LabUtopia) - Isaac Sim laboratory simulator and hierarchical benchmark with chemical-reaction modelling, 200+ instrument assets and 30+ tasks across five levels. ([paper](https://arxiv.org/abs/2505.22634))
- 📄 💻 [MATTERIX](https://doi.org/10.1038/s43588-025-00924-4) - GPU-accelerated digital twin of a chemistry lab simulating manipulation, powders, liquids, heat transfer and reaction kinetics, with sim-to-real transfer. ([code](https://github.com/AccelerationConsortium/Matterix))
- 💻 [EnvTrace](https://github.com/CFN-softbio/EnvTrace) - Evaluates instrument-control code by aligning execution traces against a beamline digital twin, scoring over 30 LLMs and enabling pre-execution validation of live experiments. ([paper](https://arxiv.org/abs/2511.09964))
- 📄 💻 [LabSafety Bench](https://doi.org/10.1038/s42256-025-01152-1) - 765 OSHA-aligned questions plus open-ended scenarios, on which no evaluated model exceeded 70% accuracy at hazard identification. ([code](https://github.com/YujunZhou/LabSafety-Bench))
  <!--lint disable double-link-->
- [LabSuperVision](https://arxiv.org/abs/2510.14861) - Egocentric laboratory perception benchmark built from over 240 researcher-worn video sessions.
  <!--lint enable double-link-->
- [ABC-Bench](https://arxiv.org/abs/2606.11150) - Agentic bio-capabilities benchmark framed for biosecurity evaluation.

## Tooling

- 💻 [PyLabRobot](https://github.com/PyLabRobot/pylabrobot) - Hardware-agnostic SDK running one protocol across Hamilton, Tecan and Opentrons, with chatterbox backends that log commands instead of sending them.
- 📄 💻 [Uni-Lab-OS](https://github.com/deepmodeling/Uni-Lab-OS) - Operating system for autonomous labs with a dual topology of logical ownership and physical connectivity, reconciling digital state against material motion through transactional rollback. ([paper](https://arxiv.org/abs/2512.21766))
- 💻 [LeeQ](https://github.com/ShuxiangCao/LeeQ) - Framework for orchestrating, simulating and automating superconducting-qubit experiments.
- 💻 [plr-mcp](https://github.com/di-omics/plr-mcp) - MCP server exposing a PyLabRobot liquid handler, plate reader, thermocycler and heater-shaker, in simulation by default with one variable to target real hardware.
- 💻 [LabMCP](https://github.com/K-Dense-AI/lab-instrument-mcps) - MCP servers for real instruments with safety limits, read-only modes, audit trails and a simulator per instrument.
- 💻 [labmcp-opentrons](https://pypi.org/project/labmcp-opentrons/) - MCP server for Opentrons OT-2 and Flex over the documented HTTP API, with tools tagged read or write. Simulator-tested, not yet hardware-verified.
- 💻 [OpenLabAI](https://github.com/nygmeta/OpenLabAI) - MCP servers for Opentrons, Hamilton, Biomek and Cellario that give no raw hardware access and never move a robot without explicit per-run approval.
- 💻 [device-use](https://github.com/labclaw/device-use) - Lets agents operate lab instruments through their existing GUI software, for devices with no API.
- 💻 [science-jubilee](https://github.com/machineagency/science-jubilee) - Python control for Jubilee motion platforms, a common low-cost substrate in academic self-driving labs.
- [IvoryOS](https://arxiv.org/abs/2605.03205) - Natural-language closed-loop control of a mobile liquid handler, where an agent built a six-parameter accuracy optimisation over 60 trials with no manual scripting. Documented in a community hackathon report rather than a dedicated paper.
- 📄 [XDL](https://doi.org/10.1126/science.aav2211) - Chemical description language used as a protocol intermediate representation.

## Critical Reading

<!--lint disable double-link-->

*The field's failure modes are as informative as its successes.*

- [Large language models do not replace chemists in a closed-loop catalysis experiment](https://doi.org/10.21203/rs.3.rs-10032842/v1) - GPT-5.1 against human experts over a 528-experiment robotic campaign; in a like-for-like final phase of 160 experiments the humans' formulation was on average more active. Preprint.
- 📄 [Author Correction: An autonomous laboratory for the accelerated synthesis of inorganic materials](https://doi.org/10.1038/s41586-025-09992-y) - Narrows the original novelty claim to materials new to the prediction platform rather than new to science, and revises the successful-compound count downward.
- 📄 [Sleepwalking in laboratory agents](https://doi.org/10.1038/s41467-025-64105-7) - Within the AILA paper: agents deviating from instructions and executing unauthorised extra steps on real instruments.
- [Score-only feedback misleads embodied agents](https://arxiv.org/abs/2608.05990) - Within the OPERA paper: 23.6–39.0% of score-only decisions improved the metric without improving the experiment, against 0.9–1.9% with physically grounded residuals.
- [Towards Human-Led, Agent-Driven Autonomous Laboratories for the Life Sciences](https://doi.org/10.20944/preprints202608.0273.v1) - Names the reality gap between AI-generated experimental intent and audit-grade wet-lab outcomes. Preprint.

**A note on safety.** This list indexes and classifies published systems, papers and open-source tools. It does not aggregate protocols, reagent specifications or operational parameters: entry descriptions say what a system is, never how to reproduce a hazardous procedure, and biosecurity and laboratory-safety benchmarks are listed by title, venue and purpose only. Safety evaluations are included because no evaluated model yet clears a reliable bar on hazard identification, and anyone wiring an agent to hardware should know that first. Removal requests go through [issues](https://github.com/gunkaynar/awesome-lab-agents/issues).

## Surveys

- [Embodied Science: Closing the Discovery Loop with Agentic Embodied AI](https://arxiv.org/abs/2603.19782) - Argues for exactly the boundary this list draws between computational and physical scientific agency.
- [Agentic AI for Self-Driving Laboratories in Soft Matter](https://arxiv.org/abs/2601.17920) - Frames laboratory autonomy as an agent-environment problem under expensive actions, delayed feedback and hard safety constraints.
- [Large Language Models Transform Organic Synthesis](https://arxiv.org/abs/2508.05427) - Source-verified evidence ladder that insists on comparing agentic autonomy against strong non-LLM autonomous baselines.
- 📄 [Autonomous Chemistry and Materials Innovation Driven by Scientific Agents](https://doi.org/10.1021/jacsau.6c00213) - Five-module framework of comprehension, design, execution, analysis and optimisation for agent-enabled self-driving labs.
- [From AI for Science to Agentic Science](https://arxiv.org/abs/2508.14111) - Broad survey of autonomous scientific discovery, useful for policing the dry-lab boundary.

## Background

Closed-loop autonomy predates language agents, and depends on far more than an LLM. The [A-Lab](https://doi.org/10.1038/s41586-023-06734-w) combined robotics, ab-initio databases, text-mined synthesis heuristics and active learning over 17 days of continuous operation — read it alongside its [correction](https://doi.org/10.1038/s41586-025-09992-y). Earlier still, the [mobile robotic chemist](https://doi.org/10.1038/s41586-020-2442-2) ran a batched Bayesian photocatalysis search with a free-roaming robot, [AlphaFlow](https://doi.org/10.1038/s41467-023-37139-y) applied reinforcement learning to a self-driven fluidic lab, and [delocalized closed-loop discovery of organic laser emitters](https://doi.org/10.1126/science.adk9227) distributed a campaign across institutions. [ChemCrow](https://doi.org/10.1038/s42256-024-00832-8) belongs here rather than above: 18 expert chemistry tools, no hardware link.

<!--lint enable double-link-->

## Organizations

*Claims made by companies about their own systems are rarely independently verifiable.*

- [Ginkgo Bioworks](https://www.ginkgobioworks.com/) - Cloud laboratory built on reconfigurable automation carts; the execution substrate in the GPT-5 protein synthesis work, and the only entry here with both a linked preprint and a product derived from an agent-run campaign.
- [Lila Sciences](https://www.lila.ai/) - Autonomous laboratories across life, chemical and materials sciences, where agents determine and vary thin-film sputtering recipes.
- [Periodic Labs](https://periodic.com/) - AI scientists paired with autonomous labs, with a first facility built around powder synthesis.
- [Radical AI](https://www.radical-ai.com/) - Full-stack materials discovery moving from AI-guided manual synthesis toward robotic high-throughput.
- [Emerald Cloud Lab](https://www.emeraldcloudlab.com/) - Remote laboratory execution accessible to external agents; the cloud lab Coscientist ran against.

## Related Lists

<!--lint disable double-link-->

- [awesome-llm-self-driving-labs](https://github.com/Jianguo99/awesome-llm-self-driving-labs#readme) - LLM-powered self-driving labs, benchmarks and surveys, organised around a five-level autonomy scale; the closest neighbour to this list.
- [awesome-physical-ai-for-science](https://github.com/labclaw/awesome-physical-ai-for-science#readme) - Resources where robotics, lab automation and AI agents converge on scientific discovery.
- [Awesome-Agent-Scientists](https://github.com/AgenticScience/Awesome-Agent-Scientists#readme) - Autonomous scientific discovery agents, centred on computational rather than physical work.
- [awesome-llm-agents-scientific-discovery](https://github.com/zhoujieli/awesome-llm-agents-scientific-discovery#readme) - LLM-powered agents in biomedical research, centred on literature and analysis.
- [awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch#readme) - Autonomous research systems and self-improving software loops.
- [awesome-lab](https://github.com/seifip/awesome-lab#readme) - Electronic lab notebooks, information management systems and laboratory tooling.

<!--lint enable double-link-->

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.

