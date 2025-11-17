# HTML学习笔记



## 一、HTML简介和环境搭建

**HTML**：超文本标记语言，通过一系列标签来定义文本、图像链接等等。HTML标签是由尖括号包围的关键字。标签经常成对出现，包括开始标签和结束标签，内容位于这两个标签之间，也有单标签，但是运用于没有内容的元素。

**文件结构**：！开头的部分、html、 head、body

**输入一个文档**：vscode里面创建新文件输入!+tab即可
（ps:在vscode里面输入的标签会自动显示开头字母，因此只需要选择想要输入的内容+tab即可）

**修改title**：找到title标签，替换尖括号之间的内容

**打开htm**l:空白右键，选择open with live sever即可

## 二、常用文本标签

```.txt
<h1>一级标签</h1>
<h2>二级标签</h2>
<h3>三级标签</h3>
<h4>四级标签</h4>
<h5>五级标签</h5>
<h6>六级标签</h6>
<p>这是一个段落标签</p>
<p>更改文本样式：<b>字体加粗</b>、<i>斜体</i>、<u>下划线</u>、<s>删除线</s></p>
```

<h1>一级标签</h1>
<h2>二级标签</h2>
<h3>三级标签</h3>
<h4>四级标签</h4>
<h5>五级标签</h5>
<h6>六级标签</h6>
<p>这是一个段落标签</p>
<p>更改文本样式：<b>字体加粗</b>、<i>斜体</i>、<u>下划线</u>、<s>删除线</s></p>

```.txt
<ul>
    <li>无序列表元素1</li>
    <li>无序列表元素2</li>
    <li>无序列表元素3</li>
</ul>
```

<ul>
    <li>无序列表元素1</li>
    <li>无序列表元素2</li>
    <li>无序列表元素3</li>
</ul>

```
<ol>
    <li>有序列表元素1</li>
    <li>有序列表元素2</li>
    <li>有序列表元素3</li>
</ol>
```



<ol>
    <li>有序列表元素1</li>
    <li>有序列表元素2</li>
    <li>有序列表元素3</li>
</ol>

```
<h1>table row</h1>
<h1>table data</h1>
<h1>table header</h1>
<table border="2">
    <tr>
        <th>列标题1</th>
        <th>列标题2</th>
        <th>列标题3</th>
    </tr>
    <tr>
        <td>元素1</td>
        <td>元素2</td>
        <td>元素3</td>
    </tr>
     <tr>
        <td>元素21</td>
        <td>元素22</td>
        <td>元素23</td>
    </tr>
     <tr>
        <td>元素31</td>
        <td>元素32</td>
        <td>元素33</td>
    </tr>
```



<h1>table row</h1>
<h1>table data</h1>
<h1>table header</h1>
<table border="2">
    <tr>
        <th>列标题1</th>
        <th>列标题2</th>
        <th>列标题3</th>
    </tr>
    <tr>
        <td>元素1</td>
        <td>元素2</td>
        <td>元素3</td>
    </tr>
     <tr>
        <td>元素21</td>
        <td>元素22</td>
        <td>元素23</td>
    </tr>
     <tr>
        <td>元素31</td>
        <td>元素32</td>
        <td>元素33</td>
    </tr>

## 三、标签属性

属性在HTML中起到非常重要的作用，他们用于定义元素的行为和外观，以及与其他元素的关系。

基本语法;

```
<开始标签 属性名=“属性值”>
```

- 每个HTML元素可以有不同的属性
- 属性名称不区分大小写，属性值对大小写敏感

```
class     为HTML元素定义一个或者多个类名
id        定义元素唯一个id
style     规定元素的行内样式
```

```
<a href="https://www.baidu.com">这是一个超链接</a>
<br>
<a href="https://www.baidu.com"target="_blank">这是第二个超链接</a>

<hr>
<img src="image-20251105224040147-17623536422901.png" alt="">
<br>
<img src="error-20251105224040147-17623536422901.png" alt="该图片无法显示">
<br>
<img src="image-20251105224040147-17623536422901.png" alt="" width="200" height="200">
<img src="" alt="">
```

