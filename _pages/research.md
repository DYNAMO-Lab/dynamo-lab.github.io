---
layout: page
title: research
page-title: Research
permalink: /research/
description: Highlighted research from the DYNAMO.
nav: true
nav_order: 3
display_categories:
horizontal: false
---

DYNAMO develops mathematical and computational foundations for learning, understanding, and reasoning with complex structured data. Our research spans machine learning, graph algorithms, network science, geometry, and optimization, with applications in scientific discovery and human–AI systems.

A central question in our work is **how representations determine what can be learned, explained, and reasoned about**. Representations capture relationships and regularities in data, but their geometry, symmetry, and structure also influence the capabilities and limitations of learning systems. Understanding these relationships is essential for developing models that are robust, interpretable, and capable of generalizing beyond their training data.

Our research combines theoretical analysis, algorithm development, and empirical investigation across four interconnected directions.

## Representation Learning, Geometry, and Symmetry

Learned representations are central to modern machine learning, yet their mathematical structure and relationship to model behavior remain poorly understood. We investigate the geometry, symmetry, and invariances of representation spaces, and how these properties relate to generalization, robustness, interpretability, and reasoning.

Our work develops methods for comparing and aligning representations across models, layers, and datasets, including spaces of different dimensionalities. We also study the role of geometric structure in graph learning, the relationship between symmetry and representation, and the conditions under which nonlinear transformations admit simpler descriptions in learned spaces.

These investigations address fundamental questions: What makes two representations equivalent or comparable? Which geometric properties carry task-relevant information? How do representations change during learning, and what determines their ability to support reliable inference?

**Representative research**

- *Normalized Space Alignment: A Versatile Metric for Representation Analysis* — KDD 2025
- *FlowSymm: Physics-Aware, Symmetry-Preserving Graph Attention for Network Flow Completion* — ICLR 2026
- *Concorde: Geometry-Aware Link Prediction via Decoupled Energy Minimization* — NeurIPS 2026

## Graph Learning, Reasoning, and Explainability

Graphs provide a natural representation for systems whose behavior depends on relationships among entities. We develop learning and algorithmic methods for graph-structured data, with an emphasis on representation quality, reasoning, robustness, and explainability.

Our research examines the capabilities and limitations of graph neural networks and language models when working with relational structure. We investigate graph representation learning, link prediction, graph classification, graph algorithms, and the ability of learned models to perform structural and relational reasoning.

A major focus is understanding why graph models make particular predictions. We develop factual and counterfactual explanation methods, study their computational properties, and design benchmarks for evaluating explanation quality. We also investigate how graph models respond to perturbations, adversarial attacks, and changes in data distributions.

Underlying this work is a broader question: **When does a learned model capture meaningful relationships, rather than merely exploit predictive correlations?**

**Representative research**

- *GCFExplainer: Global Counterfactual Explainer for Graph Neural Networks* — ACM TIST 2025
- *GNNX-BENCH: Unravelling the Utility of Perturbation-based GNN Explainers through In-depth Benchmarking* — ICLR 2024
- *GraphEval36K: Benchmarking Coding and Reasoning Capabilities of Large Language Models on Graph Datasets* — NAACL 2025
- *Are LLMs Truly Graph-Savvy? A Comprehensive Evaluation of Graph Generation* — ACL 2025

## Network Science and Human–AI Systems

The behavior of complex systems emerges from interactions among their constituent entities. Network structure, information exchange, influence, and feedback can produce collective behavior that cannot be understood by studying individual components in isolation.

Building on foundations in network science, we develop computational models and algorithms for analyzing the structure and dynamics of social, information, and engineered networks. Our research includes network optimization, influence propagation, resilience, dynamic networks, and the interaction between network topology and behavior.

An important direction concerns teams composed of humans and AI agents. We investigate how information, trust, influence, and expertise shape collective decision-making, and how these processes change when AI agents become active participants. We also study the vulnerability of human–AI teams to manipulation and adversarial behavior.

Our goal is to understand the principles governing collective intelligence and to develop computational methods that support robust, effective, and trustworthy human–AI collaboration.

**Representative research**

- *Learning to Lie: Adversarial Attacks on Human-AI Teams and LLMs* — ICLR 2026
- *Predictive Models for Human–AI Nexus in Group Decision Making* — Annals of the New York Academy of Sciences, 2022
- *Dynamic Gradient Influencing for Viral Marketing Using Graph Neural Networks* — WWW 2025

## AI for Scientific Discovery

Scientific data present distinctive challenges for machine learning. They are often heterogeneous, limited, noisy, and governed by physical or biological constraints. Successful models must capture meaningful scientific structure while providing predictions and insights that can be evaluated against experimental observations.

We develop and apply representation learning, geometric analysis, graph algorithms, and optimization methods to problems in molecular science, drug discovery, and neuroscience. These applications also motivate new foundational questions about learning, reasoning, and generalization.

### Molecular Science and Drug Discovery

We investigate representations of molecular structure and chemical space for predicting molecular properties, understanding structure–activity relationships, and identifying promising compounds. Our work includes molecular graph learning, fragment-based representations, counterfactual molecular explanations, and computational approaches to the design and analysis of therapeutic molecules.

A particular interest is understanding how structural differences between molecules relate to changes in their biological and physicochemical behavior, and how these relationships can be captured by learned representations.

### Brain Science and Neural Representations

We develop computational methods for analyzing neural data and understanding the relationship between brain activity, external stimuli, and learned representations in artificial neural networks.

Our research includes multimodal neuroimaging, brain connectivity, reconstruction of sensory stimuli from neural responses, and the analysis of representations across biological and artificial systems. We seek to understand how neural representations encode information, how they vary across individuals and conditions, and how their structure can be compared with representations learned by machine learning models.

**Representative research**

- *Fragment-based Pretraining and Finetuning on Molecular Graphs* — NeurIPS 2023
- *Global Human-guided Counterfactual Explanations for Molecular Properties via Reinforcement Learning* — KDD 2024
- *Mind Reader: Reconstructing Complex Images from Brain Activities* — NeurIPS 2022
- *Deep Representations for Time-varying Brain Datasets* — KDD 2022

## Connecting Representations, Reasoning, and Discovery

These research directions are closely connected. Graphs provide a language for representing relationships; geometry and symmetry reveal structure in learned representations; explainability and reasoning investigate what models have learned and how they use that information; and scientific applications test whether these methods capture meaningful relationships in the world.

Our long-term goal is to develop AI systems whose representations support reliable reasoning, whose predictions can be understood and evaluated, and whose capabilities extend from recognizing patterns to discovering meaningful structure in complex systems.

For additional research contributions, see our [Publications]({{ '/publications/' | relative_url }}) page.
