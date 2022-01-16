# py_wechat
使用python爬取指定微信公众号的文章

先如今我知道的有两种思路：
第一种思路：进入公众号管理平台，在那个网页里进行爬取，但是速度不可过快，否则会被封，缺点是爬的很慢，不太稳定
第二种思路：使用fiddler对指定公众号进行抓包，通过过滤出微信文章，然后把json格式的数据包全都保存到本地，再使用json批量进行数据提取

两种方法都试过，但是最好使用第二种思路，本次我就是用的第二种思路
要记得设置过滤条件：mp.weixin.qq.com/mp/profile_ext?action=getmsg

我抓包抓出来的是这样的

![image](https://user-images.githubusercontent.com/58964582/149646422-44580281-39e9-425d-8f6a-7d40dc5be83d.png)

格式化后是这样

![image](https://user-images.githubusercontent.com/58964582/149646442-90f1caf3-8729-4223-89f6-1d12278497f7.png)

然后使用python获取里面标题、发布时间、文章url等等
我保存在excel里面的

![image](https://user-images.githubusercontent.com/58964582/149646474-bdd35ae4-0a5b-422f-9f59-1366636bb5b4.png)

当然也可以把网页下载到本地，或者转成PDF格式

![image](https://user-images.githubusercontent.com/58964582/149646634-bb6d54e6-0c1a-44a5-827e-87de0e4c40c4.png)

网页里的图片可以保存在PDF中，视频就不能保存了。
本项目是因为需要查看很多文章做数据分析，做研究。

本次只是提供思路，并不进行恶意爬取。
请勿用于商业用途，否则一切后果自行承担。
