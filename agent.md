呢度為你將「Chapter 3: Building AI Agents（建立 AI 代理）」嘅內容
---

## 1. 乜嘢係 AI Agents (AI 代理)？

AI Agent 係一啲**以生成式 AI 為基礎**嘅軟件應用程式。佢哋同一般就咁對答嘅 Chatbot 唔同，佢哋有以下特點：

* **用自然語言去推理：** 佢哋識得像人類咁用日常語言去思考同推理解決問題嘅方法。
* **利用工具自動化：** 佢哋識得自己搵工具去幫手完成工作。
* **多步驟、目標導向：** 你俾一個最終目標佢，佢會自己分拆成幾個步驟（Workflow），一步步去塞完成。

### 🤖 AI Agent 嘅三大核心支柱 (Core Components)

一個完整嘅 AI Agent 由呢三樣嘢組成：

1. **Model (模型/大腦)：** 負責語言理解同推理嘅生成式 AI。
2. **Instructions (指令/角色)：** 亦即係 System Prompt（系統提示詞），用嚟定義呢個 Agent 嘅身份、行為守則、語氣同限制。
3. **Tools (工具/行動)：** 賦予 Agent 同外界互動、創作或者做出改變嘅能力（例如：上網、寫檔案）。

---

## 2. Microsoft Foundry Tools (工具庫管理)

喺 Microsoft Foundry 入面有一個 **Tool Catalog (工具目錄)**，佢就好似一個工具箱，等不同嘅 Agent 可以集中喺度搜尋同埋調用需要嘅工具：

* **Knowledge Tools (知識工具)：** 俾 Agent 接通外圍資訊（例如：網頁搜尋引擎、文檔數據庫）。
* **Action Tools (行動工具)：** 等 Agent 可以真正幫你做嘢（例如：寄 Email、寫 Calendar/行事曆、Call API）。

---

## 3. Retrieval-Augmented Generation (RAG / 檢索增強生成)

RAG 係一種**幫 Prompt（提示詞）增加背景資料**嘅技術，令到 AI 可以回答一啲佢原本喺 Training（訓練）階段未學過嘅特定數據。

### 🔄 RAG 嘅運作流程：

1. **User Query (用戶查詢)：** 你問 Agent 一個問題。
2. **Search Index (搜尋索引)：** Agent 收到問題後，先去數據庫/文件入面搜尋相關資料。
3. **Retrieved Context (獲取背景資料)：** 搵到相關嘅有用資料。
4. **Augmented Prompt (增強提示詞)：** 系統將你原本嘅問題，加上啱啱搵到嘅資料，打包成一個更詳細嘅新 Prompt。
5. **Model Response (模型回覆)：** AI 睇完呢堆新資料之後，給予你一個準確嘅答案。

### 🎯 點解要用 Knowledge Tools？(Grounding 同準確度)

* **Domain Specificity (領域專一性)：** 強迫 AI 必須根據你俾嘅「授權數據」去答，防止 AI 講大話、胡言亂語（Hallucinations）。
* **Traceability (可追溯性)：** RAG 生成嘅答案會附帶引用來源（例如「來源：HR_Policy.pdf」），令 AI 嘅諗法清清楚楚。
* **Trust (信任度)：** 有咗 Source，人類用家就可以自己去 Verify（核實）個答案，用得更安心。

### 🧠 Microsoft Foundry IQ 嘅優勢

* **Central Connection (中央連接)：** 佢係一個多源知識層，幫 Agent 一口氣駁通 SharePoint、Azure Storage 或者網頁數據。
* **Agentic Retrieval (智能檢索)：** Foundry IQ 會自動幫你做「Chunking（文件切片/分段）」同埋「Vector Embeddings（向量化）」，唔洗你自己寫 Code 處理。
* **Efficiency (高效能)：** 喺 Foundry IQ 起好一個知識庫之後，可以同時分享俾多個不同嘅 Agent 用，唔洗重複寫 Code。

---

## 4. Multi-Agent Systems (多代理系統)

* **Specialization (專業分工)：** 唔再係靠一個 Agent 做晒所有嘢，而是由多個**專門化**嘅 Agent 一齊分工合作。
* **Workflows (工作流)：** 例如：第一個 Agent 負責搵 Raw Data（原始數據），第二個 Agent 做 Technical Analysis（技術分析），第三個 Agent 就負責將結果寫成最終報告。
* **Communication (互相溝通)：** 呢啲 Agent 之間會互相傳遞 Prompt 嚟溝通同交接任務，成個過程就好似一班真人 Teamwork 咁。

### 🔌 Model Context Protocol (MCP / 模型上下文協議)

* **Universal Adapter (通用適配器)：** 佢係一個開放標準，定義咗 Agent 應該點樣駁去外圍工具同數據。
* **Separation of Concerns (關注點分離)：** * **MCP Client (Agent/客端)：** 負責發出請求（Request）。
* **MCP Server (Service/伺服端)：** 負責真正執行嗰個功能（Capability）並交還結果。


* **Managed Services (託管服務)：** 例如 Azure Language MCP server，佢可以將一啲 NLP 工具（好似 PII Redaction ── 自動拿走身份證/電話等個人私隱資料嘅功能）以標準化嘅方式提供給 Agent 使用。

---

## 5. Project API (開發與整合)

當你想將整好嘅 Agent 放落自己嘅 App 嗰陣，就會用到呢啲：

* **Foundry Projects SDK：** 俾工程師用 Python 等程式語言，寫 Code 去駁通 Project 同埋呼叫（Call）啲 Agent。
* **Project API：** 等你大規模咁將 AI Agent 整合落去網頁（Web apps）、Chatbots 或者 Backend（後端）嘅自動化 Workflow。
* **Agent-ID：** 喺 Playground 介面度可以搵到嘅一串獨一無二嘅 ID。你喺寫 Program 嗰陣，就係靠呢個 ID 去指明要叫醒邊一隻你 Config（設定）好嘅 Agent 幫手。

---

呢個章節嘅核心概念就係：**「點樣利用 Model、Role、Tools 組成智能代理，並透過多代理（Multi-agent）同埋 RAG 技術，令 AI 變身成一個識得幫手返工、處理複雜任務嘅團隊。」**
