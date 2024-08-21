# HTML语言

网页的扩展名是 .html

Html （超文本标记语言）使用标记标签来描述网页，包含视频、音频、图片等等

各个浏览器版本：[https://caniuse.com/](https://caniuse.com/)，查看某个关键词是否可用

VScode 安装：[https://code.visualstudio.com/](https://code.visualstudio.com/)

可以去插件库里下载 Chinese 汉化包、Auto Rename Tag 插件（可以跟着一起改标签）

view-in-browser 插件可以直接打开浏览器查看网页

Live Server 插件可以实时看到浏览器的变化

htmltagwrap 插件可以添加标签更快速，选中文本 ALT+W 就可以对文本前后加入标签

开发工具有很多：Visual Studio Code、Webstorm、Sublime、Dreamweaver、Hbuilder

```jsx
<!--
		html 根标签，一个页面有且只有一个根标签
-->
<!doctype html>
<!--
	H5 的文档声明，声明当前的网页是按照 H5 标准编写的，
	编写网页时一定要把该声明放在网页的最上边，
	如果不写文档声明，则会导致有些浏览器会进入一个怪异模式
-->
<html>
				<!--
					head 标签，该标签中的内容，不会在网页中显示，它用来帮助浏览器解析页面的
				-->
				<head>
								<!--
									title 网页的标题标签，默认会显示在浏览器的标题栏中
										搜索引擎在检索页面时，会首先检索 title 标签中的内容
										它是网页中对于搜索引擎来说最重要的内容，会影响到网页在搜索引擎中的排名
								-->
								<title>网页的标题</title>
				</head>
				<body>
							<!--
									在这个结构中，可以来编写 HTML 的注释
									注释中的内容，不会在页面中显示，但是可以在源码中查看
									我们可以通过编写注释来对代码进行描述，从而帮助其他的开发人员工作
							-->
							<!--
								属性：可以通过属性来设置标签，如果处理标签中的内容
									可以在开始标签中添加属性
									属性需要写在开始标签中，实际上是一个键值对的结构
									属性名="属性值"
									一个标签中可以同时设置多个属性，属性之间用空格隔开
							-->
							<h1>这是我的<font color="red" size=="4">第一个</font>网页</h1>
				</body>
</html>
```

### 字符集会影响网页显示乱码

```jsx
<!doctype html>
<html>
    <head>
        <!--
            需要来告诉浏览器，网页所采用的的编码字符集
            meta 标签用来设置网页的一些元数据，比如网页的字符集、关键字、简介
            meta 是一个自结束标签，编写一个自结束标签时，可以在开始标签中添加一个 /
            meta 里面的字符集编码要与 文件编辑器保存时的字符集一致，否则会乱码
        -->
        <meta charset="utf-8" />
        <title>网页的标题</title>
    </head>
</html>
```

### HTML 常用标签演示

```jsx
<!DOCTYPE html>
<html>
    <head>
        <meata charset="utf-" />
        <title>常用的标签</title>
    </head>
    <body>
        <!--
            标题标签
                在 HTML 中，一共有六级标题标签
                h1 ~ h6
                在显示效果上，h1最大，h6最小，但是文字的大小我们不关心
                6级标题中，h1 的最重要，表示一个网页中的主要内容，h2~h6 重要性依次降低
                    对于搜索引擎来说，h1 的重要性仅次于 title，搜索引擎检索完 title，会立即检查
                    h1 中的内容，h1 标签非常重要，它会影响页面在搜索引擎中的排名
                    一般页面中石油 h1~h3，h3 以后很少用
        -->
        <h1>一级标题</h1>
        <h2>一级标题</h2>
        <h3>一级标题</h3>
        <h4>一级标题</h4>
        <h5>一级标题</h5>
        <h6>一级标题</h6>
        <!--
            段落标签，用于表示内容中的一个自然段
            使用 p 标签来表示一个段落
            p 标签中的文字，默认会独占一行，并且段与段之间会有一个间距
        -->
        <p> 我是一个 P 标签，我来表示一个段落</p>
        <p> 我是一个 P 标签，我来表示一个段落</p>

        <!--
            在 HTML 中，字符之间写再多的空格，浏览器也会只当做一个空格解析，
            换行也会当做空格解析
        -->
        <p>
            锄禾日当午，<br/>
            汗滴禾下土，<br/>
            谁知盘中餐，<br/>
            粒粒皆辛苦。
        </p>
        <!--
            hr 是一个自结束标签，可以生成一个水平线
        -->
        <hr />
    </body>
</html>
```

一些标签的具体说明，可以打开 W3C 文档进行查看

```jsx
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>实体</title>
    </head>
    <body>
        <!--
            在 HTML 中，一些如 < > 这种特殊字符是不能直接使用的
                需要使用一些特殊的符号来表示这些符号，这些特殊符号我们称为实体（转义字符串）
                实体的语法：
                    < &lt;
                    > &gt;
                    空格 &nbsp;
                    版权符号 &copy;
        -->
        a&ltb c&gtd
        <p>&copy;今天天气很好&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;你好呀</p>
    </body>
</html>
```

### 图片标签

```html
<!DOCTYPE html>
<html>
    <head>
        <!--
            使用 meta 标签还可以设置网页的关键字 
                name 属性可以用来说明是否是关键字，而 content 可以写多个关键字，搜索引擎可以
                通过这个来搜索到我们的网页
            还可以用来指定网页的描述
            搜索引擎在检索页面时，会同时检索页面中的关键词和描述，但是这两个值不会影响页面在
            搜索引擎中的排名
            使用 meta 可以用来做请求的重定向 content 指定了秒数
        -->
        <meta charset="utf-8" name="keywords" content="HTML5, JavaScript, Java"/>
        <meta name="description" content="发布 H5,js 等前端相关的信息"/>
        <meta http-equiv="refresh" content="5;url=http://www.baidu.com" />p
        <title>图片标签</title>
    </head>
    <body>
        <!--
            使用 img 标签来向网页引入一个外部图片
                img 标签也是一个自结束标签
            属性：
                src: 设置一个外部图片的路径
                alt: 可以用来设置图片的描述(在图片不能显示时)
                搜索引擎可以通过 alt 属性来识别不同的图片，如果不设置 alt 属性，则
                搜索引擎不会对 img 图片进行收录
                width: 修改图片的宽度 一般使用 px 作为单位
                height: 修改图片的高度 一般使用 px 作为单位

                当宽度和高度两个属性如果只设置一个，另一个则会按照等比例调整大小
                一般开发页面，除了自适应页面，一般不直接设置这两个属性

                src 属性设置的是图片的路径，目前我们所要使用的路径全都是相对路径
                    相对路径是相对于当前资源所在目录而言的
        -->
        <img src="1.png" alt="这是一张图片" />
    </body>
</html>
```

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title>xHtml 的语法规范</title>
    </head>
    <body>
        <h1>我是 index6 </h1>
        <!--
            1.HTML 中不区分大小写，但是一般都使用小写
            2.HTML 中的注释不能嵌套
            3.HTML 标签必须结构完整，要么成对出现，要么自结束标签
            浏览器尽最大努力正确解析页面，你所有的不符合语法规范的内容，
                浏览器都会为你自动修正，但是有些情况会修正错误
            4. HTML 标签可以嵌套，但是不能交叉嵌套
            5.HTML 标签中的属性必须有值，且值必须加引号（双引号单引号都可以）

            使用内联框架可以引入一个外部的页面
                使用 iframe 来创建一个内联框架
                属性：
                    src: 外部页面的路径，可以使用相对路径
                    width:
                    height:
                    name: 可以为内联框架指定一个 name 属性
                在现实开发中不推荐使用内联框架，因为内联框架中的内容不会被搜索引擎所检索
        -->
        <iframe src="index1.html"></iframe>

        <!--
            使用超链接可以让我们从一个页面跳转到另一个页面
            属性：
                href: 指向链接跳转的目标地址，可以写相对路径也可以写完整路径
                target: 可以指定如何打开这个新的超链接页面
                    可选值：
                        _self, 表示在当前窗口中打开（默认值）
                        _blank, 在新的窗口中打开链接
                        可以设置一个内联框架的 name 属性值，链接将会在内联框架中打开
        -->
        <a href="http://www.baidu.com">我是一个超链接</a>

        <!--
            center 标签中的内容，会默认在页面中居中显示
        -->
        <center>
            <p>
                我是一个段落
            </p>
        </center>
    </body>
</html>
```

## 其他简单案例

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <b>你好呀！</b>
    <center>华南师范大学</center>
    <h1>Lady!</h1>
    <h2>Lady!/h2>
    <h3>Lady!</h3>
    <h4>Lady!</h4>
    <h5>Lady!</h5>
    <h6>Lady!</h6>

    <p>
        网页的扩展名是 .html

Html 使用标记标签来描述网页，包含视频、音频、图片等等

各个浏览器版本：[https://caniuse.com/](https://caniuse.com/)，
<!--
    水平线标签 br
-->
<br>查看某个关键词是否可用

VScode 安装：[https://code.visualstudio.com/](https://code.visualstudio.com/)

可以去插件库里下载 Chinese 汉化包、Auto Rename Tag 插件（可以跟着一起改标签）
<br>
<hr>
<strong>view-in-browser 插件可以直接打开浏览器查看网页</strong>

<em>强调文本</em>

Live Server <i>插件可以实时看到浏览器的变化</i>
    </p>

<p>
    <s>SOA（Service-Oriented Architecture）: 面向服务架构，它可以根据需求通过网络对松散耦合的粗粒度应用组件进行分布式部署、组合和使用，有利于提升组件可重用性，可维护性。
        
        </s>
    <br>
    <del>
        IDE（Integrated Development Environment）: 用于提供程序开发环境的应用程序，一般包括代码编辑器、编译器、调试器和图形用户界面等工具，本《手册》泛指 IntelliJ IDEA 和 eclipse。
        OOM（Out Of Memory）: 源于 java.lang.OutOfMemoryError，当 JVM 没有足够的内存来为对象分配空间并且垃圾回收器也无法回收空间时，系统出现的严重状况。
    </del>
    <u><b>12<sub>[2]</sub>345</b>hello<sup>[1]</sup> world!</u>
</p>

<p>
    说明：敏捷开发是快速交付迭代可用的系统，省略多余的设计方案，摒弃传统的审批流程，但核心关键点上的必要设计和文档沉淀是需要的。
    
    反例：某团队为了业务快速发展，敏捷成了产品经理催进度的借口，系统中均是勉强能运行但像面条一样的代码，可维护性和可扩展性极差，一年之后，不得不进行大规模重构，得不偿失。
    
    14）【参考】系统设计主要目的是明确需求、理顺逻辑、后期维护，次要目的用于指导编码。
    
    说明：避免为了设计而设计，系统设计文档有助于后期的系统维护和重构，所以设计结果需要进行分类归档保存。
    
    15）【参考】设计的本质就是识别和表达系统难点，找到系统的变化点，并隔离变化点。
    
    说明：世间众多设计模式目的是相同的，即隔离系统变化点。
</p>

<p>
    16）【参考】系统架构设计的目的：
    
    确定系统边界。确定系统在技术层面上的做与不做。<br>
    <b>确定系统内模块之间的关系。确定模块之间的依赖关系及模块的宏观输入与输出。</b>
    确定指导后续设计与演化的原则。使后续的子系统或模块设计在规定的框架内继续演化。
    确定非功能性需求。非功能性需求是指安全性、可用性、可扩展性等。
</p>

</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled.png)

### hr 的其他用法

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <hr color=""green>
    <hr color=""red>
    <hr color="yellow", width="300px">
    <hr color="yellow", width="600px">
    <hr color="red", width="600px", align="left">
    <hr noshade>    <!--  取消阴影  -->
</body>
</html>
```

## 常用标签

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%201.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%202.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%203.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%204.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%205.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%206.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>123</p>
    <p>446</p>
    <img src="2.jpeg", alt="Saber", title="你好呀">
</body>
</html>
```

title 属性：鼠标悬停提示文字，alt 属性：则是图片不显示时的提示词

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%207.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%208.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%209.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2010.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2011.png)

音频标签目前支持三种格式：MP3、Wav、Ogg

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2012.png)

视频标签目前支持三种格式：MP4、WebM、Ogg

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2013.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2014.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2015.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2016.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2017.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2018.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2019.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2020.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2021.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2022.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>123</p>
    <p>446</p>
    <img src="2.jpeg", alt="Saber", title="你好呀", width="200px">
    <ul>
        <li>
            榴莲
        </li>
        <li>
            菠萝
        </li>
        <li>
            香蕉
        </li>
    </ul>

    <ol>
        <li>张三：100</li>
        <li>张三：100</li>
        <li>张三：100</li>
        <li>张三：100</li>
        <li>张三：100</li>
    </ol>

    <dl>
        <dt>12345</dt>
        <dt>12345</dt>
        <dt>12345</dt>
        <dd>layd</dd>
        <dd>layd</dd>
        <dd>layd</dd>
    </dl>

    <table border="4px">
        <caption><strong>我的表格</strong></caption>    
        <tr>
            <th>123</th>
            <th>123</th>
            <th>123</th>
        </tr>
        <tr>
            <td>456</td>
            <td>456</td>
            <td>456</td>
        </tr>
        <tr>
            <td>789</td>
            <td>789</td>
            <td>789</td>
        </tr>
    </table>
</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2023.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2024.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table>
        <thead>
            <th>姓名</th>
            <th>成绩</th>
            <th>评语</th>
        </thead>
        <tbody>
            <tr>
                <td>张三</td>
                <td rowspan="2">100分</td>
                <td>小帅锅</td>
            </tr>
            <tr>
                <td>小哥哥</td>
                <td>小哥哥</td>
                <td>小哥哥</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2025.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2026.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2027.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2028.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    性别：<input type="radio", name="sex"> 男
    <!-- checked 默认选中 -->
          <input type="radio", name="sex" checked> 女
    <br>
    选择文件：<input type="file" multiple>
</body>
</html>
```

按钮，提交表单

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 表单域标签 -->
    <form>
    性别：<input type="radio", name="sex"> 男
    <!-- checked 默认选中 -->
          <input type="radio", name="sex" checked> 女
    <br>
    选择文件：<input type="file" multiple>
    <br>
    用户名：<input type="text">
    <br>
    密码：<input type="password">
    <br>
    <input type="submit" value="免费注册">
    <input type="reset">
    </form>
</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2029.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- 表单域标签 -->
    <form>
    性别：<input type="radio", name="sex"> 男
    <!-- checked 默认选中 -->
          <input type="radio", name="sex" checked> 女
    <br>
    选择文件：<input type="file" multiple>
    <br>
    用户名：<input type="text">
    <br>
    密码：<input type="password">
    <br>
    <input type="submit" value="免费注册">
    <input type="reset">
    </form>
    <button type="submit">提交按钮</button>
    <button type="reset">重置按钮</button>
    <button type="button">普通按钮，没有任何功能</button>
</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2030.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <select>
        <option>北京</option>
        <option>北京</option>
        <option>北京</option>
        <option>北京</option>
        
        <option selected>深圳</option>
    </select>
</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2031.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2032.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <textarea cols="50" rows="30">
        DataEase 是开源的数据可视化分析工具，帮助用户快速分析数据并洞察业务趋势，
        <br>从而实现业务的改进与优化。DataEase 支持丰富的数据源连接，能够通过拖拉拽方式快速制作图表，并可以方便地与他人分享。
    </textarea>
    <br>
    性别：
    <input type="radio" name="sex" id="nan"> <label for="nan">男</label>
    <label><input type="radio" name="sex"> 女</label>

</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2033.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div>14123251</div>
    <div>14123251</div>
    <div>14123251</div>
    <div>14123251</div>

    <span>这是 span 标签</span>
    <span>这是 span 标签</span>
    <span>这是 span 标签</span>
</body>
</html>
```

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2034.png)

![Untitled](HTML%E8%AF%AD%E8%A8%80%20d101ec8da2d0489b8565454939a4ac0f/Untitled%2035.png)

### 表单综合案例

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>华南师范大学</h1>
    <br>
    <form action="">
        昵称：<input type="text" placeholder="请输入昵称">
        <br>
        <br>
        性别：
        <label><input type="radio" name="sex" checked> 男</label>
        <label><input type="radio" name="sex"> 女</label>
        <br>
        <br>
        所在城市：
        <select>
            <option>上海</option>
            <option>广州</option>
            <option selected>北京</option>
        </select>
        <br>
        <br>
        喜欢的类型：
        <label><input type="checkbox" checked> 可爱</label>
        <label><input type="checkbox" checked> 性感</label>
        <label><input type="checkbox"> 御姐</label>
        <br>
        <br>
        个人介绍：<br>
        <textarea name="" id="" cols="60", rows="10"></textarea>
        <h3>我承诺</h3>
        <ul>
            <li>年满18岁、单身</li>
            <li>年满18岁、单身</li>
            <li>年满18岁、单身</li>
        </ul>
        <input type="submit" value="免费注册">
        <button type="reset">重置</button>
    </form>
</body>
</html>
```