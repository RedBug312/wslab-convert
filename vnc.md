# Using VNC

If you need to use VNC for GUI, please log in to any workstation. In
this tutorial, we use linux1 as example.

1.  execute `vncserver`

        ACCOUNT@linux1:~$ vncserver

    and you will see the following message:

        New 'linux1:1 (ACCOUNT)' desktop is linux1:1
        Starting applications specified in /home/dept/ta/lydian/.vnc/xstartup  
        Log file is /home/dept/ta/ACCOUNT/.vnc/linux1:1.log

2.  If you haven’t used VNC server before, you will be asked to set a
    password. This password is needed when you are to log in to your VNC
    server.
3.  After that, please view  ~/.vnc/linux1:1.log , and you will see the
    following log:

        Xvnc Free Edition 4.1.1 - built Mar 10 2010 22:35:30

        Copyright (C) 2002-2005 RealVNC Ltd.
        See http://www.realvnc.com for information on VNC.
        Underlying X server release 40300000, The XFree86 Project, Inc

        Mon Apr 9 15:18:50 2012
        vncext: VNC extension running!
        vncext: Listening for VNC connections on port 5901 
        vncext: created VNC server for screen 0```

    The line

        vncext: Listening for VNC connections on port 5901

    tells the connection port.

4.  Open your VNC client (e.g. VNC-Viewer)  
    **Server** is the machine you execute `vncserver`, in this case, it
    would be linux1.csie.ntu.edu.tw.  
    **Port** is the number in the previous step.

5.  Enjoy it!

<span class="entry-title">Using VNC</span>

Tagged on:
[gui](https://wslab.csie.ntu.edu.tw/tag/gui/)    [vnc](https://wslab.csie.ntu.edu.tw/tag/vnc/)

<span class="by-author author vcard">[Ting-Yen
Lee](https://wslab.csie.ntu.edu.tw/author/lydian/){.url .fn .n}</span>
<span
class="date">[2012-04-092014-09-25](https://wslab.csie.ntu.edu.tw/2012/04/vnc/ "3:27 PM")</span>
<span
class="category">[Tutorial](https://wslab.csie.ntu.edu.tw/category/tutorial/)</span>
