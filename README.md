# 📅 Internship Daily Report – AI-Powered Resume Screening System

## 🎯 Project Title  
Resume Screening System using NLP and Semantic Similarity  

## 🧠 Internship Domain  
Machine Learning / Natural Language Processing  

## ✍️ Author  
**Vishruti Parekh**  

## 📅 Internship Period  
**12/05/2025 – 22/06/2025**  

---

## ✅ Overview  
The objective of this internship project is to build an **AI-powered Resume Ranking System** that automatically matches resumes to job descriptions using NLP techniques such as **TF-IDF**, **Word2Vec**, and **BERT-based embeddings**.  

This document provides a **day-by-day report** of the internship progress (5 working days per week).  

---

## 📌 Daily Progress Log  

### 📍 Week 1: Dataset Identification and Exploration  



| Day | Task Description |
|-----|------------------|
| **Day 1** | Researched public resume datasets on **Kaggle, GitHub**, and other sources. Shortlisted 3 potential datasets. |
| **Day 2** | Selected the **Kaggle Resume Dataset** containing `Category` and `Resume` fields. Loaded dataset in **Pandas**. |
| **Day 3** | Conducted initial **exploratory data analysis (EDA)** – checked dataset size, fields, and basic statistics. |
| **Day 4** | Verified dataset quality – handled null values, inspected sample resumes for consistency. |
| **Day 5** | Documented dataset understanding in research notes. Prepared checklist for preprocessing requirements. |

---

### 📍 Week 2: Data Cleaning and Preprocessing  

| Day | Task Description |
|-----|------------------|
| **Day 6** | Installed and tested **spaCy** (with `en_core_web_sm`) for NLP preprocessing. |
| **Day 7** | Wrote `clean_text()` function: lowercasing, punctuation removal, tokenization. |
| **Day 8** | Added **lemmatization** and stopword removal to cleaning pipeline. |
| **Day 9** | Applied cleaning function to all resumes → created `Cleaned_Resume` column. |
| **Day 10** | Verified output samples to ensure normalization. Stored intermediate results. |

---

### 📍 Week 3: Text Extraction from PDF Resumes  

| Day | Task Description |
|-----|------------------|
| **Day 11** | Installed and explored **pdfminer.six** for PDF parsing. |
| **Day 12** | Tested **PyMuPDF (fitz)** to compare parsing accuracy. |
| **Day 13** | Wrote batch script to process multiple resumes in PDF format. |
| **Day 14** | Verified extracted text vs. original PDF (manual sampling). |
| **Day 15** | Cleaned inconsistencies (extra spaces, encoding issues) → ensured dataset compatibility. |

---

### 📍 Week 4: Updating and Structuring the Dataset  

| Day | Task Description |
|-----|------------------|
| **Day 16** | Merged **PDF-extracted resumes** with Kaggle dataset. |
| **Day 17** | Added metadata columns → `Source` (PDF / Kaggle), `Category`. |
| **Day 18** | Handled duplicates, trimmed whitespaces, fixed encoding issues. |
| **Day 19** | Saved clean master dataset → `final_resumes.csv`. |
| **Day 20** | Documented dataset schema and cleaning pipeline for reproducibility. |

---

### 📍 Week 5: Implementing TF-IDF and BERT Embeddings  

| Day | Task Description |
|-----|------------------|
| **Day 21** | Implemented **TF-IDF vectorizer** (`max_features=1000`). |
| **Day 22** | Computed **cosine similarity** between job descriptions and resumes using TF-IDF vectors. |
| **Day 23** | Installed and tested **sentence-transformers** (BERT). |
| **Day 24** | Encoded resumes and job descriptions using **all-MiniLM-L6-v2** model. |
| **Day 25** | Benchmarked results – observed **BERT outperforming TF-IDF** in contextual accuracy. |

---

### 📍 Week 6: Word2Vec Embeddings and Model Comparison  

| Day | Task Description |
|-----|------------------|
| **Day 26** | Downloaded pre-trained **GloVe embeddings (100D)** via Gensim. |
| **Day 27** | Created document-level vectors by averaging word embeddings. |
| **Day 28** | Computed cosine similarities and compared ranking results with TF-IDF and BERT. |
| **Day 29** | Compiled results into comparison table (TF-IDF, Word2Vec, BERT). |
| **Day 30** | Finalized **BERT for deployment**. Saved models, embeddings, and scripts. Documented entire pipeline. |

---

## 📊 Model Comparison Table  

| Model    | Accuracy (Top-K Relevance) | Remarks |
|----------|-----------------------------|---------|
| **TF-IDF** | Medium (60–70%) | Fast, but lacks contextual understanding |
| **Word2Vec** | Medium-High (65–75%) | Captures word semantics, limited context |
| **BERT** | High (80–90%) | Best contextual accuracy, chosen for deployment |

---

## 📦 Final Deliverables  

- ✅ **Clean Dataset**: `final_resumes.csv`  
- ✅ **Models**: `tfidf_model.pkl`, `resume_embeddings.pkl`  
- ✅ **Scripts**: Preprocessing, Embedding, Ranking Logic  
- ✅ **Documentation**: Full pipeline explanation  

---

## 🛠️ Tools & Frameworks  

- **Python** 🐍  
- **spaCy** (Text Cleaning)  
- **pdfminer.six / PyMuPDF** (PDF Parsing)  
- **scikit-learn** (TF-IDF, Similarity)  
- **gensim** (Word2Vec / GloVe)  
- **sentence-transformers** (BERT Embeddings)  
- **Flask** (Deployment Ready)  

---

## 🚀 Conclusion  

This internship enabled me to build a **resume ranking system** using multiple NLP techniques and evaluate their effectiveness. Among all tested approaches, **BERT embeddings** achieved the highest accuracy and contextual understanding, making it the most suitable choice for deployment in real-world recruitment systems.  

---
