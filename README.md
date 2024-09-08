👨‍💻 Humanly Sculpted, 🤖 AI-Scripted: The Perfect Synergy
### 

# RAG-Retrieval Augmented Generation
## Welcome to the RAG Revolution!


#### RAG Enhancement Repository: Expanding Horizons through Varied Approaches✨
RAG-Retrieval Augmented Generation is at the core of this repository's mission. The collection of Jupyter notebooks is dedicated to enhancing RAG through various approaches and thought processes, aiming to push the boundaries of natural language understanding and generation. 

### Introduction to RAG:

Welcome to the forefront of natural language processing innovation! Retrieval Augmented Generation (RAG) represents a paradigm shift, harnessing the synergy between language models and external knowledge sources to revolutionize text generation. Let's embark on a journey to uncover the transformative power of RAG and explore its endless possibilities.


![image](https://github.com/user-attachments/assets/b8c08eff-888c-458f-a6de-8983d52696d5)

###### Image Source: (https://miro.medium.com/v2/resize:fit:720/format:webp/1*392fzT_PzFtD-wFQlU8ITg.png)

### What is RAG?

Retrieval Augmented Generation (RAG) is not just another acronym in the world of AI; it's a game-changer. Imagine infusing the intelligence of large language models (LLMs) with the vast expanse of external knowledge. RAG achieves precisely that! It seamlessly integrates pre-trained retriever and generator components to produce contextually relevant and accurate responses, setting new standards in natural language understanding and generation.

### Unveiling RAG's Architecture:

RAG is not just a black box; it's a meticulously designed framework comprising several interconnected components. Let's dissect its architecture:

1. **Indexing:** The foundation of RAG lies in indexing. This process involves organizing and encoding vast amounts of text data into a structured index, enabling efficient retrieval of relevant information during the generation phase.


2. **Retrieval:** Here's where the magic happens! RAG retrieves contextually relevant information from the indexed knowledge sources based on user queries. Think of it as a virtual librarian fetching the most pertinent books from a vast library.


3. **Generation:** Armed with the retrieved knowledge, RAG's generator component works its magic, crafting coherent and informed responses that reflect a deep understanding of the input query and the external context retrieved during the retrieval phase.


### Why RAG Matters:
In a world inundated with information, accuracy is paramount. RAG addresses the limitations of traditional LLMs by:

1. **Enhancing Accuracy:** By leveraging external knowledge sources, RAG produces responses grounded in facts, minimizing the risk of generating incorrect or misleading information.

2. **Reducing Hallucinations:** Gone are the days of nonsensical responses! RAG's integration of external knowledge significantly reduces the occurrence of hallucinated or irrelevant outputs.

## Enhancing RAG Performance: 

##  Naive Rag also known as Vanilla Rag : 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

![image](https://github.com/user-attachments/assets/4db4db94-795e-4657-9f07-0c7d6b2f4fac)

###### Image Source : (https://www.clarifai.com/hs-fs/hubfs/rag-query-drawio%20(1)-png-2.png?width=2056&height=1334&name=rag-query-drawio%20(1)-png-2.png)

This code implements a Retrieval Augmented Generation (RAG) pipeline in three main stages:

Indexing: Libraries are imported, and HuggingFace Bge Embeddings are initialized. PDF documents are loaded from the 'Data' directory and split into chunks. These chunks are then indexed using a Chroma vector store with cosine similarity, which is saved for later retrieval.

Retrieval: The vector store is loaded and configured as a retriever to fetch the top 2 relevant chunks based on user queries. This ensures that the most pertinent information is retrieved for response generation.

Generation: A language model is loaded with specific configurations, and a prompt template is defined. The language model and retriever are combined into a RetrievalQA chain to generate responses based on the retrieved context. A sample query demonstrates the system's ability to produce relevant answers

## Rag using Parent Document Retriever (PC Rag)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

![image](https://github.com/user-attachments/assets/248aaf33-8dcd-4000-a6b6-fe1614a57d0e)

###### Image Source : (https://clusteredbytes.pages.dev/images/parent-retriever/full-ret.png)


This code sets up a Retrieval Augmented Generation (RAG) pipeline using a Parent Document Retriever (PC RAG) approach, organized into three stages. Indexing involves importing libraries, initializing HuggingFace Bge Embeddings, loading PDF documents, extracting unique sources, and splitting documents into large and small chunks. A Chroma vector store and InMemoryStore are created, and a ParentDocumentRetriever is configured to manage document retrieval.

In the Retrieval stage, the vector store and retriever are set up, and documents are added. The big_chunks_retriever fetches relevant documents based on user queries.




###  CRAG

The Generation stage involves loading a language model with CTransformers and defining a PromptTemplate for formatting queries. The PC RAG approach first uses the Parent Document Retriever to handle user queries. The chunks returned by the retriever are then processed by the generate_response function, which creates a base RAG on top of a parent-child RAG framework. This function retrieves, splits, and generates responses using the RetrievalQA chain. A sample query demonstrates the pipeline’s ability to produce relevant answers.

