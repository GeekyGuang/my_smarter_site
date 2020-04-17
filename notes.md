- html ignores carriage returns
- <p>paragraph tag</p> 
- <br> 
- <h1></h1> ... <h6></h6> heading 省掉closing tag也不会报错
- 字体有空格要用引号
```css
p {
    font-family: Georgia, "Times new Roman", Times, serif;
}
```
- html里不管有多少空格/换行，都只显示一个空格
- font-weight 范围： 100-900 或者：lighter normal bold bolder
- font-style: italic; 斜体
- 在默认的html样式中<i>和<em>,<b>和<strong>的样式一样。不过从语义上来讲<i>和<b>是表现元素，仅仅改变外观,<em>和<strong>分别意味着行为的强调和加重强调，在搜索引擎中更受重视,一些语音阅读器也会根据它在阅读时加强语气。另外所有的表现元素其实都是不推荐使用的，应该使用css来代替

- color
```css
.standout {
    color: #cc0000;
}
```

- space
```css
p.spacy {
    letter-spacing: 1em; /*增加*/
    word-spacing: 2em;
    line-height: 2.4em; /* normal 是1.2em*/
}
```
- text-indent 缩进一行
```css
p.tabbed {
    text-indent: 1.5em;
}
```

- <blockquote>标签 每一行都缩进

- margin 
```css
p.offset {
    margin: 5em 2em 5em .75em; /* clockwise */
    margin-left: 7em;
    margin: 2em; /* 四个都一样可简写 */
}
```

- em是相对parent的单位，例如body的font-size是1.2em, h2的font-size是0.5em, 则相对default是0.6em

- group
```css
h1, h3, h5 {
font-family: Arial, Helvetica, sans-serif;
text-align: center;
}
```

- 一个id在html界面只能出现一次
```css
h2#warm {
    color: orange;
}
```
- img
```html
<img src=“images/founder.jpg”>
```

- Divs are block elements, but we place them side-by-side all the time using something called float

- block element begins and ends a line, without sharing the line with another element; inline element can share a line with other elements
```css
img {
    display: block;
}
```

- Centering an image
```css
img.smack-in-the-middle {
    display: block;
    margin-right: auto; 
    margin-left: auto; /*两个缺一不可*/
}
```

- float
```css
img.float {
    float: right;
    margin: 0 2em 2em 2em;
}
```

- clear 取消wrap
```css
p.no-wrap {
    clear: both;
}
```
- link
```html
 <a href="http://www.stackoverflow.com">Stack Overflow</a> 
```
- back to the top
```html
<div class=“content” id=“top”>
<a href=”#top“>Back to the top</a>
```
- open in new windows
```html
<a href=“http://www.wikipedia.org” target=“_blank”>
```

- style links
```css
a:hover {
    text-decoration: none; /* 去掉下划线 */
    font-weight: bold;
    color: orange;
}

a:active { /*点击时*/

    color: red;
}

a:visited { /*点击后*/
    color: green;
}
```

- map-area
```html
<area shape=“rect” alt=“Tuttle House” coords=“76,42,279,510” href=“tuttle-house.html”>
<!--coordinate 坐标 rect时是第四象限 -->
```

- selector
```css
div p  /* div内所有p */

div + p /* div后的第一个相邻的p */

div > p  /* div内第一层的p */
```

- table
```html
    <table>
      <tr>
        <th scope="col"></th>  <!-- 可以不加scope -->
        <th scope="col">姓名</th>
        <th scope="col">年龄</th>
        <th scope="col">城市</th>
      </tr>
      <tr>
        <th scope="row">1</th>
        <td>小王</td>
        <td>20</td>
        <td>纽约</td>
      </tr>
      <tr>
        <th scope="row">2</th>
        <td>小李</td>
        <td>18</td>
        <td>沈阳</td>
      </tr>
    </table>


    <td colspan="3">休</td>
    <td rowspan="2">物理</td> <!-- 数字不加引号也没错 -->
```

- eliminate spaces
```css
table {
  border-collapse: collapse;
  /*border-collapse: seperate;*/
}
```

- border-spacing
```css
table {
    /*只在border-collapse不是collapse时有效*/
    border-spacing: 2em 1em; /*第一个是水平距离，第二个垂直距离，如果只给一个参数，就是水平和垂直距离*/
}
```

- vertical-align
```css
th, td {
    vertical-align: top;  /*top center bottom*/
}

```

- form
```html
    <form action="xxx.php" method="post">
      <input type="text" name="username" size="25" maxlength="40"> <!-- type text password-->
      <textarea name="message" rows="4" cols="30"></textarea>
      <input type="submit" value="Send the message"> <!-- Button -->
      <input type="image" src="http://www.asmarterwaytolearn.com/stooges.jpg" alt="send" width="20" height="30">
      <!-- radio -->
      Gender:
      <input type="radio" name="gender" value="male" checked="checked">male
      <input type="radio" name="gender" value="female">female

      <!-- checkbox -->
      Gender:
      <input type="checkbox" name="gender" value="male" checked="checked">male
      <input type="checkbox" name="gender" value="female">female

      <!-- select box -->
      Your education background:
      <select name="edu">
        <option value="小学">小学</option>
        <option value="中学">中学</option>
        <option value="社会人">社会人</option>
      </select>

      <!-- label -->
      Gender:
      <label><input type="radio" name="gender" value="male" checked="checked">male</label>
      <label><input type="radio" name="gender" value="female">female</label>

      <br><br>
      Your favorite food:<br>
      <input type="checkbox" name="fav_food" id="app" value="apple" checked="checked">
      <label for="app">apple</label>
      <input type="checkbox" name="fav_food" id="mel" value="melon">
      <label for="mel">melon</label>
      <input type="checkbox" name="fav_food" id="ora" value="orange">
      <label for="ora">orange</label>
      <input type="checkbox" name="fav_food" id="ban" value="banana">
      <label for="ban">banana</label>
      <br><br>
    </form>
```

- comments注释
<!-- html -->
/* css */

- div
the most important function of divs is layout positioning. 
div就是个大箱子，把其他小箱子装进去

After coding side-by-side divs in HTML, you’d code an empty div whose only
purpose is to clear the float above it.
<div class=“no-wrap”></div>

```css
div#d1 {
    width: 30%;
    float: left;
    border: 1px solid red;
}

div#d2 {
    width: 65%;
    float: right;
    border: 1px solid red;
}

div.no-wrap {
    clear: both;
    border: 1px solid red;
}
```

- avoid pixels
> we’re avoiding pixels because they prevent the page from adapting to different-size windows.

- fixed positon
```css
/* 不会随屏幕滚动 */
div#header {
    position: fixed;
    left: 0;
    top: 0;
}
```

- When you specify position: absolute or position: fixed, you remove the div from the normal flow of the HTML.
other elements ignore it, They behave as if it weren’t there.

- z-index
```css
z-index: -1;
``

- 去掉a标签下划线
```css
a {
    text-decoration: none;  /* 只能作用在a标签上 */
}
```









