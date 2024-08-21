# CSS 语言

层叠样式表

## 1.内联样式的 CSS

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf8" />
        <title>CSS</title>
    </head>
    <body>
        <!--
            可以将 CSS 样式编写到元素的 style 属性中
                将 CSS 样式直接编辑到 style 属性中，这种样式我们称为内联样式
                内联样式只对当前元素中的内容起作用，内联样式不方便复用
                内联样式属于结构与表现耦合，不方便后期的维护，不推荐使用
        -->
        <p style="color: red;font-size: 40px;">锄禾日当午，汗滴禾下土</p>
        <p>谁知盘中餐，粒粒皆辛苦！</p>
    </body>
</html>
```

### head 标签内部的 style 样式

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8" />
        <title> CSS2 </title>
        <!--
            也可以将 CSS 编写到 head 中的 style 标签中
                将样式表编写的 style 标签中，然后通过 css 选择器选中指定元素，
                然后可以同时为这些元素一起设置样式，这样可以使样式进一步的复用
        -->
        <style type="text/css">
            /*
                CSS 的注释，作用和 HTML 类似，只不过它必须写在 style 标签中，或者是 css 文件中
                CSS 的语法：
                    选择器 声明块
                选择器：
                    -通过选择器可以选中页面中指定的元素，
                        并且将声明块中的样式应用到选择器对应的元素上
                声明块：
                    声明块紧跟在选择器的后边，使用一对 {} 括起来
                    声明块中实际上是一组一组的键值对
                        这一组一组的键值对被我们称为声明
                    在一个声明块中可以写多个声明，多个声明之间使用 ; 隔开
                    声明的键值用 : 隔开
            */
            p{
                color: blue;
                font-size: 40px;
            }
        </style>
    </head>
    <body>
        <p>  1223 </p>
        <p>  1223 </p>
        <p>  1223 </p>
        <p>  1223 </p>
        <p>  1223 </p>
    </body>
</html>
```

### 外部 Style CSS

```jsx
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Document</title>
		<link rel="stylesheet" type="text/css" href="style.css" />
	</head>
	<body>
		<h1>这是一个非常漂亮的网页</h1>
		<h2>你看我出不出来</h2>
	</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled.png)

选择器，就是去 HTML 中寻找标签：

1. 标签选择器

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%201.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%202.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p{
            color: red;
            font-size: 30px;
            background-color: green;
            width: 400px;
            height: 400px;
        }
        .one{
            color:gold;
        }
    </style>
</head>
<body>
    <p>这是一个标签</p>
    <div class="one">类选择器</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%203.png)

id 一般一个页面不用第二次，它主要通过 js 来找标签的

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%204.png)

一般用这个来清除所有标签的默认边距（margin、padding)

### 1.字体和文本样式

1.字体大小：

font-size

单位：px

(2) 字体粗细

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%205.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%206.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%207.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%208.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%209.png)

实际开发中会提供多种字体，就是因为很多电脑不一定安装了该字体，最后那个是 sans-serif（无衬线字体）

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2010.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2011.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p{
            font-size: 30px;
            font-weight: 700;
            font-style: italic;
            font-family: 宋体;
        }
        em{
            font-family: 微软雅黑, 黑体, sans-serif;
        }
        span{
            font: italic 700 66px 宋体;
            /* 一个属性冒号后面书写多个值的写法 */
        }
    </style>
</head>
<body>
    <!-- 浏览器默认字号是 16 -->
    <p>段落文字</p>
    <em>段落文字</em>
    <span>asdfasdfasdfds</span>
</body>
</html>
```

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p{
            /* 首行缩进 2 个字的大小，默认字号 16px */
            /* text-indent: 30px; */
            text-indent: 2em;
            /* 无论字体大小如何变， em 都可以保证，首行缩进 2 个字 */
            font-size: 40px;
        }
    </style>
</head>
<body>
    <p>大型银行中，美国资产值最大银行摩根大通涨近3%，花旗和美国银行最高涨超4%，富国银行涨近3%，脱离九个月最低。同时，摩根士丹利涨3.6%，高盛涨2.6%，均至一周新高。资管巨头嘉信理财涨6%。

        第一共和银行最高涨近60%领跑地区银行股，收涨超29%，创史上最大单日涨幅，但上周跌近72%后，3月仍跌超87%。
        
        昨日涨超30%、创上市后最大单日涨幅的纽约社区银行再涨近7%，昨日收盘转跌的阿莱恩斯西部银行涨15%，昨日涨近11%的西太平洋合众银行再涨近19%，KeyCorp和美国合众银行涨9%，Zions Bancorporation涨7%。
        
        瑞士信贷欧股涨超7%并收于日高，其美股涨超6%后收涨2.5%，上逼1美元关口。瑞银UBS欧股和美股均涨12%，完全收复了3月10日硅谷银行倒闭引发银行业危机以来的跌幅，上周五曾创三个月新低。
        
        欧股连续两日齐涨超1%，金融服务和银行板块均涨约4%领跑，德国商业银行和意大利裕信银行涨7%表现突出。
    </p>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2012.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2013.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p{
            /* 首行缩进 2 个字的大小，默认字号 16px */
            /* text-indent: 30px; */
            text-indent: 2em;
            /* 无论字体大小如何变， em 都可以保证，首行缩进 2 个字 */
            font-size: 40px;
        }
        h2{
            text-align: center;
        }
        #saber{
            text-align: center;
        }
    </style>
