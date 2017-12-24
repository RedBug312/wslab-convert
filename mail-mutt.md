# Email 設定-mutt

在 ~/.muttrc
中改下面的設定（**USERNAME** 請代換成你的帳號名，如 **b94000**）：  
Put the following in your ~/.muttrc (Replace **USERNAME** with your
account name, e.g. **b94000**):

``` Plum_Code_Box
set spoolfile="imaps://USERNAME@imap.csie.ntu.edu.tw/INBOX"
set move=no
set mail_check=300
set timeout=15
set record=+sent-mail # make sure it begins with +
set postponed=+postponed # make sure it begins with a +
set realname="USERNAME"
set from="USERNAME@csie.ntu.edu.tw"
set use_from=yes
                                    
```

如果想把 ~/mail（pine 存寄件備份或自己分的信件匣的地方）也放在 mail
server 上：

If you want to put ~/mail on mail server:

``` Plum_Code_Box
set folder="imaps://USERNAME@imap.csie.ntu.edu.tw/"  # ONLY if you want to put ~/Mail on mail server

                                    
```

 

需要更詳細的設定，請參考 [Mutt’s Documentation  
](http://www.mutt.org/#doc "http://www.mutt.org/#doc")For more detailed
settings, please refer to [Mutt’s
Documentation](http://www.mutt.org/#doc "http://www.mutt.org/#doc")

<span class="entry-title">Email 設定-mutt</span>

<span class="by-author author vcard">[Ting-Yen
Lee](https://wslab.csie.ntu.edu.tw/author/lydian/){.url .fn .n}</span>
<span
class="date">[2012-05-042014-09-25](https://wslab.csie.ntu.edu.tw/2012/05/mail-mutt/ "1:16 PM")</span>
<span
class="category">[Tutorial](https://wslab.csie.ntu.edu.tw/category/tutorial/)</span>
