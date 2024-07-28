
# Candidate Search System

This project is a Candidate Search System that uses FAISS for efficient similarity search and TF-IDF for text vectorization. The system allows users to search for candidates based on job descriptions, and it returns the most relevant candidates from a database.

## Features

- Efficient Candidate Search: Uses FAISS for fast nearest neighbor search.

- Text Vectorization: Utilizes TF-IDF to convert textual data into numerical vectors.

- Data Preprocessing: Includes functions to preprocess candidate data and job descriptions.

- Command Line Interface: Allows users to input job descriptions and get relevant candidates via the command line.
## Installation

The project requires the following dependencies:

- numpy: For numerical operations.
- scikit-learn: For TF-IDF vectorization and cosine similarity.
- faiss-cpu: For efficient similarity search.
- sqlite3: For database operations.

```bash
  pip install numpy scikit-learn faiss-cpu

```
    
    
## Database Setup

Ensure that you have a SQLite database named candidates.db in the same directory as the script. The database should have a table named candidates with relevant candidate data.


## Roadmap

Set Up Environment

- Install necessary libraries: numpy, scikit-learn, faiss-cpu, and sqlite3.

- Ensure you have a SQLite database (candidates.db) with a candidates table containing the candidate data. Fetch Candidate Data

- Connect to the SQLite database. Fetch all candidate records from the candidates table. Convert the fetched records into a list of dictionaries for easier manipulation. 

- Preprocess candidate data: Combine candidate fields (name, skills, experience, projects, comments) into a single string.

- Use TfidfVectorizer to convert the preprocessed candidate data into TF-IDF vectors. Convert the sparse TF-IDF vectors to dense vectors of type float32.

- Initialize a FAISS index (IndexFlatIP) for fast nearest neighbor search. Normalize the dense vectors using faiss.normalize_L2. Add the normalized vectors to the FAISS index.


- Preprocess the input job description. Convert the preprocessed job description to a TF-IDF vector and normalize it. Use the FAISS index to search for the most similar candidates. Filter the matching candidates based on cosine similarity of job skills. Return the top N candidates that match the job description.


- Perform the candidate search and print the matching candidates.
## Feedback

If you have any feedback, please reach out to me at work.arooprath@gmail.com
