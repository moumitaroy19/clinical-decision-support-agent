# 🏥 Clinical Decision Support Agent

![Python](https://img.shields.io/badge/Python-3.10-blue)
![LangGraph](https://img.shields.io/badge/LangGraph-Agent-green)
![Groq](https://img.shields.io/badge/Groq-LLaMA3.3-orange)
![PubMed](https://img.shields.io/badge/PubMed-API-red)

## 🔍 Overview
An intelligent Medical AI Agent that takes patient symptoms as natural language input, searches real PubMed medical literature in real-time, and generates structured clinical recommendations with citations. Built with LangGraph for agent orchestration and LLaMA 3.3 70B via Groq for clinical reasoning.

## 🎯 Live Demo
👉 [Try it on Hugging Face Spaces](https://huggingface.co/spaces/mou11/clinical-decision-support-agent)

## 🤖 How the Agent Works

Patient Symptoms → Extract Search Query (LLM) → Search PubMed API → Generate Clinical Recommendation (LLM) → Format Structured Output → Evaluate with BERTScore

## 📊 Test Results

| Test Case | Symptoms | Urgency | Correct? |
|-----------|----------|---------|----------|
| Case 1 | Fever, cough, chest pain | High | ✅ |
| Case 2 | Headache, stiff neck, fever | Emergency | ✅ |
| Case 3 | Chest pain, sweating, diabetes | Emergency | ✅ |

## 📈 BERTScore Evaluation

| Metric | Score |
|--------|-------|
| Precision | 0.8449 |
| Recall | 0.8887 |
| F1 Score | 0.8663 ✅ |

Scores above 0.85 indicate high quality responses.

## 🏗️ Agent Architecture

- **Orchestration:** LangGraph — stateful directed graph workflow
- **LLM:** LLaMA 3.3 70B via Groq API (free tier)
- **Knowledge Base:** PubMed API — real medical literature
- **Evaluation:** BERTScore — semantic response quality
- **Memory:** Multi-turn conversation history
- **UI:** Gradio web interface

## ✨ Key Features

- Real-time PubMed literature search
- Structured JSON output — conditions, tests, treatments, urgency
- Multi-turn conversation memory
- BERTScore quality evaluation
- Responsible AI — medical disclaimer on every response
- Completely free to run — no paid APIs required beyond Groq free tier

## 🛠️ Tech Stack

- LangGraph
- LangChain
- Groq API (LLaMA 3.3 70B)
- PubMed NCBI API
- BERTScore
- Gradio
- Google Colab (CPU)

## 🚀 How to Run

1. Get a free Groq API key at console.groq.com
2. Open Clinical_Decision_Support_Agent.ipynb in Google Colab
3. Replace your-groq-api-key-here with your actual key
4. Run all cells in order

## ⚠️ Medical Disclaimer

This system is for educational and research purposes only. It does not provide medical advice. Always consult a qualified healthcare professional for medical decisions.

## 📌 Project Status

✅ Agent built and tested
✅ PubMed integration working
✅ BERTScore evaluation implemented
✅ Gradio demo deployed on Hugging Face Spaces
✅ Live demo available
