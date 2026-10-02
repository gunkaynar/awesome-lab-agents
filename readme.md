# Awesome Lab Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![Last Commit](https://img.shields.io/github/last-commit/gunkaynar/awesome-lab-agents)](https://github.com/gunkaynar/awesome-lab-agents/commits/main)

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

Type tags (blue): ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) ![Simulator](https://img.shields.io/badge/Simulator-1f6feb) ![Framework](https://img.shields.io/badge/Framework-1f6feb) ![MCP](https://img.shields.io/badge/MCP-1f6feb) ![Survey](https://img.shields.io/badge/Survey-1f6feb) ![Platform](https://img.shields.io/badge/Platform-1f6feb)

Domain tags (green): ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) ![Materials](https://img.shields.io/badge/Materials-2da44e) ![Biology](https://img.shields.io/badge/Biology-2da44e) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) ![Microscopy](https://img.shields.io/badge/Microscopy-2da44e) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) ![Quantum](https://img.shields.io/badge/Quantum-2da44e) ![Optics](https://img.shields.io/badge/Optics-2da44e) ![Safety](https://img.shields.io/badge/Safety-2da44e)

Company tags (purple): ![Cloud-Lab](https://img.shields.io/badge/Cloud--Lab-8250df) ![Company](https://img.shields.io/badge/Company-8250df)

See the [contribution guidelines](contributing.md#tag-taxonomy) for tag definitions.

## Chemistry & Materials

🧪 Robotic synthesis, electrochemistry and materials discovery.

- \[2026-09\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "Hypothesis-Driven Autonomous Materials Synthesis with Multimodal LLM Agents (SynAgent)." Izumi Takahara et al. arXiv 2026. [paper](https://arxiv.org/abs/2609.18598)
- \[2026-09\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "La Agente Óptima: Towards Agentic Self-Driving Laboratories." Marcel Müller et al. arXiv 2026. [paper](https://arxiv.org/abs/2609.04564)
- \[2026-06\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) "AutoLabs: cognitive multi-agent systems with self-correction for autonomous chemical experimentation." Gihan Panapitiya et al. Scientific Reports 2026. [paper](https://doi.org/10.1038/s41598-026-45593-z) | [code](https://github.com/pnnl/autolabs)
- \[2026-04\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "Agentic LLM Reasoning in a Self-Driving Laboratory for Air-Sensitive Lithium Halide Spinel Conductors." Yuxing Fei et al. arXiv 2026. [paper](https://arxiv.org/abs/2604.11957)
- \[2026-03\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "AgentChemist: A Multi-Agent Experimental Robotic Platform Integrating Chemical Perception and Precise Control." Xiangyi Wei et al. arXiv 2026. [paper](https://arxiv.org/abs/2603.23886)
- \[2026-01\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "Knowledge-driven autonomous materials research via collaborative multi-agent and robotic system (MARS)." Tongyu Shi et al. Matter 2026. [paper](https://doi.org/10.1016/j.matt.2025.102577)
- \[2025-09\] ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "A multimodal robotic platform for multi-element electrocatalyst discovery (CRESt)." Zhen Zhang et al. Nature 2025. [paper](https://doi.org/10.1038/s41586-025-09640-5) | [code](https://github.com/zhang21mit/CRESt)
- \[2025-03\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "A Multiagent-Driven Robotic AI Chemist Enabling Autonomous Chemical Research On Demand (ChemAgents)." Tao Song et al. Journal of the American Chemical Society 2025. [paper](https://doi.org/10.1021/jacs.4c17738) | [code](https://github.com/pic-ai-robotic-chemistry/ChemAgents)
- \[2024-11\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "ORGANA: A robotic assistant for automated chemistry experimentation and characterization." Kourosh Darvish et al. Matter 2025. [paper](https://doi.org/10.1016/j.matt.2024.10.015) | [code](https://github.com/ac-rad/organa)
- \[2024-11\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "An automatic end-to-end chemical synthesis development platform powered by large language models (LLM-RDF)." Yixiang Ruan et al. Nature Communications 2024. [paper](https://doi.org/10.1038/s41467-024-54457-x)
- \[2023-12\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Autonomous chemical research with large language models (Coscientist)." Daniil A. Boiko et al. Nature 2023. [paper](https://doi.org/10.1038/s41586-023-06792-0) | [code](https://github.com/gomesgroup/coscientist)
- \[2023-10\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Large language models for chemistry robotics (CLAIRify)." Naruki Yoshikawa et al. Autonomous Robots 2023. [paper](https://doi.org/10.1007/s10514-023-10136-2) | [project](https://ac-rad.github.io/clairify/)

## Life Science

🧬 Cell culture, protein production, liquid handling and wet-lab biology.

- \[2026-02\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Biology](https://img.shields.io/badge/Biology-2da44e) "Using a GPT-5-driven autonomous lab to optimize the cost and titer of cell-free protein synthesis." Alexus A. Smith et al. bioRxiv 2026. [paper](https://doi.org/10.64898/2026.02.05.703998) | [blog](https://openai.com/index/gpt-5-lowers-protein-synthesis-cost/)
- \[2026-02\] ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Biology](https://img.shields.io/badge/Biology-2da44e) "LUMI-lab: A foundation model-driven autonomous platform enabling discovery of ionizable lipid designs for mRNA delivery." Yue Xu et al. Cell 2026. [paper](https://doi.org/10.1016/j.cell.2026.01.012)
- \[2025-10\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) ![Biology](https://img.shields.io/badge/Biology-2da44e) "Execution-aware agent harness for accessible and responsible synthetic biology automation (LabscriptAI)." Yuan Gao et al. bioRxiv 2025. [paper](https://doi.org/10.1101/2025.09.30.679666) | [project](https://labscriptai.cn/)
- \[2025-10\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Biology](https://img.shields.io/badge/Biology-2da44e) "LabOS: The AI-XR Co-Scientist That Sees and Works With Humans." Le Cong et al. arXiv 2025. [paper](https://arxiv.org/abs/2510.14861) | [code](https://github.com/zaixizhang/LabOS)
- \[2025-07\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Biology](https://img.shields.io/badge/Biology-2da44e) "BioMARS: A Multi-Agent Robotic System for Autonomous Biological Experiments." Yibo Qiu et al. arXiv 2025. [paper](https://arxiv.org/abs/2507.01485)

## Instruments & Facilities

🔬 Microscopes, beamlines, quantum hardware and optical setups.

- \[2026-09\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Microscopy](https://img.shields.io/badge/Microscopy-2da44e) "Unmodeled states and uncertain action outcomes in agentic scanning tunneling microscopy (Quailbot)." Siyu Cheng et al. arXiv 2026. [paper](https://arxiv.org/abs/2609.27302)
- \[2026-08\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Optics](https://img.shields.io/badge/Optics-2da44e) "OPERA: Operator-residual feedback for reliable autonomous optical experiments with language-model agents." Ning Xu et al. arXiv 2026. [paper](https://arxiv.org/abs/2608.05990)
- \[2026-07\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) "An agentic artificially intelligent X-ray scientist." Zhantao Chen et al. Nature Machine Intelligence 2026. [paper](https://doi.org/10.1038/s42256-026-01261-5) | [code](https://doi.org/10.5281/zenodo.20017991)
- \[2026-07\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Microscopy](https://img.shields.io/badge/Microscopy-2da44e) "AIMS: an AI experimentalist turns uncertainty into quantum matter discovery." Siyuan Qiu et al. arXiv 2026. [paper](https://arxiv.org/abs/2607.16544)
- \[2026-05\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Framework](https://img.shields.io/badge/Framework-1f6feb) "From Prompts to Protocols: An AI Agent for Laboratory Automation." Angelos Angelopoulos, James F. Cahoon, and Ron Alterovitz. arXiv 2026. [paper](https://arxiv.org/abs/2605.16552)
- \[2026-03\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) "Operating advanced scientific instruments with AI agents that learn on the job." Aikaterini Vriza et al. npj Computational Materials 2026. [paper](https://doi.org/10.1038/s41524-026-02005-0) | [code](https://github.com/AdvancedPhotonSource/CALMS/tree/sdl_agents)
- \[2026-03\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Framework](https://img.shields.io/badge/Framework-1f6feb) "Owl-AuraID 1.0: An Intelligent System for Autonomous Scientific Instrumentation and Scientific Data Analysis." Han Deng et al. arXiv 2026. [paper](https://arxiv.org/abs/2603.29828)
- \[2026-02\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Microscopy](https://img.shields.io/badge/Microscopy-2da44e) "EAA: Automating materials characterization with vision language model agents." Ming Du et al. arXiv 2026. [paper](https://arxiv.org/abs/2602.15294)
- \[2025-12\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) "Agentic artificial intelligence for multistage physics experiments at a large-scale user facility particle accelerator." Thorsten Hellert et al. Physical Review Research 2026. [paper](https://doi.org/10.1103/jtqy-9jz1)
- \[2025-10\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) ![Microscopy](https://img.shields.io/badge/Microscopy-2da44e) "Evaluating large language model agents for automation of atomic force microscopy (AILA, AFMBench)." Indrajeet Mandal et al. Nature Communications 2025. [paper](https://doi.org/10.1038/s41467-025-64105-7) | [code](https://github.com/M3RG-IITD/AILA)
- \[2025-09\] ![Multi-Agent](https://img.shields.io/badge/Multi--Agent-1f6feb) ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Quantum](https://img.shields.io/badge/Quantum-2da44e) "Automating quantum computing laboratory experiments with an agent-based AI framework (k-agents)." Shuxiang Cao et al. Patterns 2025. [paper](https://doi.org/10.1016/j.patter.2025.101372) | [code](https://github.com/ShuxiangCao/LeeQ)
- \[2025-05\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) "VISION: a modular AI assistant for natural human-instrument interaction at scientific user facilities." Shray Mathur et al. Machine Learning: Science and Technology 2025. [paper](https://doi.org/10.1088/2632-2153/add9e4) | [code](https://github.com/CFN-softbio/VISION)
- \[2024-11\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) "Opportunities for retrieval and tool augmented large language models in scientific facilities (CALMS)." Michael H. Prince et al. npj Computational Materials 2024. [paper](https://doi.org/10.1038/s41524-024-01423-2) | [code](https://github.com/mcherukara/CALMS)

## Benchmarks & Simulation

📊 Benchmarks, simulators and digital twins for laboratory agents.

- \[2026-07\] ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Large language models do not replace chemists in a closed-loop catalysis experiment." Andrew Ian Cooper et al. Research Square 2026. [paper](https://doi.org/10.21203/rs.3.rs-10032842/v1)
- \[2026-06\] ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) ![Safety](https://img.shields.io/badge/Safety-2da44e) "ABC-Bench: An Agentic Bio-Capabilities Benchmark for Biosecurity." Andrew Bo Liu et al. arXiv 2026. [paper](https://arxiv.org/abs/2606.11150)
- \[2026-01\] ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) ![Safety](https://img.shields.io/badge/Safety-2da44e) "Benchmarking large language models on safety risks in scientific laboratories (LabSafety Bench)." Yujun Zhou et al. Nature Machine Intelligence 2026. [paper](https://doi.org/10.1038/s42256-025-01152-1) | [code](https://github.com/YujunZhou/LabSafety-Bench)
- \[2025-12\] ![Simulator](https://img.shields.io/badge/Simulator-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "MATTERIX: toward a digital twin for robotics-assisted chemistry laboratory automation." Kourosh Darvish et al. Nature Computational Science 2025. [paper](https://doi.org/10.1038/s43588-025-00924-4) | [code](https://github.com/AccelerationConsortium/Matterix)
- \[2025-11\] ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) ![Simulator](https://img.shields.io/badge/Simulator-1f6feb) ![Synchrotron](https://img.shields.io/badge/Synchrotron-2da44e) "EnvTrace: Simulation-Based Semantic Evaluation of LLM Code via Execution Trace Alignment -- Demonstrated at Synchrotron Beamlines." Noah van der Vleuten et al. arXiv 2025. [paper](https://arxiv.org/abs/2511.09964) | [code](https://github.com/CFN-softbio/EnvTrace)
- \[2025-05\] ![Simulator](https://img.shields.io/badge/Simulator-1f6feb) ![Benchmark](https://img.shields.io/badge/Benchmark-1f6feb) "LabUtopia: High-Fidelity Simulation and Hierarchical Benchmark for Scientific Embodied Agents." Rui Li et al. NeurIPS 2025. [paper](https://arxiv.org/abs/2505.22634) | [code](https://github.com/Rui-li023/LabUtopia)

## Lab Tooling

🛠️ Protocol languages, lab operating systems, SDKs and MCP servers that agents act through.

- \[2026-09\] ![MCP](https://img.shields.io/badge/MCP-1f6feb) "LabMCP" (code-only release). [code](https://github.com/K-Dense-AI/lab-instrument-mcps) | [package](https://pypi.org/project/labmcp-opentrons/)
- \[2026-07\] ![MCP](https://img.shields.io/badge/MCP-1f6feb) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) "plr-mcp" (code-only release). [code](https://github.com/di-omics/plr-mcp)
- \[2026-05\] ![Framework](https://img.shields.io/badge/Framework-1f6feb) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) "From Knowledge to Action: Outcomes of the 2025 Large Language Model (LLM) Hackathon for Applications in Materials Science and Chemistry (IvoryOS)." Aritra Roy et al. arXiv 2026. [paper](https://arxiv.org/abs/2605.03205)
- \[2026-04\] ![MCP](https://img.shields.io/badge/MCP-1f6feb) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) "OpenLabAI" (code-only release). [code](https://github.com/nygmeta/OpenLabAI)
- \[2026-03\] ![Framework](https://img.shields.io/badge/Framework-1f6feb) "device-use" (code-only release). [code](https://github.com/labclaw/device-use)
- \[2025-12\] ![Framework](https://img.shields.io/badge/Framework-1f6feb) ![Platform](https://img.shields.io/badge/Platform-1f6feb) "UniLabOS: An AI-Native Operating System for Autonomous Laboratories." Jing Gao et al. arXiv 2025. [paper](https://arxiv.org/abs/2512.21766) | [code](https://github.com/deepmodeling/Uni-Lab-OS)
- \[2023-08\] ![Framework](https://img.shields.io/badge/Framework-1f6feb) "science-jubilee" (code-only release). [code](https://github.com/machineagency/science-jubilee)
- \[2022-08\] ![Framework](https://img.shields.io/badge/Framework-1f6feb) ![Liquid-Handling](https://img.shields.io/badge/Liquid--Handling-2da44e) "PyLabRobot" (code-only release). [code](https://github.com/PyLabRobot/pylabrobot)
- \[2018-11\] ![Framework](https://img.shields.io/badge/Framework-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Organic synthesis in a modular robotic system driven by a chemical programming language (XDL)." Sebastian Steiner et al. Science 2019. [paper](https://doi.org/10.1126/science.aav2211)

## Surveys & Perspectives

📚 Reviews and perspectives on agents in experimental science.

- \[2026-08\] ![Survey](https://img.shields.io/badge/Survey-1f6feb) ![Biology](https://img.shields.io/badge/Biology-2da44e) "Towards Human-Led, Agent-Driven Autonomous Laboratories for the Life Sciences." Wenduo Cheng et al. Preprints.org 2026. [paper](https://doi.org/10.20944/preprints202608.0273.v1)
- \[2026-05\] ![Survey](https://img.shields.io/badge/Survey-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) ![Materials](https://img.shields.io/badge/Materials-2da44e) "Autonomous Chemistry and Materials Innovation Driven by Scientific Agents." Zikai Xie et al. JACS Au 2026. [paper](https://doi.org/10.1021/jacsau.6c00213)
- \[2026-03\] ![Survey](https://img.shields.io/badge/Survey-1f6feb) "Embodied Science: Closing the Discovery Loop with Agentic Embodied AI." Xiang Zhuang et al. arXiv 2026. [paper](https://arxiv.org/abs/2603.19782)
- \[2026-01\] ![Survey](https://img.shields.io/badge/Survey-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "Agentic AI for Self-Driving Laboratories in Soft Matter: Taxonomy, Benchmarks,and Open Challenges." Xuanzhou Chen et al. arXiv 2026. [paper](https://arxiv.org/abs/2601.17920)
- \[2025-08\] ![Survey](https://img.shields.io/badge/Survey-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Large Language Models Transform Organic Synthesis From Reaction Prediction to Automation." Kartar Kumar, Rajesh Kumar, and Nikesh Lagun. arXiv 2025. [paper](https://arxiv.org/abs/2508.05427)
- \[2025-08\] ![Survey](https://img.shields.io/badge/Survey-1f6feb) "From AI for Science to Agentic Science: A Survey on Autonomous Scientific Discovery." Jiaqi Wei et al. arXiv 2025. [paper](https://arxiv.org/abs/2508.14111)

## Foundations

🏛️ Earlier autonomous laboratories and tool-using chemistry agents that this work builds on.

- \[2024-05\] ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "Delocalized, asynchronous, closed-loop discovery of organic laser emitters." Felix Strieth-Kalthoff et al. Science 2024. [paper](https://doi.org/10.1126/science.adk9227)
- \[2024-05\] ![LLM-Agent](https://img.shields.io/badge/LLM--Agent-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "Augmenting large language models with chemistry tools (ChemCrow)." Andres M. Bran et al. Nature Machine Intelligence 2024. [paper](https://doi.org/10.1038/s42256-024-00832-8)
- \[2023-11\] ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Materials](https://img.shields.io/badge/Materials-2da44e) "An autonomous laboratory for the accelerated synthesis of inorganic materials (A-Lab)." Nathan J. Szymanski et al. Nature 2023. [paper](https://doi.org/10.1038/s41586-023-06734-w)
- \[2023-03\] ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "AlphaFlow: autonomous discovery and optimization of multi-step chemistry using a self-driven fluidic lab guided by reinforcement learning." Amanda A. Volk et al. Nature Communications 2023. [paper](https://doi.org/10.1038/s41467-023-37139-y)
- \[2020-07\] ![Closed-Loop](https://img.shields.io/badge/Closed--Loop-1f6feb) ![Chemistry](https://img.shields.io/badge/Chemistry-2da44e) "A mobile robotic chemist." Benjamin Burger et al. Nature 2020. [paper](https://doi.org/10.1038/s41586-020-2442-2)

## Companies & Cloud Labs

🏢 Companies and cloud laboratories working on autonomous experimentation.

- ![Cloud-Lab](https://img.shields.io/badge/Cloud--Lab-8250df) "Emerald Cloud Lab." [website](https://www.emeraldcloudlab.com/)
- ![Cloud-Lab](https://img.shields.io/badge/Cloud--Lab-8250df) "Ginkgo Bioworks." [website](https://www.ginkgobioworks.com/)
- ![Company](https://img.shields.io/badge/Company-8250df) "Lila Sciences." [website](https://www.lila.ai/)
- ![Company](https://img.shields.io/badge/Company-8250df) "Periodic Labs." [website](https://periodic.com/)
- ![Company](https://img.shields.io/badge/Company-8250df) "Radical AI." [website](https://www.radical-ai.com/)

## Related Lists

- [awesome-physical-ai-for-science](https://github.com/labclaw/awesome-physical-ai-for-science#readme) - Physical AI for science, including robotics, lab automation and AI agents.
- [Awesome-Agent-Scientists](https://github.com/AgenticScience/Awesome-Agent-Scientists#readme) - Agents for autonomous scientific discovery.
- [awesome-llm-agents-scientific-discovery](https://github.com/zhoujieli/awesome-llm-agents-scientific-discovery#readme) - LLM agents in biomedical research.
- [awesome-autoresearch](https://github.com/alvinreal/awesome-autoresearch#readme) - Autonomous research loops and research agents.
- [awesome-lab](https://github.com/seifip/awesome-lab#readme) - Lab notebooks, information management systems and laboratory tooling.

## Contributing

Contributions are very welcome. Please read the [contribution guidelines](contributing.md) before opening a pull request, or suggest a paper by opening an [issue](https://github.com/gunkaynar/awesome-lab-agents/issues/new/choose).
