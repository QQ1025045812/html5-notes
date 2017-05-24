# html5-notes
记录以前的一些笔记，慢慢更新
## 语义化标签
#####  结构语义
```
<header>页面头部</header>

<footer>页面底部</footer>

<nav>导航</nav>

<nav>
    <a href="#"></a>
    <a href="#"></a>
    <a href="#"></a>
</nav>

<hgroup>标题组合</hgroup>

<hgroup>
    <h1>马铃薯</h1>
    <h2>马铃薯是个...</h2>
</hgroup>

<section>划分区域</section>

<article>
    结构完整，独立部分
</article>

<aside>article/主体附属信息/友情链接</aside>
```
##### 内容语义
```
媒体

<figure>
    <img />
    <figcaption>描述</figcaption>
</figure>

时间

<time>12:00</time>

//datalist表示input可能会出现的值

<input type="text" list="bindid" />

<datalist id="bindid">
    <option value="javascript">javascript</option>
    <option value="css">css</option>
    <option value="html">html</option>
</datalist>

缩略信息

<details open>
    <summary>信息</summary>
    <p>内容</p>
</details>

<dialog open>
    <dt>老师</dt>
    <dd>2+2=？</dd>
    <dt>学生</dt>
    <dd>等于4</dd>
</dialog>

定义文章/页面作者信息
<address></address>

标记

<mark></mark>

进度条

<progress max="200" value="100">
    <span>76</span>%
</progress>
```
```
html5标签兼容html5shiv.js

原理document.createElement("header")

//自定义标签没有display等标签属性
```
##表单
```
<form>

    <input type="email">//手机切换到英文键盘

    <input type="tel">//手机切换到数字键盘

    <input type="url">//手机切换到数字键盘

    <input type="searck">//后面有一键清除内容

    <input type="range" step="2" min="0" max="30">//后面有一键清除内容

    <input type="number">

    <input type="color">

    <input type="datatime">//完整日期//////utc世界标准时间

    <input type="datatime">//完整日期

    <input type="datatime-local">//

    <input type="time">//时分

    <input type="date">//年月日

    <input type="week">//

     <input type="month">//

     //提示信息

     placeholder

     <input type="text" placeholder="请输入密码..." >

     //自动保存

      <input type="text" placeholder="请输入密码..." autocomplete="off" >

      //表单focus

       <input type="text" placeholder="请输入密码..." autocomplete="off" autofocus>

       //list   datalist

       //required

       //pattern//

       //formaction//保存到草稿箱//submit上定义提交地址

        <input type="submit" value="保存草稿箱"  formaction="http://www.baidu.com">

</form>
```
### 验证反馈
```

invalid


```

### 新的选择器

```
html5支持情况https://www.caniuse.com/#index

document.querySelector("#div1")//很像$  id  class tag [attr='']//  ie6\7不支持/////获取到第1个元素

document.querySelectorAll(".div1")//获取一组

document.getElementsByClassName()

```
### classList

```
//class集合

alert(oDiv.classList)

oDiv.classList.add()

oDiv.classList.remove()

oDiv.classList.toggle()/////

//
```
### JSON新方法

```
parsee()字符串变json------严格json格式字符串-------旧方法eval不安全，可以解析任何字符串成js语句

stringify()-----json转字符串，自动加上双引号

//浅拷贝
for(var attr in values){

}

//巧用深拷贝json.Stringify()---------字符串

//ie6，7不支持json

引入库http://www.json.org/

地址
https://github.com/douglascrockford/JSON-js

```
### 自定义属性
```
<div liu="yangyang"></div>

oDiv.dataset.miaov

jquerymobile中用的多（移动端框架）

http://knockoutjs.com/
```
### 延迟加载js
```
js的加载会影响后面的内容加载
很多浏览器都采用了并行加载js，但还是会影响其他内容

html5的defer和async

-defer：延迟加载会按顺序执行，在onload执行前被触发

-async：异步加载，加载完就触发，有顺序问题

Labjs库

```
## html5历史管理

```
onhashchange:改变hash值来管理

history：
----------服务器下运行

----------pushState:三个参数：数据 标题（都没实现） 地址（可选）

----------popState事件：读取数据 event.state

----------注意：网址是虚假的，需要在服务器指定对应页面，不然刷新找不到页面
```
