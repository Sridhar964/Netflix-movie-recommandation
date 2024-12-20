Netflix Movies Recommender System
 Overview
The Netflix Movies Recommender System** is a machine learning application designed to suggest movies based on user input. It uses content-based filtering techniques to recommend movies similar to the selected one. The system leverages movie metadata like genres and overviews for its recommendations.

---
 Features
- **Interactive User Interface:** Built with Streamlit for ease of use.
- **Content-Based Filtering:** Utilizes textual data (genres and overview) to compute similarity scores.
- **Real-Time Suggestions:** Provides top 5 movie recommendations based on cosine similarity.
- **Model Persistence:** Uses pickle to save and load the processed data and similarity matrix.

---
 Dataset
The dataset consists of 10,000 movies with the following key columns:
- 'id': Unique identifier for each movie
- 'title': Title of the movie
- 'genre': Movie genres
- 'overview': Short description of the movie

The dataset is preprocessed to create a combined feature ('tagas') by concatenating `overview' and 'genre'.

---

 Installation
 Prerequisites
Ensure you have the following installed:
- Python 3.7 or higher
- Streamlit
- Required Python libraries ('pandas', 'sklearn', 'pickle')

 Steps
1. Clone the repository:
   bash
   git clone https://github.com/your-repo/netflix-movie-recommender.git
   
2. Navigate to the project directory:
   bash
   cd netflix-movie-recommender
   
3. Install dependencies:
   bash
   pip install -r requirements.txt
   
4. Run the Streamlit app:
   bash
   streamlit run app.py
   

---

 How It Works
1. Preprocessing:
   - Columns 'overview' and 'genre' are merged into a single column 'tagas'.
   - 'CountVectorizer' is used to transform text data into a bag-of-words representation.
2. Similarity Computation:
   - Cosine similarity is calculated for the 'tagas' feature across all movies.
3. Recommendations:
   - The system retrieves the top 5 most similar movies for the selected input movie.

---

 Usage
1. Select a movie from the dropdown menu.
2. Click the "Show Recommend" button.
3. View the top 5 recommended movies displayed in columns.

---

 Code Structure
- Data Processing:
  - 'movies_list.pkl': Preprocessed dataset stored as a pickle file.
  - 'similarity.pkl': Cosine similarity matrix stored for quick access.
- Streamlit App:
  - The Streamlit app is defined in 'app.py'.
  - Handles user input and displays recommendations.

---

 Example
Input Movie: "The Godfather"

Recommended Movies:
1. The Godfather: Part II
2. Blood Ties
3. Joker
4. Bomb City
5. Once Upon a Time in America

---
 Dependencies
- python Libraries:
  - 'pandas'
  - `scikit-learn'
  - 'Streamlit'
  - 'pickle'

---

 Future Enhancements
- Integrate user ratings for collaborative filtering.
- Include additional metadata like actors and directors for hybrid recommendations.
- Improve the UI with movie posters and additional details.

---
 License
This project is licensed under the MIT License. See 'LICENSE' for details.

---

 Acknowledgments
- The dataset is sourced from TMDB.
- Inspiration from Netflix's recommendation algorithms.
