#微信公众平台demo

##注意本教程和代码以PHP作为示例

***
##网页授权获取用户基本信息

###一、操作步骤
***
####在新浪SAE上申请服务器资源
####新建空白的PHP项目
####详见http://jingyan.baidu.com/article/72ee561a432145e16138dff2.html
***
####打开[微信测试公众号申请页面](http://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login)

![login](http://i4.tietuku.com/b5ad7160dee85181.png)

####点击登录按钮，弹出二维码页面，打开手机微信，扫一扫扫描二维码登录

***
####登陆后进入配置界面，点击修改

![setting](http://i4.tietuku.com/d15da7b7649c9aa9.png)
***
####输入申请SAE时给的域名地址，作为回调页面域名，点击确认

![website](http://i4.tietuku.com/851c6208ac17a441.png)

***
####上传代码时修改lib.php中的appID和appsecret两个字段

![php](http://i4.tietuku.com/3127ebdbe2b3e690.png)

####两个字段可在登录测试号时查看到

![check](http://i4.tietuku.com/1d31d46f5af72ccd.png)
***
##以我的测试公共号为例，先关注微信号

![qrcode](http://i4.tietuku.com/00bd19820e0317dd.png)

##在微信中打开（注意只能在微信中打开）点击链接地址：

####https://open.weixin.qq.com/connect/oauth2/authorize?appid=wx337bf9978d09b6be&redirect_uri=http://zycac.sinaapp.com/user_info.php&response_type=code&scope=snsapi_userinfo&state=STATE#wechat_redirect

#####地址参数说明：

>appid 公众号的唯一标识

>redirect_uri 授权后重定向的回调链接地址，请使用urlencode对链接进行处理

>response_type 返回类型，请填写code

>scope 应用授权作用域，snsapi_base （不弹出授权页面，直接跳转，只能获取用户openid），snsapi_userinfo （弹出授权页面，可通过openid拿到昵称、性别、所在地。并且，即使在未关注的情况下，只要用户授权，也能获取其信息）

>wechat_redirect 无论直接打开还是做页面302重定向时候，必须带此参数

##在微信客户端中点击链接进入进入后即可查看获取的字段
