# Paper Descriptions

## TreeMPO: Fine-Grained Credit Assignment for LLM Training via Token-Level Trajectory Branching

**TreeMPO** studies **fine-grained credit assignment** for long LLM reasoning trajectories. Instead of assigning one reward to an entire response, it branches token-level trajectories, estimates **segment-level contribution** from mixed-success descendants, and converts the evidence into token-level advantages for LoRA/RL fine-tuning. The method supports mathematical reasoning and **tool-calling traces**, with consistent validation gains across several model families.

I am the **first author** of this manuscript in preparation. I designed the core TreeMPO algorithm, including the **token-level branching strategy**, contribution model, and advantage-generation pipeline, and built the full system for rollout collection, trajectory-tree construction, LoRA fine-tuning, and checkpoint validation under constrained GPU resources.

## Lost in Execution: On the Multilingual Robustness of Tool Calling in Large Language Models

**Lost in Execution** studies **multilingual robustness** in LLM tool calling. The paper introduces **MLCL**, a diagnostic benchmark across English, Chinese, Hindi, and Igbo, and shows that models may understand intent and select the right tool but still fail because parameter values are not executable. The key failure mode is **parameter-value language mismatch**, where semantically correct non-English arguments violate tool-interface conventions.

I am the **first author** of this **ACL 2026** paper. I built the benchmark, designed the **fine-grained error taxonomy**, analyzed failures across intent, tool selection, parameter extraction, and execution mismatch, and evaluated mitigation strategies. This project highlighted my ability to connect benchmark design with practical agent reliability.

## When Simulation Lies: A Sim-to-Real Benchmark and Domain-Randomized RL Recipe for Tool-Use Agents

**When Simulation Lies / RobustBench-TC** frames tool-use robustness as a **sim-to-real problem**. It introduces a production-grounded benchmark with perturbations organized by POMDP components: observation, action space, reward-relevant metadata, and transition dynamics. Across 21 models, the study finds that reward-relevant and transition perturbations cause much larger failures than simple observation noise, and proposes **ToolRL-DR** to narrow robustness gaps through perturbation-augmented RL.

I contributed to this **NeurIPS 2026 Evaluations and Datasets Track poster** as a co-author. My work included implementing user-query perturbations on ACEBench, supporting robustness experiments under deployment-like noise, and contributing to the analysis showing that **perturbation-augmented RL** can improve tool-use robustness beyond clean benchmark accuracy.

## Street-Level Competitive Ride-Hailing with Fixed-Rival Defensive PSRO

**Street-Level Competitive Ride-Hailing with Fixed-Rival Defensive PSRO** studies competitive fleet management at **street-level resolution** rather than coarse zone level. The paper introduces a **SUMO-backed competitive ride-hailing simulator** calibrated with NYC TLC and OpenStreetMap data, evaluates structured and residual policy designs, and proposes **Fixed-Rival Defensive PSRO** for robustness against strategically difficult rivals.

I am the **first author** of this **AAAI 2027 submission**. I developed the simulation framework, designed street-level controller features for relocation, pricing, and service decisions, implemented Manhattan-scale evaluation pipelines, and proposed the **FRDF-PSRO** protocol for robust multi-agent decision-making under competitive pressure.

## SkiLT: What Agent Reinforcement Learning Actually Learns from a Latent Skill Library

**SkiLT** studies whether retrieved text-skill libraries for LLM agents can be compressed into **compact latent skill tokens** during reinforcement learning. It reduces the skill section from roughly **970 tokens to 140 tokens per step** while maintaining performance comparable to text-skill RL checkpoints on ALFWorld. The mechanism analysis further shows that the actor may adapt around nearly fixed skill rows, complicating the interpretation of what latent skill conditioning actually contributes.

I contributed to this **AAAI 2027 submission** as a co-author. My work included designing and implementing **latent-form skill compression**, integrating compact skill tokens into the GRPO workflow, evaluating against text-skill RL baselines, and helping analyze training dynamics to understand what agent RL actually learns from auxiliary skill memory.

## Fairness or Fluency? An Investigation into Language Bias of Pairwise LLM-as-a-Judge

**Fairness or Fluency?** studies **language bias** in pairwise LLM-as-a-judge evaluation. The paper finds performance disparities across language families and shows that many models prefer English answers in cross-language comparisons. It further tests whether this bias is explained by answer perplexity, finding that perplexity is correlated with bias but **does not fully explain language preference**.

I contributed to this **NeurIPS 2026 Workshop JUDGe submission** as a co-author. My role focused on designing and implementing experiments that relate judge preference to answer perplexity, using **regression-based analysis** to separate language identity from fluency effects, and improving perplexity collection for more reliable multilingual evaluation.
