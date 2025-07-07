# 🔐 AI-Based Password Strength Classifier

This project presents an AI-powered tool designed to evaluate the strength of passwords using machine learning and entropy-based analysis. It classifies passwords into Weak, Medium, or Strong categories and provides users with actionable feedback on password robustness and potential vulnerabilities.

---

## 📘 Project Background

This password strength evaluation tool was developed alongside the work presented in **Chapter 5: Practical AI in Cybersecurity** of my Master's thesis titled *Practical AI in Cyberwarfare and Cybersecurity*.

The project was implemented by **Konstantinos Zafeiropoulos** (Student ID: 20390293) at the  
**University of West Attica**  
**Faculty of Engineering, Department of Informatics and Computer Engineering**

> ⚠️ Although the tool was fully implemented and tested, it was **not included in the final thesis submission** due to time and length constraints, as well as the decision to focus on other tools that demonstrated higher technical impact in the field of cybersecurity.

---

## 1️⃣ Why AI is Needed

- Learns from real-world leaked passwords and human-generated patterns.
- Combines statistical features like:
  - Length  
  - Symbols  
  - Digits  
  - Entropy  
  - Repetitions  
- Delivers **dynamic**, structure-aware feedback rather than static rules.

---

## 2️⃣ Can This Be Done Without AI?

Yes, but with significant limitations:

- Rule-based systems (e.g., “min 8 characters”) are:
  - Rigid and predictable  
  - Cannot adapt to new password trends  
  - Miss nuanced strength differences (e.g., `Password123!` vs. `p@5sW0rd!`)

---

## 3️⃣ AI Algorithm Used

✅ **XGBoost Classifier (XGBClassifier)**

- Builds multiple decision trees sequentially
- Uses **gradient boosting** to reduce prediction error
- Supports **multi-class classification**
- Works exceptionally well on structured, tabular data (like password feature vectors)

---

## 4️⃣ Tool & AI Architecture

### 🔄 Tool Flow

- **Input**: Raw password (text string)
- **Preprocessing**: Feature extraction (length, digits, symbols, entropy, etc.)
- **Modeling**: XGBoost classifier trained on four publicly available datasets
- **Output**:
  - Strength prediction (Weak, Medium, Strong)
  - Entropy score
  - Leak check using RockYou dataset
  - Estimated crack time
  - Visual feedback

### 🧠 AI Model

- **Learning Type**: Supervised Machine Learning
- **Input Vector**: Extracted features from password
- **Output Class**:
  - `0` = Weak  
  - `1` = Medium  
  - `2` = Strong

---

## 5️⃣ AI Subcategory

✅ **Supervised Machine Learning**  
Specifically: **Multi-class Classification**

---

## 6️⃣ Purpose & Social Impact

- Encourage the use of **stronger, safer passwords**
- Identify weak patterns and **password reuse** risks
- Visualize **entropy and crack time** to increase awareness
- Promote better **digital hygiene** through clear, personalized feedback

---

## 7️⃣ Dataset Example: `data.csv`

| Field     | Description                        | Example         |
|-----------|------------------------------------|-----------------|
| password  | Raw password string                | `"Pass123!"`    |
| strength  | Password strength label (0–2)      | `0 = Weak`  
|           |                                    | `1 = Medium`  
|           |                                    | `2 = Strong`  

---

## 🚀 Getting Started

1. Clone this repository
2. Install dependencies using `pip install -r requirements.txt`
3. Run the main notebook or script to test password strength classification

---

## 📄 License

This project is open-source and licensed under the MIT License.

---

## 👤 Author

**Konstantinos Zafeiropoulos**  
Master's Thesis: *Practical AI in Cyberwarfare and Cybersecurity*  
University of West Attica – Department of Informatics and Computer Engineering