</head>
<body>
    <p>大型银行中，美国资产值最大银行摩根大通涨近3%，花旗和美国银行最高涨超4%，富国银行涨近3%，脱离九个月最低。同时，摩根士丹利涨3.6%，高盛涨2.6%，均至一周新高。资管巨头嘉信理财涨6%。

        第一共和银行最高涨近60%领跑地区银行股，收涨超29%，创史上最大单日涨幅，但上周跌近72%后，3月仍跌超87%。
        
        昨日涨超30%、创上市后最大单日涨幅的纽约社区银行再涨近7%，昨日收盘转跌的阿莱恩斯西部银行涨15%，昨日涨近11%的西太平洋合众银行再涨近19%，KeyCorp和美国合众银行涨9%，Zions Bancorporation涨7%。
        
        瑞士信贷欧股涨超7%并收于日高，其美股涨超6%后收涨2.5%，上逼1美元关口。瑞银UBS欧股和美股均涨12%，完全收复了3月10日硅谷银行倒闭引发银行业危机以来的跌幅，上周五曾创三个月新低。
        
        欧股连续两日齐涨超1%，金融服务和银行板块均涨约4%领跑，德国商业银行和意大利裕信银行涨7%表现突出。
    </p>
    <h2>华南师范大学</h2>
    <div id="saber"><img src="2.jpeg" width="100px" height="100px" ></div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2014.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2015.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2016.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2017.png)

```jsx
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        p{
            /* 自己字号的 1.5 倍 */
            line-height: 3;
        }
        div{
            width: 400px;
            height: 400px;
            background-color: pink;
            text-align: center;
            /*
            前提是，文字是单行的 
            垂直居中：设置行高属性值 = 自身高度属性值 
            */
            line-height: 400px;
        }
        #one{
            width: 300px;
            height: 300px;
            background-color: pink;
            /* 可以让标签整体水平居中 */
            margin: 0 auto;
        }
    </style>
</head>

<body>
    <p>中俄联合声明: 用和谈解决乌克兰危机
    
        消息面上，当地时间3月21日下午，国家主席习近平在莫斯科克里姆林宫同俄罗斯总统普京共同签署并发表《中华人民共和国和俄罗斯联邦关于深化新时代全面战略协作伙伴关系的联合声明》。
    
        关于乌克兰问题，双方认为，联合国宪章宗旨和原则必须得到遵守，国际法必须得到尊重。俄方积极评价中方在乌克兰问题上的客观公正立场。双方反对任何国家或国家集团为谋求军事、政治和其他优势而损害别国的合理安全利益。俄方重申致力于尽快重启和谈，中方对此表示赞赏。俄方欢迎中方愿为通过政治外交途径解决乌克兰危机发挥积极作用，欢迎《关于政治解决乌克兰危机的中国立场》文件中阐述的建设性主张。双方指出，解决乌克兰危机必须尊重各国合理安全关切并防止形成阵营对抗，拱火浇油。双方强调，负责任的对话是稳步解决问题的最佳途径。为此，国际社会应支持相关建设性努力。双方呼吁停止一切促使局势紧张、战事延宕的举动，避免危机进一步恶化甚至失控。双方反对任何未经联合国安理会授权的单边制裁。
    </p>
    <div>华南师范大学</div>

    <div id="one"></div>
</body>

</html>
```

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 800px;
            height: 600px;
            background-color: pink;
            margin: 0 auto;
        }
        .center{
            text-align: center;
        }
        .color1{
            color: #808080;
        }
        .color2{
            color: #87ceeb;
            font-weight: 700;
        }
        a{
            text-decoration: none;
        }
        .suojin{
            text-indent: 2em;
        }
    </style>
</head>
<body>
    <div>
        <h1 class="center">《自然》评选改变科学的 10 个计算机代码项目</h1>
        <p class="center">
            <span class="color1">南华大学男生何某某编造女同学谣言、P不雅图片牟利事件</span>
            <span class="color2">新浪科技</span> <a href="#">收藏本文</a>
        </p>
        <hr>
        <p class="suojin">对何某某的处理一个接一个，先是公安部门，然后是南华大学，现在是中科大，何某某为自己的不法行为付出了严重的代价，教训深刻。
        </p>
        <p class="suojin">从媒体透露出的诸多信息不难看出，何某某是一位学习上的好学生，“别人家的孩子”。在考生越来越多、考取研究生越来越难的当下，能被推荐免试进入中科大读研究生，说是“学霸”级别，这不过分吧？那么，一位“好学生”，怎么就栽了呢？
        </p>
        <p class="suojin">3月17日晚，苏州大学一学生恶意P图侮辱女性的网帖，引发舆论关注。对此，苏州大学表示，经调查核实，该校学生赵某某违法行为属实，公安机关已作出行政处罚决定，依照学校相关规定给予该生开除学籍处分。
        </p>
        <p class="sujin">事情类似，何某某与赵某某又有所不同。何某某造黄谣的目的，不是赵某某所言的“心理有些变态”，而是为了牟利。因商业利益驱使而造黄谣更可怕，这会造成更大面积传播，更多的女性受害。
        </p>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2018.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            background-color: #F5F5F5;
        }
        .goods{
            width: 245px;
            height: 300px;
            background-color: #fff;
            margin: 0 auto;
            /* 设置图片的父级标签居中属性
            则 div 里面的所有元素都会居中 */
            text-align: center;
        }
        .img1{
            width: 200px;
            height: 200px;
        }
        .title1{
            font-size: 14px;
            line-height: 25px;
        }
        .info{
            color: #ccc;
            font-size: 12px;
            line-height: 30px;
        }
        .money{
            font-size: 14px;
            color: #ffa500;
        }
    </style>
    
