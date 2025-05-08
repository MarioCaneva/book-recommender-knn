# 📚 Book Recommender using K-Nearest Neighbors

This project builds a book recommendation system using the [Book-Crossings dataset](https://www.kaggle.com/datasets/ruchi798/bookcrossing-dataset) and K-Nearest Neighbors (KNN) from scikit-learn. 
It allows users to input a book title and receive a list of similar books based on user rating patterns.

---

## 🚀 Features

- Uses collaborative filtering with user-book ratings
- Filters for statistical significance (active users and popular books)
- Efficient sparse matrix representation
- Fast book lookup and distance-based recommendations
- Clean API function: `get_recommends(book_title)`

---

## 🔧 How It Works

1. Loads and cleans the Book-Crossings data.
2. Filters users with ≥200 ratings and books with ≥100 ratings.
3. Builds a sparse matrix of books (rows) vs users (columns).
4. Trains a `NearestNeighbors` model using cosine distance.
5. The `get_recommends()` function takes a book title and returns:
   [
     'Input Book Title',
     [['Recommended Book 1', distance1], ['Recommended Book 2', distance2], ...]
   ]
   
📊 Example

get_recommends("The Queen of the Damned (Vampire Chronicles (Paperback))")
Returns:
[
  "The Queen of the Damned (Vampire Chronicles (Paperback))",
  [
    ["Catch 22", 0.79],
    ["The Witching Hour (Lives of the Mayfair Witches)", 0.74],
    ["Interview with the Vampire", 0.73],
    ["The Tale of the Body Thief (Vampire Chronicles (Paperback))", 0.53],
    ["The Vampire Lestat (Vampire Chronicles, Book II)", 0.51]
  ]
]

🧪 Run the Notebook
You can run this project in Google Colab or any Jupyter environment. Make sure to:

Upload the dataset files (BX-Books.csv and BX-Book-Ratings.csv)

Run all cells in order.

✅ Requirements
Python 3.x

numpy, pandas, scikit-learn, scipy, matplotlib


📜 License
This project is open-source and available under the MIT License.
