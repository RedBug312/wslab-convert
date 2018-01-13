# 信箱 Mail

## GMail Provided by G Suite for Education

You can login GMail with `[username]@csie.ntu.edu.tw`, e.g. `b03902000@csie.ntu.edu.tw`, and NTU CSIE workstation password (same as CSIE email password). Using GMail, you can still check your email with your favorate email client, like Thunderbird, Outlook, and so on. Here we will introduce how to set up your mail clients when using GMail.

::: info
If you want to see your email appear in GMail but can only see they in csie web mail, please contact us.
:::

### step 1
Enable GMail IMAP.

1.  Go to [GMail](https://mail.google.com/).
2.  Click ![](https://drive.google.com/uc?export=download&id=12mtbiWmdVOsomdnt26gHyy-4jzB_fc2F) in the top right.
3.  Click “Settings”.
4.  Click the tab “Forwarding and POP/IMAP”.
5.  Check “Enable IMAP” in “Status” of “IMAP Access” section.

::: info
If you like to use POP, you can also enable POP here. Note that, when POP is used, mail will be deleted once your mail client receives the mail.
:::

### step 2
Setup Google 2-Step-Verification & App Password.

You have to generate an App Password to authenticate your csie email account. Note that if you’re using Thunderbird or Evolution, you can skip this step.

1.  Go to GMail [My Account](https://myaccount.google.com/).
2.  Click Sign-in & security.
3.  Click Signing in to Google (on the left bar).
4.  Find 2-Step-Verification and turn it on (just click on it and follow google’s step).
5.  Go back to Sign-in & security and click on App Passwords below 2-Step-Verification (you would be ask to re-enter your password).
6.  Select Mail and your device (Mac or Windows Computer) and click generate.
7.  You’ll get a generated password for the configuration below.

### step 3
Configure your email client.

#### For Outlook

1.  Go to File &gt; Info and click on Account Settings.
2.  Select your csie account and click Change (or click New for your
    first time) and fill in the following configuration.
    -   Account type: IMAP
        -   Incoming mail server: `imap.gmail.com`
        -   Outgoing mail server: `smtp.gmail.com`
    -   Login Information
        -   User Name: `[username]@csie.ntu.edu.tw`
        -   Password: App password you generate above (from step 2)
3.  Click Next and it would go through some testing.
4.  After the testing, you can enjoy GMail with Outlook.

#### For Mac Mail

1.  Go to Mail &gt; Preference (on the top bar).
2.  Select your csie account and click Server Settings (or click ‘+’ for your first time) and fill in the following configuration.
    -   Incoming mail server (IMAP)
        -   User Name: `[username]@csie.ntu.edu.tw`
        -   Password: App password you generate above (from step 2)
        -   Host Name: `imap.gmail.com`
    -   Outgoing Mail Server (SMTP)
        -   User Name: `[username]@csie.ntu.edu.tw`
        -   Password: App password you generate above (from step 2)
        -   Host Name: `smtp.gmail.com`
3.  Click Save and you can enjoy GMail with Mac Mail.

#### For Thunderbird

1.  Click “email” bellow “Create a new account”.
2.  Click buttion “Skip this and use my existing email”.
3.  Enter your name, email address and password.
4.  Click “continue”, then fill in the following configuration
    -   Incoming: IMAP
        -   Server hostname: `imap.gmail.com`
        -   Port: 993
        -   SSL: SSL/TLS
        -   Authentication: Nornal password
    -   Outgoing: SMTP
        -   Server hostname: `smtp.gmail.com`
        -   Port: 587
        -   SSL: STARTTLS
        -   Authentication: Normal password
    -   Username: `[username]@csie.ntu.edu.tw`
5.  Click “Re-test” and then “Advanced config”.
6.  In “Server Settings”, choose “OAuth2” in “Authentication Method” list.
7.  In “Outgoing Server (SMTP)”, edit the entry “[username]@csie.ntu.edu.tw – smtp.gmail.com (Default)”. Choose “OAuth2” in “Authentication Method” list, and click “Ok”.
8.  Click “Ok” again.
9.  When receiving mail for the first time, a window will prompt out ask you to login. Login with CSIE email and password, and grant permission to Thunderbird.
10. Then you can enjoy GMail with Thunderbird 😀

#### For Evolution

1.  Click “File &gt; New &gt; Mail Account” from menu bar.
2.  Step Welcome: Click “Next”.
3.  Step Identity: Fill in your name and CSIE csie email address then click “Next”.
4.  Click “Skip Lookup”.
5.  Step Receiving Email: Choose “IMAP+” as server type. Then fill in the following configurations
    -   Server: `imap.gmail.com`
    -   Port: 993
    -   Username: `[username]@csie.ntu.edu.tw`
    -   Authentication: OAuth2 Google
6.  Step Receiving Options: You can set up your preference here.
7.  Step Sending Email: Choose “SMTP” as Server Type, Then fill in the following configurations
    -   Server: `smtp.gmail.com`
    -   Check “Server requires authentication”
    -   Port: 587
    -   Authentication type: PLAIN
    -   Username: `[username]@csie.ntu.edu.tw`
8.  Step Account Summary: Check if anything is same as what you think.  Then click “Next”.
9.  Click “Apply”.
10. A window will prompt out ask you to login. Login with CSIE email and password, and grant permission to Evolution.
11. Then you can enjoy GMail with Evolution.

## Email Service Hosted by Department
:::warning
Note that, this service is mainly for faculty. For students, please check the tutorial above.
:::
### 帳號和信箱
-   帳號與密碼：同工作站實驗室之帳號與密碼。
-   Mail Address: `ID@csie.ntu.edu.tw`, e.g. `b999902067@csie.ntu.edu.tw`.

### 連線
-   POP3 Server: `pop3.csie.ntu.edu.tw` (995 for secure connection)
-   IMAP Server: `imap.csie.ntu.edu.tw` (993 for secure connection)
-   SMTP Server: `smtp.csie.ntu.edu.tw` (465 for secure connection using SSL and AUTH)

## 從其他地方收發信 Mail Client Configuration

-   [Gmail](https://wslab.csie.ntu.edu.tw/2013/01/receive-mails-using-gmail/)
-   [Android](https://wslab.csie.ntu.edu.tw/2013/01/receive-mails-using-imap-on-android/)
-   [Mozilla Thunderbird](https://wslab.csie.ntu.edu.tw/2012/03/mail-thunderbird/)
-   [Mutt](https://wslab.csie.ntu.edu.tw/2012/05/mail-mutt/)
-   [Microsoft Outlook 2003](https://wslab.csie.ntu.edu.tw/2012/03/mail-ms-outlook-2003/)

:::info
我們已不再支援 Windows XP 系統以及 Microsoft Outlook Express，請改用 Thunderbird 或其他收信軟體。
:::