</head>
<body>
    <div class="goods">
        <!-- 用来网页布局，一个页面可能用无数次，原则：
        如果使用 div，尽量使用类名 -->
        <img src="2.jpeg" class="img1">
        <div class="title1">好动漫</div>
        <div class="info">Saber</div>
        <div class="money">16岁</div>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2019.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 找到 div 的儿子 p 设置文字颜色是红色
        父选择器 后代选择器 {} */
        div p{
            color: red;
        }
    </style>
</head>
<body>
    <p>这是一个 p 标签</p>
    <div>
        <p>这是 div 中的 p 标签</p>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2020.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 找到 div 的儿子 p 设置文字颜色是红色
        父选择器 后代选择器 {} 
        这个一直选下去都行 因此它叫后代*/
        div p{
            color: red;
        }
        /* 只选择儿子 a */
        div > a{
            color: green;
        }
    </style>
</head>
<body>
    <p>这是一个 p 标签</p>
    <div>
        <p>这是 div 中的 p 标签</p>
    </div>

    <div>
        父级
        <a href="#">这是 div 里面的 a</a>
        <p>
            <a href="#"> 这是 div 里面的 p 里面的 a</a>
        </p>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2021.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* p div span h1 文字颜色是红色
        选择器1，选择器2，选择器3{} */
        p, 
        div, 
        span, 
        h1{
            color:red;
        }
    </style>
</head>
<body>
    <p>pppp</p>
    <span>pppp</span>
    <h1>pppp</h1>
    <h2>pppp</h2>
    <div>div</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2022.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* p div span h1 文字颜色是红色
        选择器1，选择器2，选择器3{} */
        p, 
        div, 
        span, 
        h1{
            color:red;
        }

        /* 必须是 p 标签 */
        p.box{
            color: skyblue;
        }
    </style>
</head>
<body>
    <p>pppp</p>
    <span>pppp</span>
    <h1>pppp</h1>
    <h2>pppp</h2>
    <div>div</div>

    <!-- 找到第一个 p，带 box 类，设置文字颜色是红色 -->
    <p class="box">box pppp</p>
    <p>pppppp</p>
    <div class="box">box pppp</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2023.png)

**Visual Studio Code 提供 emmet 语法**

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2024.png)

### 背景相关属性

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2025.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2026.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div.one{
            width: 400px;
            height: 400px;
            /* 红绿蓝三原色，a 是透明度 0-1 */
            background-color: rgba(0, 0, 0, 0.5);
        }
        div.two{
            width: 400px;
            height: 400px;
            background-color: pink;
            background-image: url(./2.jpeg);
            background-repeat: no-repeat;
            /* background-repeat: repeat-x;
            background-repeat: repeat-y; */
            /* background-position: 10 20; */
            /* 图片在 div 中居中 */
            /* background-position: center; */
            /* 这里可以设置为正负数，让图片进行左右上下平移 */
            background-position: 50px 0;
        }
    </style>
</head>
<body>
    <div class="one">div</div>
    <div class="two">div</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2027.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2028.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2029.png)

img 用来实现重要图片，比如海报、轮播图；背景图用来实现修饰性的、装饰性的

### 元素显示模式

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2030.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2031.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2032.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2033.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2034.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 300px;
            height: 300px;
            background-color: pink;

            /* 行内块 */
            display: inline-block;
        }
    </style>
</head>
<body>
    <div>12345</div>
    <div>12345</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2035.png)

### CSS 特性

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2036.png)

a 标签的 color 会继承失效、h 系列标签的 font-size 会继承失效

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2037.png)

### 5个链接的综合案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        a{
            text-decoration: none;
            width: 100px;
            height: 50px;
            background-color: red;
            display: inline-block;
            color:white;
            text-align: center;
            line-height: 50px;
        }
        a:hover{
            background-color: orange;
        }
    </style>
</head>
<body>
    <a href="#">导航1</a>
    <a href="#">导航2</a>
    <a href="#">导航3</a>
    <a href="#">导航4</a>
    <a href="#">导航5</a>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2038.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2039.png)

## 盒子模型

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2040.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 300px;
            height: 300px;
            background-color:pink;
            /* 边框线 = 纸箱子 */
            border:1px solid #000;
            /* 内边距 = 填充泡沫 出现在内容和盒子边缘之间 */
            padding: 20px;

            /* 外边距：出现在两个盒子之间，出现在盒子的外面 */
            margin: 50px;
        }
    </style>
