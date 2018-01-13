# 檢查進度

- [ ] 機房 Room215
- [ ] History
- [ ] 實驗室空間 Room 217
- [ ] 申請表單 Application Forms
- [ ] 聯絡助教 Contact

- [ ] 常見問題 FAQ

- [ ] 工作站使用規範 Computation Rule
- [ ] SSH
- [ ] 硬體 Hardware
- [ ] 軟體 Software
- [ ] 系統狀態 Status
- [ ] 作業系統 Operating System

- [ ] Mirror Service
- [ ] 工作站安裝 python package 教學
- [ ] tmp2 usage rules
- [ ] 工作站使用小技巧
- [ ] WinSCP
- [ ] FileZilla
- [ ] Using VNC
- [ ] Esystem相關連結
- [ ] Run GUI application with Xming

- [ ] 帳號 Account
- [ ] 信箱 Mail
- [ ] CSIE Email 轉遞公告 (Email Forwarding)
- [ ] 更改密碼 Change Password
- [ ] CSIE工作站更改密碼/HOW TO CHANGE CSIE PASSWORD
- [ ] 忘記CSIE工作站密碼/FORGET CSIE WORKSTATION PASSWORD
- [ ] 系友忘記工作站密碼/Alumni Forgot CSIE WORKSTATION Password

- [ ] 列印 Printer
- [ ] CSIE 列印教學
- [ ] MATLAB R2017a installation tutorial

- [ ] 個人網頁 Homepage

## 檔案重抓方法

1. 從檔案表格重新下載 `wslab.csv`
2. 執行指令
    ```
parallel 'wget -q -O - {} | xmllint --html --xpath "//h1|//article" - 2>/dev/null | pandoc --from html --to markdown_github+grid_tables+link_attributes --atx-headers > {/}.md' ::: `grep -xP '.+,.+,' wslab.csv | cut -d, -f2 | sed 's/.$//'`
    ```
