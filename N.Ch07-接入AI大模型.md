---
type: course-chapter
status: draft
tags: [obsidian, 入門, 第七階段]
time_created: 2026-01-01
time_modified: 2026-05-28
chapter: N.Ch07
difficulty: ★★★
estimated_time: 90分鐘
prerequisites: N.Ch05
description: |
  Obsidian + AI = 你的第二大腦有了思考能力。
  本章涵蓋 Copilot 實戰設定、本地模型（Ollama）設定，並附「選擇 AI 的實務考量」，
  讓你在速度/價格/隱私之間做出適合自己的選擇。
---

# N.Ch07｜接入 AI 大模型：實戰設定

> [!info]+ 這章結束時你會做到的事
> 1. 能讓 Copilot 正常運作並回答關於你的筆記的問題
> 2. 理解本地模型 vs API 模型的使用情境
> 3. 知道該把什麼資料交給 AI、什麼資料不該給 AI

---

## AI 能幫你做什麼？

在 Obsidian 裡接入 AI 不是炫技，是實用工具：

| 用途 | 例子 |
|------|------|
| **筆記摘要** | 「這篇 5000 字讀書筆記，主要在講什麼？」 |
| **知識庫問答** | 「我在 `#目標` 下的筆記中設定了哪些目標？」 |
| **寫作輔助** | 潤色、改進方向建議 |
| **連結發現** | 「你 3 月提到『習慣』，和現在這篇『動機』有很強關聯」 |
| **批量生成** | 「根據過去 30 天日誌，生成一份月報」 |

---

## 方案比一比：選哪個 AI 方案

| 方案 | 費用 | 速度 | 隱私 | 適合誰 |
|------|------|------|------|--------|
| **OpenAI GPT-4** | $0.01-0.03/次 | 快 | 資料送出外部 | 多數人 |
| **Anthropic Claude** | $0.003-0.015/次 | 快 | 資料送出外部 | 性價比更高 |
| **本地 Ollama** | 免費 | 取決於顯卡 | 完全在本地 | 有 8GB+ 顯存者 |
| **Copilot Plus** | 免費（已訂閱 Microsoft 365）| 快 | 資料送出外部 | 已有 Microsoft 365 的人 |

**新手推薦：** Copilot（支援 GPT-4 / Claude，設定最簡單）

---

## 方案一：Copilot（推薦新手）

### 設定步驟

1. 安裝 `Copilot` 插件
2. 取得 OpenAI API Key（[platform.openai.com](https://platform.openai.com)） 或 Anthropic API Key
3. `設定` → `Copilot` → 填入 API Key
4. 選擇預設模型（建議从 GPT-4o 或 Claude 3.5 Sonnet 開始）
5. 開始使用

### 實戰用法

**對話模式：** 在任意筆記，按 `Ctrl + Shift + C` 喚起 Copilot。

```
User : 請用一句話總結這篇筆記的重點
AI   : 這篇筆記的核心是「習慣的養成取決於頻率而非時間」
```

**針對特定筆記提問：**
```
User : [[原子習慣]] 這本書中，習慣迴圈的四要素是什麼？
AI   : 習慣迴圈的四個要素：
       1. 提示（Cue）：觸發行為的信號
       2. 渴求（Craving）：行為背後的動機
       3. 回應（Response）：執行的實際動作
       4. 獎賞（Reward）：行為帶來的收穫
```

---

## 方案二：本地模型（Ollama）

適合**家中有高效能電腦、重視隱私**的人。

### 設定步驟

**步驟 1：安裝 Ollama**
```bash
# macOS / Linux
curl -fsSL https://ollama.com/install.sh | sh

# Windows: 從 ollama.com 下載安裝包
```

**步驟 2：下載模型**
```bash
ollama pull llama3.2
ollama pull nomic-embed-text  # 嵌入模型
```

**步驟 3：在 Obsidian 設定**
1. 安裝 `Local AI` 插件
2. 設定 Ollama URL：`http://localhost:11434`
3. 選擇本地模型

---

## ⚠️ 隱私紅線：這些資料不給 AI

> [!warning]+ 重要原則
> **不要讓 AI 處理你有保密義務的資料。**
>
> - 商業機密（產品策略、内部代碼）
> - 個人密碼、帳戶資訊
> - 員工或客戶的私人資料
> - 機密文件、内部會議記錄

---

## 測試提示詞：確認串接成功

用這三個問題測試 AI 是否正常運作：

```
1. 「你是誰？你能看到我目前的筆記內容嗎？」
2. 「我建立了哪些標籤？」  
3. 「這篇筆記和哪些筆記有連結？」【打開任一筆記後提問】
```

---

## 插件組合推薦

| 等級 | 組合 |
|------|------|
| **初學者** | Copilot（日常對話） + Templater（格式化 AI 輸出） |
| **中級** | Copilot（日常） + Local AI（隱私敏感） + Dataview（知識庫查詢） |
| **進階** | Ollama（本地） + Copilot（切換本地/雲端） + Dataview + Obsidian Git |

---

## 驗證：你做到了嗎？

- [ ] Copilot 已安裝並成功回覆第一個問題
- [ ] 能讓 AI 針對某篇特定筆記回答問題
- [ ] 知道什麼資料不該給 AI 處理
- [ ] 如果需要隱私，能切換到本地模型（Ollama）模式

---

## 下一步

→ [[N.Ch08|第八章：快速參考]]

> [!tip]+ 學完這章，你終於可以開始構建真正的第二大腦
> 加入 LINE 群，領取「與 AI 對話模板」。
