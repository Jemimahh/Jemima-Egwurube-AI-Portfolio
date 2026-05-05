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

#### Project 1 · Administrative Assistant Agent

> An agentic AI system that automates a multi-step department kickoff meeting workflow — handling scheduling, documentation, reminders, and follow-ups through a coherent Planning-then-Execution architecture.

| Detail | Value |
|---|---|
| Architecture | Planning-then-Execution agent pattern |
| Tools | Calculator, document summarizer |
| Key techniques | Agent memory, tool integration, RL-style feedback & policy improvement |
| Safety | Input validation, boundaries, fallbacks, transparency |

**Highlights:**
- Coherent agent design: input → memory → reasoning → output pipeline
- Tool-augmented execution with a calculator and document summarizer
- Simple reinforcement learning–style feedback loop for policy improvement
- Safety and security layer with input validation, guardrails, and transparent fallbacks

📁 [`DeepLearning-ITAI2376/Project1/`](./Jemima-Egwurube-DeepLearning-ITAI2376/)



---

### Computer Vision — ITAI 1378

#### Project 1 · Food Classification — NutritionTracker CV System

> EfficientNet-B0 fine-tuned on Food-101 (101 classes, 75,750 images) to classify food from a single photo and return estimated nutritional information — calories, protein, carbs, and fat.

| Detail | Value |
|---|---|
| Model | EfficientNet-B0 (ImageNet → Food-101) |
| Dataset | torchvision Food-101 · 101 categories · 75,750 train / 25,250 val |
| Framework | PyTorch + torchvision |
| Key techniques | Two-phase fine-tuning, data augmentation, label smoothing, CosineAnnealingLR |
| Final accuracy | **86.27% Top-1** ✅ (target: ≥ 85%) |

**Highlights:**
- Two-phase transfer learning: frozen backbone (58.37%) → full fine-tune (86.27%) — a 28-point jump from one architectural decision
- Top-3 inference with nutrition lookup table (calories, protein, carbs, fat per serving)
- Best class: bibimbap F1 0.949 · Hardest class: apple_pie F1 0.684 (visual overlap with bread_pudding)
- Training curves, confusion matrix, and per-class F1 chart in `results/`

📁 [`ComputerVision-ITAI1378/Object_Detection_Project/`](./ComputerVision-ITAI1378/Food_Classification_Project/)

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
