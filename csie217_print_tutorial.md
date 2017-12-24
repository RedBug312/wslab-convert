# CSIE 列印教學

# 使用工作站列印

1.  將檔案上傳到工作站，例如 linux4.csie.ntu.edu.tw。
2.  在工作站上輸入指令列印。

列印出來的檔案可以在 217 一進入門口的印表機找到。左邊那台叫做
Snoopy，右邊那台叫做 Woodstock。  
217 一到五的白天沒有門禁限制。晚上以及假日需刷學生證或是職員識別證進入。

[![12212267\_10208452295449042\_1488931525\_n](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12212267_10208452295449042_1488931525_n-800x600.jpg){.alignnone
.wp-image-1015 width="556"
height="355"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12212267_10208452295449042_1488931525_n.jpg)

 

 

------------------------------------------------------------------------

# 

# **為了安全考量，目前暫停使用 lpr 指令 For security reason, lpr command is deprecated temporary.**

 

    lpr filename

譬如說，想要列印 slide.pdf 這個檔案。  
[![lpr\_slide\_pdf](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/lpr_slide_pdf1.jpg){.alignnone
.wp-image-1011 width="556" height="355"}  
](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/lpr_slide_pdf1.jpg)~~<span
style="color: red;">**然而，由於目前 Snoopy
的熱凝器故障了，因此大家在使用工作站列印時必須指定 Woodstock。  
**</span>~~<span style="color: red;">11/4
時已經修好了！但大家還是可以學會怎麼指定印表機！</span>

    lpr -P Woodstock filename

[![螢幕快照 2015-11-03
下午2.00.50](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-03-%E4%B8%8B%E5%8D%882.00.50.jpg){.alignnone
.wp-image-1016 width="556" height="355"}  
](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-03-%E4%B8%8B%E5%8D%882.00.50.jpg)基本的列印功能大致上是這樣。如此一來就可以在任何地方，只要將檔案上傳到工作站就可以使用217的印表機列印了。

###### 支援的格式

    Postscript(*.ps)
    Portable Document Format(*.pdf)
    Plain Text(*.txt)(ANSI, Big5, UTF-8 中文)

Microsoft Office 的檔案無法直接列印，請把他們轉成 PDF。如果使用的是 Word
或 Excel
的話，內建的匯出功能有可能會變成**亂碼**（使用中文以及標楷體的話機率很大，其它字體也有可能），因此請使用
CutePDF（204 內建）將檔案轉成 PDF。（詳細請看最後的部分）

###### 其他的指令

除了簡單的以上指令之外，還有其他的指令可以調整列印的設定。lpr
的命令其實是長

    lpr [options] filename

舉例幾個常用的例子。除了上面提過的指定印表機之外，還有  
如果想要列印單面的話（預設列印是雙面)：

    lpr -o sides=one-sided filename

如果想要把多張投影片印在同一頁上，舉例來說，我們想要把4張投影片印在一張上面的話：

    lpr -o number-up=4 filename

接著還可以調整多張投影片在一頁上面的順序，在 \[options\]
的地方打上以下其中一種 layout（雙斜線以及後面是敘述，不要打上去）：

    -o number-up-layout=btlr //Bottom to top, left to right
    -o number-up-layout=btrl //Bottom to top, right to left
    -o number-up-layout=lrbt //Left to right, bottom to top
    -o number-up-layout=lrtb //Left to right, top to bottom (default)
    -o number-up-layout=rlbt //Right to left, bottom to top
    -o number-up-layout=rltb //Right to left, top to bottom
    -o number-up-layout=tblr //Top to bottom, left to right
    -o number-up-layout=tbrl //Top to bottom, right to left

如果想要同一份檔案印很多份的話，譬如說我想要印 3
份（要別的數量請把以下的 3 改成任意數字就好）：

    lpr -# 3 filename

如果只有上面那樣的指令，那印出來的會是三張第一頁，接著是三張第二頁。往往我們想要的順序不是這樣因而要手動分頁。這個時候我們可以用：

    lpr -# 3 -o Collate=True filename

如果想要印特定幾頁的話可以使用（可以用「-」連接數字代表從第幾頁到第幾頁，也可以用「,」隔開分隔的好幾頁）：

    lpr -o page-ranges=1-4,7,9-12 filename

而如果你的-o後面有很多選項要選的話要用

    lpr -o "options options"

舉例來說：  
我個人平常列印上課的投影片的做法是：

    lpr -o "number-up=4 number-up-layout=tblr" -P Woodstock slide.pdf

