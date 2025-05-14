# 🦠 COVID-19 Research Agent 
*A QA Agent answering COVID-19, smoking, and diabetes related questions using **graph-powered** semantic search.*

The first attempt is located in the main.ipynb, but another notebook file is uploaded with a different approach.

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
- [x] Embedding core terms, and paper abstracts
- [x] Calculate cosine similarities between abstract embeddings and core term embeddings
- [x] Filtering papers matching:  
  - **`smoking OR tobacco`**  
  - **`COVID-19 OR SARS-CoV-2`**
  - **`diabetes`**
- [x] Preprocess for Graph DB
- [x] Expanding the CORD19 dataset with papers that might match the 3 keyword criteria using [`SemanticScholarReader`](https://github.com/run-llama/llama_index/tree/main/llama-index-integrations/readers/llama-index-readers-semanticscholar)
- [x] Design Graph DB Schema
   - **`Nodes`**
     - **`Paper`**
     - **`Author`**
     - **`Keyword`**
     - **`Institution`**  
   - **`Relationships`**
     - **`Paper-CITES->Paper`**
     - **`Paper-HAS_KEYWORD->Keyword`**
     - **`Author-WROTE->Paper`**

⏳ **In Progress**:

- [ ] Populate DB
- [ ] Graph-Powered Semantic Search
- [ ] QA System Integration

📌[Preview embs.ipynb](https://nbviewer.org/github/danebencedavid/NLP-A-Agent/blob/master/embs.ipynb)
📌[Embedding vector visualization](https://projector.tensorflow.org/?config=https://gist.githubusercontent.com/danebencedavid/3539ae71665798e4f64ce6f1f52049ec/raw/a06f9f2c20ca1fab00b4940d2f979375163ac3d1/config.json)
📌[Preview agent.ipynb](https://nbviewer.org/github/danebencedavid/NLP-A-Agent/blob/master/agent.ipynb)










