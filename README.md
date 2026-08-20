# INSYD AI Career Matchmaker 🚀

A student-led, lightweight Single Page Application (SPA) designed to collect targeted demographic data on high school career interests. 

This project isn't just a survey; it's a data collection tool built to advocate for systemic change. The data gathered here is being used to petition the NSW Department of Education and the ITAB (Industry Training Advisory Body) to amend policy CIB-713, specifically aiming to allow the **ICT40120 Certificate IV in Information Technology** to be undertaken as a School-Based Apprenticeship (SBAT).

## 💡 The Problem
Currently, NSW high school students face rigid limitations regarding the level of vocational training (VET/SBAT) they can undertake, often capped at Certificate II or III. This limits students who are ready for advanced pathways, particularly in the tech sector.

## 🛠️ The Solution
This web app acts as a "Trojan Horse" data collection tool:
1. **The Hook:** It offers students a free, AI-generated personalized career roadmap.
2. **The Logic:** Custom JS handles branching question paths based on the user's age and experience level.
3. **The Data:** It collects quantitative data on how many students want access to Cert IV options.
4. **The AI:** It securely POSTs the JSON payload to a Render backend, querying an LLM to return actionable HSC/VET advice.

## 💻 Tech Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript (Mobile-first, zero-dependency SPA)
* **Backend:** Node.js / Express (Hosted via Render)
* **Database / Analytics:** Pending (Supabase/Google Sheets API for data aggregation)
* **Hosting:** GitHub Pages
* **Domain Strategy:** Configured to map to a custom `.au` domain.

## 🤖 AI Disclosure
*Transparency note for recruiters and developers:* 
The architecture, core logic, and UI of this project were built with heavy assistance from AI (LLMs). I utilized AI as a pair-programmer to rapidly prototype the branching frontend logic, scaffold the UI, and structure the data payloads, allowing me to focus on the high-level system design and policy advocacy goals.

## 🚀 How to Run Locally
1. Clone the repo: `git clone [https://github.com/vincentrasskazov/insyd-career-tool.git](https://github.com/vincentrasskazov/insyd-career-tool.git)`
2. Open `index.html` in your browser.
3. No build steps required for the frontend.
