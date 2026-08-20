# INSYD AI Career Matchmaker & VET Advocacy Platform 🚀

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Host: GitHub Pages](https://img.shields.io/badge/Frontend-GitHub%20Pages-blue)](https://pages.github.com/)
[![Backend: Render](https://img.shields.io/badge/Backend-Render-black)](https://render.com/)

A lightweight, mobile-first web application designed to help high school students explore career pathways, receive AI-generated HSC/VET roadmaps, and anonymously voice support for expanded School-Based Apprenticeship and Traineeship (SBAT) qualifications in New South Wales.

---

## 🎯 Project Motivation & Impact

In New South Wales secondary education, access to higher-tier vocational qualifications—specifically **Certificate IV** level courses—is often constrained under existing Vocational Education and Training (VET) circulars (such as **CIB 713**).

This project serves a dual purpose:
1. **Student Empowerment:** Provides a fast (<60s) interactive questionnaire that generates custom post-school career advice via an LLM engine.
2. **Data-Driven Advocacy:** Gathers quantitative student sentiment regarding interest in advanced VET pathways (specifically **ICT40120 Certificate IV in Information Technology**) to present structured data to industry bodies (ITAB) and educational policy stakeholders.

---

## ✨ Key Features

* **Dynamic Branching UI:** Tailors questions based on Year Group (Junior 7–9 vs. Senior 10–12) to match educational context.
* **Single Page Application (SPA):** Zero-reload mobile user interface optimized for playground & QR-code access.
* **AI Career Engine:** Integrates with an Express/LLM backend to parse open-ended student aspirations and generate actionable 3-paragraph HSC roadmaps.
* **Public Analytics Dashboard:** Features live aggregate chart displays (`/results.html`) powered by Chart.js to highlight student demand without exposing Personally Identifiable Information (PII).

---

## 🛠️ Tech Stack

* **Frontend:** HTML5, CSS3 (Modern Dark Theme), Vanilla JavaScript (ES6+)
* **Backend:** Node.js, Express.js (Hosted on Render)
* **Data & Analytics:** REST API endpoints returning sanitized JSON payloads for real-time statistics
* **LLM Integration:** OpenAI API / DeepSeek via serverless API routes
* **Deployment:** GitHub Pages (Frontend static hosting) + Custom `.au` Domain routing

---

## 🏗️ Architecture Overview

```text
[ Client (Mobile Browser) ] 
       │
       ├──> 1. Completes Survey & Inputs Aspirations
       │
       └──> 2. POST /api/career (JSON Payload) ──> [ Express Backend on Render ]
                                                         │
                                                         ├──> Stores Anonymous Data
                                                         └──> Calls LLM Engine
                                                                   │
       <── 3. Returns Personalized AI Roadmap <────────────────────┘
