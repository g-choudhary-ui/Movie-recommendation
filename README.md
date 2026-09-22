# 🎬 Movie Recommendation System

An end-to-end **content-based movie recommendation system** built using **NLP, TF-IDF, FastAPI, Streamlit, and TMDB API**.

## 🚀 Live Demo

👉 **[Try the Movie Recommendation System](https://movie-recommendation-jexnqv9blyxzx2cjao9n3.streamlit.app/)**

## ✨ Features

- 🔎 Search movies by title or keyword
- 🎯 TF-IDF-based content recommendations
- 🎭 Genre-based recommendations
- 📄 Movie details with posters, backdrops, overview, genres, and release date
- ⚡ FastAPI REST backend
- 🎨 Interactive Streamlit frontend
- 🌐 TMDB API integration
- ☁️ Deployed using Streamlit Cloud and Render

## 🧠 Recommendation System

The system uses **content-based filtering** to recommend movies.

Movie information is processed using **NLP and TF-IDF vectorization**. Similarity between movie representations is then used to identify movies with similar content.

Two recommendation approaches are provided:

- **TF-IDF Similarity** — recommends movies with similar textual content.
- **Genre-Based Recommendation** — recommends movies sharing similar genres.

## 🏗️ Architecture

```text
                    ┌──────────────────┐
                    │      User        │
                    └────────┬─────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ Streamlit Frontend  │
                  └──────────┬──────────┘
                             │ HTTP Requests
                             ▼
                  ┌─────────────────────┐
                  │   FastAPI Backend   │
                  └──────────┬──────────┘
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
        ┌──────────┐   ┌───────────┐  ┌──────────┐
        │ TMDB API │   │  TF-IDF   │  │  Genre   │
        │          │   │Similarity │  │Recommendation│
        └──────────┘   └───────────┘  └──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ Recommended Movies  │
                  └─────────────────────┘

| Technology   | Purpose               |
| ------------ | --------------------- |
| Python       | Core programming      |
| Streamlit    | Frontend / UI         |
| FastAPI      | Backend REST API      |
| Scikit-learn | TF-IDF and similarity |
| Pandas       | Data processing       |
| NumPy        | Numerical operations  |
| SciPy        | Scientific computing  |
| TMDB API     | Movie data and images |


⚙️ Run Locally
1. Clone the repository
git clone https://github.com/g-choudhary-ui/Movie-recommendation.git
cd Movie-recommendation
2. Create a virtual environment
python -m venv .venv

Activate on Windows:

.venv\Scripts\activate
3. Install dependencies
pip install -r requirements.txt
4. Configure environment variables

Create a .env file:

TMDB_API_KEY=your_tmdb_api_key
5. Start the FastAPI backend
uvicorn main:app --host 0.0.0.0 --port 8000

FastAPI documentation:

http://127.0.0.1:8000/docs
6. Start the Streamlit frontend
streamlit run app.py
🔄 Application Flow
Search Movie
     ↓
TMDB Search
     ↓
Select Movie
     ↓
Movie Details
     ↓
Generate Recommendations
     ↓
 ┌───────────────────┐
 │ TF-IDF Similarity │
 └───────────────────┘
          +
 ┌───────────────────┐
 │ Genre Similarity  │
 └───────────────────┘
          ↓
 Recommended Movies
☁️ Deployment

The application uses separate services for frontend and backend:

Frontend: Streamlit Community Cloud
Backend: Render
Movie Data: TMDB API
🔐 Environment Variables

The TMDB API key is stored as an environment variable and is not included in the GitHub repository.

TMDB_API_KEY=your_tmdb_api_key
📌 Project Highlights
Implemented a complete frontend + backend architecture
Applied NLP and TF-IDF for content-based recommendations
Built REST APIs using FastAPI
Integrated a third-party movie API
Deployed the application using cloud platforms
Connected the deployed frontend with the deployed backend
🔗 Links

🚀 Live Demo
 -> https://movie-recommendation-jexnqv9blyxzx2cjao9n3.streamlit.app/


👩‍💻 Author
Garima Choudhary

B.Tech Computer Science & Engineering
