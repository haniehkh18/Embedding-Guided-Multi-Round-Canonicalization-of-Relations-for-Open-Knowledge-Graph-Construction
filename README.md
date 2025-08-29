EcoRAG: Multi-Hop Economic QA Benchmark for Retrieval-Augmented Generation

📖 Paper: EcoRAG: A Multi-Hop Economic QA Benchmark for Retrieval-Augmented Generation Using Knowledge Graphs
✍️ Authors: Hanieh Khorashadizadeh, Sanju Tiwari, Farah Benamara, Nandana Mihindukulasooriya, Jinghua Groppe, Soror Sahri, Morteza Ezzabady, Frédéric Ieng, Sven Groppe

🌍 Overview

Retrieval-Augmented Generation (RAG) has emerged as a powerful paradigm for enhancing large language models (LLMs) with external knowledge. However, existing multi-hop RAG benchmarks are limited by:

Shallow reasoning depth

Simplified retrieval structures

Non-descriptive answers

EcoRAG addresses these challenges by introducing a novel multi-hop benchmark built from economic knowledge graphs (KGs).
It extends reasoning depth up to 7 hops, incorporates complex subgraph structures, and emphasizes domain-specific knowledge from trusted economic datasets.

This benchmark enables more realistic evaluation of retrieval and reasoning in LLMs while bridging the gap between structured knowledge sources and generative models.

🚀 Key Contributions

Benchmarking Pipeline – A reusable pipeline for creating domain-specific RAG benchmarks.

Knowledge Graph Integration – Data derived from structured KGs (World Bank, IMF, ECB, etc.) ensures interconnected and comprehensive knowledge.

Descriptive Answers – Beyond binary/entity answers, EcoRAG provides context-rich responses.

Economic Domain Focus – First benchmark tailored specifically for economic reasoning.

Complex Retrieval Structures – Includes linear chains, converging DAGs, and divergent polytrees.

Extended Multi-Hop Reasoning – Supports 4–7 hop paths, exceeding prior benchmarks (capped at 2–4 hops).

📊 Dataset

Size: 3,114 QA pairs

Source: 62 economic reports, bulletins, and journals

Knowledge Graph Entities: Built using Cypher queries and degree-balanced node selection

Reasoning Depth: Up to 7 hops

Types of Subgraphs:

Linear (Chain reasoning)

Converging (DAG)

Divergent (Polytree)

🛠️ Benchmark Pipeline

KG Construction – Build from economic reports (World Bank, IMF, ECB).

Node Sampling – Degree-balanced selection for diversity.

Path Extraction – Generate multi-hop subgraphs via Cypher queries.

Path Validation – LLM-based validation for semantic and logical coherence.

QA Pair Generation – Produce descriptive Q&A from KG subgraphs.

RAG Evaluation – Benchmark against Hybrid RAG, ReRank RAG, and KG-RAG.

📈 Evaluation

Retrieval Metrics: MAP@K, MRR@K, Hits@K

Generation Metrics: BLEU, ROUGE, Semantic Similarity

Findings:

ReRank RAG excels in converging subgraphs (MRR up to 0.75 at 5 hops).

Hybrid RAG performs consistently across divergent paths.

KG-RAG struggles with deeper reasoning, but produces fluent answers in simpler paths.

🔗 Resources

📂 Dataset & Code: EcoRAG GitHub Repository

📑 Paper (PDF): Included in this repository
📌 Citation

If you use EcoRAG, please cite:

@InProceedings{10.1007/978-3-031-97144-0_15,
author="Khorashadizadeh, Hanieh
and Tiwari, Sanju
and Benamara, Farah
and Mihindukulasooriya, Nandana
and Groppe, Jinghua
and Sahri, Soror
and Ezzabady, Morteza
and Ieng, Fr{\'e}d{\'e}ric
and Groppe, Sven",
editor="Ichise, Ryutaro",
title="EcoRAG: A Multi-hop Economic QA Benchmark for Retrieval Augmented Generation Using Knowledge Graphs",
booktitle="Natural Language Processing and Information Systems",
year="2026",
publisher="Springer Nature Switzerland",
address="Cham",
pages="163--173",
abstract="Retrieval-Augmented Generation (RAG) enhances large language models (LLMs) by integrating external knowledge retrieval. However, existing multi-hop RAG benchmarks are limited by shallow reasoning depth, simple retrieval structures, and non-descriptive answers. We introduce EcoRAG, a novel multi-hop economic QA benchmark built on knowledge graphs (KGs). EcoRAG extends retrieval depth to seven-hop reasoning, incorporates complex subgraph structures, and leverages domain-specific economic knowledge. It enables a more realistic evaluation of retrieval and reasoning by bridging the gap between structured knowledge sources and generative models, while also providing a reusable benchmark to advance multi-hop RAG research.",
isbn="978-3-031-97144-0"
}


