# Super Nova - NLP-powered News Discovery Engine

Super Nova is an advanced, NLP-powered news discovery engine that allows users to quickly and efficiently find relevant news articles, summarize lengthy texts, and get real-time suggestions. By leveraging Natural Language Processing (NLP) techniques, Super Nova enhances information retrieval and summarization from large collections of online news, making it easier for users to stay informed with concise summaries and ranked results.

## Key Features

- **Web Scraping & Content Extraction**: Automatically extracts headlines, URLs, and article content from various news websites using `BeautifulSoup`.
- **NLP Techniques**: Uses Named Entity Recognition (NER), RAKE for keyword extraction, and word embeddings (GloVe) to improve search relevance and document ranking.
- **Cosine Similarity**: Ranks news articles based on their similarity to the user’s search query using cosine similarity on document embeddings.
- **Text Summarization**: Summarizes top-ranked news articles using transformer models (e.g., BART) for a quick understanding of long texts.
- **Auto-Suggestion & Spellcheck**: Offers real-time word suggestions based on n-grams and corrects user input using the Levenshtein Distance algorithm.
- **User Interface**: A simple, intuitive web interface built using `Gradio` that allows users to search, receive suggestions, and explore ranked and summarized news.

## Installation

To install the necessary dependencies, use the following commands:

```bash
pip install gradio
pip install rake_nltk
pip install sentence_transformers
pip install webdriver_manager
pip install python-Levenshtein
pip install spacy
pip install transformers
python -m spacy download en_core_web_sm
```

## How It Works

1. **Web Scraping**: The engine scrapes news websites like NDTV and Al Jazeera for the latest headlines and article content.
2. **Query Processing**: User input is tokenized and processed into word embeddings using pre-trained GloVe vectors.
3. **Document Ranking**: Articles are ranked by cosine similarity to the query, selecting the most relevant news pieces.
4. **Summarization**: Summarizes the top 5 articles using transformer-based models for easy consumption.
5. **Real-Time Suggestions**: As users type, next-word predictions and spelling corrections are provided.

## Workflow

1. **Web Scraping**: Fetches news headlines, URLs, and article content.
2. **Query Handling**: Processes the user’s query, ranks documents based on similarity, and provides top summaries.
3. **Real-Time Suggestions**: Offers auto-suggestions and spellchecks for improved search accuracy.
4. **Summarization**: Provides concise summaries of the top-ranked articles.

## Future Enhancements

- **Multilingual Support**: Incorporating support for multiple languages in both queries and articles.
- **Real-Time Updates**: Implementing live scraping for the most up-to-date content.
- **User Personalization**: Adding personalized search results based on user behavior and preferences.

## Usage

You can launch the application using Gradio:

```python
import gradio as gr

# Define your functions (e.g., for search, suggestions, etc.)
def search_news(query):
    # Call the search engine to fetch and display results
    pass

demo = gr.Interface(
    fn=search_news, 
    inputs="text", 
    outputs="dataframe", 
    live=True
)

demo.launch()
```

## Contributors

- **Ritwika Das Gupta (2348049)**
- **Soham Chatterjee (2348062)**
- **Sayantan Ray (2348057)**
- **Guided by Dr. Saleema J S**

## License

This project is licensed under the MIT License.

---

Stay informed, stay ahead with **Super Nova**!

---

**References**:
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/)
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [GloVe Embeddings](https://nlp.stanford.edu/projects/glove/)【5†source】【6†source】.
