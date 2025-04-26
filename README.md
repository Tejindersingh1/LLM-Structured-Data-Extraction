
# 🧠 Multimodal Data Extraction using Qwen2.5-VL

This repository contains a Jupyter Notebook for extracting structured information from images (e.g., scanned prescriptions) using the **Qwen2.5-VL-7B-Instruct** model.  
It uses HuggingFace Transformers + Outlines library for structured generation and evaluates extracted data quality using standard NLP similarity metrics.

---

## 📄 Notebook Details
- **Filename**: `data-extraction-llm.ipynb`
- **Main Goal**: Extract structured fields from images and save the outputs to an Excel file.
- **Approach**:
  - Load and quantize the **Qwen2.5-VL-7B** multimodal model.
  - Extract text from images.
  - Parse and structure the extracted outputs using **Outlines** and **Pydantic** schemas.
  - Save results into an Excel file.

---

## 🛠️ Libraries Used
- `transformers`
- `qwen_vl_utils`
- `outlines`
- `bitsandbytes`
- `torch`
- `PIL`
- `pydantic`
- `pandas`


---

## 📊 Evaluation Metrics
| **Metric**             | **Description**                       | **Interpretation**                              |
|-------------------------|----------------------------------------|-------------------------------------------------|
| Cosine Similarity        | Measures angle between text vectors.   | Closer to 1 = more similar.                     |
| BERTScore                | Contextual similarity using BERT.      | Higher score = better semantic overlap.         |
| Levenshtein Distance     | Minimum edits to match strings.        | Lower score = more similar (0 = exact match).   |

---

