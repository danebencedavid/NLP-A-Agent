# 🦠 COVID-19 Research Agent 
*A QA Agent answering COVID-19, smoking, and [3rd keyword] questions using **graph-powered** semantic search.* 

## 🔍 Overview  
🧠 **AI Agent** that:  
- 🔎 Finds relevant papers via **semantic search** (abstracts/keywords).  
- 🌐 Expands results using a **Neo4j graph DB** (citations/authors/keywords).  
- ❓ Answers questions like:  
  > *"How does smoking affect COVID-19 mortality in patients with [3rd keyword]?"*  

## 📌 Progress  
✅ **Done**:  
- [x] Getting the data (CORD19 `metadata.csv`)
- [x] Extracting keywords (using `spaCy`) from paper abstracts

⏳ **In Progress**: 
- [ ] Filtering papers matching:  
  - **`smoking OR tobacco`**  
  - **`COVID-19 OR SARS-CoV-2`**
  - **`3rd keyword`**
- [ ] Preprocess for Graph DB
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

📌[Preview Notebook](https://nbviewer.org/github/danebencedavid/NLP-A-Agent/blob/master/main.ipynb)







