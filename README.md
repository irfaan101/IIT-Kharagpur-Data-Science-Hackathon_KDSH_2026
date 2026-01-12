# 🎓📊 IIT Kharagpur Data Science Hackathon (KDSH) 2026 – Track A
This repository contains our **Track A submission** for the **IIT Kharagpur Data Science Hackathon (KDSH) 2026**, focused on **global narrative consistency reasoning over long-form texts** 📚🧠.

The objective is to determine whether a hypothetical character backstory is **causally and logically consistent** with a full-length novel, requiring long-context understanding, evidence aggregation, and constraint-aware reasoning 🔍🧩.

---
## 🧠❓ Problem Overview

Large Language Models (LLMs) perform well on local text understanding tasks such as summarization or question answering. However, they often fail to maintain **global consistency** over long narratives where meaning emerges cumulatively over time ⏳📖.

In long-form stories:
- Earlier events impose constraints on future possibilities 🔗
- Characters evolve, make commitments, and follow causal paths 🎭➡️
- Plausible-sounding explanations may still be globally inconsistent ⚠️

This challenge frames the task as a **binary classification problem** 🔢:

- **1** Backstory is consistent with the narrative ✅  
- **0** Backstory is inconsistent with the narrative ❌  

The focus is on **evidence-based reasoning**, not text generation 🔍📑.

---

## 🛠️📐 Approach Summary (Track A)

Our system follows a structured, interpretable pipeline:

1. **Long Narrative Ingestion** 📥📘  
   Full novels are loaded without truncation.

2. **Chunking for Long Context** ✂️📄  
   Each novel is split into overlapping chunks to preserve long-range dependencies.

3. **Semantic Retrieval** 🔎🧠  
   Relevant narrative excerpts are retrieved for each backstory using semantic similarity.

4. **Consistency Judgment** ⚖️🧩  
   Rule-based reasoning is applied over retrieved evidence to assess causal and logical compatibility.

5. **Final Classification** 🏁🔢  
   Evidence from multiple chunks is aggregated to produce a binary prediction.

This design prioritizes **robustness, interpretability, and global coherence** over end-to-end generative reasoning 🧠📊.

---

## 🧵📚 Handling Long Context

To manage narratives exceeding 100k words:

- Text is chunked into fixed-size overlapping segments ✂️  
- Semantic embeddings are computed for each chunk 🧠  
- Only the most relevant chunks are used during reasoning 🎯  

This ensures decisions are informed by **distributed evidence across the narrative**, not a single isolated passage 🌐📖.

---

## 🧪⚙️ Use of Pathway

Pathway’s Python framework is used as a core component for:

- Structured ingestion of long narrative data 📥  
- Managing chunked representations of novels 🗂️  
- Building a reproducible and transparent data-processing pipeline 🔁  

This satisfies **Track A’s requirement** for meaningful use of Pathway ✅📌.

---

## 🗂️ Repository Structure
The repository is organized as follows:  
IIT-Kharagpur-Data-Science-Hackathon_KDSH_2026/  
+-- trackA_solution.ipynb     # End-to-end Colab implementation 📓  
+-- report.pdf                # Detailed methodology and analysis 📄  
+-- results.csv               # Final Track A predictions 📊  

---

## 🗃️📚 Dataset Information

The dataset used in this project was **officially provided by IIT Kharagpur** as part of the KDSH 2026 competition 🎓.

It includes:
- `train.csv` 📄  
- `test.csv` 📄  
- Two full-length novels:
  - *In Search of the Castaways* 📘  
  - *The Count of Monte Cristo* 📕

🔒 Due to licensing and copyright restrictions, the dataset is **not hosted directly in this repository**.

🌐 **Official Dataset (Google Drive):**  
https://drive.google.com/drive/folders/1Z1Pt3XoF7GAb_QtLksa8q4D_U-wc65e4

During development, the dataset was loaded locally in **Google Colab** ☁️🧑‍💻.

---
## 📂 Project Artifacts

**📓🚀 Colab Notebook**
The complete end-to-end implementation was developed and executed in Google Colab.

📓 **Colab Notebook:**  `trackA_solution.ipynb` 

🔗 **Colab Notebook Link:**   
https://colab.research.google.com/drive/1K1Vy78iWrJvFs5kuq9eHf2hZmfmPWtLbP_?usp=sharing

📄 **Technical Report:**  `report.pdf`

📊 **Results File:**  `results.csv`

---

## 📬✅ Submission Status

- Track A submission ZIP (**DataVision_KDSH_2026.zip**) has been **successfully submitted** to the hackathon portal 🎉.
- This repository is maintained for **learning, reproducibility, and portfolio purposes** 📈📁.

---

## 🏁🧠 Conclusion

This project demonstrates a practical and reproducible approach to **global narrative consistency reasoning** over long-form texts 📚. By combining long-context handling, retrieval-based evidence aggregation, and explicit reasoning rules, the system addresses key limitations of standard language models when reasoning over extended narratives 🔍🤖.

---

## 👥 Team Information
- **Team Name:** DataVision 🚀 
- **Contributors:**  
  - Irfaan Mansoori  
  - Jeet Lakhera  