</head>
<body>
    <div>内内容电脑</div> 
    <div>内内容电脑</div> 
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2041.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2042.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2043.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 300px;
            height: 300px;
            background-color:pink;
            /* 边框线 = 纸箱子 */
            border:1px solid #000;
            /* 内边距 = 填充泡沫 出现在内容和盒子边缘之间 */
            padding: 20px;

            /* 外边距：出现在两个盒子之间，出现在盒子的外面 */
            margin: 50px;
        }
        .one{
            width: 200px;
            height: 200px;
            background-color: pink;
            /* solid 实线 */
            /* border: 1px solid #000; */
            /* dashed 虚线 */
            /* border: 5px dashed #000; */
            /* dotted 点线 */
            border-left: 3px dotted #000;
        }
    </style>
</head>
<body>
    <div>内内容电脑</div> 
    <div>内内容电脑</div> 

    <div class="one">你好呀</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2044.png)

盒子尺寸 = width / height + 边框线框宽度

border 撑大盒子尺寸

### 案例

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            height: 40px;
            border-top: 3px solid #ff8500;
            border-bottom: 1px solid #edeef0;
        }
        /* 后代选择器 box 里面的 a */
        .box a{
            width: 80px;
            height: 40px;
            /* 推荐加上：清楚地看到文字在什么位置 */
            background-color: #edeef0;
            /* 不生效的话 就想显示模式 */
            display: inline-block;
            line-height: 40px;
            font-size: 12px;
            color: #4c4c4c;
            text-decoration: none;
        }

        .box a:hover{
            background-color: #edeef0;
            color: #ff8400;
        }
    </style>
</head>
<body>
    <div class="box">
        <a href="#">新浪导航</a>
        <a href="#">新浪导航</a>
        <a href="#">新浪导航</a>
        <a href="#">新浪导航</a>
    </div>
</body>
</html>
```

从外到内，先宽高背景色，放内容，调节内容的位置；控制文字细节

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 240px;
            height: 240px;
            background-color: pink;
            /* 添加了 4 个方向的内边距 */
            padding: 50px;

            /* padding 属性可以当做复合属性用，表示单独设置某个方向的内边距
            最多取 4 个值
            */
            /* 四个值：上 右 下 左 */
            /* 三值：上 左右 下 */
            /* 两值： 上下 左右*/
            /* 实现一个 300 * 300 的盒子 */
            
            border: 10px solid #000;
            padding: 20px;
        }
    </style>
</head>
<body>
    <div>文字</div>
</body>
</html>
```

撑大盒子的有内边距、边框

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            height: 40px;
            border-top: 3px solid #ff8500;
            border-bottom: 1px solid #edeef0;
        }
        /* 后代选择器 box 里面的 a */
        .box a{
            /* 不要限制宽度，这样每个超链接文字不同 可以更灵活 */
            /* width: 80px; */
            height: 40px;
            /* 推荐加上：清楚地看到文字在什么位置 */
            background-color: #edeef0;
            /* 不生效的话 就想显示模式 */
            display: inline-block;
            line-height: 40px;
            font-size: 12px;
            color: #4c4c4c;
            text-decoration: none;
            padding: 0 16px;
        }

        .box a:hover{
            background-color: #edeef0;
            color: #ff8400;
        }
    </style>
</head>
<body>
    <div class="box">
        <a href="#">新浪</a>
        <a href="#">新浪导航新浪导航</a>
        <a href="#">新浪导航</a>
        <a href="#">新浪导航</a>
    </div>
