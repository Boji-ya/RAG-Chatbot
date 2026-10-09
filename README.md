## 基於 RAG 的資工系資訊查詢聊天機器人，提供系所資訊的智慧化檢索與問答
**專案簡介**

本專案使用 RAG 架構，建立嘉義大學資訊工程學系資訊查詢機器人。使用者可透過自然語言提問，系統會從系所 PDF 文件中檢索相關資訊，再由大型語言模型生成回答，提升資訊查詢的便利性。

**使用技術**

程式語言： Python

RAG 框架： LangChain

大型語言模型： Gemini 3.5 Flash

Embedding 模型： Gemini Embedding

向量資料庫： Chroma

文件處理： PyPDFLoader、RecursiveCharacterTextSplitter

介面開發： Gradio

**系統流程**

PDF 文件載入 → 文字切分 → Embedding 向量化 → Chroma 向量檢索 → RetrievalQA → Gemini 生成回答 → Gradio 顯示結果

**主要功能**

讀取並處理系所 PDF 文件

透過向量檢索取得與問題相關的文件內容

結合大型語言模型生成自然語言回答

使用 Gradio 提供網頁問答介面

透過 MD5 Hash 判斷 PDF 是否更新，避免未變更時重複建立向量資料庫

**執行環境**

本專案使用 Google Colab 執行。執行前需準備系所資訊 PDF 文件，並設定 Google Gemini API Key。

