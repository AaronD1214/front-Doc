# HTML代码规范

## 语言规范

  1. `doctype`声明使用`html5`。

    ```html
    <!doctype html>
    ```

  2. 统一页面编码格式为`utf-8` , `meta`标签`charset`设置为`utf-8`;

    ```html
    <meta charset="utf-8" />
    ```

  3. `<head>`中添加信息。

    <meta name="author" content="smile@kang.cool">  //作者
    <meta name="description" content="hello">  //网页描述
    <meta name="keywords" content="a,b,c">  //关键字,“，”分隔
    <meta http-equiv="expires" content="Wed, 26 Feb 1997 08：21：57 GMT">  //设定网页的到期时间。一旦网页过期，必须到服务器上重新调阅
    <meta http-equiv="Pragma" content="no-cache">  //禁止浏览器从本地机的缓存中调阅页面内容
    <meta http-equiv="Window-target" content="_top">  //用来防止别人在框架里调用你的页面
    <meta http-equiv="Refresh" content="5;URL=http://kahn1990.com/">  //跳转页面，5指时间停留5秒 网页搜索机器人向导。用来告诉搜索机器人哪些页面需要索引，哪些页面不需要索引
    <meta name="robots" content="none">  //content的参数有all,none,index,noindex,follow,nofollow，默认是all
    <link rel="Shortcut Icon" href="favicon.ico">  //收藏图标
    <meta http-equiv="Cache-Control" content="no-cache, must-revalidate">  //网页不会被缓存

    IE支持通过特定<meta>标签来确定绘制当前页面所应该采用的IE版本。除非有强烈的特殊需求，否则最好是设置为edge mode ，从而通知IE采用其所支持的最新的模式。

    <meta http-equiv="X-UA-Compatible" content="IE=Edge">

  4. 标签、标签属性全部小写。

    **(推荐写法)**

    ```html
    <a href="/" data-attr="attr">Home</a>

    ```

    **(不推荐写法)**

    ```html
    <A HREF="/" attr="attr">Home</A>
    ```

  5. 所有html标签必须有结束符，`<img />`, `<col />`, `<base />`, `<link />`, `<meta />`, `<input />` 除外。

  6. 标签自定义属性使用`data-name="value"`的形式来写, 如果自定义属性特别多, 可以考虑使用标准 json 的方式去写: `data-json='{"a":"a", "b":"b"}'`。

    **(推荐写法)**

    ```html
    <div data-json='{"a":1, "b":true, "c":[1, 2]}' ></div>
    ```

    **(不推荐写法)**

    ```html
    <div data-json="{a:1, b:true, c:[1, 2]}" ></div>
    <!--对于这样的写法,直接JSON.parse会出错-->
    ```

  7. 对于 JS 钩子, 以 `jCamelCase` 的驼峰形式来命名。

  8. 对于普通`class`或者`id`命名（此处id仅做样式，不做js钩子）, 统一使用小写字母, 第一个字符必须为字母, 连接符用中划线 `-`。

    **(推荐写法)**

    ```html
    <div class="sns-box"></div>
    <div class="box"></div>
    ```

    **(不推荐写法)**

    ```html
    <div class="Sns-box"></div>
    <div class="snsBox"></div>
    <div class="Box"></div>
    ```

  9. css 引用置于头部`<head>`标签内。

  10. js 引用置于底部`</body>`标签前。

## 标签使用

  1. `<base>`标签必须放在`<head>`内。

  2. `<strong>`标签用于强调重要性, `<em>`标签用于表示内容的着重点。[参考](http://www.css88.com/archives/644)

  3. 当`link`元素用于引用CSS文档时, 默认`media`是`screen`, 如为特殊终端提供样式, 请指定`media`属性, 如`media=“print”`;

  4. `img`标签必须加`alt`，尤其是logo、商品图片等关键图片信息，对SEO友好。

## 注释规范

  1. 主要的`html`模块需加注释

  2. 修改别人代码时, 加入修改信息。至少加入修改者大名和修改时间。

    ```html
    <!--主要修改IE8浏览器兼容性问题 djune 2013-09-26 13:21 -->
    ```

## 其他注意

  1. 开发时页面原则上不内嵌`style`、`script`代码，如特殊情况请标明并注释。

  2. 缩进以4个空格为基本单位，为每个块级元素或表格元素标签新起一行，并且对每个子元素进行缩进。[参考](http://www.cnblogs.com/kungfupanda/archive/2012/09/05/2671597.html)
