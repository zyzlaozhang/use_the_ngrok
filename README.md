# use_the_ngrok
本教程会教你使用ngrok内网穿透


## 第一步，注册ngrok
首先，我们去往[ngrok官网](https://ngrok.com/)注册一个ngork账户或者是使用github登录

[![image.jpg](https://i.postimg.cc/tR6dgKCt/image.jpg)](https://postimg.cc/XXVBHD5p)

## 第二布，获取密钥
如果不将ngork客户端进行一个绑定，ngrok则无法显示html文件
所以我们先要获取密钥。

在设置页面，找到
> getting started
> > **your authtoken**

进入 your authtoken 页面，点击copy就可以把你的密钥复制到剪切板

[![tempsnip.jpg](https://i.postimg.cc/QCdf2S1n/tempsnip.jpg)](https://postimg.cc/5YD5vBPw)

## 第三步，下载ngrok/绑定ngrok

[![233.jpg](https://i.postimg.cc/s2cn2tjg/233.jpg)](https://postimg.cc/sBMP6HGk)

下载ngrok并且解压，放置在任意文件夹内

打开**ngrok.exe**，输入以下命令

```cmd
  ngrok config add-authtoken 你的密钥
```

[![256.jpg](https://i.postimg.cc/wxJ6bV0j/256.jpg)](https://postimg.cc/yW14D0MM)

此时ngrok就和你绑定完成了

## 第四步，开始使用

打开**ngrok.exe**，输入以下命令


```cmd
  ngrok.exe http 你要穿透的端口
```

[![233.jpg](https://i.postimg.cc/Yqbv2Rgz/233.jpg)](https://postimg.cc/nC9F0v3X)

然后你就可以见到一个新的页面

在 **forwarding** 后面就是你映射后的网址

_提示，那个域名是由ngrok随机生成，固定域名需要购买**vip**_

[![kkk.jpg](https://i.postimg.cc/pXGdMTb0/kkk.jpg)](https://postimg.cc/QH7DpjM5)

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

[![455.jpg](https://i.postimg.cc/8547Fm9G/455.jpg)](https://postimg.cc/dk7sprJN)

嗯访问成功:v::v::v:

[![678.jpg](https://i.postimg.cc/bvTyLNTH/678.jpg)](https://postimg.cc/DWS3whR8)

:laughing::laughing::laughing::laughing::laughing::laughing::laughing::laughing::laughing::laughing:
