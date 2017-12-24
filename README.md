# 檢查進度

- [ ] account.md
- [ ] application-download.md
- [ ] colocation.md
- [ ] computation-rule.md
- [ ] contact.md
- [ ] csie217_print_tutorial.md
- [ ] csie-email-forwarding.md
- [ ] csie-email-transfer.md
- [ ] csie工作站更改密碼how-to-change-csie-password.md
- [ ] faq.md
- [ ] filezilla.md
- [ ] ftp.md
- [ ] hardware.md
- [ ] history.md
- [ ] homepage.md
- [ ] mail.md
- [ ] mail-ms-outlook-2003.md
- [ ] mail-ms-outlook-2003.md.md
- [ ] mail-mutt.md
- [ ] mail-thunderbird.md
- [ ] matlab-r2017a-installation-tutorial.md
- [ ] mirror-service.md
- [ ] operating-system.md
- [ ] password-change.md
- [ ] printer.md
- [ ] receive-mails-using-gmail.md
- [ ] receive-mails-using-imap-on-android.md
- [ ] room.md
- [ ] run-gui-application-with-xming.md
- [ ] software.md
- [ ] ssh.md
- [ ] status.md
- [ ] tmp2-usage-rules.md
- [ ] using-svn-with-https.md
- [ ] vnc.md
- [ ] winscp.md
- [ ] 工作站使用小技巧.md
- [ ] 工作站安裝-python-package-教學.md
- [ ] 忘記csie工作站密碼forget-csie-workstation-password.md
- [ ] 系友忘記工作站密碼alumni-forgot-csie-workstation-password.md

**檔案重抓方法**
1. 從檔案表格重新下載 `wslab.csv`
2. 執行指令
    ```
    parallel 'wget -q -O - { | xmllint --html --xpath "//h1|//article" - 2>/dev/null | pandoc --from html --to markdown_github+grid_tables+link_attributes --atx-headers > pandoc/{/}.md' ::: `grep -xP '.+,.+,' wslab.csv | cut -d, -f2 | sed 's/.$//'`}
    ```