</body>
</html>
```

如何不用做减法，比如我就要一个 100*100 的盒子，同时可以设置内边距和边框

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: pink;
            border: 10px solid #000;
            padding: 20px;

            /* 变成 CSS3 的盒子模型，加了 border 和 padding 不需要手动减法 */
            box-sizing: border-box;
        }
    </style>
</head>
<body>
    <div>文字</div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2045.png)

### 案例

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2046.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            /* 所有标签都可能添加内边距和边框 ，都内减模式 */
            box-sizing: border-box;
        }

        .news{
            width: 500px;
            height: 400px;
            border: 1px solid #000;
            margin: 50px auto;
            padding: 42px 30px 0;
        }

        .news h2{
            border-bottom: 1px solid #ccc;
            font-size: 30px;
            /* 行高是 1 倍，就是字号的大小 */
            line-height: 1;
            padding-bottom: 9px;
        }

        /* 去掉列表的符号  */
        ul{
            list-style: none;
        }

        .news li{
            height: 50px;
            border-bottom: 1px dashed #ccc;
            line-height: 50px;
            padding-left: 28px;
        }

        .news a{
            text-decoration: none;
            color: #666;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <!-- 从外到内 -->
    <div class="news">
        <h2>最新文章/New Articles</h2>
        <ul>
            <li><a href="#">北京招聘网页设计，平面设计，php</a></li>
            <li><a href="#">北京招聘网页设计，平面设计，php</a></li>
            <li><a href="#">北京招聘网页设计，平面设计，php</a></li>
            <li><a href="#">北京招聘网页设计，平面设计，php</a></li>
            <li><a href="#">北京招聘网页设计，平面设计，php</a></li>
        </ul>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2047.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2048.png)

**行内元素的内外边距的问题**

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        span{
            /* margin: 100px; */
            /* 利用行高可以改变 */
            line-height: 100px;
        }
    </style>
</head>
<body>
    <!-- 行内元素 内外边距 margin padding -->
    <!-- 如果想要通过 margin 或 padding 改变行内标签的位置，无法生效  -->
    <!-- 行内标签的 margin-top 或 bottom 不生效-->
    <!-- 行内标签的 padding-top 或 bottom 不生效-->
    <span>span</span>
    <span>span</span>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2049.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2050.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        span{
            /* margin: 100px; */
            /* 利用行高可以改变 */
            line-height: 100px;
        }

        /* 选中第一个 */
        li:first-child{
            background-color: green;
        }

        .li_two:nth-child(2n){
            background-color: pink;
        }

        /* 设置 li 中的超链接文字颜色 */
        .li_3:nth-child(3) a{
            color: aqua;
        }

         /* 去掉列表的符号  也就是前面三个小点*/
        .li_3{
            list-style: none;
        }

        .li_3:nth-child(1) a:nth-child(2){
            color:pink;
        }
    </style>
</head>
<body>
    <!-- 行内元素 内外边距 margin padding -->
    <!-- 如果想要通过 margin 或 padding 改变行内标签的位置，无法生效  -->
    <!-- 行内标签的 margin-top 或 bottom 不生效-->
    <!-- 行内标签的 padding-top 或 bottom 不生效-->
    <span>span</span>
    <span>span</span>
    <ul>
        <li>这是第1个li</li>
        <li>这是第2个li</li>
        <li>这是第3个li</li>
        <li>这是第4个li</li>
        <li>这是第5个li</li>
        <li>这是第6个li</li>
        <li>这是第7个li</li>
        <li>这是第8个li</li>
    </ul>

    <ul>
        <li class="li_two">这是第1个li</li>
        <li class="li_two">这是第2个li</li>
        <li class="li_two">这是第3个li</li>
        <li class="li_two">这是第4个li</li>
        <li class="li_two">这是第5个li</li>
        <li class="li_two">这是第6个li</li>
        <li class="li_two">这是第7个li</li>
        <li class="li_two">这是第8个li</li>
    </ul>

    <ul>
        <li class="li_3"><a href="#">这是第1个li</a><a href="#">这是第1个li</a><a href="#">这是第1个li</a></li>
        <li class="li_3"><a href="#">这是第2个li</a></li>
        <li class="li_3"><a href="#">这是第3个li</a></li>
        <li class="li_3"><a href="#">这是第4个li</a></li>
        <li class="li_3"><a href="#">这是第5个li</a></li>
        <li class="li_3"><a href="#">这是第6个li</a></li>
        <li class="li_3"><a href="#">这是第7个li</a></li>
        <li class="li_3"><a href="#">这是第8个li</a></li>
    </ul>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2051.png)

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .father{
            width: 300px;
            height: 300px;
            background-color: pink;
        }

        .father::before{
            /* 内容 */
            /* 伪元素 通过 CSS 创建标签，装饰性的不重要的小图 */
            content: '老鼠';    
            /* content 必须有，否则伪元素不生效 */
            color: green;
            width: 100px;
            height: 100px;
            background-color: blue;
            /* 默认是行内元素，宽高不生效 */
            display: block;
        }
        .father::after{
            /* 内容 */
            content: '大米';
        }
    </style>
</head>
<body>
    <div class="father">爱</div>
</body>
</html>
```

### 标准流

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2052.png)

浏览器解析行内块或行内标签的时候，如果标签换行书写时，会产生一个空格；哪怕转行内块显示模型也不行

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2053.png)

浮动可以让两个标签完美的排列

```jsx
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 
        浮动的标签  顶对齐
        与行内块标签特点类似，在一行排列，宽高生效
        */
        .one{
            width: 100px;
            height: 100px;
            background-color: pink;
            float:left;

            margin-top: 10px;
        }

        .two{
            width: 200px;
            height: 200px;
            background-color: skyblue;

            float:left;

            /* 因为有浮动，不能生效 - 盒子无法水平居中 */
            margin: 0 auto;
        }

        .three{
            width: 300px;
            height: 300px;
            background-color: orange;
        }
    </style>
</head>
<body>
    <div class="one">one</div>
    <div class="two">two</div>
    <div class="three">three</div>
</body>
</html>
```

## 综合案例

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2054.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }

        .top{
            height: 40px;
            background-color: #333;
        }

        .header{
            width: 1226px;
            height: 100px;
            background-color: #ffc0cb;
            margin:0 auto
        }

        .content{
            margin: 0 auto;
            width: 1226px;
            height: 460px;
            background-color: green;
        }

        .left{
            float:left;

            width: 234px;
            height: 460px;
            background-color: #ffa500;
        }

        .right{
            float:left;

            width: 992px;
            height: 460px;
            background-color: #87ceeb;
        }

        /* CSS 书写顺序：浏览器执行效率更高
            1.浮动 / display
            2.盒子模型相关的属性： margin borderr padding 宽度高度 背景色
            3.文字样式
        */
    </style>
