## D-Link Routers Command Injection
### Info
Demo product: D-Link DIR-878 (Refer: [https://support.dlink.com/productinfo.aspx?m=DIR-878](https://support.dlink.com/productinfo.aspx?m=DIR-878))  
Version: The latest firmware -- v1.30b10Beta (Refer: [https://support.dlink.com/productinfo.aspx?m=DIR-878](https://support.dlink.com/productinfo.aspx?m=DIR-878))  
![](./pics/1.png)
![](./pics/2.png)
Vulnerability Type: Command Injection  
Affected versions:  DIR-878(v1.30b10Beta & Below), DIR-882(v1.30b10Beta & Below), DIR-867(v1.20b10Beta & Below)
Author: c014  
Institution: Shanghai Jiao Tong University  

 
### POC
There are some filters in front end, we can use burpsuite to bypass it.
![](./pics/9.png)
![](./pics/10.png)
When we click `save`, it will generate 2 requests, the first one is an authentication. We need to `Forward` it quickly or we will get a "no device found" error.
![](./pics/11.png)
Then add evil command here:
![](./pics/12.png)

Then we can see changed successfully:
![](./pics/13.png)

Finally getshell:
![](./pics/14.png)


