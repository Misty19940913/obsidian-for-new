---
type: course-chapter
status: draft
tags: [obsidian, 入門, 第六階段]
time_created: 2026-01-01
time_modified: 2026-05-28
chapter: N.Ch06
difficulty: ★★☆
estimated_time: 60分鐘
prerequisites: N.Ch01
description: |
  同步與備份是新手最容易忽略、但一旦出問題就後悔莫及的環節。
  本章用「備份健康檢查」取代教課書式說明，5 個問題讓你立即知道自己的風險狀態。
---

# N.Ch06｜同步與備份：保護你的第二大腦

> [!info]+ 這章結束時你會做到的事
> 1. 用「備份健康檢查」確認目前的風險等級
> 2. 知道不同同步方案的適用情境
> 3. 設定好之後不再為備份困擾

---

## ⚠️ 備份健康檢查（做這 5 題）

回答每一題。如果你有任何一題答「否」，**現在立刻修正**。

**問題 1：Vault 在雲端同步資料夾裡嗎？**
- Windows：OneDrive / Dropbox
- macOS：iCloud / Dropbox
- Linux：Syncthing
- **回答「否」 → 立刻把 vault 移到雲端資料夾**

**問題 2：有沒有「電腦壞了」的後備方案？**
裸機故障（硬碟壞掉）：本地備份不夠，需要雲端或外接硬碟。
- **沒有第二份 → 設定每日自動備份到雲端**


**問題 5：行動裝置有讀取 vault 的能力嗎？**
iOS / Android 用 Obsidian app。
- **需要嗎？ → vault 在 iCloud Drive（iOS）或 OneDrive（Android）**

---

> [!danger]+ 一個真實案例
> 有人的 vault 只存在電腦硬碟，結果 SSD 掛了，兩年份的筆記全部報銷。
> 備份不是選項，是基本責任。

---

## 五種同步方案比較

| 方案 | 優點 | 缺點 | 適合誰 |
|------|------|------|--------|
| **Obsidian Sync** | 原生整合、穩定 | 需付費（約 $8/月） | 不想折騰的用戶 |
| **iCloud Drive** | macOS 原生 | 跨平台麻煩 | macOS 專用 |
| **堅果雲** | 中國可用、免費配額 | 對大檔案不友善 | 中國用戶 |
| **Syncthing** | 完全免費、P2P | 需技術設定 | 自架同步需求 |

**多數人推薦：** Obsidian Sync（付費省心）或雲端硬碟如 iCloud/OneDrive（免費）。

---



## 災難復原：真的出事怎麼辦

| 情境 | 怎麼救 |
|------|--------|
| 誤刪一篇筆記 | 核心外掛「檔案復原 (File recovery)」 → 查看快照 |
| 整個 vault 損壞 | 從 OneDrive / iCloud / 本地備份 恢復最新備份 |

---

## 驗證：你做到了嗎？

- [ ] Vault 在雲端同步資料夾（OneDrive / iCloud / Dropbox）
- [ ] 有第二份備份（GitHub 或外接硬碟）
- [ ] 行動裝置可以讀取 vault（如需行動端）

---

## 下一步

→ [[N.Ch07|第七章：接入 AI 大模型]]

> [!note]+ 加入我們的 LINE 群
> 曾經資料丟失的人，都在這裡。
