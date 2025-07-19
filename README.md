# Web Mining and Applied NLP (44-620)

## Requests, JSON, and NLP

### Student Name: Matthew Block
[JSON Sentiment Repository](https://github.com/matthewpblock/json-sentiment)  

Complete the tasks in the Python Notebook in this repository.
To be submitted for credit, all changes must be committed and pushed to this repository (do not create your own repository unless instructed to on the course website).

## Rubric

* (Question 1) Lyrics printed: 1 pt
* (Question 1) File created and submitted with notebook: 1 pt
* (Question 2) Correct polarity reported: 1 pt
* (Question 2) Question answered thoughtfully: 1 pt
* (Question 3) Function defined as specified: 1 pt
* (Question 3) Song lyrics retrieved and stored in separate files (0.5 pts/song): 2 pts
* (Question 4) Polarity scores printed (with appropriate label containing song title, .25 pts/song): 1 pt
* (Question 4) Questions answered thoughtfully: 2 pts

---
# Sentiment Analysis of Edgar Allan Poe's Poetry
## Features

*   **API Integration**: Fetches poem titles and lyrics from the poetrydb.org public API.
*   **File I/O**: Saves downloaded poems to local text files for repeatable analysis.
*   **Lexicon-Based Sentiment Analysis**: Uses `spaCy` and the `spacytextblob` extension to calculate polarity and subjectivity scores based on word dictionaries.
*   **Transformer-Based Sentiment Analysis**: Employs a sophisticated, context-aware model from Hugging Face (`transformers`) to provide more nuanced sentiment labels (`POSITIVE`/`NEGATIVE`) and confidence scores.
*   **Comparative Analysis**: Demonstrates the strengths and weaknesses of both lexicon and transformer models, particularly on text with complex or conflicting emotions (e.g., "The Bells").
*   **Data Handling & Visualization**: Leverages `pandas` to structure the analysis results and `matplotlib`/`seaborn` to create clear, comparative bar charts of the sentiment scores.

## Technologies Used

*   **Language**: Python 3
*   **Environment**: Jupyter Notebook
*   **Core Libraries**:
    *   `requests`: For making HTTP requests to the API.
    *   `pandas`: For data manipulation and aggregation.
    *   `matplotlib` & `seaborn`: For data visualization.
*   **NLP Libraries**:
    *   `spaCy`: For foundational NLP processing.
    *   `spacytextblob`: For lexicon-based sentiment analysis.
    *   `transformers` (Hugging Face): For advanced, context-aware sentiment analysis.
    *   `torch`: As a backend for the `transformers` library.

## Setup and Installation

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/matthewpblock/json-sentiment.git
    cd json-sentiment
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    # For Windows
    python -m venv .venv
    .\.venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install the required packages:**
The repository contains a requirements.txt for dependency installation.

## How to Run

1.  Launch Jupyter Notebook or JupyterLab from your terminal:
    ```bash
    jupyter notebook
    ```
2.  Open the `requests-json-nlp.ipynb` file.
3.  Run the cells sequentially from top to bottom to see the entire workflow, from data fetching to final visualization. The notebook is designed to be self-contained and will create a `poe_poems/` directory to store the downloaded poem files.