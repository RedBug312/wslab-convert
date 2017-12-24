# 工作站安裝 python package 教學

大部份的python package 安裝都很簡單，只要執行

python setup.py install

就可以了，可是這個指令會把一些檔案copy 到/lib/
之類需要有root權限才能讀寫的資料夾， 一般的user
不會有這個權限，但是只要加上 prefix 後就可以自由選擇安裝路徑

python setup.py install
–prefix=/home/student/00/b00902001/python-packages/package-name

這樣library
檔就會裝到/home/student/00/b00902001/python-packages/package-name
裡面了，但是因為路徑是自己設的，所以這時候如果在python
裡面直接import，會顯示出錯誤訊息，告訴你沒有這個module。這時我們要記得

export
PYTHONPATH=$HOME/python-packages/package-name/lib/python2.7/site-packages/:$PYTHONPATH

然後python 就會知道要去這個路徑找我們要的module
了，當然我們也可以把這個指令放在.bashrc
之類的地方，這樣每次重新登入的時候，package path
就會自動被加到PYTHONPATH中了。

<span class="entry-title">工作站安裝 python package 教學</span>

<span class="by-author author vcard">[Ting-Yen
Lee](https://wslab.csie.ntu.edu.tw/author/lydian/){.url .fn .n}</span>
<span
class="date">[2012-03-132014-09-25](https://wslab.csie.ntu.edu.tw/2012/03/%e5%b7%a5%e4%bd%9c%e7%ab%99%e5%ae%89%e8%a3%9d-python-package-%e6%95%99%e5%ad%b8/ "11:41 AM")</span>
<span
class="category">[Tutorial](https://wslab.csie.ntu.edu.tw/category/tutorial/)</span>
