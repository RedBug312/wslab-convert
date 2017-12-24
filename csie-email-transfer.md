# CSIE Email 複製與轉移教學

在設定完[轉信](https://wslab.csie.ntu.edu.tw/2015/01/csie-email-forwarding/ "CSIE Email Forwarding")後，您可以使用支援
IMAP 通訊協定的 email 軟體來將原先存放在系上 mail server
的信完整複製到另一個信箱。如果您平常並沒有使用桌面版本 email
軟體的習慣，建議可以嘗試跨平臺的 Mozilla Thunderbird ，以下會以
Thunderbird 為例說明設定步驟。

## 在開始操作之前

1.  請自行下載並安裝 [Thunderbird](https://www.mozilla.org/thunderbird/ "Mozilla Thunderbird")
    軟體。如果您使用的是 GNU/Linux 或 \*BSD
    作業系統，建議直接使用系統提供的套件管理程式安裝。
2.  由於 email 複製過程中會 Thunderbird
    會自動將所有信件下載到系統預設存放個人資料的資料夾，例如 Windows 的
    C:\\Users 或是多數 Unix-like 系統的
    /home。如果您因為磁碟空間問題，需要將資料改放置到其他資料夾，請參考
    Thunderbird 的 [Using Multiple
    Profiles](https://support.mozilla.org/en-US/kb/using-multiple-profiles "Using Multiple Profiles")
    說明，在建立設定檔時將路徑指向其他磁碟。

## 連線至 CSIE mail server

1.  帳號設定  
    [![2015-03-11 23:33:14
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233314-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-730 width="1102" height="476"
    sizes="(max-width: 1102px) 100vw, 1102px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233314-的螢幕擷圖.png 1102w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233314-的螢幕擷圖-800x346.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233314-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
2.  新增帳號  
    [![2015-03-11 23:33:47
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233347-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-732 width="693"
    height="545"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233347-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
3.  輸入 email address 和密碼  
    [![2015-03-11 23:35:28
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233528-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-733 width="605"
    height="465"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233528-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
4.  由於 Thunderbird 自動偵測設定會失敗，所以我們必須自行填入設定  
    [![2015-03-11 23:36:25
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233625-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-734 width="859" height="473"
    sizes="(max-width: 859px) 100vw, 859px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233625-的螢幕擷圖.png 859w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233625-的螢幕擷圖-800x441.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233625-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
5.  按「重新測試」確認設定正確後即可按「完成」  
    [![2015-03-11 23:36:40
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233640-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-735 width="859" height="473"
    sizes="(max-width: 859px) 100vw, 859px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233640-的螢幕擷圖.png 859w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233640-的螢幕擷圖-800x441.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233640-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
6.  回到 Thunderbird 主畫面可看到 CSIE mail server 上的信件  
    [![2015-03-11 23:38:58
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233858-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-736 width="910" height="476"
    sizes="(max-width: 910px) 100vw, 910px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233858-的螢幕擷圖.png 910w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233858-的螢幕擷圖-800x418.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-11-233858-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

## 將所有 email 複製到另一個 mail server，這裡以 NTU mail 為例

1.  連線方法與 CSIE mail 設定方法類似[![2015-03-12 00:01:31
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-000131-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-738 width="859" height="473"
    sizes="(max-width: 859px) 100vw, 859px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-000131-的螢幕擷圖.png 859w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-000131-的螢幕擷圖-800x441.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-000131-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
2.  首先我們先新增一個空白資料夾，名稱自訂，這裡以 CSIE 為例  
    [![2015-03-12 00:39:47
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-003947-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-740 width="309"
    height="222"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-003947-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
3.  由於 Thunderbird 不允許直接複製收件匣，因此我們必須手動新增  
    [![2015-03-12 00:40:13
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-004013-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-741 width="309"
    height="222"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-004013-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)
4.  切換至 CSIE mail 的收件匣，按 Ctrl+A 全選所有信件後，按住 Ctrl
    並拖放至剛才在 NTU mail 新增的資料夾  
    [![螢幕快照 - 西元2015年03月12日 -
    00時46分12秒](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-%E8%A5%BF%E5%85%832015%E5%B9%B403%E6%9C%8812%E6%97%A5-00%E6%99%8246%E5%88%8612%E7%A7%92.png){.alignnone
    .size-full .wp-image-742 width="910" height="476"
    sizes="(max-width: 910px) 100vw, 910px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/螢幕快照-西元2015年03月12日-00時46分12秒.png 910w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/螢幕快照-西元2015年03月12日-00時46分12秒-800x418.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-%E8%A5%BF%E5%85%832015%E5%B9%B403%E6%9C%8812%E6%97%A5-00%E6%99%8246%E5%88%8612%E7%A7%92.png)
5.  按住 Shift 選取所有要複製到 NTU mail
    的其他資料夾，注意選取時不能選到收件匣  
    [![螢幕快照 - 西元2015年03月12日 -
    00時47分01秒](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-%E8%A5%BF%E5%85%832015%E5%B9%B403%E6%9C%8812%E6%97%A5-00%E6%99%8247%E5%88%8601%E7%A7%92.png){.alignnone
    .size-full .wp-image-743 width="910" height="476"
    sizes="(max-width: 910px) 100vw, 910px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/螢幕快照-西元2015年03月12日-00時47分01秒.png 910w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/螢幕快照-西元2015年03月12日-00時47分01秒-800x418.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-%E8%A5%BF%E5%85%832015%E5%B9%B403%E6%9C%8812%E6%97%A5-00%E6%99%8247%E5%88%8601%E7%A7%92.png)
6.  複製完成！  
    [![2015-03-12 14:06:05
    的螢幕擷圖](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-140605-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png){.alignnone
    .size-full .wp-image-749 width="894" height="543"
    sizes="(max-width: 894px) 100vw, 894px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-140605-的螢幕擷圖.png 894w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-140605-的螢幕擷圖-800x486.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-140605-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96.png)

## 可能會遇到的問題

1.  如果您使用 GNU/Linux 作業系統和
    [Wayland](http://wayland.freedesktop.org/ "Wayland")
    顯示伺服器，發現無法在 Thunderbird
    中正常拖放資料夾時，建議登出並改用使用 X Window 的 session
    登入（即桌面名稱中沒有出現 Wayland 的選項）。
2.  如果您發現有部份信件沒有被複製到另一個信箱，如下圖所示。這可能因為您的另一個信箱（例如
    NTU mail）有限制單一訊息大小（例如最大 20
    MiB），如果遇到這類狀況，請取消選取太大的信件，再重新複製。  
    [![2015-03-12 01:04:09
    的螢幕擷圖紅框](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-010409-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96%E7%B4%85%E6%A1%86.png){.alignnone
    .size-full .wp-image-751 width="910" height="489"
    sizes="(max-width: 910px) 100vw, 910px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-010409-的螢幕擷圖紅框.png 910w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-010409-的螢幕擷圖紅框-800x430.png 800w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/03/2015-03-12-010409-%E7%9A%84%E8%9E%A2%E5%B9%95%E6%93%B7%E5%9C%96%E7%B4%85%E6%A1%86.png)

<span class="entry-title">CSIE Email 複製與轉移教學</span>

<span class="by-author author vcard">[NTU CSIE Workstation
Team](https://wslab.csie.ntu.edu.tw/author/ta217/){.url .fn .n}</span>
<span
class="date">[2015-03-232015-09-28](https://wslab.csie.ntu.edu.tw/2015/03/csie-email-transfer/ "10:35 AM")</span>
<span
class="category">[Tutorial](https://wslab.csie.ntu.edu.tw/category/tutorial/)</span>
