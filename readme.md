# Awesome Lab Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](LICENSE)

> A curated list of AI agents that operate physical laboratories.

Papers, tools and platforms where an AI agent plans or runs experiments on real laboratory hardware, from robotic chemistry and biology platforms to microscopes, beamlines and cloud labs, together with the benchmarks, simulators and tooling around them.

## Contents

- [Tag Legend](#tag-legend)
- [Chemistry & Materials](#chemistry--materials)
- [Life Science](#life-science)
- [Instruments & Facilities](#instruments--facilities)
- [Benchmarks & Simulation](#benchmarks--simulation)
- [Lab Tooling](#lab-tooling)
- [Surveys & Perspectives](#surveys--perspectives)
- [Foundations](#foundations)
- [Companies & Cloud Labs](#companies--cloud-labs)

## Tag Legend

Type: `multi-agent` `llm-agent` `closed-loop` `benchmark` `simulator` `framework` `mcp` `survey` `platform`

Domain: `chemistry` `materials` `biology` `liquid-handling` `microscopy` `synchrotron` `quantum` `optics` `safety`

Company: `cloud-lab` `company`

Evidence: `preprint` `simulation-only` `partial-hardware`

See the [contribution guidelines](contributing.md#tag-taxonomy) for tag definitions.

## Chemistry & Materials

🧪 Robotic synthesis, electrochemistry and materials discovery.

- \[2026-09\] `llm-agent` `closed-loop` `materials` `preprint` [SynAgent](https://arxiv.org/abs/2609.18598) - LLM agents run an automated thin-film deposition system while keeping an explicit, revisable account of the synthesis process as the campaign's main output. Takahara et al., "Hypothesis-Driven Autonomous Materials Synthesis with Multimodal LLM Agents," arXiv 2026.
- \[2026-09\] `llm-agent` `closed-loop` `materials` `preprint` [La Agente Óptima](https://arxiv.org/abs/2609.04564) - Builds and supervises Bayesian-optimisation campaigns with auditable state, and caught a mid-run measurement failure during a contact-angle campaign. Müller et al., "La Agente Óptima: Towards Agentic Self-Driving Laboratories," arXiv 2026.
- \[2026-06\] `multi-agent` `chemistry` `liquid-handling` [AutoLabs](https://doi.org/10.1038/s41598-026-45593-z) - Self-correcting multi-agent system turning natural-language instructions into executable protocols for a high-throughput liquid handler. Panapitiya et al., "AutoLabs: cognitive multi-agent systems with self-correction for autonomous chemical experimentation," Scientific Reports 2026. [code](https://github.com/pnnl/autolabs)
- \[2026-04\] `llm-agent` `closed-loop` `materials` `preprint` [A-Lab GPSS](https://arxiv.org/abs/2604.11957) - Glovebox solid-state synthesis of air-sensitive materials, with agents reasoning abductively and inductively across a 352-sample campaign. Fei et al., "Agentic LLM Reasoning in a Self-Driving Laboratory for Air-Sensitive Lithium Halide Spinel Conductors," arXiv 2026.
- \[2026-03\] `multi-agent` `chemistry` `preprint` [AgentChemist](https://arxiv.org/abs/2603.23886) - Multi-agent robotic platform pairing task decomposition with chemical perception for real-time reaction monitoring and feedback-driven execution. Wei et al., "AgentChemist: A Multi-Agent Experimental Robotic Platform Integrating Chemical Perception and Precise Control," arXiv 2026.
- \[2025-09\] `closed-loop` `materials` [CRESt](https://doi.org/10.1038/s41586-025-09640-5) - Multimodal models over compositions, text and microstructural images driving robotic electrochemistry, exploring over 900 catalyst chemistries. Zhang et al., "A multimodal robotic platform for multi-element electrocatalyst discovery," Nature 2025. [code](https://github.com/zhang21mit/CRESt)
- \[2025-03\] `multi-agent` `closed-loop` `chemistry` [ChemAgents](https://doi.org/10.1021/jacs.4c17738) - Hierarchical multi-agent robotic chemist on an on-board Llama-3.1-70B, with a task manager coordinating literature, design, computation and robot-operator agents. Song et al., "A Multiagent-Driven Robotic AI Chemist Enabling Autonomous Chemical Research On Demand," Journal of the American Chemical Society 2025. [code](https://github.com/pic-ai-robotic-chemistry/ChemAgents)
- \[2024-11\] `multi-agent` `chemistry` [LLM-RDF](https://doi.org/10.1038/s41467-024-54457-x) - Six GPT-4 agents, including a hardware executor, covering end-to-end development of a copper/TEMPO aerobic alcohol oxidation. Ruan et al., "An automatic end-to-end chemical synthesis development platform powered by large language models," Nature Communications 2024.
- \[2023-12\] `llm-agent` `closed-loop` `chemistry` [Coscientist](https://doi.org/10.1038/s41586-023-06792-0) - GPT-4 system that searches documentation, writes and executes code, and runs experiments on automated hardware, including palladium-catalysed cross-coupling optimisation. Boiko et al., "Autonomous chemical research with large language models," Nature 2023. [code](https://github.com/gomesgroup/coscientist) — supporting data and a simple implementation; commercial use restricted
- \[2023-10\] `llm-agent` `chemistry` [CLAIRify](https://doi.org/10.1007/s10514-023-10136-2) - Translates natural language into the XDL protocol language behind a syntactic verifier, then executes it through a task-and-motion planner. Yoshikawa et al., "Large language models for chemistry robotics," Autonomous Robots 2023. [project](https://ac-rad.github.io/clairify/)
- `multi-agent` `materials` [MARS](https://doi.org/10.1016/j.matt.2025.102577) - Collaborative multi-agent and robotic system for knowledge-driven autonomous materials research. Shi et al., "Knowledge-driven autonomous materials research via collaborative multi-agent and robotic system," Matter 2026.
- `llm-agent` `chemistry` [ORGANA](https://doi.org/10.1016/j.matt.2024.10.015) - Chemistry robot that derives goals through dialogue and schedules parallel work, including a 19-step electrochemistry characterisation of quinone derivatives. Darvish et al., "ORGANA: A robotic assistant for automated chemistry experimentation and characterization," Matter 2025. [code](https://github.com/ac-rad/organa)

## Life Science

🧬 Cell culture, protein production, liquid handling and wet-lab biology.

- \[2026-02\] `llm-agent` `closed-loop` `biology` `preprint` [GPT-5 autonomous lab](https://doi.org/10.64898/2026.02.05.703998) - GPT-5 runs iterative cell-free protein synthesis experiments on a cloud laboratory, reducing the specific cost of protein by 40% relative to the prior state of the art. Smith et al., "Using a GPT-5-driven autonomous lab to optimize the cost and titer of cell-free protein synthesis," bioRxiv 2026. [blog](https://openai.com/index/gpt-5-lowers-protein-synthesis-cost/)
- \[2026-02\] `closed-loop` `biology` [LUMI-lab](https://doi.org/10.1016/j.cell.2026.01.012) - Foundation model with active learning, rather than an agentic LLM, that synthesised and screened over 1,700 lipid nanoparticles and found brominated tails improve mRNA delivery. Xu et al., "LUMI-lab: A foundation model-driven autonomous platform enabling discovery of ionizable lipid designs for mRNA delivery," Cell 2026.
- \[2025-10\] `llm-agent` `liquid-handling` `biology` `preprint` [LabscriptAI](https://doi.org/10.1101/2025.09.30.679666) - Translates natural-language instructions into platform-specific liquid-handling robot scripts with bounded recovery under human oversight, including cell-free characterisation of 854 GFP designs. Gao et al., "Execution-aware agent harness for accessible and responsible synthetic biology automation," bioRxiv 2025. [project](https://labscriptai.cn/)
- \[2025-10\] `multi-agent` `biology` `preprint` [LabOS](https://arxiv.org/abs/2510.14861) - Couples a self-evolving multi-agent dry-lab core to wet-lab work through XR smart glasses and robots. Cong et al., "LabOS: The AI-XR Co-Scientist That Sees and Works With Humans," arXiv 2025. [code](https://github.com/zaixizhang/LabOS) — dry-lab core only
- \[2025-07\] `multi-agent` `closed-loop` `biology` `preprint` [BioMARS](https://arxiv.org/abs/2507.01485) - Robotic platform with biologist, technician and inspector agents performing autonomous cell passaging and retinal pigment epithelial differentiation. Qiu et al., "BioMARS: A Multi-Agent Robotic System for Autonomous Biological Experiments," arXiv 2025.

## Instruments & Facilities

🔬 Microscopes, beamlines, quantum hardware and optical setups.

- \[2026-09\] `llm-agent` `microscopy` `preprint` [Quailbot](https://arxiv.org/abs/2609.27302) - Agent harness that places an LLM inside the instrument feedback loop and completed end-to-end tip conditioning on a scanning tunnelling microscope. Cheng et al., "Unmodeled states and uncertain action outcomes in agentic scanning tunneling microscopy," arXiv 2026.
- \[2026-08\] `llm-agent` `optics` `preprint` `partial-hardware` [OPERA](https://arxiv.org/abs/2608.05990) - Represents optical experiments as operators with physically interpretable residuals, selecting protocols in digital twins and transferring them to three optical instruments. Xu et al., "OPERA: Operator-residual feedback for reliable autonomous optical experiments with language-model agents," arXiv 2026.
- \[2026-07\] `llm-agent` `synchrotron` [AI X-ray Scientist](https://doi.org/10.1038/s42256-026-01261-5) - Aligns single crystals on a synchrotron beamline, deploying a workflow developed on a virtual diffractometer directly to real hardware. Chen et al., "An agentic artificially intelligent X-ray scientist," Nature Machine Intelligence 2026. [code](https://doi.org/10.5281/zenodo.20017991)
- \[2026-07\] `closed-loop` `microscopy` `preprint` [AIMS](https://arxiv.org/abs/2607.16544) - Operates cryogenic microwave impedance microscopy through loops that convert perceptual, sampling and interpretive uncertainty into the next measurement. Qiu et al., "AIMS: an AI experimentalist turns uncertainty into quantum matter discovery," arXiv 2026.
- \[2026-05\] `llm-agent` `framework` `preprint` `simulation-only` [From Prompts to Protocols](https://arxiv.org/abs/2605.16552) - Agent integrated with the Experiment Orchestration System that creates and monitors lab protocols from natural language, evaluated on three simulated labs. Angelopoulos, Cahoon and Alterovitz, "From Prompts to Protocols: An AI Agent for Laboratory Automation," arXiv 2026.
- \[2026-03\] `llm-agent` `synchrotron` [Learn-on-the-job instrument agents](https://doi.org/10.1038/s41524-026-02005-0) - Human-in-the-loop LLM agents operating an X-ray nanoprobe beamline and an autonomous robotic materials station, improving through operator input. Vriza et al., "Operating advanced scientific instruments with AI agents that learn on the job," npj Computational Materials 2026. [code](https://github.com/AdvancedPhotonSource/CALMS/tree/sdl_agents)
- \[2026-03\] `framework` `preprint` [Owl-AuraID](https://arxiv.org/abs/2603.29828) - GUI-native agent system that operates instruments through the same software interfaces as human experts. Deng et al., "Owl-AuraID 1.0: An Intelligent System for Autonomous Scientific Instrumentation and Scientific Data Analysis," arXiv 2026. [code](https://github.com/OpenOwlab/AuraID)
- \[2026-02\] `llm-agent` `microscopy` `preprint` [EAA](https://arxiv.org/abs/2602.15294) - Vision-language-model agents automating microscopy workflows, with instrument-control tools both consumed and served over the Model Context Protocol. Du et al., "EAA: Automating materials characterization with vision language model agents," arXiv 2026.
- \[2026-01\] `llm-agent` `synchrotron` [Accelerator Assistant](https://doi.org/10.1103/jtqy-9jz1) - Executes multistage physics experiments on a production synchrotron light source through plan-first orchestration, cutting preparation time by two orders of magnitude. Hellert et al., "Agentic artificial intelligence for multistage physics experiments at a large-scale user facility particle accelerator," Physical Review Research 2026.
- \[2025-10\] `llm-agent` `benchmark` `microscopy` [AILA](https://doi.org/10.1038/s41467-025-64105-7) - LLM agents run atomic force microscopy from calibration to property measurement, evaluated with AFMBench's 100 expert-curated tasks. Mandal et al., "Evaluating large language model agents for automation of atomic force microscopy," Nature Communications 2025. [code](https://github.com/M3RG-IITD/AILA)
- \[2025-09\] `multi-agent` `closed-loop` `quantum` [k-agents](https://doi.org/10.1016/j.patter.2025.101372) - Decomposes experimental procedures into agent-based state machines, and planned and executed experiments on a superconducting quantum processor for hours. Cao et al., "Automating quantum computing laboratory experiments with an agent-based AI framework," Patterns 2025. [code](https://github.com/ShuxiangCao/LeeQ) — LeeQ, the experiment framework k-agents connects to
- \[2025-06\] `llm-agent` `synchrotron` [VISION](https://doi.org/10.1088/2632-2153/add9e4) - Modular assembly of LLM-scaffolded cognitive blocks that ran the first voice-controlled experiment at an X-ray scattering beamline. Mathur et al., "VISION: a modular AI assistant for natural human-instrument interaction at scientific user facilities," Machine Learning: Science and Technology 2025. [code](https://github.com/CFN-softbio/VISION)
- \[2024-11\] `llm-agent` `synchrotron` [CALMS](https://doi.org/10.1038/s41524-024-01423-2) - Retrieval- and tool-augmented assistant that moved a diffractometer by turning a user's lattice query into motor positions. Prince et al., "Opportunities for retrieval and tool augmented large language models in scientific facilities," npj Computational Materials 2024. [code](https://github.com/mcherukara/CALMS) — last updated April 2024

## Benchmarks & Simulation

📊 Benchmarks, simulators and digital twins for laboratory agents.

- \[2026-06\] `benchmark` `safety` `preprint` [ABC-Bench](https://arxiv.org/abs/2606.11150) - Agentic bio-capabilities benchmark for biosecurity evaluation. Liu et al., "ABC-Bench: An Agentic Bio-Capabilities Benchmark for Biosecurity," arXiv 2026.
- \[2026-01\] `benchmark` `safety` [LabSafety Bench](https://doi.org/10.1038/s42256-025-01152-1) - Benchmark of 765 multiple-choice questions plus open-ended laboratory scenarios on hazard identification, risk assessment and consequence prediction. Zhou et al., "Benchmarking large language models on safety risks in scientific laboratories," Nature Machine Intelligence 2026. [code](https://github.com/YujunZhou/LabSafety-Bench)
- \[2025-12\] `simulator` `chemistry` [MATTERIX](https://doi.org/10.1038/s43588-025-00924-4) - GPU-accelerated digital twin of a chemistry lab simulating manipulation, powders, liquids, heat transfer and reaction kinetics, with sim-to-real transfer. Darvish et al., "MATTERIX: toward a digital twin for robotics-assisted chemistry laboratory automation," Nature Computational Science 2026. [code](https://github.com/AccelerationConsortium/Matterix)
- \[2025-11\] `benchmark` `simulator` `synchrotron` `preprint` [EnvTrace](https://arxiv.org/abs/2511.09964) - Evaluates instrument-control code by aligning execution traces against a beamline digital twin, scoring over 30 LLMs and enabling pre-execution validation of live experiments. van der Vleuten et al., "EnvTrace: Simulation-Based Semantic Evaluation of LLM Code via Execution Trace Alignment -- Demonstrated at Synchrotron Beamlines," arXiv 2025. [code](https://github.com/CFN-softbio/EnvTrace)
- \[2025-05\] `simulator` `benchmark` [LabUtopia](https://arxiv.org/abs/2505.22634) - Isaac Sim laboratory simulator and hierarchical benchmark with chemically meaningful interactions and 30 tasks from atomic actions to long-horizon mobile manipulation. Li et al., "LabUtopia: High-Fidelity Simulation and Hierarchical Benchmark for Scientific Embodied Agents," NeurIPS 2025. [code](https://github.com/Rui-li023/LabUtopia)

## Lab Tooling

🛠️ Protocol languages, lab operating systems, SDKs and MCP servers that agents act through.

- \[2026-09\] `mcp` [LabMCP](https://github.com/K-Dense-AI/lab-instrument-mcps) - MCP servers for real instruments with safety limits, read-only modes, audit trails and a simulator per instrument; its Opentrons server is tested against a simulator and not yet verified on hardware. [package](https://pypi.org/project/labmcp-opentrons/)
- \[2026-07\] `mcp` `liquid-handling` [plr-mcp](https://github.com/di-omics/plr-mcp) - MCP server exposing a PyLabRobot liquid handler, plate reader, thermocycler and heater-shaker, running in simulation by default with one environment variable to target real hardware.
- \[2026-05\] `framework` `liquid-handling` `preprint` [IvoryOS](https://arxiv.org/abs/2605.03205) - Natural-language closed-loop control of a mobile liquid handler through MCP and the IvoryOS orchestration layer, where an agent ran a 60-trial accuracy optimisation; documented in a community hackathon report. Roy et al., "From Knowledge to Action: Outcomes of the 2025 Large Language Model (LLM) Hackathon for Applications in Materials Science and Chemistry," arXiv 2026. [code](https://github.com/ivoryos-ai/IvoryOS)
- \[2026-04\] `mcp` `liquid-handling` [OpenLabAI](https://github.com/nygmeta/OpenLabAI) - MCP servers for Opentrons, Hamilton, Biomek and Cellario that give no raw hardware access and never move a robot without explicit per-run approval.
- \[2026-03\] `framework` [device-use](https://github.com/labclaw/device-use) - Lets agents operate lab instruments through their existing GUI software, for devices with no API.
- \[2025-12\] `framework` `platform` `preprint` [Uni-Lab-OS](https://arxiv.org/abs/2512.21766) - Operating system for autonomous labs with a dual topology of logical ownership and physical connectivity, reconciling digital state with material motion through a transactional protocol. Gao et al., "UniLabOS: An AI-Native Operating System for Autonomous Laboratories," arXiv 2025. [code](https://github.com/deepmodeling/Uni-Lab-OS)
- \[2023-08\] `framework` [science-jubilee](https://github.com/machineagency/science-jubilee) - Python library for controlling Jubilee motion platforms for science.
- \[2022-08\] `framework` `liquid-handling` [PyLabRobot](https://github.com/PyLabRobot/pylabrobot) - Hardware-agnostic Python SDK that runs the same liquid-handling protocol on Hamilton, Tecan and Opentrons robots.
- \[2018-11\] `framework` `chemistry` [XDL](https://doi.org/10.1126/science.aav2211) - Chemical programming language that maps written procedures into unit operations executed on a modular robotic platform. Steiner et al., "Organic synthesis in a modular robotic system driven by a chemical programming language," Science 2019.

## Surveys & Perspectives

📚 Reviews and perspectives on agents in experimental science.

- \[2026-08\] `survey` `biology` `preprint` [Towards Human-Led, Agent-Driven Autonomous Laboratories](https://doi.org/10.20944/preprints202608.0273.v1) - Distinguishes scripted automation from AI-enabled autonomy and outlines a staged roadmap toward human-led, agent-driven life-science laboratories. Cheng et al., "Towards Human-Led, Agent-Driven Autonomous Laboratories for the Life Sciences," Preprints.org 2026.
- \[2026-05\] `survey` `chemistry` `materials` [Autonomous Chemistry and Materials Innovation Driven by Scientific Agents](https://doi.org/10.1021/jacsau.6c00213) - Five-module framework of comprehension, design, execution, analysis and optimisation for agent-enabled self-driving labs. Xie et al., "Autonomous Chemistry and Materials Innovation Driven by Scientific Agents," JACS Au 2026.
- \[2026-03\] `survey` `preprint` [Embodied Science](https://arxiv.org/abs/2603.19782) - Proposes a perception-language-action-discovery framework in which embodied agents couple scientific reasoning with physical execution. Zhuang et al., "Embodied Science: Closing the Discovery Loop with Agentic Embodied AI," arXiv 2026.
- \[2026-01\] `survey` `materials` `preprint` [Agentic AI for Self-Driving Laboratories in Soft Matter](https://arxiv.org/abs/2601.17920) - Frames laboratory autonomy as an agent-environment problem under expensive actions, delayed feedback and hard safety constraints. Chen et al., "Agentic AI for Self-Driving Laboratories in Soft Matter: Taxonomy, Benchmarks,and Open Challenges," arXiv 2026.
- \[2025-08\] `survey` `chemistry` `preprint` [Large Language Models Transform Organic Synthesis](https://arxiv.org/abs/2508.05427) - Review tracing language models from reaction prediction and retrosynthesis to robotic execution, with numerical claims checked against primary sources. Kumar, Kumar and Lagun, "Large Language Models Transform Organic Synthesis From Reaction Prediction to Automation," arXiv 2025.
- \[2025-08\] `survey` `preprint` [From AI for Science to Agentic Science](https://arxiv.org/abs/2508.14111) - Domain-oriented survey of autonomous scientific discovery across life sciences, chemistry, materials science and physics. Wei et al., "From AI for Science to Agentic Science: A Survey on Autonomous Scientific Discovery," arXiv 2025.

## Foundations

🏛️ Earlier autonomous laboratories and tool-using chemistry agents that this work builds on.

- \[2024-05\] `closed-loop` `materials` [Delocalized closed-loop discovery](https://doi.org/10.1126/science.adk9227) - Cloud-based AI planner coordinating distributed robotic synthesis and characterisation across laboratories to discover organic laser materials. Strieth-Kalthoff et al., "Delocalized, asynchronous, closed-loop discovery of organic laser emitters," Science 2024.
- \[2024-05\] `llm-agent` `chemistry` [ChemCrow](https://doi.org/10.1038/s42256-024-00832-8) - GPT-4 chemistry agent with 18 expert-designed tools that planned and executed syntheses autonomously. M. Bran et al., "Augmenting large language models with chemistry tools," Nature Machine Intelligence 2024.
- \[2023-11\] `closed-loop` `materials` [A-Lab](https://doi.org/10.1038/s41586-023-06734-w) - Autonomous solid-state synthesis of inorganic powders combining computations, literature data, machine learning and active learning over 17 days of continuous operation. Szymanski et al., "An autonomous laboratory for the accelerated synthesis of inorganic materials," Nature 2023. [correction](https://doi.org/10.1038/s41586-025-09992-y)
- \[2023-03\] `closed-loop` `chemistry` [AlphaFlow](https://doi.org/10.1038/s41467-023-37139-y) - Self-driven fluidic lab that uses reinforcement learning to discover and optimise multi-step chemistries. Volk et al., "AlphaFlow: autonomous discovery and optimization of multi-step chemistry using a self-driven fluidic lab guided by reinforcement learning," Nature Communications 2023.
- \[2020-07\] `closed-loop` `chemistry` [Mobile robotic chemist](https://doi.org/10.1038/s41586-020-2442-2) - Mobile robot that autonomously ran 688 experiments searching for improved hydrogen-production photocatalysts. Burger et al., "A mobile robotic chemist," Nature 2020.

## Companies & Cloud Labs

🏢 Companies and cloud laboratories working on autonomous experimentation.

- `cloud-lab` [Emerald Cloud Lab](https://www.emeraldcloudlab.com/) - Remotely controlled, highly automated life-science laboratory in Austin.
- `cloud-lab` [Ginkgo Bioworks](https://www.ginkgobioworks.com/) - Cloud laboratory and autonomous-lab automation for biotech research and development.
- `company` [Lila Sciences](https://www.lila.ai/) - Company building an operating system for science.
- `company` [Periodic Labs](https://periodic.com/) - AI research and deployment company creating models and autonomous labs.
- `company` [Radical AI](https://www.radical-ai.com/) - Company focused on accelerating materials research and development.

## Related Lists

- [awesome-physical-ai-for-science](https://github.com/labclaw/awesome-physical-ai-for-science#readme) - Physical AI for science, including robotics, lab automation and AI agents.
- [Awesome-Agent-Scientists](https://github.com/AgenticScience/Awesome-Agent-Scientists#readme) - Agents for autonomous scientific discovery.
- [Awesome-LLM-Agents-Scientific-Discovery](https://github.com/zjlrock777/Awesome-LLM-Agents-Scientific-Discovery#readme) - LLM agents in biomedical research.
- [awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch#readme) - Autonomous research loops and research agents.
- [awesome-lab](https://github.com/seifip/awesome-lab#readme) - Lab notebooks, information management systems and laboratory tooling.

## Contributing

Contributions are very welcome. Please read the [contribution guidelines](contributing.md) before opening a pull request, or suggest a paper by opening an [issue](https://github.com/gunkaynar/awesome-lab-agents/issues/new/choose).
