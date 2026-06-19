# Build a Semantic Book Recommender with LLMs – Full Course

This repo contains all of the code to complete the freeCodeCamp course, "Build a Semantic Book Recommender with LLMs – Full Course". There are five components to this tutorial:

- Text data cleaning (code in the notebook `data-exploration.ipynb`)
- Semantic (vector) search and how to build a vector database (code in the notebook `vector-search.ipynb`). This allows users to find the most similar books to a natural language query (e.g., "a book about a person seeking revenge").
- Doing text classification using zero-shot classification in LLMs (code in the notebook `text-classification.ipynb`). This allows us to classify the books as "fiction" or "non-fiction", creating a facet that users can filter the books on.
- Doing sentiment analysis using LLMs and extracting the emotions from text (code in the notebook `sentiment-analysis.ipynb`). This will allow users to sort books by their tone, such as how suspenseful, joyful or sad the books are.
- Creating a web application using Gradio for users to get book recommendations (code in the file `gradio-dashboard.py`).

This project was initially created in Python 3.11. In order to run the project, the following dependencies are required:

- [kagglehub](https://pypi.org/project/kagglehub/)
- [pandas](https://pypi.org/project/pandas/)
- [matplotlib](https://pypi.org/project/matplotlib/)
- [seaborn](https://pypi.org/project/seaborn/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)
- [langchain-community](https://pypi.org/project/langchain-community/)
- [langchain-opencv](https://pypi.org/project/langchain-opencv/)
- [langchain-chroma](https://pypi.org/project/langchain-chroma/)
- [transformers](https://pypi.org/project/transformers/)
- [gradio](https://pypi.org/project/gradio/)
- [notebook](https://pypi.org/project/notebook/)
- [ipywidgets](https://pypi.org/project/ipywidgets/)

A requirements.txt file containing all the project dependencies is provided as part of this repo.

This version uses a free, local Hugging Face embedding model (`sentence-transformers/all-MiniLM-L6-v2`) instead of OpenAI's embeddings, so no API key or paid account is required to build the vector database.

The data for this project can be downloaded from Kaggle. Instructions on how to do this are also in the repo.

step by step to run the code:

- 1. Make sure conda is installed.
- 2. Get your project folder ready.
- gradio-dashboard.py
- requirements.txt
- books_with_emotions.csv (output of sentiment-analysis.ipynb)
- tagged_description.txt (output of vector-search.ipynb)
- cover-not-found.jpg
- 4.  Create and activate the conda environment:
- conda create -n book-recommender python=3.11 -y
- conda activate book-recommender
- 5.  Install the dependencies:
- pip install -r requirements.txt
- 6.  Point VS Code at this environment. Press Ctrl+Shift+P → type "Python: Select Interpreter" → pick the one that says book-recommender (it'll show a path with envs/book-recommender in it). This makes sure VS Code's editor/debugger use the right environment, not your system Python.
- 7. Run the dashboard. In the same activated terminal:
- - python gradio-dashboard.py
- Running on local URL: http://127.0.0.1:7860