[![螢幕快照 2015-11-04
下午11.01.32](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-04-%E4%B8%8B%E5%8D%8811.01.32-800x495.jpg){.alignnone
.size-medium .wp-image-1046 width="800" height="495"
sizes="(max-width: 800px) 100vw, 800px"
srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/螢幕快照-2015-11-04-下午11.01.32-800x495.jpg 800w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/螢幕快照-2015-11-04-下午11.01.32.jpg 964w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-04-%E4%B8%8B%E5%8D%8811.01.32.jpg)

其他更詳細的可以參考：<https://www.cups.org/documentation.php>

以上是工作站上列印的介紹

 

 

------------------------------------------------------------------------

 

# 使用網站列印(Web Print)

除了使用工作站列印之外，我們也可以使用 <https://printing.csie.ntu.edu.tw> 列印。  
如此一來，就不用麻煩的上傳檔案到工作站再輸入指令了，而可以在圖型介面下進行列印。

1.  到 <https://printing.csie.ntu.edu.tw>。
2.  用你的學號以及工作站密碼登入（忘記工作站密碼的話請參考[這裡](https://wslab.csie.ntu.edu.tw/2015/10/%E5%BF%98%E8%A8%98csie%E5%B7%A5%E4%BD%9C%E7%AB%99%E5%AF%86%E7%A2%BCforget-csie-workstation-password/)）。
3.  左邊選擇「網路列印」，會看到右邊有「發送工作」。[![螢幕快照
    2015-11-03
    下午11.00.37](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-03-%E4%B8%8B%E5%8D%8811.00.37-800x509.jpg){.alignnone
    .size-medium .wp-image-1031 width="556" height="355"
    sizes="(max-width: 556px) 100vw, 556px"
    srcset="https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/螢幕快照-2015-11-03-下午11.00.37-800x509.jpg 800w, https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/螢幕快照-2015-11-03-下午11.00.37.jpg 901w"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-03-%E4%B8%8B%E5%8D%8811.00.37.jpg)
4.  可以選擇印表機。Elsa 跟 Minnie 在 204，而 Woodstock 跟 Snoopy 在
    217。選擇完成後按右下角進入下一步。  
    [![螢幕快照 2015-11-03
    下午11.02.30](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-03-%E4%B8%8B%E5%8D%8811.02.301-800x419.jpg){.alignnone
    .size-medium .wp-image-1033 width="556"
    height="355"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7-2015-11-03-%E4%B8%8B%E5%8D%8811.02.301.jpg)
5.  接著一路照做就可以了。這裡支援的格式有

<!-- -->

    pdf, bmp, dib, gif, jfif, jif, jpe, jpeg, jpg, png, tif, tiff

<span style="color: red;">要注意的是</span>

1.  舊的 PaperCut 伺服器 <span
    style="color: #1155cc; font-family: arial, helvetica, sans-serif;"><span
    class="underline"><https://r204pdc.csie.ntu.edu.tw:9192/user></span></span><span
    style="font-family: arial, helvetica, sans-serif;">
    及 <https://snoopy.csie.ntu.edu.tw:9192/user></span>
    ，皆已關閉服務。
2.  217 跟 204 的餘額現在是合併計算的。
3.  無法在 219 或是 204
    的電腦中開機時直接登入自己的帳號，然後直接使用電腦的列印功能。

以上是 Web Print 的介紹。

 

# 使用 CutePDF 將 Word 或 Excel 轉成 PDF

如果使用 Word 或 Excel 內建的匯出功能將檔案匯出成為 PDF
時，有可能會變成亂碼。即使在自己的電腦上打開 PDF
顯示正常，從印表機印出來的依然有可能會是亂碼。  
因此，我們必須使用 204 的 CutePDF 將 Word 或 Excel 的工作轉成 PDF 檔案。

做法很簡單。假設我們今天有一份 Word 檔。  
[![12211261\_10208458766410812\_862003802\_o](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12211261_10208458766410812_862003802_o-800x500.jpg){.alignnone
.size-medium .wp-image-1042 width="556"
height="355"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12211261_10208458766410812_862003802_o.jpg)

1.  到列印的地方，在印表機的選單裡選擇「CutePDF Writer」。  
    [![12208933\_10208458785931300\_852087782\_o](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12208933_10208458785931300_852087782_o-800x500.jpg){.alignnone
    .size-medium .wp-image-1043 width="556"
    height="355"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12208933_10208458785931300_852087782_o.jpg)
2.  按下「Print」之後，會出現問你要把 PDF 檔案存在哪裡的視窗。  
    [![12204057\_10208458798611617\_570734119\_o](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12204057_10208458798611617_570734119_o-800x500.jpg){.alignnone
    .size-medium .wp-image-1044 width="556"
    height="355"}](https://wslab.csie.ntu.edu.tw/wp-content/uploads/2015/11/12204057_10208458798611617_570734119_o.jpg)
3.  選好自己存放 PDF 的地方以及檔案名稱，就可以得到不會變成亂碼的 PDF
    了！

以上是使用 CutePDF 把 Word 或 Excel 轉成 PDF 檔案的介紹。

<span class="entry-title">CSIE 列印教學</span>

<span class="by-author author vcard">[NTU CSIE Workstation
Team](https://wslab.csie.ntu.edu.tw/author/ta217/){.url .fn .n}</span>
<span
class="date">[2015-11-052016-06-24](https://wslab.csie.ntu.edu.tw/2015/11/csie217_print_tutorial/ "12:31 PM")</span>
<span
class="category">[Tutorial](https://wslab.csie.ntu.edu.tw/category/tutorial/),
[Uncategorized](https://wslab.csie.ntu.edu.tw/category/uncategorized/)</span>

# 使用工作站列印

# 

# **為了安全考量，目前暫停使用 lpr 指令 For security reason, lpr command is deprecated temporary.**

# 使用網站列印(Web Print)

# 使用 CutePDF 將 Word 或 Excel 轉成 PDF
