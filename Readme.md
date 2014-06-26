---

Title: 关于 FarBox 模板 GrayshadeLight 的使用说明
Date: 2014-06-23 23:41
Tags: FarBox 主题 模板 技术杂烩

---

本模板是从[IF404](http://blog.if404.com/)的[GrayshadeM](https://github.com/mapleobserver/FarBox-Template-GreyshadeM)模板修改而来。[GrayshadeM](https://github.com/mapleobserver/FarBox-Template-GreyshadeM)模板比较艳丽，而本人比较喜欢清爽的分割，因此，将模板的默认风格改的比较清淡。

##相比[GrayshadeM](https://github.com/mapleobserver/FarBox-Template-GreyshadeM)，主要修改如下：

-默认模板左边栏改为白色背景
-去掉了左边栏的头像（在淡色背景下很难对齐，显得比较突兀）
-去除了对google fonts、外部jQuery的引用，以提高加载速度
-增加了一些属性允许对左侧边栏的背景色、字体颜色进行定制


##网站自定义参数配置

如果需要修改本模板的自定义项，需要在网站目录（比如 `FarBox/My Blog/` ）下放置一个名为 `site.md` 的文件，如下是一个范例：

    title: 南方更南
    subtitle: doc001's blog
    author: doc001
    authorinfo: 醉的人们呀举起杯，笑得眼里都是泪
    facebook: http://facebook.com
    google: http://plus.google.com
    twitter: http://twitter.com
    github: http://github.com
    linkedin: http://linkedin.com
    pinterest: http://pinterest.com
    delicious: http://delicious.com
    pinboard: http://pinboard.com
    instagram: http://instagram.com
    weibo: http://weibo.com
    qq: http://t.qq.com
    qq2: http://wpa.qq.com/msgrd?v=3&uin=123456&site=qq&menu=yes
    qqqun: http://wp.qq.com/wpa/qunwpa?idkey=1234567890abcdefghijklmn
    qqqunname: QQ群名字
    weixin: 我叫微信
    douban: http://douban.com
    fanfou: http://fanfou.com
    zhihu: http://zhihu.com
    email: mailto:123@abc.com
    rss: /feed
    alipay: http://me.alipay.com/123456
	highlight: true
    sidebar_background: white
    sidebar_color: "#666"
    sidebar_color_hover: "#1593c9"
    sidebar_subtitle_color: "#999"


格式说明：

**title**
> 添加该属性，网站左侧将显示博客名称。

**subtitle**
> 添加该属性，网站左侧博客名称下方将显示网站副标题。

**author**
> 添加该属性，网站底部将显示版权信息，包含作者笔名。

**authorinfo**
> 添加该属性，网站左侧将显示作者自我介绍。

**社交链接**
> 目前支持 Facebook、Google+、Twitter、GitHub、Linkedin、Pinterest、Delicious、Pinboard、Instagram、新浪微博、腾讯微博、QQ、QQ群、微信、豆瓣、饭否、知乎、EMail、RSS订阅 。对应属性请参考上面的范例。

> 默认显示为不同颜色圆形图案，如果要显示 Logo ，可在博客文件夹中新建 `\images\social\` 文件夹，放入和属性相同名字的 png 文件，注意图片尺寸不要超过 30x30 ß。

**QQ社交链接 & QQ群社交链接**
> QQ社交链接属性为 `qq2` ，通过 [wp.qq.com](http://wp.qq.com/ "QQ在线状态") 获取代码，例如：  
> `<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=123456&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:123456:53" alt="点击这里给我发消息" title="点击这里给我发消息"/></a>`  
> 在属性中填入上述范例代码中的 `http://wpa.qq.com/msgrd?v=3&uin=123456&site=qq&menu=yes`  
> 该功能无法实现QQ在线离线状态的图片切换，点击社交图标即可弹出QQ对话窗口。  
> QQ群社交链接属性为 `qqqun` ，设置方法和QQ社交链接一样。  
> 另有 `qqqunname` 属性，可添加QQ群的群名称，鼠标覆盖社交图标时会显示。

**微信社交链接**
> 微信社交链接的属性为 `weixin` ，填入微信个人或者公众账号即可。  
> **务必要在 `images/social/` 文件夹中放入二维码文件，命名为 `weixinqrcode.png` ，二维码图片会被自动压缩或拉伸到 160 像素宽高的正方形图片。**  
> 鼠标覆盖微信图标时，会显示微信账号，同时*顶部作者头像会变成微信二维码图片*，移开鼠标则恢复显示头像。点击微信图标将在新窗口打开二维码图片，方便手机用户操作。   

**支付宝付费功能**
> 通过添加 `alipay` 属性，可以在文章底部显示支付宝付款内容，网友若觉得文章有用，可以通过支付宝收款主页向博客作者付款。

**代码高亮**
> 添加 `highlight` 属性，可以使文章中的代码高亮着色，属性值任意，比如 `true` 。有需要代码高亮的童鞋可以使用。
> 该功能利用 *Pygments* 功能实现，我采用的是 Pygments 的 monokai 样式，本模板控制代码高亮着色的 css 文件为 `highlight.css` 。  
> 有兴趣自定义高亮样式的童鞋可以参考：  
> [Farbox 代码高亮语法](https://github.com/hepochen/FarBox-Doc/blob/master/docs/%E4%B9%A6%E5%86%99/%E4%BB%A3%E7%A0%81%E9%AB%98%E4%BA%AE.md "FarBox 代码高亮语法")
> [Pygments 代码高亮样式](http://pygments.org/ "Pygments 代码高亮样式")
> [Pygments CSS文件](https://github.com/richleland/pygments-css "Pygments CSS文件")

**左侧边栏定制**
> sidebar_background：用于定制左侧边栏的背景色，默认为white
> sidebar_color：用于定制左侧边栏处副标题外的字体颜色，默认为"#666"
> sidebar_color_hover：用于定制左侧边栏链接悬停颜色，默认为"#1593c9"
> sidebar_subtitle_color：用于定制左侧边栏副标题字体颜色，默认为"#999"

##其它

左侧边栏属性不定义的时候，以默认值进行显示。但是Farbox存在一个bug，就是属性只能增加，不能删除（也许是我没找到怎么删除）。因此，一旦定制过左侧边栏之后，只能通过设置属性来恢复默认值，直接删除是没有用的。
模板还有很多不尽如意的地方，例如，相册的显示就不够好。暂时放着，作为后续的修改工作。

##显示效果

见[显示效果](http://doc001.farbox.com/post/2014-06-23#content)