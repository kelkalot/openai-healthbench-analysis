# In-Depth Analysis of OpenAI's HealthBench 🩺📊

This repository contains code and resources related to an in-depth analysis of **OpenAI's HealthBench**, a benchmark designed for evaluating Large Language Models in the healthcare sector.

OpenAI's Announcement: [HealthBench Index](https://openai.com/index/healthbench/)

This analysis looks closely into the benchmark's data, providing insights into its structure, nuances, and implications for evaluating AI in healthcare.

More details can also be found here: [Blog post about analysis](https://medium.com/@michael_79773/a-closer-look-at-openais-new-healthbench-evaluation-benchmark-ed3455110a29)

---

## 🔑 Key Insights from the Analysis

My in-depth analysis of HealthBench's data shows a robust framework with specific characteristics that users and developers should consider:

* **Conversation Structure:** While designed for multi-turn interactions (averaging 2.6 turns), a notable **58.3% of conversations are single-turn**, emphasizing comprehensive initial responses.
* **Rubric Emphasis:** Evaluation is guided by an average of 11.4 criteria per example, with a **leaning towards positive reinforcement (69.3% positive criteria)**. Criteria text length averages 40.7 words but can extend up to 481 words.
* **Thematic Focus:** The dataset shows concentrations in themes like **“global_health” (21.9%) and “hedging” (21.4%)**, which may influence overall model performance insights.
* **Internal Criteria Consistency:** An exploration of textual similarity within individual examples found an average cosine similarity of 0.090 between criteria pairs. However, **642 examples (12.8%) contained at least one pair of criteria with high similarity (≥0.8)**, suggesting potential for evaluative overlap.
* **“Hard” Examples:** The 1,000 “HealthBench Hard” examples maintain a similar average number of criteria but show shifts in thematic distribution and subtle differences in criteria point distributions, indicating difficulty likely stems from nuanced requirements.
* **Initial Prompt Integrity:** A first-turn content classification analysis revealed that while most prompts initiate with relevant content, **a subset begins with clearly non-medical or inappropriate material**. This highlights the importance of inspecting prompt origins. (Resulting dataset and code for this specific analysis are shared below).

This detailed examination aims to provide a nuanced understanding of HealthBench’s construction, helping the community to interpret its results more effectively and advance the development of safer, more reliable AI in healthcare. *For a more detailed discussion, please see the full analysis [TODO: Link to your blog post/paper if you have one, otherwise remove this sentence or rephrase]*.

---

## 💻 Code and Data Resources

All code and data resources related to this analysis are provided below:

### Analysis Notebooks (Google Colab)
* **Main Analysis:** [https://colab.research.google.com/drive/1ROsxGAgsaq_2ThuMbfwhkL0IkTYH2CoB?usp=sharing](https://colab.research.google.com/drive/1ROsxGAgsaq_2ThuMbfwhkL0IkTYH2CoB?usp=sharing)
* **First-Turn Content Classification Analysis:** [https://colab.research.google.com/drive/1rs4lqSGwXzzgObrf6tLkei9kRKIMJEfI?usp=sharing](https://colab.research.google.com/drive/1rs4lqSGwXzzgObrf6tLkei9kRKIMJEfI?usp=sharing)

### Datasets
* **Version of HealthBench Data Used in this Analysis:** [Google Drive Link](https://drive.google.com/file/d/1JozLh_mpCz_gfVGDfsFBPFNZU00HX_my/view?usp=sharing)
* **Original HealthBench Data (from OpenAI):**
    * Eval: [oss_eval.jsonl](https://openaipublic.blob.core.windows.net/simple-evals/healthbench/2025-05-07-06-14-12_oss_eval.jsonl)
    * Hard: [hard_2025-05-08-21-00-10.jsonl](https://openaipublic.blob.core.windows.net/simple-evals/healthbench/hard_2025-05-08-21-00-10.jsonl)
    * Consensus: [consensus_2025-05-09-20-00-46.jsonl](https://openaipublic.blob.core.windows.net/simple-evals/healthbench/consensus_2025-05-09-20-00-46.jsonl)
* **Dataset of Flagged Non-Medical/Ambiguous Prompts (from Content Integrity Analysis):** [Google Drive Link](https://drive.google.com/file/d/1yPZhYySPcA4HktkTew2AbKDWP3AnI7hV/view?usp=sharing)

---

## 💡 Conclusion

HealthBench is a valuable contribution for evaluating AI in healthcare. This analysis provides a deeper look into its characteristics, aiming to aid researchers and developers in its effective use and interpretation. Critically examining benchmarks is key to guiding the development of AI that is safe, reliable, and truly beneficial.

---
