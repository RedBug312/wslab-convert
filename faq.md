# 常見問題 FAQ

## 常見問題

### 我想申請工作站帳號

請參考 [[待處理] 帳號](/account/)。

### 忘記工作站密碼

若您的 CSIE 工作站帳號為學生帳號，可透過系統自動申請重設密碼，不必寄信。

重設密碼 SOP：

1.  開啟 esystem 忘記密碼系統：
    <https://esystem.csie.ntu.edu.tw/forget_password>
2.  輸入工作站帳號名稱，按下「Reset Password」送出申請
3.  請稍等 3 分鐘，系統將寄重設確認信到 NTU 信箱，寄件者是 CSIE Esystem
    &lt;esystem@csie.ntu.edu.tw&gt;，標題為 \[CSIE Workstation\]
    password reset
4.  點選信中的連結，注意連結的網址開頭必須是
    https://esystem.csie.ntu.edu.tw/reset\_password，以防止遭到釣魚
5.  網頁會顯示成功重設密碼，並把新密碼寄到 NTU 信箱
6.  使用此密碼登入到工作站或 CSIE Info 更改密碼

### 畢業生工作站 Quota 縮減

請至 [[待處理] CSIE Info](https://info.csie.ntu.edu.tw/graduation) 完成手續

## Linux

-   I’m using GNOME. Why does it suddenly stop working?  
    This usually happens after upgrading to a new GNOME version. You can
    remove your GNOME related settings by

cd ~ && rm -rf .gconf\* .gnome\* .gnomehackrc .recently-used

**Please backup them before doing this.** Usually this helps, if not,
please contact the TAs. **Note that you may lose your Firefox or Mozilla
settings.**

-   Where is my favorite KDE?  
    We no longer support KDE as our desktop environment. Please switch
    to GNOME.
-   Why the outputs from ”dict” are broken?  
    The output by dict protocol is UTF-8. You can use `dictl` which
    automatically transforms the encoding for you. You have to set LANG
    or LC\_CTYPE correctly. For example, they should be zh\_TW.Big5 for
    most of you.

-   Can I use X window environment of BSD and Linux boxes on my Windows
    desktop?  
    Yes. You have to start a VNC server on any one of workstations
    first. Then, use a VNC client to connect. **We strongly recommend
    you use VNC over an encrypted channel.** To setup, please refer to
    [[待處理] this URL](http://www.csie.ntu.edu.tw/~rafan/vnc-ssh.html) and
    remember to add `-localhost` when you start the vnc server.

-   Why does my mail forwarding not work?  
    Please make sure you modify your forwarding setting in the [[待處理] webmail
    service](http://webmail.csie.ntu.edu.tw/). If it does not work,
    please contact the TAs.

-   How do I know my home directory space usage?  
    You can use the command `du` to list the space usage. For example,

On Linux

du –max-depth=1 ~ \| sort -n

On BSD

du -d 1 ~ \| sort -n

## Account

-   Could I name my account after my name for students?  
    No, because of management issue. We use a student id as the account
    name for undergraduate students, graduate students and phd students.

-   How many user space I can use?  
    For undergraduate and master student, each student has 1G user
    quota. For alumni, each alumnu has 100M user quota.

## Mail

-   May I put files on mail server?  
    No. you cannot. The system automatically removes non-mail files on
    the server.

-   Why I have to enter my password each time in pine or mutt?  
    Pine and Mutt access mailbox via IMAP (or POP3) which requires
    authentication. You may want to use screen to keep pine/mutt open.

-   What is ~/mail and ~/Mail?  
    ~/Mail is where Mutt stores mail. ~/mail is for Pine.

-   How to forward my mail?  
    Plaese login Webmail and set it in “Preference”.

-   What is Greylisting?  
    Check this URL for detail.

## BSD

-   Can we run MATLAB on BSD machines?  
    Yes. But this is **EXPERIMENTAL**, not officially supported by
    MATLAB.

-   Can we run linux binary on BSD machines?  
    Yes.