target属性定义链接的打开方式
a标签属于行内标签
设置直接在标签内设置宽高

<a href="https://www.baidu.com">这是一个超链接</a>
<br>
<a href="https://www.baidu.com"target="_blank">这是第二个超链接</a>

<hr>
<img src="image-20251105224040147-17623536422901.png" alt="">
<br>
<img src="error-20251105224040147-17623536422901.png" alt="该图片无法显示">
<br>
<img src="image-20251105224040147-17623536422901.png" alt="" width="200" height="200">
<img src="" alt="">

(当图片加载或损坏时在alt""内写解释)

## **四、HTML区块-块元素和行内元素**

块级元素通常用于组织和布局页面的主要结构和内容，他们用于创建页面的主要部分，将内容分割为逻辑块

- 块级元素通常会从新行开始，并且占据整行的宽度，因此它们会在页面上呈现为一块独立的内容块。
- 可以包含其他块级元素和行内元素
- 常见的块级元素：div ,p ,h1-h6,ul,ol,li,table,form等 

行内元素通常用于添加文本样式或为文本中的一部分应用样式。他们可以在文本中插入小的元素

- 行内元素通常在同一行内呈现，不会单独占一行
- 它们只占据其内容所需的宽度，而不是整行的宽度
- 行内元素不能包含块级元素，但可以包含其他行内元素
- 常见的行内元素span,a,strong,em,img,br,input

```
<div class="nav-bar">
        <a href="#">链接1</a>
        <a href="#">链接2</a>
        <a href="#">链接3</a>
        <a href="#">链接4</a>
        <a href="#">链接5</a>
    </div>

    <div class="content">
        <h1>文章标题</h1>
        <p>文章内容</p>
        <p>文章内容</p>
        <p>文章内容</p>
        <p>文章内容</p>
        <p>文章内容</p>
    </div>

    <span>这是第一个span标签</span>
    <span>这是第二个span标签</span>
    <span>这是第三个span标签</span>
    <span>这是第四个span标签</span>
    <hr>
    <span>链接点击这里：<a href="https://www.baidu.com">百度</a></span>
```

<div class="nav-bar">
        <a href="#">链接1</a>
        <a href="#">链接2</a>
        <a href="#">链接3</a>
        <a href="#">链接4</a>
        <a href="#">链接5</a>
    </div>

    <div class="content">
        <h1>文章标题</h1>
        <p>文章内容</p>
        <p>文章内容</p>
        <p>文章内容</p>
        <p>文章内容</p>
        <p>文章内容</p>
    </div>
​    <span>这是第一个span标签</span>
​    <span>这是第二个span标签</span>
​    <span>这是第三个span标签</span>
​    <span>这是第四个span标签</span>

    <hr>
    <span>链接点击这里：<a href="https://www.baidu.com">百度</a></span>
## 五、HTML表单

```
 <form>
        <label for="username">用户名：</label>
        <input type="text" id="username" placeholder="请输入用户名">
        <br><br>
        <label for="pwd">密码：</label>
        <input type="password" id="pwd" placeholder="请输入密码"><br><br>
    
        <label >性别</label>
        <input type="radio" name="gender"> 男
        <input type="radio" name="gender"> 女
        <input type="radio" name="gender"> 其他 <br><br>
   
        <label>爱好</label>
        <input type="checkbox" name="hobby">唱歌
        <input type="checkbox" name="hobby">跳舞
        <input type="checkbox" name="hobby">rap
        <input type="checkbox" name="hobby">篮球<br><br>

        <input type="submit" value="上传">
    </form>
    <form action="#"></form>
```

placeholder显示提示输入信息，输入后消失
value规定输入的值
radio表示单选框+name属性表示只能选一个
type="password“表示不是明文显示比如密码
checkbox表示多选框
submit提交
