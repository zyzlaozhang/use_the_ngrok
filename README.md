# use_the_ngrok
本教程会教你使用ngrok内网穿透


## 第一步，注册ngrok
首先，我们去往[ngrok官网](https://ngrok.com/)注册一个ngork账户或者是使用github登录

[![bTUeU.jpg](https://s1.328888.xyz/2022/08/22/bTUeU.jpg)](https://imgloc.com/i/bTUeU)

## 第二布，获取密钥
如果不将ngork客户端进行一个绑定，ngrok则无法显示html文件
所以我们先要获取密钥。

在设置页面，找到
> getting started
> > **your authtoken**

进入 your authtoken 页面，点击copy就可以把你的密钥复制到剪切板

[![bT8od.jpg](https://s1.328888.xyz/2022/08/22/bT8od.jpg)](https://imgloc.com/i/bT8od)

## 第三步，下载ngrok/绑定ngrok

下载ngrok并且解压，放置在任意文件夹内

打开**ngrok.exe**，输入以下代码

```cmd
  ngrok config add-authtoken 你的密钥
```



