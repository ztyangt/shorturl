##  介绍

一个基于Python-Flask框架开发的短网址生成器，数据库使用python内置的Sqlite3，直接部署即可使用，不需额外再创建数据库。同时提供短网址生成API与心灵毒鸡汤API。


![短网址生成器](https://qiniu.ztyang.com/picgo/blog-short.png-yasuo)

[点击预览](https://surl.ztyang.com)

## 短网址API

> 1. 方法: GET, POST
> 2. 接口: http(s)://[域名]/api

| 参数 | 必选 | 类型   | 说明             |
| ---- | ---- | ------ | ---------------- |
| url  | 是   | string | 需要转换的长链接 |

请求返回的数据结构:

```json
{
    "code": 200,
    "data": {
        "creatTime": "2022-09-12 15:02:26",
        "longUrl": "https://www.ztyang.com",
        "shortID": "6zTC11",
        "shortUrl": "http://127.0.0.1:5000/6zTC11"
    },
    "msg": "短链接创建成功!"
}
```



## 心灵毒汤API

> 1. 方法: GET,
> 2. 接口: http(s)://[域名]/soup
> 3. 参数: 无

请求成功返回的数据结构:

```json
{
    "code": 200,
    "data": {
        "id": 432,
        "text": "遇到闪电记得要微笑，因为那是天空在给你拍照。"
    }
}
```

## 安装

这里以宝塔为例：

1. 首先在宝塔软件商店里安装`python项目管理器v`

![](https://qiniu.ztyang.com/picgo/image-20220912173522952.png-yasuo)

1. 将源码上传到宝塔任一指定的网站目录，如下图所示：

![](https://qiniu.ztyang.com/picgo/20220912170551.png-yasuo)

3. 打开python项目管理器，填写相关安装信息：

![](https://qiniu.ztyang.com/picgo/20220912170641.png-yasuo)

> 注意：端口号需要提前打开，不然部署后会无法访问网站

4. 域名映射，将域名解析到项目所部署的服务器，填写域名：

![](https://qiniu.ztyang.com/picgo/20220912170724.png-yasuo)

5. 部署完成

![](https://qiniu.ztyang.com/picgo/20220912173247.png-yasuo)
