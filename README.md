\# PDF Deciphering Assistant — RAG Pipeline



\*\*Microsoft–Simplilearn Agentic AI Program | Course 4 End Project\*\*



\## Project Overview



This project implements a Retrieval-Augmented Generation (RAG) pipeline for extracting and retrieving meaningful information from scientific PDF documents.



The system loads PDFs, divides their contents into manageable chunks, converts the chunks into vector embeddings, and stores them in a FAISS vector database. Relevant passages are retrieved through semantic similarity search and supplied to a language model to generate context-grounded answers.



An additional local embedding pipeline was implemented to compare API-based and locally generated embeddings.



\## Technologies Used



\- Python and Jupyter Notebook

\- LangChain

\- PyPDFLoader

\- RecursiveCharacterTextSplitter

\- OpenAI `text-embedding-3-small`

\- FAISS vector database

\- GPT-4.1-mini

\- Sentence Transformers (SBERT)

\- `all-MiniLM-L6-v2`



\## RAG Pipeline Architecture



```text

Scientific PDF Documents

&#x20;         |

&#x20;         v

&#x20;    PDF Loading

&#x20;         |

&#x20;         v

&#x20;   Text Chunking

&#x20;         |

&#x20;         v

&#x20;  OpenAI Embeddings

&#x20;         |

&#x20;         v

&#x20;   FAISS Vector Store

&#x20;         |

&#x20;         v

&#x20;   Semantic Retrieval

&#x20;         |

&#x20;         v

&#x20;     GPT-4.1-mini

&#x20;         |

&#x20;         v

&#x20;  Context-Grounded Answer

```



\## Implementation



\### 1. PDF Loading and Chunking



Scientific PDF documents are loaded using `PyPDFLoader` and divided into text chunks using `RecursiveCharacterTextSplitter`.



\### 2. Embedding Generation



The main pipeline uses OpenAI's `text-embedding-3-small` model to generate 1536-dimensional vector representations of document chunks.



\### 3. Vector Storage



FAISS stores the embeddings and supports efficient similarity-based retrieval.



\### 4. Semantic Retrieval



The system retrieves document passages relevant to a user's query.



\### 5. Answer Generation



GPT-4.1-mini uses retrieved passages as context to generate grounded responses.



\## Additional Extension: Local RAG Pipeline



Beyond the instructor's requirements, an alternative local embedding pipeline was implemented using:



\- SBERT `all-MiniLM-L6-v2`

\- 384-dimensional embeddings

\- FAISS vector storage

\- Local semantic similarity search



This enables semantic retrieval without requiring paid embedding API calls and provides an alternative to the OpenAI embedding pipeline.



\## Project Outputs



The completed notebook contains code and saved execution outputs demonstrating PDF processing, chunking, embedding, semantic retrieval, and answer generation.



The implementation also reports chunking metrics and sample retrieval results.



\## Repository Structure



```text

pdf\_deciphering\_assistant/

├── notebooks/

│   └── pdf\_rag\_capstone.ipynb

├── data/

│   └── (add your own PDF documents)

├── .gitignore

└── README.md

```



The scientific PDF source documents are not redistributed in this repository. Users should supply their own PDF documents in the `data/` directory.



\## Security



API credentials are not included in the repository. Local credentials should be stored in a `.env` file excluded from version control.



\## Academic Context



Developed as a Course-End Project in the Microsoft-associated Simplilearn Agentic AI program.



The project demonstrates document processing, semantic embeddings, vector search, retrieval-augmented generation, and an additional local retrieval implementation.

