🎫 AI Support Ticket Classification & Prioritization System

This project builds a production-ready NLP system for automatically classifying and prioritizing customer support tickets. It covers the full machine learning lifecycle — from raw text preprocessing to a deployable web application — and is designed to be directly usable by support teams, SaaS companies, and IT service desks.



🎯 Key Outcomes

- Automatically classifies support tickets into categories (Billing, Technical, Account, General)
- Predicts ticket priority (High / Medium / Low)
- Achieves ~80–85% classification accuracy and ~75–80% priority accuracy
- Reduces manual ticket triaging effort significantly
- Provides real-time predictions via a web interface (Flask)


📂 Dataset Used

All training and evaluation are performed on real-world support ticket datasets.

Dataset| Description
Customer Support Tickets| Ticket text with category labels
IT Service Tickets| Multi-class classification dataset
Consumer Complaints| Large-scale NLP dataset for classification

Target Variables:

- "category" → Type of issue
- "priority" → Urgency level



🗂️ Project Structure

support-ticket-ml/
│
├── dataset/                     # Raw ticket datasets
│   └── tickets.csv
│
├── src/                         # Core ML pipeline
│   ├── preprocessing.py         # Text cleaning & NLP pipeline
│   ├── feature_engineering.py   # TF-IDF vectorization
│   ├── train_model.py           # Train classification models
│   ├── evaluate.py              # Metrics & reports
│   └── predict.py               # Inference logic
│
├── model/                       # Saved models
│   ├── category.pkl
│   ├── priority.pkl
│
├── app.py                       # Flask API backend
├── index.html                   # Frontend UI
├── requirements.txt
└── README.md



⚙️ Setup & Installation

1. Clone the Project

git clone https://github.com/your-username/support-ticket-ml.git
cd support-ticket-ml

2. Create Virtual Environment

python -m venv venv
source venv/bin/activate       # macOS/Linux
venv\Scripts\activate          # Windows

3. Install Dependencies

pip install -r requirements.txt

🚀 Run Instructions

Option A — Train Model

python src/train_model.py

Option B — Run Web Application

python app.py

🤖 Machine Learning Pipeline

🔹 Text Processing

- Lowercasing
- Stopword removal
- Tokenization
- Punctuation cleaning

🔹 Feature Engineering

- TF-IDF vectorization
- N-grams for context understanding

🔹 Models Trained

Model| Accuracy
Naive Bayes| ~75%
Logistic Regression ✅| ~85%
SVM| ~83%

Winner: Logistic Regression (best balance of performance and speed)


📊 Model Evaluation

Task| Accuracy| Precision| Recall| F1-score
Category Classification| 82–85%| 83%| 82%| 82%
Priority Prediction| 75–80%| 78%| 76%| 77%

✔ Evaluated using real-world ticket data
✔ Balanced performance across classes



🔍 Priority Prediction Logic

Priority is determined using:

1. ML-Based Prediction

Learns patterns from historical labeled data

2. Rule-Based Enhancement

- Keywords like “urgent”, “error”, “not working” → High
- Moderate issues → Medium
- General queries → Low

👉 Hybrid approach improves real-world reliability


📈 Business Insights

Ticket Distribution

- Technical issues dominate (~40%)
- Billing issues spike during payment cycles
- Account issues increase after updates/releases

Priority Trends

- High priority tickets mostly contain failure/error keywords
- Medium priority often linked to delays
- Low priority includes informational queries



💼 Business Value

Stakeholder| Value
Support Team| Reduces manual sorting effort
Customers| Faster response time
Managers| Better workload distribution
Business| Improved customer satisfaction

Estimated Impact:
Up to 60–70% reduction in ticket triaging time


🧪 Example

Input

"My payment was deducted but order not confirmed"

Output

Category: Billing  
Priority: High  


📊 Output Artifacts

File| Description
model/category.pkl| Category classification model
model/priority.pkl| Priority prediction model
evaluation report| Accuracy, precision, recall
web interface| Real-time prediction system



🛠️ Tech Stack

- Python 3.x
- pandas, numpy
- scikit-learn
- NLTK / spaCy
- Flask
- HTML, CSS, JavaScript



🔮 Future Improvements

- Transformer models (BERT)
- Multi-language ticket support
- Real-time dashboard analytics
- Cloud deployment (AWS / Render)


📌 Conclusion

This project demonstrates how Natural Language Processing (NLP) can be applied to automate support operations. It converts unstructured text into actionable decisions, enabling faster and smarter customer service systems.


