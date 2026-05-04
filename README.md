# Jemima Egwurube — AI Portfolio

**AI Engineer · Robotics Builder**  
M.S. Computer Science · A.A.S. Artificial Intelligence (in progress) · Houston Community College  
AWS Certified Cloud Practitioner · Azure AZ-900  

[![LinkedIn](https://img.shields.io/badge/LinkedIn-jemima--egwurube-0077B5?style=flat&logo=linkedin)](www.linkedin.com/in/jemimaegwurube)
[![GitHub](https://img.shields.io/badge/GitHub-jemima-181717?style=flat&logo=github)](https://github.com/Jemimahh)

---

## About This Portfolio

This repository documents hands-on AI/ML projects built across my graduate coursework at Houston Community College. Each project goes beyond lecture exercises — these are working systems with real pipelines, deployable interfaces, and code I wrote and own.

My work spans four domains I care about deeply: **natural language processing**, **computer vision**, **AI security**, and **autonomous robotics**. Where possible, projects are designed to be reproducible — you should be able to clone, install, and run them.

---

---

## Project Index

### Deep Learning — ITAI 2376

#### Project 1 · Food Classification with EfficientNet-B0

> Fine-tuned EfficientNet-B0 on a 20-category food image dataset (Kaggle) to classify dishes from photos.

| Detail | Value |
|---|---|
| Model | EfficientNet-B0 (transfer learning) |
| Dataset | Food-101 subset · 20 categories |
| Framework | PyTorch / TensorFlow |
| Key techniques | Transfer learning, data augmentation, learning rate scheduling |

**Highlights:**
- Fine-tuned pretrained ImageNet weights on a food-specific distribution
- Evaluated per-class precision, recall, and F1 across all 20 categories
- Results and confusion matrix visualizations in `results/`



---

### NLP — ITAI 2373

---

#### Project 1 · NewsBot Intelligence System 2.0 *(Final)*

> An extended, modular NLP intelligence system adding LLM-powered Q&A, multilingual support, topic modeling, and summarization to the midterm NewsBot.

| Detail | Value |
|---|---|
| Dataset | BBC News (multi-category) |
| LLM backend | LLaMA 3.2 via Ollama (local inference) |
| New modules | LLM Q&A, multilingual NLP, topic modeling (LDA), abstractive summarization |
| Stack | Python, spaCy, NLTK, Ollama, langdetect, Gradio |

**New modules:**

| Module | Description |
|---|---|
| `llm_module.py` | LLaMA 3.2 integration via Ollama for article Q&A |
| `multilingual_module.py` | Language detection + cross-lingual NLP support |
| `topic_model.py` | LDA-based topic discovery across the corpus |
| `summarizer.py` | Abstractive and extractive summarization |


---

## Skills Demonstrated

| Area | Technologies |
|---|---|
| **LLMs & RAG** | LLaMA 3.2 (Ollama), LangChain, LlamaIndex, ChromaDB |
| **NLP** | spaCy, NLTK, TF-IDF, VADER, LDA, HuggingFace Transformers |
| **Computer Vision** | EfficientNet-B0, SSD MobileNet V2, PyTorch, TensorFlow |
| **Robotics** | ROS 2 Jazzy, RPLIDAR C1, AprilTags, sensor fusion |
| **AI Security** | NIST AI RMF, MITRE ATT&CK, RAG shield layers, SOC logging |
| **Cloud & Infra** | AWS (CCP certified), Azure (AZ-900), Google Colab, Gradio |
| **Languages** | Python, C++, AVR Assembly |

---

## How to Run Projects

Each project directory contains its own `README.md` with setup instructions. General requirements:

```bash
# Clone the repo
git clone https://github.com/jemimaegwurube/Jemima-Egwurube-AI-Portfolio.git
cd Jemima-Egwurube-AI-Portfolio

# Most projects use a standard Python environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt  # located in each project folder
```

> **Note on LLM projects:** NewsBot 2.0 requires [Ollama](https://ollama.ai) running locally with the `llama3.2` model pulled (`ollama pull llama3.2`).

---

## Presentation

The portfolio slide deck (built for ITAI 2373) is available in the `Presentation/` directory.  
📄 [`Presentation/Pf_JemimaEgwurube_ITAI2373.pdf`](./Presentation/Pf_JemimaEgwurube_ITAI2373.pdf)

---

## Contact
**Jemima Egwurube**   
🔗 [linkedin.com/in/jemima-egwurube](https://linkedin.com/in/jemima-egwurube)  
💻 [github.com/jemimaegwurube](https://github.com/jemimaegwurube)  
📍 Houston, TX
