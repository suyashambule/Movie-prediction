# Movie Recommendation System

This project implements a content-based movie recommendation system using the TMDb (The Movie Database) 5000 Movie Dataset. The system analyzes movie features such as genres, cast, crew, keywords, and plot overviews to recommend similar movies based on content similarity.

## 🚀 Features

- **Content-Based Filtering**: Recommends movies based on movie attributes and content similarity
- **Multi-Feature Analysis**: Uses genres, cast, crew, keywords, and overview for comprehensive similarity calculation
- **Text Processing**: Implements advanced text preprocessing and feature extraction
- **Similarity Computation**: Uses cosine similarity to find the most similar movies
- **Interactive Jupyter Notebook**: Complete workflow from data preprocessing to recommendation generation

## 📊 Dataset

The project uses the TMDb 5000 Movie Dataset which includes:

- **Dataset File**: `tmdb_5000_movies.csv`
- **Total Movies**: 5,000 movies
- **Data Range**: Various years of movie releases
- **Key Features**:
  - `genres`: Movie genres (Action, Comedy, Drama, etc.)
  - `cast`: Main actors (top 3)
  - `crew`: Key crew members including directors
  - `keywords`: Associated keywords and tags
  - `overview`: Movie plot descriptions
  - `title`: Movie titles
  - `movie_id`: Unique identifiers

## 🛠️ Technology Stack

- **Python 3.7+**
- **pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **scikit-learn**: Machine learning algorithms and text processing
- **NLTK/TextBlob**: Natural language processing (optional)
- **SciPy**: Scientific computing and similarity calculations
- **AST**: Abstract Syntax Trees for parsing JSON-like strings
- **Jupyter Notebook**: Interactive development environment

## 📋 Requirements

Install the required packages using:

```bash
pip install -r requirements.txt
```

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd Movie-prediction
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook
```

### 4. Open the Main Notebook
Navigate to and open `Untitled.ipynb` in your browser.

### 5. Run the Analysis
Execute the cells in order to:
- Load and explore the movie dataset
- Clean and preprocess the data
- Extract and process movie features
- Create feature vectors for similarity computation
- Build the recommendation system
- Test recommendations for different movies

## 🏗️ Project Structure

```
Movie-prediction/
├── Untitled.ipynb           # Main Jupyter notebook
├── tmdb_5000_movies.csv     # Movie dataset
├── requirements.txt         # Python dependencies
└── README.md               # Project documentation
```

## 🔄 Data Processing Pipeline

### 1. Data Loading and Exploration
- Load TMDb movie dataset
- Explore data structure and statistics
- Identify missing values and data quality issues

### 2. Data Cleaning
- Remove movies with missing crucial information
- Handle duplicate entries
- Standardize data formats

### 3. Feature Extraction
- **Genres**: Extract genre lists from JSON-like strings
- **Cast**: Extract top 3 main actors
- **Crew**: Extract directors and key crew members  
- **Keywords**: Process movie keywords and tags
- **Overview**: Tokenize and process plot descriptions

### 4. Text Preprocessing
- Remove spaces from multi-word terms
- Convert to lowercase for consistency
- Create unified feature vectors

### 5. Feature Engineering
- Combine all features into comprehensive tags
- Create text-based feature representations
- Prepare data for similarity computation

## 🔍 Recommendation Algorithm

The system uses **Content-Based Filtering** with the following approach:

1. **Feature Vectorization**: Convert movie features into numerical vectors
2. **Similarity Calculation**: Use cosine similarity to measure movie similarities
3. **Ranking**: Sort movies by similarity scores
4. **Recommendation**: Return top-N most similar movies

### Similarity Metrics
- **Cosine Similarity**: Primary metric for measuring content similarity
- **Multi-dimensional Analysis**: Considers multiple movie attributes simultaneously

## 💡 Usage Examples

### Basic Movie Recommendation
```python
# Get recommendations for a specific movie
movie_title = "Avatar"
recommendations = get_recommendations(movie_title, num_recommendations=5)
print(f"Movies similar to {movie_title}:")
for movie in recommendations:
    print(f"- {movie}")
```

### Feature Analysis
```python
# Analyze movie features
movie_data = get_movie_features("The Dark Knight")
print(f"Genres: {movie_data['genres']}")
print(f"Cast: {movie_data['cast']}")
print(f"Director: {movie_data['crew']}")
```

## 📈 Key Components

### Data Preprocessing Functions
- `easy()`: Extracts names from JSON-like genre/keyword strings
- `easy2()`: Extracts top 3 cast members
- `direc()`: Extracts directors from crew data

### Feature Processing
- Genre extraction and standardization
- Cast and crew information processing
- Keyword and overview text processing
- Space removal and text normalization

### Recommendation Engine
- Feature combination and tag creation
- Vector space model implementation
- Similarity computation and ranking

## 🔮 Future Enhancements

- **Collaborative Filtering**: Implement user-based recommendations
- **Hybrid Approach**: Combine content-based and collaborative filtering
- **User Interface**: Build a web interface for easier interaction
- **Advanced NLP**: Implement more sophisticated text processing
- **Rating Integration**: Include user ratings for better recommendations
- **Real-time Updates**: Add capability to update with new movies
- **Performance Optimization**: Improve recommendation speed for large datasets

## 🤝 Contributing

Feel free to contribute to this project by:
- Improving the recommendation algorithm
- Adding new features or data sources
- Enhancing data preprocessing techniques
- Building a user interface
- Optimizing performance

## 📊 Sample Results

The system can provide recommendations like:

**Input**: "Avatar"
**Recommendations**:
- John Carter
- Guardians of the Galaxy
- Star Trek Into Darkness
- Pacific Rim
- Interstellar

## 🎯 Performance Considerations

- **Data Size**: Handles 5,000 movies efficiently
- **Processing Time**: Fast feature extraction and similarity computation
- **Memory Usage**: Optimized for reasonable memory consumption
- **Scalability**: Can be extended to larger datasets with minor modifications

## 📄 License

This project is available under the MIT License. See LICENSE file for details.

## ⚠️ Disclaimer

This project is for educational and research purposes. The movie recommendations are based purely on content similarity and may not reflect personal preferences or ratings.

---

**Happy Movie Watching! 🎬🍿**
