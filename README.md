# Content-Based Movie Recommendation System

## Summary

This project implements a content-based movie recommendation system using TF-IDF vectorization and cosine similarity. Users can input their movie preferences, and the system will return the most relevant movie recommendations based on genre, description, rating, and release year.

## Dataset

The dataset contains records of Indian movies, including:

- **Movie Names** (Title of the movie)
- **Genere** (Movie genre)
- **Rating** (IMDb or relevant rating)
- **Year** (Release year)
- **Description** (Short plot summary)

### Data Preprocessing

- Dropped rows with missing values.
- Removed duplicate entries based on 'Movie Names'.
- Cleaned the 'Genere' column by removing unwanted text (",Back to top").
- Combined relevant features (genre, year, rating, and description) into a single text field for similarity analysis.

## Setup

### Requirements

- Python 3.11+ (Recommended)
- Virtual Environment (Optional but Recommended!)

### Installation Steps

Clone the repository:

```bash
git clone https://github.com/ChinmayBitne/lumaa-spring-2025-ai-ml.git
```

Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Running the Code

### Option 1: Running in a Jupyter Notebook

1. Open Jupyter Notebook:

```bash
jupyter notebook
```

2. Run the cells step by step.

### Option 2: Running the Script in Terminal

To get movie recommendations based on user input:

```bash
python Recommender.py "User Input"
```

The script will prompt the user to enter their movie preference and display recommendations interactively.

## Features

- **User Input Prompt**: The system asks for user preferences dynamically.
- **Duplicate Handling**: Ensures unique movie entries.
- **Text Preprocessing**: Cleans and combines key movie attributes.
- **Interactive Query Editing**: Users can refine their queries after receiving recommendations.
- **Efficient Similarity Calculation**: Uses TF-IDF vectorization and cosine similarity for fast recommendations.

## Example Query and Output

**User Input:**

```text
Enter your movie preference: "Can I have thriller with some drama for family"
```

**Output:**

Top Movie Recommendations:

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Movie Names</th>
      <th>Genre</th>
      <th>Year</th>
      <th>Rating</th>
      <th>Description</th>
      <th>Similarity Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Drishyam 2</td>
      <td>Crime, Drama, Thriller</td>
      <td>2021</td>
      <td>8.4</td>
      <td>A gripping tale of an investigation and a family’s struggle.</td>
      <td>0.400691</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Drishyam</td>
      <td>Crime, Drama, Thriller</td>
      <td>2013</td>
      <td>8.3</td>
      <td>A man goes to extreme lengths to save his family.</td>
      <td>0.393829</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Joseph</td>
      <td>Crime, Drama, Thriller</td>
      <td>2018</td>
      <td>8.0</td>
      <td>The story develops through the life of four retired policemen.</td>
      <td>0.290516</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Papanasam</td>
      <td>Crime, Drama, Thriller</td>
      <td>2015</td>
      <td>8.4</td>
      <td>Desperate measures are taken by a man who tries to save his family.</td>
      <td>0.247727</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Nil Battey Sannata</td>
      <td>Drama, Family</td>
      <td>2015</td>
      <td>8.2</td>
      <td>A story about a single mother and her dream for her daughter’s future.</td>
      <td>0.221899</td>
    </tr>
  </tbody>
</table>
</div>

## Salary Expectation

### [$2000 - $2500] monthly
