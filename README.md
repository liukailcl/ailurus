简介
=======

小熊猫微信开发框架是一个便利的微信公众平台开发框架，
基于此框架，开发者可以便利开发：

* 基于信息上行的应用
* 朋友圈文章发布系统

快速开始
=======

请参考文章<http://lazy.changes.com.cn/html/655.html>

通过SAE应用商店可以快速安装：<http://sae.sina.com.cn/?m=apps&a=detail&aid=164>


运行环境
=======

本系统基于SAE运行，依赖MySQL和Memcache、Storage服务，并依赖于config.yaml。
请默认开启：

* storage服务并创建domain `upload`
* 初始化mysql服务
* 初始化memcache服务并至少提供2M空间

你没有使用过SAE，请访问<http://sae.sina.com.cn>了解。

token
=======
token是用户在创建微信应用时需要填写的长度大于七位的数字和字母的组合。此token用于验证上行接口。

上行短信处理类
=======
上行短信处理类为处理上行微信信息，给出响应的类。请填写完整的处理文件名称，并放置于 根目录/lib/ 下。文件中的类名请填写微信应用名+Chat,如myappChat，在找到处理类的时候，会启用default_chat.class.php，使用defaultChat处理上行信息。

处理类请继承Chat类，默认实现

* onSubscribe
* onScanonUnsubscribe
* onEventLocation
* onText
* onImage
* onLocation

函数，具体可以参考default_chat.class.php。

接口地址
=======
在应用列表中生成的接口地址是填写于微信公众平台后台的`URL`，包含了接口认证和上行消息的处理。

广告
=======
广告用于cms文章的底部广告，建议可以给出微信公众帐号的二维码和一些介绍信息，以图片的方式提供，如果创建的微信应用包含广告，在生成文章时会默认在文章的底部带上该广告，如果不想附带，可以从此处删除广告图片。

二维码
=======
在非手机浏览器访问生成的文章时，底部会默认带上`分享到微信`按钮，点击会出现一个二维码引导访问者微信扫码分享到朋友圈。

开发团队
=======
* [lazypeople](http://weibo.com/1222673811 "lazypeople")
* [菜菜月儿](http://weibo.com/2095880214 "菜菜月儿")
* [Howls_Castle](http://weibo.com/2076600723 "Howls_Castle")