</head>
<body>
    <!-- 通栏效果 -->
    <div class="top"></div>
    <div class="header"></div>

    <div class="content">
        <div class="left"></div>
        <div class="right"></div>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2055.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        *{
            margin: 0;
            padding: 0;
        }

        .box{
            margin: 0 auto;
            width: 1226px;
            height: 614px;
            background-color: pink;
        }

        .left{
            float: left;
            width: 234px;
            height: 614px;
            background-color: #800000;
        }
        
        .right{
            float:right;
            width: 978px;
            height: 614px;
            background-color: green;
        }
        ul{
            list-style: none;
        }

        .right li{
            float: left;

            margin-right: 14px;
            margin-bottom: 14px;

            width: 234px;
            height: 300px;
            background-color: #87cceb;
        }

        /* 如果父级的宽度不够，子级会自动换行 */
        /* 第四个 li 和 第 八个 li 清楚右边距 */
        .right li:nth-child(4n){
            margin-right: 0px;
        }
    </style>
</head>
<body>
    <div class="box">
        <div class="left"></div>
        <div class="right">
            <ul>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ul>
        </div>

    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2056.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2057.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2058.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2059.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2060.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2061.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>学成在线</title>
    <link rel="stylesheet" href="./css/index.css">
<body>
    <!-- 网站的首页，所有网站的首页都叫 index.html
    因为服务器找首页都是找 index.html -->
    <!-- 布局：从外到内 从上到下 从左到右
    CSS: 浮动 /display; 盒子模型； 文字样式 -->
    <!-- 头部header: 负责头部区域的样式  wrapper 只负责版心效果 -->
    <div class="header wrapper">
        <h1>
            <a href="#"><img src="./images/logo.png" alt=""></a>
        </h1>

        <!-- 导航 -->
        <div class="nav">
            <ul>
                <li><a href="#">首页</a></li>
                <li><a href="#">课程</a></li>
                <li><a href="#">职业规划</a></li>
            </ul>
        </div>

        <!-- 搜索 -->
        <div class="search">
            <input type="text" placeholder="输入关键词">
            <button></button>
        </div>
    </div>

    <!-- 轮播图 banner -->
    <div  class="banner">
        <div class="wrapper">
            <div class="left">
                <ul>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                    <li><a href="#">前端开发 <span>></span></a></li>
                </ul>
            </div>
            <div class="right">
                <h2>我的课程表</h2>
                <div class="content">
                    <dl>
                        <dt>继续学习 程序语言设计</dt>
                        <dt>正在学习-使用对象</dt>
                    </dl>
                    <dl>
                        <dt>继续学习 程序语言设计</dt>
                        <dt>正在学习-使用对象</dt>
                    </dl>
                    <dl>
                        <dt>继续学习 程序语言设计</dt>
                        <dt>正在学习-使用对象</dt>
                    </dl>
                </div>
                <a href="#" class="more">全部课程</a>
            </div>
        </div> 
    </div>

    <!-- 精品推荐 -->
    <div class="goods wrapper">
        <h2>精品推荐</h2>
        <ul>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
            <li><a href="#">jQuery</a></li>
        </ul>
        <a href="#" class="xingqu">修改兴趣</a>
    </div>

    <!-- 精品推荐课程 -->
    <div class="box wrapper">
        <div class="title">
            <h2>精品推荐</h2>
            <a href="#">查看全部</a>
        </div>

        <!-- 下面的 li 是浮动的，会撑开 下面这个 div
        因此需要清除浮动 -->
        <div class="content clearfix">
            <ul>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                
                <li>
                    <a href="#">
                        <img src="./images/course07.png" alt="">
                        <h3>Think PHP 5.0 博客系统实战项目演练</h3>
                        <p><span>高级</span>  ·  1125人在学习</p>
                    </a>
                </li>
                
            </ul>
        </div>
    </div>

    <!-- 版权 注意要清除浮动的影响，课程的 li 的父级 -->
    <!-- li 都浮动了，脱标，撑不开父级的高度 -->
    <div class="footer">
        <div class="wrapper">
            <div class="left">
                <img src="./images/logo.png" alt="">
                <p>学成在线致力于铺啊发生的防守打法打撒范德萨发大水发
                    打撒法师打发第三方 <br>@ 2017年XGGG 。 呼被12431224
                </p>
                <a href="#">下载 APP</a>
            </div>
            <div class="right">
                <dl>
                    <dt>合作伙伴</dt>
                    <dd><a href="#">合作机构</a></dd>
                    <dd><a href="#">合作导师</a></dd>
                </dl>
                <dl>
                    <dt>合作伙伴</dt>
                    <dd><a href="#">合作机构</a></dd>
                    <dd><a href="#">合作导师</a></dd>
                </dl>
                <dl>
                    <dt>合作伙伴</dt>
                    <dd><a href="#">合作机构</a></dd>
                    <dd><a href="#">合作导师</a></dd>
                </dl>
            </div>
        </div>
    </div>
</body>
</html>
```

css 文件

```css
/* 美化首页的 */

*{
    margin: 0;
    padding: 0;

    /* 内减模式 */
    box-sizing: border-box;
}

/* 清除小圆点 */
li{
    list-style: none;
}

/* 清除下划线 */
a{
    text-decoration: none;
}

/* 清除浮动 */
.clearfix:before, .clearfix:after{
    content: "";
    display: table;
}

.clearfix:after{
    clear:both;
}

body{
    background-color: #f3f5f7;
}

/* 版心 */
.wrapper{
    width: 1200px;
    margin: 0 auto;
}

