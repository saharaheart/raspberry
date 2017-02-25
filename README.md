# raspberry
the basic tutorial of the raspberry
this tutorial will show how to use a laptop(or desktop) with ubuntu operating system to configure a raspberry with ethernet.
1.fisrt we need a TF card with your favourite operating system installed in it.(this can be easily found on the Internet)
we need to modify the cmdline.txt file which is in the TF card.
we add ip = 192.168.1.2 in the last and save the file
2.In the Ubuntu system on your computer,check all the Internet connections.
    use   $ ifconfig -a    (this will show all kinds of Internet connections)
    (It is important to know that there is lo,ethernet... and it may not performed like the usual format listed below,sometimes use en~~ to stand ethernet while wl~~ to stand wlan )
    lo  -- 回环接口
    eth0~9  --以太网
    br0 --网桥接口
    wlan0 --无线接口
    
    (UP代表网卡开启状态，RUNNING表示网卡的网线被接上，MULTICAST支持组播，MTU：～～ 最大传输单元～～字节)
3.sometimes we find that our ethernet do not have an    inet addr and have only inet6 addr.
so we need to command
sudo dhclient (here is the name of the ethernet)
4.use $ifconfig (ethernet-name) | grep inet
will show the inet addr
5.use $sudo ifconfig (ethernet-name) 192.168.1.4
to set the port of the pc
6.use 
ping 192.168.1.2
to check if it can operate correctly
7. use & ssh pi@192.168.1.2 
to access the raspberry.

here you can refer this link 
https://xusiwei.github.io/post/2016/raspberry-pi-headless-setup/



    
    
