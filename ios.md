## IOS SDK 使用文档相关说明

* ##### 基本需求参数

```
@param:
    gameid (平台生成的游戏唯一标识)
    gamekey (平台生成的游戏key)
    channelid (推广渠道的编码)
```

* ##### 对接文档，SDK下载

```
@url : 
    SDK git 版本地址：https://github.com/wdgwgz/IOS-SDK/releases
    SDK 文档： https://github.com/wdgwgz/IOS-SDK/blob/master/Document/DBSDK%E4%BD%BF%E7%94%A8%E6%96%87%E6%A1%A3.pdf
```

* **特别说明**

```
SDK 初始化选择登录界面有预留游戏或品牌 logo ，默认情况无 logo
如果想显示游戏或者品牌 logo 请准备一张270*100像素（推荐尺寸）的 png 图片，并命名为 d_gamelogo 放入到 SDKResources.bundle！
充值SDK已经添加了蒙版，防止多次点击，请自行添加 Loading 动画
```



