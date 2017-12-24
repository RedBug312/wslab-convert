# Using SVN with https

Usually, when you connect to a SVN server via https, you will receive
following messages:  

``` Plum_Code_Box
SSL handshake failed: Secure connection truncated 
                                    
```

This is due to the buggy gnutls. To avoid the problem, please edit
“~/.subversion/servers”, add one line:

``` Plum_Code_Box
http-library = serf
                                    
```

 

Then you can use svn with https now.

<span class="entry-title">Using SVN with https</span>

<span class="by-author author vcard">[Ting-Yen
Lee](https://wslab.csie.ntu.edu.tw/author/lydian/){.url .fn .n}</span>
<span
class="date">[2012-04-172014-09-25](https://wslab.csie.ntu.edu.tw/2012/04/using-svn-with-https/ "3:51 PM")</span>
<span
class="category">[Tutorial](https://wslab.csie.ntu.edu.tw/category/tutorial/)</span>
