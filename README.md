<div align="center">

# Mahmoud Ayman

**AI / ML Engineer · Computer Vision · LLMs & RAG · Full-stack AI products**

I build AI systems that leave the notebook - from edge devices and model pipelines to APIs and the dashboards people actually use.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mahmoud--aymann-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mahmoud-aymann/)
[![Portfolio](https://img.shields.io/badge/Portfolio-mahmoudayman.me-111827?style=flat-square)](https://mahmoudayman.me)
[![Email](https://img.shields.io/badge/Email-mahmoudaymann153%40gmail.com-3B82F6?style=flat-square&logo=gmail&logoColor=white)](mailto:mahmoudaymann153@gmail.com)
[![Medium](https://img.shields.io/badge/Medium-Articles-000000?style=flat-square&logo=medium&logoColor=white)](https://medium.com/@mahmoudayman1)

</div>

---

## About

I'm an AI/ML engineer from Egypt. I take a real-world problem, design the right AI approach, and ship it as a complete product: data and models, a production API, and a clean user interface.

- **Computer vision** - face verification, object detection, OCR, real-time inference on edge hardware.
- **LLM systems** - Retrieval-Augmented Generation with vector databases, grounded and source-cited answers.
- **Full-stack delivery** - FastAPI / NestJS backends, Next.js and vanilla-JS frontends, PostgreSQL, MongoDB, Redis, Docker.
- B.Sc. Communications & Electronics Engineering *(in progress)* · Advanced Diploma in AI & ML.

## What I build

| | |
|---|---|
| **Vision systems** | Detection, recognition and OCR pipelines - from training to ONNX export and on-device inference (Raspberry Pi). |
| **RAG & LLM apps** | Chunking, embeddings, pgvector retrieval, prompt design, provider-agnostic LLM layers and hallucination guards. |
| **AI products end to end** | Secure REST APIs, role-based access, background workers, reporting, and bilingual (Arabic / English) dashboards. |
| **Industrial AI** | Safety monitoring with computer vision, such as PPE compliance detection on oil & gas drilling sites. |

## Featured projects

### [DVD - Digital Verified Driver](https://github.com/mahmoud-aymann/DVD-Digital-Verified-Driver)
Real-time driver identity verification for vehicles. A Raspberry Pi in the car captures the driver and plate, runs YOLO + CNN plate OCR at the edge, and a FastAPI server verifies the face with InsightFace (ArcFace embeddings). Matches, violations and GPS-tagged road hazards (accidents, potholes, violence) stream into a bilingual command dashboard with alerts and reports.
*Repository contains partial source (API, dashboard, docs) - core AI components withheld; full source on request.*
`InsightFace` `YOLO` `PyTorch` `ONNX` `Raspberry Pi` `FastAPI` `MongoDB` `JavaScript`

### [Sanad - Islamic Knowledge RAG Chatbot](https://github.com/mahmoud-aymann/Islamic-Knowledge-RAG-Chatbot)
An Arabic-first RAG assistant that answers only from a curated library of ~80k passages and cites the book, author and page for every answer - and declines when no reliable source is found.
*Repository contains partial source (API skeleton, auth, frontend) - RAG core withheld; full source on request.*
`RAG` `FastAPI` `PostgreSQL + pgvector` `Celery` `Redis` `OpenAI-compatible LLMs` `Docker`

### [Blood Cell Prediction](https://github.com/mahmoud-aymann/blood_cell_prediction)
End-to-end medical-imaging classifier for blood cell types, with a web UI, REST API and a Dockerized deployment.
`PyTorch` `Flask` `OpenCV` `Docker`

### Private / client work
- **PPE monitoring system** - computer-vision detection of personal protective equipment compliance for industrial oil & gas drilling sites.
- **Nurvia** - a full-stack web platform built with NestJS, Next.js, PostgreSQL and Redis.

<details>
<summary><b>More public projects</b></summary>

| Project | Focus |
|---|---|
| [Question-Answering-with-Transformers](https://github.com/mahmoud-aymann/Question-Answering-with-Transformers) | Extractive QA with Transformer models fine-tuned on SQuAD |
| [insightface-flask-app](https://github.com/mahmoud-aymann/insightface-flask-app) | Face recognition with InsightFace + Flask |
| [Resume-Screening-Using-NLP](https://github.com/mahmoud-aymann/Resume-Screening-Using-NLP) | NLP resume screening |
| [AI-Travel-Agent-Flask](https://github.com/mahmoud-aymann/AI-Travel-Agent-Flask) | LLM-powered travel assistant |
| [-News_Headline_Classifier](https://github.com/mahmoud-aymann/-News_Headline_Classifier) | News headline classification with scikit-learn + Gradio |
| [Sentiment_Analysis_on_Product_Reviews](https://github.com/mahmoud-aymann/Sentiment_Analysis_on_Product_Reviews) | Sentiment analysis on product reviews |
| [Build-a-Neural-Network-from-Scratch](https://github.com/mahmoud-aymann/Build-a-Neural-Network-from-Scratch) | Neural network implemented from first principles |

</details>

## Tech stack

**AI / ML**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![YOLO](https://img.shields.io/badge/Ultralytics_YOLO-111F68?style=flat-square)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)

**Backend & data**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white)

**Frontend & DevOps**
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

## GitHub stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=mahmoud-aymann&show_icons=true&hide_border=true&theme=default&count_private=true" height="160" alt="GitHub stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mahmoud-aymann&layout=compact&langs_count=6&hide_border=true&theme=default" height="160" alt="Top languages" />
</p>

## Contact

Open to full-time roles, freelance projects and collaborations in AI / computer vision / LLM engineering.
The best way to reach me is [LinkedIn](https://www.linkedin.com/in/mahmoud-aymann/) or [email](mailto:mahmoudaymann153@gmail.com). Source code for private projects is available to recruiters and companies on request.
