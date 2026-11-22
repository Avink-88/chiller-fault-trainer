# 04｜Git 與 GitHub 入門

## 它們是什麼？

| 名稱 | 是什麼 | 比喻 |
|---|---|---|
| **Git** | 裝在你電腦上的軟體，幫專案記錄**每一次修改** | 維修紀錄簿：每次改了什麼、什麼時候改的，都記下來 |
| **GitHub** | 網站（github.com），把你的專案**存在雲端** | 把維修紀錄簿影印一份，放在雲端保管 |
| **GitHub Pages** | GitHub 的免費網頁空間 | 讓學生直接用網址打開遊戲 |
| **commit（提交）** | 存一個「版本」 | 在紀錄簿寫下一筆紀錄 |
| **push（推送）** | 把電腦上的新版本傳到 GitHub | 把新紀錄同步到雲端 |

## 這個專案的位置

- 電腦：桌面上的 `chiller-fault-trainer` 資料夾（實際位置是 `D:\chiller-fault-trainer`）
- GitHub 與遊戲網址：寫在 [README.md](../README.md) 最上面

## 改完之後，怎麼更新到網路上？

最簡單的方法是**請 Claude 幫你做**：說「幫我把修改推上 GitHub」。

想自己來的話，在專案資料夾打開 PowerShell（在資料夾空白處按 Shift + 右鍵 →「在這裡開啟 PowerShell 視窗」），依序輸入：

```powershell
git add .
```

```powershell
git commit -m "這次改了什麼，例如：答錯改扣 5 分"
```

```powershell
git push
```

1～2 分鐘後，遊戲網址就會更新成新版本。

| 指令 | 意思 |
|---|---|
| `git add .` | 把所有修改放進「準備存檔區」（`.` 代表全部） |
| `git commit -m "說明"` | 存成一個版本，並寫下說明 |
| `git push` | 上傳到 GitHub |
| `git status` | 查看目前有哪些檔案改過、還沒存版本 |
| `git log --oneline` | 列出所有歷史版本 |

## 改壞了怎麼辦？

**還沒 commit**，想放棄這次所有修改，回到上一個版本：

```powershell
git restore index.html
```

**已經 commit 了**：直接請 Claude 幫你「回到之前的某個版本」最安全。

## 小提醒

- 儲存庫是**公開**的，任何人都看得到程式碼，所以**不要把密碼、學生個資放進這個資料夾**。
- GitHub 網站上也能直接編輯檔案（打開檔案 → 右上角鉛筆圖示）。小改文字很方便，但改完要在電腦上執行 `git pull`，把雲端的修改下載回來，兩邊才會一致。
