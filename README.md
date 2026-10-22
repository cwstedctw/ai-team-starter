# 研究小隊範本（ai-team-starter）

把這個資料夾打開，你的 AI 就變成一個小隊：**領隊**把工作想清楚、寫成紙條，**隊員**照紙條做，領隊再對著原始資料驗收。紙條和每一版成品都留在資料夾裡，事後查得到誰在什麼時候做了什麼。

只用一家 AI 也可以：單人模式由同一個 AI 輪流當領隊和隊員。

## 三步開始

1. **用範本建自己的私人儲存庫**：在 GitHub 這個範本頁按 **Use this template → Create a new repository**，名字取 `my-research-team`，選 **Private**。
   也可以請 AI 助手代勞（電腦要先裝好 `gh` 並登入 GitHub）：
   `gh repo create my-research-team --private --clone --template cwstedctw/ai-team-starter`
2. **抓到電腦上**：請 AI 助手把它 clone 到你的練習資料夾（例如 `AI-workshop`）。
3. **在桌面版打開它**：ChatGPT 桌面版的 Codex，或 Claude 桌面版的 Code，選這個資料夾。AI 會先報到，並印出資料夾的完整路徑。

## 第一個任務

在 AI 助手裡貼：

> 這次用單人模式。請把 material/練習用 裡的虛構訪談做初步編碼：列出 3 到 5 個主題，每個主題附一到兩句原文當證據，並標出你不確定的地方。

然後自己打開這些檔案看：

- `workspace/inbox/`：領隊寫的紙條
- `workspace/outbox/`：隊員交的 `-v1`；有退回紙條的話還有 `-v2`
- `workspace/log.md`：每一棒做了什麼、領隊怎麼驗收
- 從成品複製一句原文證據，到 `material/練習用/虛構訪談-X01.md` 按 Ctrl＋F（Mac：Command＋F）貼上：找得到嗎？

`.md` 檔按兩下打不開或開得很怪：對檔案按右鍵 → 開啟檔案 → 記事本（Mac：右鍵 → 打開方式 → 文字編輯）。

## 三種模式

| 模式 | 需要什麼 | 適合 |
|---|---|---|
| 單人 | 一家 AI 的桌面版 | 只買得起一家；最常用 |
| 手動接力 | 兩家桌面版都打開這個資料夾 | 想看兩家怎麼分工，每一棒由你傳 |
| 自動接力 | 兩家的命令列工具 `codex`、`claude` 都裝好、登入 | 想讓領隊自己叫隊員；你只跟領隊說話 |

模式寫在 `team.md`，開工時講一句也可以臨時換。規則全寫在 `AGENTS.md`。

## 換成自己的材料

先把 `material/練習用/` 移走，再把材料放進 `material/`（先另存成 `.txt` 或 `.md`）。研究資料能不能放、要符合哪四個條件，看 `material/README.md`：**Private 不等於可以放受試者資料。**

## 換電腦也一樣

這個資料夾推上 GitHub 後，辦公室、家裡、筆電 clone 下來都是同一份。規則只有一條：**開工先拉（pull），做完就推（push）。**

## 檔案一覽

```
AGENTS.md            小隊公約（Codex 讀這份）
CLAUDE.md            一行 @AGENTS.md（Claude 讀這份，等於照同一份公約）
team.md              用哪一種模式
roles/leader.md      領隊的個性與原則
roles/member.md      隊員的個性與原則
material/            你的材料（公約規定 AI 只讀）；練習用/ 是虛構的
workspace/inbox/     紙條
workspace/outbox/    成品，每一版都留
workspace/log.md     小隊紀錄，每一棒一行
```
