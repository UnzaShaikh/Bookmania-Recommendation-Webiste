# 📚 Bookmania — Book Recommendation E-Commerce Website

> A smart book recommendation web platform that helps readers discover educational books tailored to their preferences using content-based filtering, TF-IDF, and collaborative filtering techniques.

**Developed by:** Anber Sattar (19SW33) & Unza Shaikh (19SW113)  
**Supervised by:** Dr. Areej Fatemah

---

## 🌟 Features

- 🔍 **Book Search** — Search for books by title, author, or genre
- 🤖 **Personalized Recommendations** — Content-based recommendations using TF-IDF and Cosine Similarity tailored to user preferences
- 🏆 **Popularity-Based Suggestions** — Displays a curated list of the Top 30 highest-rated books based on average user ratings
- 📋 **Personalized Recommendation Form** — Users fill in preferences to receive customized book suggestions
- 🆕 **New Releases** — Browse the latest book additions
- 👤 **User Authentication** — Sign up and log in with user accounts and profile management
- 🗄️ **Database-Backed** — Stores user accounts, profiles, and book data

---

## 🧠 Recommendation System

Bookmania implements multiple recommendation approaches:

### 1. Content-Based Filtering (TF-IDF + Cosine Similarity)
- Builds user profiles based on book features and user preferences
- Converts textual book information into numerical vectors using **TF-IDF**
- Measures similarity between books using **Cosine Similarity**
- Provides personalized suggestions aligned with individual reading tastes

### 2. Popularity-Based Algorithm
- Calculates average ratings for each book across all users
- Surfaces the **Top 30 most popular and highly-rated books**
- Helps new users discover trusted, widely-endorsed titles (addresses the cold-start problem)

### 3. Collaborative Filtering (KNN & SVD)
Explored during development:
- **KNN Collaborative Filtering** — Item-based and user-based variants
- **KNN with Additional User Data** — Enhanced with enriched user metadata
- **Matrix Factorization using SVD** — Evaluated for recommendation accuracy

> ⚠️ **Cold-Start Problem:** The system uses content-based and popularity-based methods to handle new users with limited data history.

---

## 🛠️ Tech Stack

| Layer       | Technology                                      |
|-------------|-------------------------------------------------|
| Frontend    | HTML, CSS, JavaScript (via `static/` & `templates/`) |
| Backend     | Python, Flask (`app.py`)                        |
| ML / NLP    | TF-IDF, Cosine Similarity, KNN, SVD (`Recommendation.ipynb`) |
| Runtime     | Node.js (`package.json`, `node_modules/`)       |
| Deployment  | Heroku (`Procfile`)                             |
| Libraries   | pandas, numpy, scikit-learn (see `requirements.docx`) |

---

## 📊 Dataset

Two custom datasets were designed and curated for this project (stored in the `data/` folder):

- **Book Dataset** — Book titles, authors, genres, descriptions, ratings, and cover information specific to educational books
- **User Dataset** — User accounts, reading preferences, and rating history

### Data Preprocessing Steps
1. **Exploratory Data Analysis (EDA)** to understand data distributions
2. Identification and removal of **null values** and **duplicate records**
3. Clean, structured data prepared for feature engineering and model training

> The full preprocessing and model experimentation pipeline is in `Recommendation.ipynb`.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- pip
- Node.js & npm
- Git

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/UnzaShaikh/Bookmania-Recommendation-Webiste.git
   cd Bookmania-Recommendation-Webiste
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv

   # On Windows
   venv\Scripts\activate

   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Python dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Install Node dependencies**

   ```bash
   npm install
   ```

5. **Generate a secret key**

   ```bash
   python generate_secret_key.py
   ```

6. **Set up environment variables**

   Create a `.env` file in the root directory:

   ```env
   SECRET_KEY=your_generated_secret_key_here
   DATABASE_URL=your_database_url_here
   ```

7. **Run the application**

   ```bash
   python app.py
   ```

8. Open your browser and navigate to `http://localhost:5000`

---

## 📁 Project Structure

```
Bookmania-Recommendation-Webiste/
│
├── data/                        # Book and user datasets
│
├── static/                      # CSS, JS, and image assets
│
├── templates/                   # HTML (Jinja2) templates
│
├── app.py                       # Flask application entry point
├── generate_secret_key.py       # Utility to generate Flask secret key
├── Recommendation.ipynb         # ML model experimentation notebook
│
├── Procfile                     # Heroku deployment configuration
├── package.json                 # Node.js dependencies
├── package-lock.json            # Node.js lock file
└── requirements.docx            # Python dependencies list
```

---

## ☁️ Deployment

This project is configured for deployment on **Heroku** via the `Procfile`. To deploy:

1. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
2. Log in and create a new app:
   ```bash
   heroku login
   heroku create bookmania-app
   ```
3. Push to Heroku:
   ```bash
   git push heroku main
   ```

---

## 🔮 Future Work

- Integrate **advanced recommendation algorithms** for improved accuracy
- Develop a **mobile application** for wider accessibility
- Add **social media features** (follow users, share reading lists)
- Expand catalogue beyond educational books
- Prioritize **ethical data management** and user privacy
- Offer **e-readers and merchandise** within the platform

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👩‍💻 Authors

**Anber Sattar** — 19SW33  
**Unza Shaikh** — 19SW113  
- GitHub: [@UnzaShaikh](https://github.com/UnzaShaikh)

**Supervised by:** Dr. Areej Fatemah

---

# Book_Website Project Demo
https://drive.google.com/file/d/1GXx4i2q8RBvaHavoEL8yp1H6xXJDNpJl/view?usp=drive_link

> Made with ❤️ for book lovers and curious readers everywhere.


