# Embedding-Guided, Multi-Round Canonicalization of Relations for Open Knowledge Graph Construction  

*May 2025*  

---

**Overview**  
Open Knowledge Graphs (OpenKGs) often contain redundant relation phrases (e.g., *“ignores”*, *“disregards”*, *“disregarded in”*). This project introduces a **multi-round, embedding-guided Chain-of-Thought (CoT) canonicalization pipeline** that generates expressive canonical labels instead of just selecting existing phrases.  

---

**Key Features**  
- Embedding-based clustering (E5 + HDBSCAN + fallback Agglomerative).  
- Multi-round CoT prompting to refine relation labels.  
- LLM-as-a-judge evaluation on generalization, coverage, and faithfulness.  
- Outperforms CESI, EDC, and LLM-only baselines.  

---

**Pipeline**  

1. Embed and cluster relation phrases  
2. Multi-round CoT prompting for canonical labels  
3. LLM-as-a-judge scoring  
4. Refinement loop for low-quality outputs  

📌 Canonicalization pipeline:  

![Hybrid Canonicalization Flow](pipeline.png)  

---

**Results**  
- CoT-Hybrid produced the best canonical label in **45% of clusters**.  
- Highest semantic evaluation scores: Generalization (4.09), Coverage (4.07).  

---

**Resources**  
- Dataset & code: [GitHub Repository](https://github.com/haniehkh18/Embedding-Guided-Multi-Round-Canonicalization-of-Relations-for-Open-Knowledge-Graph-Construction)  
- Paper: included in this repo  

---

**Citation**  
```bibtex
@inproceedings{khorashadizadeh2025canonicalization,
  title={Embedding-Guided, Multi-Round Canonicalization of Relations for Open Knowledge Graph Construction},
  author={Khorashadizadeh, Hanieh and Mihindukulasooriya, Nandana and Ranji, Nilufar and Ezzabady, Morteza and Ieng, Fr{\'e}d{\'e}ric and Groppe, Jinghua and Benamara, Farah and Groppe, Sven},
  year={2025},
  booktitle={Proceedings of ...}
}

