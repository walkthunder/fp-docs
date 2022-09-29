# ⚙ 七牛云

配置项及说明：

```
{
  "accessKey": "",
  "secretKey": "",
  "bucket": "", // 存储空间名
  "url": "", // 自定义域名
  "area": "z0" | "z1" | "z2" | "na0" | "as0", // 存储区域编号
  "options": "", // 网址后缀，比如?imgslim
  "path": "" // 自定义存储路径，比如img/
}
```

![image](https://user-images.githubusercontent.com/12621342/34243072-191cc4ae-e65a-11e7-99f6-ebe6b7dcaf86.png)

对应的密钥信息需要到七牛自己的[控制台](https://portal.qiniu.com/user/key)里找到。其中需要注意的是，自己的存储空间的区域需要确定：

![image](https://user-images.githubusercontent.com/12621342/34243146-69af085a-e65a-11e7-965c-2a3d15856480.png)

在配置文件里，存储区域对应的键是`area`，值是下图所示（如果你是用PicGo-Core或者其他非electron版本的PicGo请注意此项），比如华东的话就是`z0`。完整的存储区域[点击这里](https://developer.qiniu.com/kodo/1671/region-endpoint-fq)查看。

![image](https://user-images.githubusercontent.com/12621342/50533009-e5189100-0b5c-11e9-9812-438576990828.png)

在配置文件里，存储空间需要

设定上传地址是指七牛云 ~~自动分配给你的网址，或者~~ 是你自己绑定的域名（**注意要加`http://`或者`https://`**）：

![image](https://user-images.githubusercontent.com/12621342/34245183-c38d9766-e663-11e7-964e-2d7a9ab9e9e9.png)

网址后缀通常是你用到了七牛的图片处理工具的时候会用到的一些处理参数，比如图片瘦身。
