---
layout: about
title: about
permalink: /
subtitle: >
  PhD Candidate @ <a href='https://www.cs.hku.hk/'>HKU Computer Science</a> &middot;
  COO @ <a href='https://www.stellaris-ai.com/'>Stellaris AI</a> &middot;
  Partner @ <a href='https://www.brainvestai.com/'>Brain Investing</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: true
  more_info:

news: true
selected_papers: false
social: true
---

I am a final-year PhD candidate in the [Department of Computer Science](https://www.cs.hku.hk/) at [The University of Hong Kong](https://www.hku.hk/), advised by [Prof. Siu-Ming Yiu](https://www.cs.hku.hk/index.php/people/academic-staff/smyiu).

I study the **fundamental limits of AI systems** — when they fail, how to verify their reasoning, and how to coordinate multiple AI agents without manipulation. Then I build the infrastructure to deploy them at scale.

My research spans five interconnected areas at the intersection of **theory and practice of large language models**:

- **LLM Foundations** — expressivity and descriptive complexity of transformers, chain-of-thought error propagation, knowledge editing bounds, distillation complexity, and LoRA convergence.
- **Multi-Agent Systems** — mechanism design with ε-IC guarantees, strategic manipulation detection, coalition formation, and VCG impossibility results.
- **Retrieval-Augmented Generation** — verification efficiency, adaptive retrieval, causal attribution via do-calculus, and knowledge graph poisoning defense.
- **AI Safety & Alignment** — reward hacking detection, scalable oversight theory, XAI regulatory critique, and model collapse characterization.
- **Learning Theory** — tight minimax rates, PAC/sample complexity, preference learning beyond Bradley-Terry, and synthetic data learnability.

On the industry side, I lead LLM infrastructure at [Stellaris AI](https://www.stellaris-ai.com/) and AI-driven quantitative trading systems at [Brain Investing](https://www.brainvestai.com/).

## Current Projects

I am actively working on the following research projects. If any of these align with your interests, I'd love to collaborate — feel free to reach out.

- **Logical characterization of transformer expressivity** — Connecting the computational power of softmax attention to formal logic hierarchies, establishing what classes of problems transformers can provably solve or fail on.
- **Crash recovery for multi-agent LLM workflows** — Building a fault-tolerant runtime that allows multi-agent LLM pipelines to survive agent crashes and resume execution without losing intermediate reasoning state.
- **Strategy-proof coordination of LLM agents** — Designing auction- and voting-based protocols for settings where multiple LLM agents have competing objectives, with formal guarantees on when manipulation can be prevented.
- **Conflict detection in retrieval-augmented generation** — Developing a verification layer that identifies subtle contradictions between retrieved documents and LLM-generated answers before they reach the end user.
- **Query-adaptive retrieval for reasoning tasks** — Building a retrieval system that decides when, what, and how much to retrieve based on the reasoning complexity of the input query, rather than retrieving uniformly.
- **Multi-tenant LLM serving under fairness constraints** — Designing scheduling and batching algorithms that guarantee quality-of-service fairness across users when serving shared LLM infrastructure.
