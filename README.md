# 🩺 Medical Report AI Agent

A state-of-the-art, hybrid medical report analysis system that combines document extraction, local NLP regex parsing, interactive Plotly visualizations, and Google Gemini LLM intelligence. 

This agent is built completely in Python and is designed to run directly inside a Jupyter Notebook with a beautiful, responsive dark-themed **Gradio web GUI**.

---

## 🌟 Key Features

*   **📁 Multi-Format Document Processing:** Upload digital PDFs, scanned PDFs, or photos of lab reports (`.png`, `.jpg`, `.jpeg`).
*   **🛠️ Interactive Text Editor:** decoupeles raw text extraction and validation. Extracted text appears in an editor where you can manually fix typos or paste lab values directly.
*   **🧬 Hybrid Parsing Engine:**
    *   **Offline Mode:** Uses a advanced regex parser and standard medical reference dictionary to extract 20+ common lab tests (Glucose, Hemoglobin, WBC, RBC, Cholesterols, Liver & Kidney markers, Electrolytes, etc.), map normal ranges, and flag anomalies.
    *   **Online Mode (Gemini-Powered):** Connects to the **Google Gemini API** (`gemini-2.5-flash`) to perform high-fidelity medical summaries, complex translations of clinical jargon, lifestyle suggestions, and run cloud OCR on scans/images.
*   **📈 Visual Reference Ranges:** Automatically renders interactive Plotly bullet charts showing where your values sit relative to the normal reference intervals (Green zones show normal limits, dotted lines indicate thresholds, and out-of-range marks show up in red).
*   **👤 Interactive Patient Metadata:** Patient name, age, gender, and report date are parsed automatically but remain fully editable in the UI.
*   **💬 Ask the Medical Agent:** An interactive chatbot pre-seeded with the report's details to answer follow-up questions in real time.
*   **📖 Clinical Dictionary:** An integrated reference dictionary explaining what each lab marker represents.

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

### 2. Install Dependencies
Make sure you have Python 3.10+ installed, then run:
```bash
pip install -r requirements.txt
```

### 3. Run the Application
Open the Jupyter Notebook:
```bash
jupyter notebook Untitled.ipynb
```
Run **all cells** in the notebook. The final cell will spin up a local web server and print a link:
```
http://127.0.0.1:7860
```
Open this link in your web browser to access the dashboard!

---

## 💡 How to Test Offline (No Key / No Files)
1. Open the Gradio dashboard in your browser.
2. Click **💡 Load Sample** on the left panel. This will instantly fill the editor with a mock laboratory report.
3. Click **🔍 Analyze Report**. The local rule engine will immediately parse the values, flag abnormalities (WBC, Cholesterol, Glucose, Potassium), and render the Plotly reference chart!

---

## ⚕️ Medical Disclaimer
This software is for informational and educational purposes only. It is not diagnostic, and does not provide medical advice or treatment recommendations. Always consult a qualified physician or healthcare provider regarding any clinical test results or health concerns.
