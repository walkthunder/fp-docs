# ⚙ 阿里云

配置项及说明：

```
{
  "accessKeyId": "",
  "accessKeySecret": "",
  "bucket": "", // 存储空间名
  "area": "", // 存储区域代号
  "path": "", // 自定义存储路径
  "customUrl": "" // 自定义域名，注意要加http://或者https://
}
```

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/aliyun.png)

首先先在阿里云OSS的[控制台](https://usercenter.console.aliyun.com/#/manage/ak)里找到你的`accessKeyId`和`accessKeySecret`： ![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/aliyun-key.png)

创建一个`bucket`后，存储空间名即为`bucket`:

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/aliyun-bucket.png)

确认你的[存储区域](https://www.alibabacloud.com/help/zh/doc-detail/31837.htm?spm=a2c63.p38356.a3.3.179112f0PBtYui)的代码：

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/aliyun-area.png)

也可以在bucket页面找到：

![](https://raw.githubusercontent.com/Molunerfinn/test/master/picgo/aliyun-bucket-2.png) 如上图，存储区域就是`oss-cn-beijing`

存储路径比如`img/`的话，上传的图片会默认放在OSS的`img`文件夹下。注意存储路径一定要以`/`结尾！存储路径是可选的，如果不需要请留空。
