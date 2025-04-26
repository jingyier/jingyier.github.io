---
title: HTML简单总结
date: 2025-04-26 09:37:34
tags: [HTML]
categories: [学习]
---
## HTML基础知识
- HTML 代码是由 “标签” 构成的；
- 整体的 HTML 代码是由一对 html 包裹的；
- head 标签是页面的头部，标签中写页面的属性；
- body 标签是页面的主体，标签中写的是页面显示的内容；
- title 标签中写的是页面的标题。
#### 默认页面模板：！+tab,生成代码如下
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
```
### 一、常见标签
#### 1.注释标签

```
<!--我是注释-->
```
#### 2.标题标签
```
<body>
    <h1>这是一级标签</h1>
    <h2>这是二级标签</h2>
    <h3>这是三级标签</h3>
    <h4>这是四级标签</h4>
    <h5>这是五级标签</h5>
    <h6>这是六级标签</h6>
</body>
```
#### 3.段落标签
```
<body>
    <p>段落一</p>
    <p>段落二</p>
    <p>段落三</p>
</body>
```
#### 4.换行标签
```
<body>
    第一行<br>
    第二行<br>
    第三行<br>
</body>
```
#### 5.格式化标签
```
<body>
    <strong>加粗</strong>
    <b>加粗</b>

    <em>倾斜</em>
    <i>倾斜</i>

    <del>删除线</del>
    <s>删除线</s>

    <ins>下划线</ins>
    <u>下划线</u>

</body>
```
#### 6.图片标签
```
<body>
    <img src="相对路径，绝对路径或网络路径" alt="图片加载错误时的描述信息" width="宽" height="高" >
</body>
```
注意width 单位是px 像素。
#### 7.超链接标签
```
<body>
    <a href="网址">点击此处跳转</a>
</body>
```
超链接标签用<a> </a>来表示，其中的href属性表示点击后会跳转到哪个页面，target表示打开方式，默认是_self，在本标签页打开，如果设置为_blank，则用新的标签页打开。
#### 8.表格标签
```
<table border="1">
    <!-- 表头 -->
    <th>列标题1</th>
    <th>列标题2</th>    
    <th>列标题3</th>    
    <th>列标题4</th>    
 <tr> 
    <!-- 每一行都是一个tr标签 -->
     <!-- 每一列都是一个td标签 -->
        <td>444</td>
        <td>欸嘿嘿</td>
        <td>444</td>
        <td>444</td>

</tr>
    
    <tr>
        <td>444</td>
        <td>444</td>
        <td>好玩</td>
        <td>444</td>

    </tr>
    
    <tr>
        <td>666</td>
        <td>444</td>
        <td>444</td>
        <td>444</td>

    </tr>
    
</table>
```


#### 9.列表标签
```
 <!-- 无序列表 -->
   <ul>

        <li>lalala</li>
        <li>lalala</li>
        <li>lalala</li>
        <li>lalala</li>

   </ul>

   <!-- 有序列表 -->
   <ol>

    <li>111111</li>
    <li>111111</li>
    
   </ol>
```
#### 10.表单标签
```
<body>
    <form action="">
        <label for="">用户名：</label>
        <input type="text" id="username"  placeholder="有点意思">
        <br><br>
        <label for="">密码：</label>
        <input type="password" id="psw" placeholder="有点意思">
        <br><br>
        <label>性别</label>
        <input type="radio" name="gender">男    
        <input type="radio" name="gender">女
         <br>
        <label for="">爱好</label>
                          <!-- 通过相同的name使得单选框互斥，构成单选 -->
        <input type="checkbox" name="hobby">唱跳
        <input type="checkbox" name="hobby">rap
        <input type="checkbox" name="hobby">篮球
        <br><br>
                         <!-- value生成固定字样 -->
        <input type="submit" value="上传">
    </form>
</body>
```


