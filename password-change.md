# 更改密碼 Change Password

一、您可以透過工作站變更密碼，方法如下：

1.  下載 [Putty](http://www.chiark.greenend.org.uk/~sgtatham/putty/)
2.  打開 Putty，在「**Host Name (or IP
    address)**」輸入你想登入的工作站，選擇用「**SSH**」連線。（如下圖，以
    linux1 為例）  
    [![putty1](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/10/putty1.png){.alignnone
    .size-full .wp-image-950 width="434"
    height="415"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/10/putty1.png)
3.  輸入帳號和密碼（以 b99902067 為例）  
    ![](/wp-content/uploads/2014/12/password-change-1.png)
4.  成功登入以後，請執行 `passwd`，先輸入原始密碼，再輸入 2
    次新密碼（輸入密碼時不會有任何字元顯示）。沒有錯誤訊息就表示更改密碼成功。  
    ![](/wp-content/uploads/2014/12/password-change-2.png)

二、CSIE Info 更改密碼系統：<https://info.csie.ntu.edu.tw/user/passwd>

原先僅能透過工作站 passwd 指令更改密碼，現在可從 CSIE Info 進行更改。  
從 [CSIE Info](https://info.csie.ntu.edu.tw/) 首頁點選「更改密碼 Change
Password」即可使用，或直接點選上方連結。

※
補充：此系統仍會檢查您的密碼是否和原密碼過於接近，以及太過簡單的密碼。如果不知道密碼該取什麼，可利用
<http://www.mytsoftware.com/dailyproject/PassGen/PassGen.html>
產生亂數密碼。（此網頁產生亂數是由瀏覽器執行，不會傳輸到伺服器，可安心使用）
