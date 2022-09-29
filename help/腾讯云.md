# ⚙ 腾讯云

配置项及说明：

```
{
  "secretId": "",
  "secretKey": "",
  "bucket": "", // 存储桶名，v4和v5版本不一样
  "appId": "",
  "area": "", // 存储区域，例如ap-beijing-1
  "path": "", // 自定义存储路径，比如img/
  "customUrl": "", // 自定义域名，注意要加http://或者https://
  "version": "v5" | "v4" // COS版本，v4或者v5
}
```

> 从PicGo v1.5版本开始，支持COSv4和v5版本。

[**#**](https://picgo.github.io/PicGo-Doc/zh/guide/config.html#v4%E7%89%88%E6%9C%AC%E8%AF%B4%E6%98%8E)**V4版本说明**

v4版本是这个：

![image](https://user-images.githubusercontent.com/12621342/35483306-5e7ed570-047b-11e8-95a9-d56a3b4d2ba9.png)

需要登录腾讯云控制台。打开[密钥管理](https://console.qcloud.com/cos4/secret)

![image](https://user-images.githubusercontent.com/12621342/34243294-082c97cc-e65b-11e7-9412-dbc86433a91d.png)

按照对应的提示找到自己的`APPID`、`SecretId`、`SecretKey`。

存储的空间名是你的bucket名字。

存储的区域需要额外注意，请到bucket列表里打开需要上传的bucket空间，然后如图可以看到对应的区域以及区域代码，比如我的是`tj`：

![image](https://user-images.githubusercontent.com/12621342/34243443-befa715e-e65b-11e7-8404-aa5b8938a82b.png)

对应的区域代码如下：

![image](https://user-images.githubusercontent.com/12621342/34243476-edcc7798-e65b-11e7-8d59-8714cd0a59aa.png)

如果你想把图片上传到你的bucket空间的某个文件夹下，则需要在PicGo里的`指定存储路径`里加上你的文件夹路径。比如`temp/`（注意一定要加`/`）

[**#**](https://picgo.github.io/PicGo-Doc/zh/guide/config.html#v5%E7%89%88%E6%9C%AC%E8%AF%B4%E6%98%8E)**V5版本说明**

**1.** 获取你的APPID、SecretId和SecretKey

访问：https://console.cloud.tencent.com/cam/capi

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/get\_key\_id\_secret.png)

**2.** 获取bucket名以及存储区域代号

访问：https://console.cloud.tencent.com/cos5/bucket

创建一个存储桶。然后找到你的存储桶名和存储区域代号：

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/get\_bucket\_area.png)

v5版本的存储桶名称格式是`bucket-appId`，类似于`xxxx-12312313`。存储区域代码和v4版本的也有所区别，v5版本的如我的是`ap-beijing`，别复制错了。

**3.** 选择v5版本并点击确定

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/choose\_v5.png)

然后记得点击`设为默认图床`，这样上传才会默认走的是腾讯云COS。
