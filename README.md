# Samba 管理 Python 腳本
這是用於在 Raspberry Pi 上管理 Samba 服務的 Python 腳本。可以幫助你安裝、啟動、停止 Samba 服務，並操作共享資料夾。若你有多個資料夾需要管理，這個工具將讓你透過命令列輕鬆執行。

---

## 功能介紹
1. 檢查是否已安裝 Samba 服務：程式啟動後，會自動檢查是否已安裝 Samba 服務，並提供安裝選項。
2. 顯示當前共享資料夾：列出系統中當前的 Samba 共享資料夾。
3. 新增/刪除共享資料夾：透過 Python 腳本管理資料夾的共享設定。
4. 啟動/停止 Samba 服務：根據服務狀態，使用者可以選擇啟動或停止 Samba 服務。
5. 查看錯誤日誌：可以查看 Samba 相關的錯誤日誌，幫助排除故障。

---

## 使用說明
1. 安裝
- 在使用此腳本之前，你需要安裝以下套件：
    - python3
    - python3-pip
    - samba 或 samba-common (可在程式中安裝)
    - 安裝必要的套件：

    ```bash
    sudo apt update
    sudo apt install python3 python3-pip
    ```
2. 執行
- 下載並放置 main.py（或者你的腳本名稱），然後使用以下命令運行：

```bash
sudo python3 main.py
```
腳本啟動後，會自動檢查 Samba 服務是否安裝。如果未安裝，會提示用戶選擇是否安裝服務。

3. 選單
- 程式運行後會顯示以下選單：

```bash
=== Samba 管理選單 ===
1. 顯示當前共享資料夾
2. 新增共享資料夾
3. 刪除共享資料夾
4. 啟動/停止 Samba 服務
5. 查看錯誤日誌
0. 離開
```

你可以根據提示，選擇相應的操作。

4. 功能說明

- 顯示當前共享資料夾 (選項 1)
顯示當前已設定的 Samba 共享資料夾。

- 新增共享資料夾 (選項 2)
通過輸入資料夾路徑，將該資料夾加入到 Samba 的共享設定中。

- 刪除共享資料夾 (選項 3)
刪除指定的共享資料夾。

- 啟動/停止 Samba 服務 (選項 4)
根據當前的 Samba 服務狀態來選擇啟動或停止服務。

- 查看錯誤日誌 (選項 5)
查看 Samba 的錯誤日誌，有助於排查問題。

- 離開 (選項 0)
離開腳本，結束程式運行。

---

## 預期結果
在啟動腳本之後，你應該可以根據提示選擇對 Samba 進行操作，包含共享資料夾的增刪、服務的啟動和停止、以及錯誤日誌的查看。

## 日誌系統
腳本運行時會產生日誌記錄。日誌會儲存在my_package/目錄中，並以 samba_manager.log 作為文件名稱。

## 注意事項
請確保你有足夠的權限來操作 Samba 服務，通常需要 root 權限。
本腳本使用 logging 系統來記錄操作過程，若有需要可以查看日誌以檢查服務的狀態。

## 貢獻
如有任何問題或建議，歡迎在 GitHub 上提 Issue，或提交 Pull Request。

## 許可協議
- 這個專案採用 MIT 許可證。

這份 README 範本介紹了專案的目的、安裝流程、使用方式和各功能的詳細描述。你可以根據需要作出進一步調整！