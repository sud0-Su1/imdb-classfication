#  IMDB Sentiment Analysis Pipeline  

This project is an **end-to-end machine learning pipeline** that predicts whether a movie review is **positive or negative**.  
I used the **IMDB dataset (50k reviews)** and built everything from data preprocessing all the way to deployment with FastAPI and Docker.  

It’s designed to show how machine learning, data engineering, and MLOps all come together in a single project.  

---

## 🚀 What I Built  
- Cleaned and processed raw IMDB reviews (text cleaning, tokenization, TF-IDF).  
- Trained multiple models (Logistic Regression, XGBoost) and compared them.  
- Used **MLflow** to track experiments, metrics, and save models.  
- Deployed the best model as a **FastAPI web service**, wrapped in **Docker**.  
- Set up **GitHub Actions** to automatically test and build the project (CI/CD).  

---

## 🛠️ Tech Stack  
**Python, Scikit-learn, XGBoost, MLflow, FastAPI, Docker, GitHub Actions**  

---

## 📂 Project Structure  
imdb-sentiment/
│── src/ # preprocessing + training scripts
│── app/ # FastAPI app for predictions
│── models/ # saved models / MLflow artifacts
│── tests/ # unit tests
│── Dockerfile # container setup
│── requirements.txt
│── README.md


---

## ▶️ How to Run  

**1. Clone the repo**  
```bash
git clone https://github.com/yourusername/imdb-sentiment.git
cd imdb-sentiment
```
**2. Install dependencies**

pip install -r requirements.txt

```
**3. Train the model**

python src/train.py

```
**4. Start the FastAPI server**

uvicorn app.main:app --reload

```
5. Test a review

curl -X POST "http://127.0.0.1:8000/predict" \
     -H "Content-Type: application/json" \
     -d '{"review": "This movie was amazing!"}'



---

📊 Results

Logistic Regression → ~85% accuracy

XGBoost → ~89% accuracy
