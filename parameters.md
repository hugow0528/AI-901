# Parameters of a model 

### 1. Max Response / Max Tokens (最大生成長度)

* **English:** Controls the maximum length of the generated text by setting a hard limit on tokens.
* **Cantonese (廣東話):** 控制生成文字嘅最大長度。你可以設定一個上限（Token數量），費事佢寫得太長。如果寫得太少，AI 可能會講講吓變咗「爛尾」斷咗。

### 2. Temperature (溫度)

* **English:** Controls the **randomness and creativity** of the output (not verbosity). Low temperature = predictable/factual; high temperature = creative/diverse.
* **Cantonese (廣東話):** 控制 AI 嘅**隨機同埋創意度**（而唔係字數多寡）。溫度低（例如 0.2），AI 就會好正經、老實同埋死板；溫度高（例如 0.9），AI 就會好天馬行空、有創意，每次俾嘅答案都唔同。

### 3. Stop Sequence (停止序列)

* **English:** Tells the model to immediately stop generating text once a specific character or word appears.
* **Cantonese (廣東話):** 話俾 AI 知一見到某個特定嘅字或者符號（例如 `[END]` 或者換行），就要即刻收口停低，唔好再寫落去。

### 4. Presence Penalty (存在懲罰)

* **English:** Discourages the model from repeating topics/words that have already appeared, encouraging it to introduce new subjects.
* **Cantonese (廣東話):** 只要某個字或者話題出現過一次，AI 就會被扣分。呢個參數可以迫使 AI 講多啲**新話題**，而唔係兜圈子。

### 5. Past Messages Included (包含歷史訊息 / 記憶範圍)

* **English:** Controls the short-term context window by deciding how many previous messages are resent to the AI so it remembers the ongoing conversation.
* **Cantonese (廣東話):** 控制 AI 嘅**短期記憶**。每一次你同 AI 對話，系統其實會將你之前講過嘅舊對話一齊打包傳送返過去。呢個參數決定咗打包幾多條舊訊息，等 AI 可以記住上文下理。

---

Which of these parameters are you looking to adjust for your workflow or project?
你打算喺你嘅項目或者工作入面調校邊一個參數先？
