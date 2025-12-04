# 🔬 HealthLens — AI-Powered Lab Report Analysis

HealthLens is an AI healthcare assistant that analyzes blood test reports, detects health risks using Machine Learning, and generates personalized nutrition & fitness plans using Google Gemini — all through a Streamlit web app.

---

## 🚀 Features

- 🧾 Upload PDF / Image lab reports
- 🔍 OCR extraction of medical values
- 🤖 ML classification for Anemia, Diabetes & High Cholesterol
- 📊 Interactive health dashboard with score & insights
- 🍎 Personalized Indian diet plan (Gemini AI)
- 💪 Fitness routine based on health conditions
- ⏰ Health reminders & checkup tracking

---

## 🧠 Tech Stack

| Technology | Purpose |
|-----------|---------|
| Streamlit | Web UI |
| Python | Core backend |
| Scikit-Learn | ML Classification |
| Pandas / NumPy | Data Processing |
| Tesseract OCR | Report text extraction |
| Google Gemini | AI Recommendations |

---

## 📁 Project Structure

```
HealthLens/
├── app.py
├── requirements.txt
├── .env.example
├── data/
├── models/
├── visuals/
└── src/
    ├── ml_classifier.py
    ├── ocr_module.py
    ├── ai_recommendation.py
    └── download_datasets.py
```

---

## ⚙️ Setup Guide

### 1️⃣ Clone and open project

```sh
git clone https://github.com/AnushreeRavichandran26/HealthLens.git
cd HealthLens
```

### 2️⃣ Create & activate venv

```sh
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # Mac/Linux
```

### 3️⃣ Install dependencies

```sh
pip install -r requirements.txt
```

### 4️⃣ Add Gemini API key

Create a `.env` file:

```ini
GEMINI_API_KEY=your_google_api_key_here
```

Get your API key from: [Google AI Studio](https://aistudio.google.com/app/apikey)

### 5️⃣ Install Tesseract OCR

**Windows:**
- Download from: [Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki)
- Install to `C:\Program Files\Tesseract-OCR\`

**Mac:**
```sh
brew install tesseract
```

**Linux:**
```sh
sudo apt-get install tesseract-ocr
```

### 6️⃣ (Optional) Download datasets & train ML models

```sh
python src/download_datasets.py --all
python src/ml_classifier.py
```

### 7️⃣ Run the web app

```sh
streamlit run app.py
```

---

## 📈 ML Model Summary

| Condition | Dataset | Target |
|-----------|---------|--------|
| Anemia | diagnosed_cbc_data_v4.csv | Hemoglobin-based |
| Diabetes | diabetes.csv | Outcome |
| Cholesterol | heart.csv | Cholesterol > 200 |

**Model:**
```
RandomForestClassifier + StandardScaler + Joblib
```

**Outputs** (saved in `visuals/`):
- Confusion Matrix
- ROC Curve
- Feature Importance

---

## 📸 Screenshots

![HealthLens HomePage](visuals/Home_page.png)
*Dashboard showing Health Lens Home Page*

![HealthLens Dashboard](visuals/dashboard_preview.png)
*Dashboard showing health analysis results*

![Diet Recommendations](visuals/diet_plan.png)
*AI-generated personalized diet plan*

---

## 🛡 Disclaimer

⚠️ **This project is for educational & research purposes only and must not be used as medical advice.**

Always consult with qualified healthcare professionals for medical decisions. The AI predictions are not a substitute for professional medical diagnosis.

---

## 👨‍💻 Author

**Anushree Ravichandran**

- GitHub: [@AnushreeRavichandran26](https://github.com/AnushreeRavichandran26)
- LinkedIn: [Your LinkedIn Profile](https://linkedin.com/in/yourprofile)

---

## 🙏 Acknowledgments

- [Kaggle](https://kaggle.com) for medical datasets
- [Google Gemini](https://ai.google.dev) for AI recommendations
- [Streamlit](https://streamlit.io) for the amazing web framework
- Open-source ML community

---

## 📞 Support

If you encounter any issues or have questions:

- Open an [Issue](https://github.com/AnushreeRavichandran26/HealthLens/issues)
- Star ⭐ this repository if you find it helpful!

---
