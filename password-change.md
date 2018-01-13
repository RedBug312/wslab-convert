# 更改密碼 Change Password

## 您可以透過工作站變更密碼
方法如下：

1.  下載 [Putty](http://www.chiark.greenend.org.uk/~sgtatham/putty/)
2.  打開 Putty，在「**Host Name (or IP address)**」輸入你想登入的工作站，選擇用「**SSH**」連線。（如下圖，以 linux1 為例）
    ![](https://drive.google.com/uc?export=download&id=1LQ6qnxfF5Qzatic76fpDi2zHQJYhygKw)
3.  輸入帳號和密碼（以 b99902067 為例）
    ![](https://drive.google.com/uc?export=download&id=1Rn9mVi0d8tMcLqUd0HAdt7vw9pJHHfwN)
4.  成功登入以後，請執行 `passwd`，先輸入原始密碼，再輸入 2 次新密碼（輸入密碼時不會有任何字元顯示）。沒有錯誤訊息就表示更改密碼成功。
    ![](https://drive.google.com/uc?export=download&id=1h-Rmnq5dMUUXC9BrsKQJ_05dbqNvWPTj)

## CSIE Info 更改密碼系統

原先僅能透過工作站 `passwd` 指令更改密碼，現在可從 CSIE Info 進行更改。從 [CSIE Info](https://info.csie.ntu.edu.tw/) 首頁點選「[更改密碼 Change Password](https://info.csie.ntu.edu.tw/user/passwd)」即可使用，或直接點選上方連結。

:::info
補充：此系統仍會檢查您的密碼是否和原密碼過於接近，以及太過簡單的密碼。如果不知道密碼該取什麼，可利用 [Strong Password Generator](http://www.mytsoftware.com/dailyproject/PassGen/PassGen.html) 產生亂數密碼。（此網頁產生亂數是由瀏覽器執行，不會傳輸到伺服器，可安心使用）
:::
