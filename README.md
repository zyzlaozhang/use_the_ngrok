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

[![bTg0C.jpg](https://s1.328888.xyz/2022/08/22/bTg0C.jpg)](https://imgloc.com/i/bTg0C)

下载ngrok并且解压，放置在任意文件夹内

打开**ngrok.exe**，输入以下命令

```cmd
  ngrok config add-authtoken 你的密钥
```

[![bTJmB.jpg](https://s1.328888.xyz/2022/08/22/bTJmB.jpg)](https://imgloc.com/i/bTJmB)

此时ngrok就和你绑定完成了

## 第四步，开始使用

打开**ngrok.exe**，输入以下命令


```cmd
  ngrok.exe http 你要穿透的端口
```

[![bTtkR.jpg](https://s1.328888.xyz/2022/08/22/bTtkR.jpg)](https://imgloc.com/i/bTtkR)

然后你就可以见到一个新的页面

在 **forwarding** 后面就是你映射后的网址

_提示，那个域名是由ngrok随机生成，固定域名需要购买**vip**_

[![bTytP.jpg](https://s1.328888.xyz/2022/08/22/bTytP.jpg)](https://imgloc.com/i/bTytP)

## 第五步，测试

我在本地起了一个flask项目


```python
    from flask import Flask
    app=Flask(__name__)
    
    @app.route('/')
    def index():
      return "hello_world"
    
    if __name__=="__main__":
      app.run(host='0.0.0.0',debug=True,port=80)
```
然后启动ngrok，并且访问

点击**visit site**
[![bTAyE.jpg](https://s1.328888.xyz/2022/08/22/bTAyE.jpg)](https://imgloc.com/i/bTAyE)

嗯访问成功:v::v::v:

[![bTWfi.jpg](https://s1.328888.xyz/2022/08/22/bTWfi.jpg)](https://imgloc.com/i/bTWfi)

:laughing::laughing::laughing::laughing::laughing::laughing::laughing::laughing::laughing::laughing:
