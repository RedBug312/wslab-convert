# tmp2 usage rules

==== Scroll down for English version ====

目前本系二十部工作站個別主機 (linux\*) 的 /tmp2 暫存空間在 0.5-1.1TB
之間，不過經常有使用者投訴 /tmp2
空間不敷使用，主要原因是有人暫時或累積佔用了大量的空間。經助教群與負責老師討論後，我們將限制
/tmp2 的個人空間使用量，當個別主機或所有主機總合的 /tmp2
空間小於安全下限時，或個別空間超量使用時，系統會限制其寫入權限，甚至在預警五日後自動刪除部份被警告的檔案，以保障多數使用者權益。217工作站主要是支援大多數使用者的一般需求，請大家空間用完儘早刪除，個人有長期大量硬碟空間使用需求的，請尋求相關教授實驗室支援。詳細的
/tmp2 使用規則訂定如下：  
<span id="more-677"></span>

1.  各工作站之 /tmp2 提供暫存資料作不特定用途，位於各工作站之 local
    端。使用者將資料放置於 /tmp2 存取速度較 NFS (Network File System)
    快，也可舒緩 NFS 的負載。唯 /tmp2 不提供作為大量資料備份用途，因採用
    RAID 0 配置，故也不保證資料之完整，請自行備份。
2.  \[單一機器使用量限制條款\] 當某工作站的 /tmp2 剩餘空間小於 5%
    時，該工作站上佔用量最多的若干使用者將無法寫入
    (read-only)，系統會警告使用者們於五日內清除部份資料。五日後，系統將視情況移動部份過度佔用資料(見第4條)並恢復所限制的寫入權限。

3.  \[單一使用者使用量上限條款\] 當工作站 /tmp2
    總使用量¹比率大於安全上限²時，超過 user limit³
    用量的使用者們將無法在所有工作站上的 /tmp2 寫入 (read-only)
    ，系統會寄信警告使用者們於五日內清除部份資料，直到該使用者總使用量低於
    user limit
    方能恢復寫入權限。此外，系統將視情況移動部份過度佔用資料(見第4條)。

4.  在第 2、3
    條中，若使用者們未於五日內清出足夠空間回復安全下限，系統會將部分大檔案與長久閒置檔案移置其他硬碟空間並通知使用者。若使用者需要拿回被刪除的資料，請於收信時間起三日內聯絡工作站助教
    (217ta@csie.ntu.edu.tw)
    ，並自行準備儲存裝置複製資料，逾時則無法取回資料。

5.  例外：對於有課程需求 (如 DSA、SP)
    的課程助教或老師，若有收到系統警告信件，請來信向工作站助教
    (217ta@csie.ntu.edu.tw)
    說明需要多少空間及資料放置時間，以免造成課程上的不便。

以上五點規則是為了保障諸多數使用者的使用權利，謝謝大家的體諒與配合。

217助教團隊敬上

------------------------------------------------------------------------

¹ 總使用量：指該使用者在所有工作站 /tmp2 內使用的空間總和，可從
mrtg.csie.ntu.edu.tw 網頁上的分頁查詢。  
² 安全上限是 0~100% 的百分比，以 /tmp2 的總使用量比率計算，user limit
則以GB來計算使用者使用量，當該比率超過安全上限時，才會限制超過 user
limit 的使用者的寫入權限。這兩個數值會依全體使用者使用情形動態調整。  
³ user limit 的計算方式為將所有 /tmp2 使用者平均可以使用的 /tmp2
空間乘以某個倍率。例如(數字依實際情形調整)： /tmp2
使用者人數為100，將總空間如18T 除以 100 (人) 後得出 180 GB，將 180 GB
乘以 10 則得出 1800 GB，定為 user
limit。即當某使用者使用超過平均值10倍才會被認為是超量使用。

------------------------------------------------------------------------

The workstation have received complaints from users that there’s no
enough storage on /tmp2. Currently the size of /tmp2 on workstation
servers range from 0.5 to 1 TB, and the shortage is arisen from the
large-size and long-term data on /tmp2. As a result, for the sake of
public interest, workstation will start restricting the usage of /tmp2.
If the remaining storage of individual/all servers is below safety lower
bound or there is excess usage on individual users, and these users’
data will be moved from /tmp2. For users who have demand on large or
long-term storage, you should store your data on individual device. The
following is the usage rules:

1.  /tmp2 is a local partition on workstation servers(linux\*) with
    faster access time than network file system(NFS). However, /tmp2 is
    used for storage of temporary data, and it does not guarantee the
    reliability of data because of RAID 0 configuration, thus users
    should not treat /tmp2 as a backup partition.
2.  \[Restricted Rule on Individual Server\] If the remaining usage of
    /tmp2 on any servers is below 5%, workstation will send mail and
    restrict write permission for users with the most usage on that
    server. These users should remove their data in 5 days, otherwise
    workstation will move their data from /tmp2(see rule 4) and restore
    their permission.

3.  \[Restricted Rule on Individual User\] If the total usage¹ on
    workstation servers exceeds safety upper bound², workstation will
    send mail and restrict write permission for users who exceeds user
    limit³. These users should remove their data in 5 days, otherwise
    workstation will move their data from /tmp2(see rule 4) and restore
    their permission.

4.  In rule 2 and 3, if users don’t clean enough space on /tmp2, the
    server will move their data to other disk. If users want to take
    their data back, they should send mail to TAs(217ta@csie.ntu.edu.tw)
    in 3 days and prepare external storage device, otherwise they will
    lose their data.

5.  Exception: Teachers or TAs that need to put long-term, large-size
    course material on /tmp2 should send mail to
    TAs(217ta@csie.ntu.edu.tw) to specify how much storage and how much
    time they need to store their data.

------------------------------------------------------------------------

¹ Total usage is the sum of usage of /tmp2 on all servers, which can be
checked at mrtg.csie.ntu.edu.tw  
² Safety upper bound, with range 0~100%, is the threshold of the usage
on /tmp2. Once the ratio of /tmp2 usage exceeds safety upper bound, the
write permission will be restricted. These two values are adjusted
dynamically.  
³ User limit is the average usage of the users who currently use /tmp2
multiplies a constant. For example, there are 100 users using /tmp2, if
the total size of /tmp2 is 18T, and the constant is 10, than the user
limit is 18T/100\*10=1800GB.

We hope these rules can benefit users with demand on temporary storage
for any purpose, thanks for your cooperation.

Best regards,  
217 TAs

<span class="entry-title">tmp2 usage rules</span>

<span class="by-author author vcard">[NTU CSIE Workstation
Team](https://wslab.csie.ntu.edu.tw/author/ta217/){.url .fn .n}</span>
<span
class="date">[2015-01-242015-01-26](https://wslab.csie.ntu.edu.tw/2015/01/tmp2-usage-rules/ "4:38 PM")</span>
<span
class="category">[Announcement](https://wslab.csie.ntu.edu.tw/category/announcement/)</span>
