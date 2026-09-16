# cjonline 公司專案組態檔案維護專案

本專案主要用於管理與維護 **cjonline 公司專案**的核心網路與系統組態檔案，確保內部主機設定與網路連線配置的正確性與同步。

---

## 👥 專案資訊

* **專案負責人：** XXX
* **聯絡信箱：** [test@gmail.com](mailto:test@gmail.com)

---

## 📂 維護檔案清單

本專案目前包含並管理以下關鍵組態檔案：

### 1. `hosts` 檔案
* **用途：** 管理本機主機名稱與 IP 位址的對應關係（DNS 靜態解析）。
* **常見路徑：** 
  * Linux / macOS: `/etc/hosts`
  * Windows: `C:\Windows\System32\drivers\etc\hosts`
* **維護重點：** 確保公司內部測試環境與正式環境的域名（Domain）對應正確，避免連線到錯誤的伺服器。

### 2. `ens160 connection` 檔案
* **用途：** 負責管理 Linux 系統（常見於 CentOS / RHEL / Rocky Linux 等）中 `ens160` 實體網卡的網路連線組態。
* **常見路徑：** `/etc/sysconfig/network-scripts/ifcfg-ens160` 或經由 `NetworkManager` 進行管理。
* **維護重點：** 紀錄與配置靜態 IP 位址（Static IP）、子網路遮罩（Netmask）、預設閘道（Gateway）以及 DNS 伺服器等網卡參數。

---

## 🚀 使用與更新說明

1. **變更變更：** 任何關於 IP 變更或域名新增之需求，請先向負責人確認。
2. **版本控制：** 修改檔案後，請務必提交（Commit）並推送到遠端數據庫，以便追蹤歷史修改紀錄。
