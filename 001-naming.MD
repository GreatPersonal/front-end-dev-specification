# 命名:
> 文件/变量/方法/class/id/组件/

><font color="#dd0000">注意事项：所有命名方式均采用英文或者组合方式，清晰明朗，不允许使用汉字、拼音、字母简写</font><br /> 
## 变量命名:
+ 一般情况下,取有意义的英文单词作为变量名(如下参考表)
+ 尽量短,语义准确(如:status/state这种情况)

## 方法命名:
+ 传入参数：尽量短,语义准确(如:status/state这种情况)
+ 命名可以长一点,但一定语义准确,使用驼峰规则，不加额外符号作为命名字符，不要去做代码压缩工具帮你做的事情(如：getQueryString/getData/getDocumentData)

## 文件命名：
+ 统一使用英文命名
+ 以中划线分割，如:tabbar.js 或者 `user-info.js`
+ 如果user-info.js里的是class，则以`UserInfo`的方式来命名
+ 有种文件是这个模块里的private模块，可以以`_`开头
+ 在一些编辑器里，模块的配置文件，希望显示在第一个，也会以`_`开头，如：`_config.js`
+ html、js、css共用base.css，首页文件命名使用统一的index(index.html/index.js/index.css)
## 类命名:
+ 大写，有意义
+ 几个单词的组合
+ 宁可名字长，也要一目了然（当然，尽量不要生僻）

##代码格式规则
+ 用4个空格缩进
+ 括号开头不要另起一行
+ 不要写只有一行的if , 以及不要省略 if else 的花括号
+ const > let > var
+ 不要省略分号
+ 类型用 PascalCase, 其他用 camelCase
+ 一行不要过长. 基本上原则是永远不应该需要用鼠标滚动才能看全

作者：李正博
链接：https://www.zhihu.com/question/55701103/answer/146488329
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
## DIV+CSS命名参考表:
|CSS样式命名	|说明|备注|
| ------------ | :----------- | :---- |
| #wrapper|	页面外围控制整体布局宽度 |
| #container或#content|	容器,用于最外层 |
| #layout|	布局 |
| #head, #header|	页头部分 |
| #foot, #footer|	页脚部分 |
| #nav	|主导航 |
| #subnav	|二级导航 |
| #menu	|菜单 |
| #submenu	|子菜单 |
| #sideBar	|侧栏 |
| #sidebar_a, #sidebar_b	|左边栏或右边栏 |
| #main	|页面主体 |
| #tag	|标签 |
| #msg #message	|提示信息 |
| #tips	|小技巧 |
| #vote	|投票 |
| #friendlink|	友情连接 |
| #title|	标题 |
| #summary	|摘要 |
| #loginbar	|登录条 |
| #searchInput	|搜索输入框 |
| #hot|	热门热点 |
| #name_search	|名称+下划线+搜索 |例如：baidu_search|
| #name_search_output|名称+下划线+搜索输出和搜索结果相似 |例如：baidu_search_output
| #searchBar|	搜索条 |条件同上
| #search_results	|搜索结果 |条件同上
| #copyright|	版权信息 |
| #branding	|商标 |
| #logo	|网站LOGO标志 |
| #siteinfo|	网站信息 |
| #siteinfoLegal	|法律声明 |
| #siteinfoCredits	|信誉 |
| #joinus	|加入我们 |
| #partner	|合作伙伴 |
| #service	|服务 |
| #regsiter	|注册 |
| arr/arrow	|箭头 |
| #guild|	指南 |
| #sitemap	|网站地图 |
| #list	|列表 |
| #homepage	|首页 |
| #subpage	|二级页面子页面 |
| #tool, #toolbar|	工具条 |
| #drop	|下拉 |
| #dorpmenu	|下拉菜单 |
| #status	|状态 |
| #scroll	|滚动 |
| .tab	|标签页 |
| .left .right .center	|居左、中、右 |
| .news	|新闻 |
| .download	|下载 |
| .banner	|广告条(顶部广告条) |
| .products	|产品 |
| .products_prices	|产品价格 |
| .products_description	|产品描述 |
| .products_review	|产品评论 |
| .editor_review|	编辑评论 |
| .news_release	|最新产品 |
| .publisher|	生产商 |
| .screenshot|	缩略图 |
| .faqs	|常见问题 |
| .keyword	|关键词 |
| .blog	|博客 |
| .forum|	论坛 |



| CSS文件命名          | 说明       |
| -------------------- | :--------- |
| master.css,style.css | 主要的     |
| module.css           | 模块       |
| base.css             | 基本共用   |
| layout.css           | 布局，版面 |
| themes.css           | 主题       |
| columns.css          | 专栏       |
| font.css             | 文字、字体 |
| forms.css            | 表单       |
| mend.css             | 补丁       |
| print.css            | 打印       |
 然后一些div包含的元素的命名可以以div名字为前缀再加其所在位置属性的英文名缩写