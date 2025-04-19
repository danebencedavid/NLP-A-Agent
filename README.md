# 🦠 COVID-19 Research Agent 
*A QA Agent answering COVID-19, smoking, and diabetes related questions using **graph-powered** semantic search.*

The first attempt is located in the main.ipynb, but another notebook file will be uploaded with a different approach.

## 🔍 Overview  
🧠 **AI Agent** that:  
- 🔎 Finds relevant papers via **semantic search** (abstracts/keywords).  
- 🌐 Expands results using a **Neo4j graph DB** (citations/authors/keywords).  
- ❓ Answers questions like:  
  > *"How does smoking affect COVID-19 mortality in patients with diabetes?"*  

## 📌 Progress  
✅ **Done**:  
- [x] Getting the data (CORD19 `metadata.csv`)
- [x] Defining core terms for:
  - **`smoking OR tobacco`**  
  - **`COVID-19 OR SARS-CoV-2`**
  - **`diabetes`**
- [x] Embedding core terms, and paper abstracts using [`BioBert v1.1`](https://huggingface.co/dmis-lab/biobert-v1.1)
- [x] Calculate cosine similarities between abstract embeddings and core term embeddings
    

⏳ **In Progress**: 
- [ ] Filtering papers matching:  
  - **`smoking OR tobacco`**  
  - **`COVID-19 OR SARS-CoV-2`**
  - **`diabetes`**
- [ ] Preprocess for Graph DB
- [ ] Expanding the CORD19 dataset with papers that might match the 3 keyword criteria using [`SemanticScholarReader`](https://github.com/run-llama/llama_index/tree/main/llama-index-integrations/readers/llama-index-readers-semanticscholar)
- [ ] Design Graph DB Schema
   - **`Nodes`**
     - **`Paper`**
     - **`Author`**
     - **`Keyword`**
     - **`Institution`**  
   - **`Relationships`**
     - **`Paper-CITES->Paper`**
     - **`Paper-HAS_KEYWORD->Keyword`**
     - **`Author-WROTE->Paper`**
     - **`Author-AFFILIATED_WITH->Institution`**
- [ ] Populate DB
- [ ] Graph-Powered Semantic Search
- [ ] QA System Integration
- [ ] Trend Analysis
    - Detecting emerging topics and subtopics
    - Sentiment analysis of the topics surrounding the keywords
    - Identifying high-impact papers
    > *Tracking how keywords, topics, or research focus areas evolve in CORD19 dataset over time*

📌[Preview main.ipynb](https://nbviewer.org/github/danebencedavid/NLP-A-Agent/blob/master/main.ipynb)
📌[Preview nlp-agent.ipynb](https://nbviewer.org/github/danebencedavid/NLP-A-Agent/blob/master/npl_agent.ipynb)