/* 头部 */
.header{
    height: 42px;
    background-color: pink;
    /* margin-top: 30px;
    margin-bottom: 30px; */
    /* 不要 写 0 ，会把 wrapper 的居中给覆盖掉 */
    margin: 30px auto;
}

h1{
    float:left;
}

/* 导航 */
.nav{
    float:left;

    margin-left: 70px;

    height: 42px;
    /* background-color: green; */
}

.nav li{
    float:left;
    margin-right: 26px;
}

.nav li a{
    display: block;
    padding: 0 9px;

    height: 42px;
    line-height: 42px;
    /* border-bottom: 2px solid #00eeff; */

    font-size: 18px;
    color: #050505;
}

.nav li a:hover{
    border-bottom: 2px solid #00eeff;
}

/* 搜索 */
.search{
    float:left;
    margin-left: 59px;
    width: 412px;
    height: 40px;
    border: 1px solid #00a4ff;
}

.search input{
    float:left;
    padding-left: 20px;
    /* 左右加一起的尺寸要小于等于 410 */
    width: 360px;
    height: 38px;
    border: 0;
}

/* 控制 placeholder 的样式 */
.search input::placeholder{
    font-size: 14px;
    color: #bfbfbf;
}

.search button{
    float:left;
    width: 50px;
    height: 40px;
    background-image: url(../images/btn.png);
    border: 0;
}

/* 轮播图 */
.banner{
    height: 420px;
    background-color: #1c036c;
}

.banner .wrapper{
    height: 420px;
    background-image: url(../images/banner2.png);
}

.banner .left{
    float:left;
    padding: 0 20px;
    width: 190px;
    height: 420px;
    background-color: rgba(0, 0, 0, 0.3);
    /* 行高属于控制文字的属性
    能继承 */
    line-height: 44px;
}

.banner .left span{
    float: right;
}

.banner .left a{
    font-size: 14px;
    color: #fff;
}

.banner .left a:hover{
    color: #00b4ff;
}

.banner .right{
    float:right;
    margin-top: 50px;
    width: 228px;
    height: 300px;
    background-color: #fff;
}

.banner .right h2{
    height: 48px;
    background-color: #9bceea;
    text-align: center;
    line-height: 48px;

    font-size: 18px;
    color: #fff;
}

.banner .right .content{
    padding: 0 18px;
}

.banner .right .content dl{
    padding: 12px 0;
    border-bottom: 2px solid #e5e5e5;
}

.banner .right .content dt{
    font-size: 16px;
    color: #4e4e4e;
}

.banner .right .content dd{
    font-size: 14px;
    color: #4e4e4e;
}

.banner .right .more{
    display: block;
    margin: 4px 14px 0;
    width: 200px;
    height: 40px;
    border: 1px solid #00a4ff;

    font-size: 16px;
    color: #00a4ff;
    font-weight: 700;

    text-align: center;
    line-height: 40px;
}

/* 精品推荐 */
.goods{
    margin-top: 8px;
    padding-left: 34px;
    padding-right: 26px;
    height: 60px;
    background-color: #fff;
    box-shadow: 0px 2px 3px 0px
    rgba(118, 118, 118, 0.2);

    line-height: 60px;

}

.goods h2{
    float: left;
    font-size: 16px;
    color: #00a4ff;
    font-weight: 400;
}

.goods ul{
    float: left;
    margin-left: 30px;
}

.goods ul li{
    float: left;
}

.goods li a{
    border-left: 1px solid #bfbfbf;
    padding: 0 30px;
    font-size: 16px;
    color: #050505;
}

.goods .xingqu{
    float: right;
    font-size: 14px;
    color: #00a4ff;
}

/* 精品课程 */
.box{
    margin-top: 35px;
}

.box .title{
    height: 40px;
    /* background-color: pink; */
}

.box .title h2{
    float:left;
    font-size: 20px;
    color: #494949;
    font-weight: 400;
}

.box .title a{
    float:right;
    margin-right: 30px;
    font-size: 12px;
    color: #a5a5a5;
}

.box .content li{
    float: left;
    margin-right: 15px;
    margin-bottom: 15px;
    width: 228px;
    height: 270px;
    background-color: #fff;
}

.box .content li:nth-child(5n){
    margin-right: 0;
}

.box .content li h3{
    padding: 20px;
    font-size: 14px;
    color: #050505;
    font-weight: 700;
}

.box .content li p{
    padding: 0 20px;
    font-size: 12px;
    color: #999;
}

.box .content li span{
    color: #ff7c2d;
}

/* 版权 */
.footer{
    margin-top: 40px;

    padding-top: 30px;

    height: 417px;
    background-color: #fff;
}

.footer .left{
    float: left;
}

.footer left p{
    margin: 20px 0 10px;
    font-size: 12px;
    color: #666;
}

.footer .left a{
    display: inline-block;
    width: 120px;
    height: 36px;
    border: 1px solid #00a4ff;
    text-align: center;
    line-height: 36px;
    font-size: 16px;
    color: #00a4ff;
}

.footer .right{
    float: right;
}

