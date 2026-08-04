# Historical Medical Text Explorer



## Overview



Historical Medical Text Explorer is a Retrieval-Augmented Generation (RAG) application for exploring historical medical literature using modern Natural Language Processing techniques.



The project uses Nicholas Culpeper's *The Complete Herbal* (Project Gutenberg edition) as its initial corpus. Instead of performing simple keyword searches, it retrieves passages based on semantic similarity using Sentence Transformers and FAISS, then summarizes and answers user questions using pre-trained transformer models.



---



## Main Application

The final application is contained in:

`main.ipynb`

The notebook is designed to run in Google Colab.



---



## Features



- Upload a historical medical text

- Automatic text cleaning

- Hybrid chunking strategy

  - Semantic chunking for herb descriptions

  - Fixed-size overlapping chunking for pharmaceutical recipes

- Semantic embeddings using Sentence Transformers

- Vector similarity search with FAISS

- Automatic summarization using BART

- Question answering using FLAN-T5

- Displays retrieved historical source passages



---



## Technologies Used



- Python

- Google Colab

- Sentence Transformers

- Hugging Face Transformers

- FAISS

- NumPy

- Regular Expressions



---



## Project Workflow



Historical text



↓



Cleaning



↓



Hybrid Chunking



↓



Sentence Transformer



↓



Embeddings



↓



FAISS Index



↓



Semantic Retrieval



↓



Summarization



↓



Question Answering



---



## Installation



Install the required libraries:



```bash

pip install transformers==4.41.2 \

sentence-transformers==2.7.0 \

accelerate==0.30.1 \

peft==0.11.1 \

sentencepiece \

faiss-cpu
```



---

## Usage


1. Upload The Complete Herbal (Project Gutenberg edition).
2. Run the notebook.
3. Enter a plant name (for example: garlic, rosemary, violet) or question, such as "What does Culpeper say about garlic?"
4. The system:
   - retrieves the most relevant historical passages,
   - summarizes them,
   - answers the user's question,
   - displays the source passages.



---



## Challenges



Several challenges were encountered during development:



* Preserving the original structure of the historical text.
* Designing a hybrid chunking strategy appropriate for different sections of the book.
* Managing transformer token limits.
* Combining semantic retrieval with hierarchical summarization.
* Producing focused answers from retrieved historical passages.



---



## Future Improvements



* Support multiple historical medical texts.
* Search across multilingual corpora.
* Interactive Streamlit interface.
* Named Entity Recognition for medicinal plants and diseases.
* Interactive co-occurrence network visualization.
* Comparison of treatments across different historical authors.
* OCR support for historical manuscripts.



---



## Ethical Considerations



This application is intended exclusively for historical research and educational purposes.



The generated summaries and answers describe historical medical knowledge and must **not** be interpreted as modern medical advice.



---



## Contributing



Suggestions and improvements are welcome.



Please fork the repository, make your changes, and submit a pull request.



---



## License


The original code in this project is released under the MIT License.


The MIT License applies only to the original software and code in this
repository. It does not apply to third-party source materials.


Nicholas Culpeper's *The Complete Herbal* is a historical public-domain work.
The electronic text used in this project was obtained from Project Gutenberg;
users should consult Project Gutenberg's terms for the use and distribution
of its electronic texts.
