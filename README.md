# FOOD-ADULTERATION-
📖 Overview

PureCheck is an AI-driven web application that helps everyday consumers detect food adulteration before it reaches their plate. Food adulteration — the practice of mixing, diluting, or substituting food with inferior, harmful, or non-permitted substances — remains a widespread food safety issue, particularly in staples like milk, spices, grains, oils, and produce.

PureCheck combines a clean, guided analysis flow with generative AI to flag likely adulterants, explain their health risks, and suggest practical detection tests and precautions — all in a single, easy-to-use interface.


⚠️ Disclaimer: PureCheck is built for educational and informational purposes. It does not replace certified laboratory testing or official food safety authorities.




✨ Features


🔍 Guided Food Analysis — Enter a food name, pick a category, optionally attach an image, and add contextual details (appearance, smell, texture, source).
🤖 AI-Powered Reports — Backed by the Gemini API to generate a structured adulteration report including a safety score, risk level, likely adulterants, and health impact.
🎯 Safety Gauge — An animated visual gauge (0–100) instantly communicates how safe a food item is likely to be.
📋 Detailed Adulterant Breakdown — Expandable cards for each detected adulterant with description, health impact, and how it can be detected at home.
💡 Actionable Recommendations — Practical tips on safer purchasing, storage, and simple home verification tests.
🗂️ Report History — All past analyses are saved and searchable, so users can revisit previous results.
📤 Easy Sharing — Share reports directly via Gmail or Google Drive.
📚 Knowledge Base — A built-in library of common adulterants (formalin, synthetic dyes, sawdust, stone particles, pesticide residues, and more) categorized by risk level.
📱 Fully Responsive — Clean, modern UI that works seamlessly across desktop and mobile.



🧪 Categories Covered

CategoryExamples of Detected Issues🥛 DairyWater dilution, synthetic milk, urea, formalin, detergent contamination🌶️ Spices & HerbsArtificial colors (metanil yellow, Sudan dyes), brick powder, sawdust, starch🌾 Grains & CerealsStone particles, artificial polishing agents, pesticide residues🫒 Oils & FatsAdulteration with cheaper oils, argemone contamination🥤 BeveragesArtificial sweeteners, unauthorized colorants🍗 Meat & FishFormalin preservation, unsafe additives🍎 Fruits & VegetablesPesticide residues, artificial ripening agents


🛠️ Tech Stack

Frontend


React 18 (via CDN, no build step)
Tailwind CSS (via CDN)
Babel Standalone (in-browser JSX transform)
Vanilla JS state management (no external state libraries)


Backend


FastAPI (Python)
Google Gemini API (gemini-2.0-flash) for AI-generated analysis
CORS-enabled REST endpoint



📂 Project Structure

purecheck/
├── index.html          # Single-file React frontend (CDN-based, no build tools required)
├── app.py               # FastAPI backend serving the Gemini-powered analysis endpoint
└── README.md


🚀 Getting Started

Frontend

The frontend is a single self-contained index.html file — no installation or build step required.

bash# Simply open it in a browser
open index.html

Or serve it locally:

bashpython -m http.server 8000

Backend


Install dependencies:


bash   pip install fastapi uvicorn google-generativeai


Add your Gemini API key inside app.py (server-side only — never exposed to the client).
Run the server:


bash   uvicorn app:app --reload --port 8000


🔄 How It Works


Upload or Describe — Provide a food name, category, and optionally an image or additional details.
AI Analysis — The backend sends the input to the Gemini API, which evaluates it against known adulteration patterns and safety data.
Get Your Report — Receive a structured report: safety score, risk level, detected adulterants, health impact, and detection methods.
Take Action — Follow tailored recommendations, and revisit or share saved reports anytime.



🗺️ Roadmap


 Persistent cloud storage for reports (replace local storage)
 User authentication and multi-device sync
 Barcode/label scanning for packaged foods
 Localized detection tips by region
 Multi-language support



🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the issues page or open a pull request.


📄 License

This project is open source and available under the MIT License.