.footer .right dl{
    float: left;
    margin-left: 120px;
}
```

## 定位

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2062.png)

定位，可以解决导航栏不动，但是网页内容可以上下滑动

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2063.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2064.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2065.png)

```r
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* CSS 定位:
            1.定位 / 浮动 / display
            2.盒子模型
            3.文字属性
             */
        .box{
            position: relative;
            left: 100px;
            top: 200px;
            /* 
            1.占有原来的位置
            2.仍然具有标签原有的显示模式特点
            3.改变位置是参考自己原来的位置

            如果 left 和 right 都有，以 left 为准
            如果 top 和 bottom 都有，以 top 为准
            */

            width: 200px;
            height: 200px;
            background-color: pink;
        }
    </style>
</head>
<body>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <div class="box">box</div>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
    <p>测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试测试定位</p>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2066.png)

```r
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .father{
            position: relative;
            width: 400px;
            height: 400px;
            background-color: pink;
        }

        .son{
            /* 相对，绝对 */
            /* 父级采用相对定位，子级绝对定位
            子绝父相
            */
            /* position: relative; */
            width: 300px;
            height: 300px;
            background-color: skyblue;
        }

        .sun{
            /* 
            只要父级有定位，它就会跟随父级进行改变位置
            无论父级是相对定位还是绝对定位
            工作中一般采用相对定位
            */
            position: absolute;
            /* left: 20px;
            top:30px; */
            right: 20px;
            bottom: 50px;

            width: 200px;
            height: 200px;
            background-color: green;
        }

        /* 
            绝对定位查找父级的方式：
                就近查找定位的父级，如果找不到这样的父级
                就以浏览器窗口为参考
        */
    </style>
</head>
<body>
    <div class="father">
        <div class="son">
            <div class="sun"></div>
        </div>
    </div>
</body>
</html>
```

### 案例

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2067.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        .banner{
            position: relative;
            margin: 0 auto;
            width: 1226px;
            height: 600px;
        }

        .mask{
            position: absolute;
            left: 0;
            bottom: 0;

            /* 
            绝对定位的盒子显示模式具备行内块特定：加宽度高度生效
            没有内容的话，盒子的宽度尺寸就是 0 

            如果子级和父级的宽度相同，宽度可以这样写：
                width: 100%;
            */
            /* width: 1226px; */
            width: 100%;
            height: 150px;
            background-color: rgba(0, 0, 0, 0.5);
        }
    </style>
</head>
<body>
    <div class="banner">
        <img src="./images/bg.jpg" alt="">
        <!-- 遮罩 -->
        <div class="mask"></div>
    </div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2068.png)

**具备行内块的特点**

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2069.png)

**默认情况下，定位的盒子，后来者居上；z-index： 整数;  数字越大，显示顺序越靠上**

**默认 z-index 为 0** 

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2070.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2071.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2072.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2073.png)

```r
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        input{

            /* 
            浏览器遇到行内和行内块标签当做文字处理，默认文字是按基线对齐
            */
            height: 50px;
            /* 内减 */
            box-sizing: border-box;
            vertical-align: middle;
        }
    </style>
</head>
<body>
    <input type="text"><input type="button" value="搜索">
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2074.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2075.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2076.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2077.png)

overflow:hidden;  比较常用

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2078.png)

一般采用  display: none;

visibility: hidden;  它虽然隐藏了 但是它占位置

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2079.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2080.png)

一定要加给  table 标签

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2081.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2082.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2083.png)

### 项目样式补充

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2084.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2085.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        span{
            display: inline-block;
            width: 18px;
            height: 24px;
            background-color: pink;
            background-image: url(./images/taobao.png);
            /* 背景图位置属性：改变背景图的位置
            水平方向设置 垂直方向的位置

            想要向左侧移动图片，位置取负数
            */
            background-position: -3px 0;
        }

        b{
            display: block;
            width: 25px;
            height: 21px;
            background-color: green;

            background-image: url(./images/taobao.png);
            background-position: 0 -90px;
        }
    </style>
</head>
<body>
    <!-- 精灵图的标签都用行内标签 span b i -->
    <span></span>

    <b></b>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2086.png)

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2087.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            width: 400px;
            height: 300px;
            background-color: pink;
            background-image: url("./images/1.jpg");
            background-repeat: no-repeat;
            /* 
            如果图的宽或高与盒子的尺寸相同了，另一个方向停止缩放
            导致盒子可能会有留白
            */
            /* background-size: 50%; */
            /* 如果宽度或高度和盒子尺寸完全相同，导致图片显示不全 */
            /* background-size: contain; */

            /* 工作中，图的比例和盒子的比例都是相同的
            contain 和 cover 效果完全相同 */
            background-size: 400px 300px;
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2088.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            width: 200px;
            height: 200px;
            background-color: pink;
            box-shadow: 5px 10px 20px 1px green inset;
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```

![Untitled](CSS%20%E8%AF%AD%E8%A8%80%206ab6193f2de54ed0b2f5337e13a75539/Untitled%2089.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 过渡配合 hover 使用  谁变化谁加过渡属性*/
        .box{
            width: 200px;
            height: 200px;
            background-color: pink;

            /* 宽度 200 宽度 600  花费 1秒钟 */
            /* transition: width 1s, background-color 2s; */
            /* 如果变化的属性多，直接写 all，表示所有 */
            transition: all 1s;
        }

        .box:hover{
            width: 600px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="box"></div>
</body>
</html>
```