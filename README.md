# AI CUP 2024 玉山人工智慧公開挑戰賽－RAG與LLM在金融問答的應用

**專案結構**
```
./
├── ai_cup_2024/ # Chroma database
├── documents/
│   ├── faq.json # FAQ documents
│   ├── finance.json #Finance documents
│   ├── insurance.json # Insurance documents
├── finance_markdown/ # finance資料集
├── insurance_markdown/ # insurance資料集
├── Model/
│   └── llm_generate.py # LLM進行預測的程式
├── Preprocess/
│   ├── build_json.py # 資料集前處理及建立document json
│   └── indexing.py # 建立向量資料庫
├── final_pred.json
├── ground_truths_example.json #測試題目的答案
├── pid_map_content.json #FAQ資料集
├── questions_example.json # 測試題目
├── README.md
└── requirements.txt
```
## 使用環境與安裝
- 作業系統: Linux
- Python版本: 3.8.10
- 請先安裝相依套件與下載資料集:
    ```
    pip install -r requirements.txt
    ```
- 資料集下載連結: [Google Drive 資料夾](https://drive.google.com/drive/u/0/folders/1ldEWRbzwjKm6Q3_dyoq8YIJRfygjiNFl)

### 模型資訊
本專案所使用的模型如下：
- **Embeddings 模型**: jinaai/jina-embeddings-v3
- **Rerank 模型**: jinaai/jina-reranker-v2-base-multilingual
- **LLM**: kenneth85/llama-3-taiwan:latest
## 執行順序
請依照以下順序執行各程式，以完成整個流程：
1. build_json.py 
1. indexing.py
1. llm_generate.py
