# 列印 Printer

## 印東西之前

請想想你會砍掉幾顆樹。 請不要利用印表機列印任何與課業無關的東西。
印大檔案時(超過50頁)請為其他人想想，最好在無人使用的冷門時段才印。

## 印表機在哪裡？

在209辦公室外頭走廊，目前有兩台印表機，Ariel 和 Elsa。

## 網頁列印

[網頁列印](https://printing.csie.ntu.edu.tw:9192/user)目前只支援PDF檔。

## 網頁列印可能遇到的問題？

Q1.上傳PDF後一直轉圈圈，沒印出來也沒被扣款?  
A1.可能是系統無法解析檔名，請將檔名改為123.pdf後重試。

Q2.印出來的文件上英文正常，但是中文字體破損、重疊，很像印表機碳粉不足(如下圖)?  
![](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2012/03/PaperCut_%E5%88%97%E5%8D%B0%E5%A4%B1%E6%95%97-800x234.jpg){.alignnone
.size-medium .wp-image-1143 width="800" height="234"
sizes="(max-width: 800px) 100vw, 800px"
srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2012/03/PaperCut_列印失敗-800x234.jpg 800w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2012/03/PaperCut_列印失敗-768x224.jpg 768w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2012/03/PaperCut_列印失敗.jpg 845w"}  
A2.因為系統無法正確解析標楷體而導致，解決方式為把要列印的PDF檔用其他PDF列印軟體(Ex.CutePDF
Writer)先印一次，所產生的新PDF檔即可正常列印。  
PS.如有需要，R217有已安裝PDF列印軟體的公用電腦可以使用。

## 基本列印

可以從工作站用以下指令列印：

lpr \[options\] filename

若您需要關於任何額外的設定，請使用以下指令查看 options：

lpr –help

使用 `lpq` 指令可以印出最近一小時的列印工作

lpq

使用 X window 的程式時，選擇列印後會看到 R217\_Printer
設定選項，按下列印即可。

## 可列印的檔案

### 下列格式的檔案，可以直接透過 lpr 列印

-   PostScript (\*.ps)
-   Portable Document Format (\*.pdf)
    (若無法列印或列印不正常，建議用閱讀程式如 evince 打開後再印)
-   Plain Text (純文字檔)(\*.txt) (ANSI、Big5 或 UTF-8 中文)

### office檔案

doc, ppt, xls 等 office 檔案，無法直接透過 lpr 列印，若需要列印，請利用
oowriter，指令如下

oowriter -p filename

### 程式碼

如果萬一真的非不得已，要印出來的時候，可以用下面的指令：

a2ps code.c

剩下的用法請參考 `man a2ps`。

### 其他檔案

對於不可直接列印的檔案，必須透過適當的程式**轉換成 PostScript
後**，才能印出來喔。  
為求最佳的列印效果，除 PostScript 以外，建議先用閱讀程式打開後再列印。

## 列印失敗該如何處理?

1.  指定另外一台印表機 lpr -P {Ariel,Elsa} filename
2.  換另外一台工作站

## 一些小技巧

### 指定列印範圍

你可以用下面這些方式來指定想要列印的範圍

lpr -o page-ranges=1 filename  
lpr -o page-ranges=1-4 filename  
lpr -o page-ranges=1-4,7,9-12 filename

### 多張印成一頁

有些時候，想把投影片印出來看，但是一張一張印很浪費紙，這邊提供一個將多張印成一頁的方式。假設原本的檔案是
slides.pdf，然後要印成一頁四張投影片

lpr -o number-up=4 slides.pdf\`

還有一些不同功能的參數可以使用，請見 [CUPS
doc](http://www.cups.org/documentation.php/doc-1.3/options.html)，N-Up
Printing

### 符合頁面

lpr -o fit-to-page file\`

### 指定縮放比率（相對於頁面大小，僅能用於影像）

lpr -o scaling=80 image\_file\`

### 更多指令

[請看這邊！](http://www.cups.org/doc-1.1/sum.html#4_1)

## 印錯了！

如果不小心印錯檔案，想砍掉不印的話，可以用下面的指令把你最新的列印工作砍掉：

lprm

如果你一次印了很多檔案，想砍掉特定一個的話，你得先用 `lpq`
去看你要砍掉的列印工作的編號：

ID User File Size Time Status  
R217\_Printer-278 artoo Test Page 17408 09:48:19
job-completed-successfully

在這裡，列印工作的編號是 **278**，所要下的指令是：

lprm 278

要注意的是，如果印表機**已經**開始印東西出來的話，上面的方式就不管用了。這時候，你必須走到印表機前面，按鈕取消列印工作：

按ｘ -&gt; 取消工作

## 等好久東西都沒出來？

有些時候，你可能 `lpr` 後，東西好久都沒出來。可能有幾種原因：

### 印表機相當忙碌（很多人在印東西）

你可以用 `lpq` 這個指令來看現在有那些人在印東西，輸出可能長得像是：

ID User File Size Time Status  
R217\_Printer-304 artoo pdf-1.3.pdf 950272 11:08:03
job-completed-successfully  
R217\_Printer-305 artoo pdf-1.5.pdf 3597312 11:08:08
job-completed-successfully  
R217\_Printer-306 artoo pdf-1.2.pdf 797696 11:11:12
job-completed-successfully  
R217\_Printer-307 artoo pdf-1.4-embed.pdf 652288 11:12:12 job-printing  
R217\_Printer-308 artoo pdf-1.4-embed.pdf 652288 11:13:44 none  
R217\_Printer-309 artoo pdf-1.3.pdf 950272 11:13:57 none  
R217\_Printer 從 2009年02月16日 (週一) 11時13分48秒 開始接受請求

可以看到目前有一個大小為 652288 bytes
的工作正在列印，而後面還有兩個工作在等待。

### 你印了無法列印的檔案格式

在 `lpq` 的輸出，會看到類似：

R217\_Printer-324 artoo tes.pdf 24576 11:46:39 job-stopped

這樣子的東西，或是 job 直接顯示
`job-completed-successfully`，但印表機沒有動作

### 印表機看不懂

有些程式生出來的
PostScript，印表機會無法正常的解讀，導致無法印出來。如果碰到這種情形，可以用下列的指令處理過：

ps2ps old.ps new.ps

然後再印 `new.ps` 看看。

### 你的 Quota 爆炸了

請先[查詢 Quota](https://printing.csie.ntu.edu.tw:9192/user)。217
每人每學期有初始 500 quota
的限制，為了提醒大家愛護紙張的重要性，217不提供增加quota
的服務。希望大家列印時多想想，是不是真的有需要印出來，是不是有更省紙的印法，愛護地球人人有責！
