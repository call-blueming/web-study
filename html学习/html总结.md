<center><h1>html总结</h1></center>

```html
0.html是有什么组成的？
  元素-标签
1.通用的属性有哪些？
 id class style title
2.行内元素和块级元素的区别？
  特点：行内元素共享一行 块级元素独占一行
  常见元素：块级（div,h1-h6,p,pre,ul,ol,li,form,table, ）行级元素  （ a,img,span，i（斜体）,em（强调）,sub(下标)，sup（上标）labe等）
  如何使用：块级元素常用于布局，行内元素常用于描述局部内容
3 标题标签：hn 
  独占一行
4 超链接标签语法，默认打开新窗口的方式
<a href="#" target=_blank></a>
5相对路径和绝对路径
<a href="https://www.jd.com"></a>
       box
            -news
                --a.html
                --about
                    ---b.html
            -pro
                --e.html
            c.html
         <a href="about/b.html">a链接到b</a>
         <a href="../about/b.html">e链接到b</a>
         <a href="../c.html">b链接到c</a>
6. 什么是标签语义化,为什么要使用?
根据标签的含义来选择对应的标签
根据页面的结构来选择对应的标签
方便浏览器和seo收录与识别
7. 无序列表结构和自定义列表结构?
<ul>
    <li><li> 
    <li><li>
    <li><li>
    <li><li>
</ul>
<dl>
    <dt></dt>
    <dd></dd>
     <dd></dd>
     <dd></dd>
</dl>
8. 图片标签结构?
<img src="" alt="">
9. 表单结构
    文本框: <input type="text" name="">
    密码框: <input type="password" name="">
    单选框:  <input type="radio" name="">
    复选框: <input type="checkbox" name="">
    下拉框:<select>
        <option></option>
        <option></option>
</select>
文本域框: <textarea></textarea>
    input提交按钮: <input type="submit" value="提交">
    input普通按钮:<input type="button" value="按钮">
    input重置按钮:<input type="reset" vatijiaolue="重置">

    button提交按钮:<button type="submit">
        提交
</button>
button普通按钮:<button></button>
    button重置按钮:<button type ="reset">
        
</button>
10. get和post的区别?
get将提交的值和参数附于url之后url?参数=值&参数=值
get提交的数据一般不超过4kb
get相对来说并不安全
post将提交到后台的值隐藏起来
没有大小限制
相对安全
11. 只读属性: readonly
12. 禁用属性: disable
13. 占位符:placeholder
14. 单选框选中属性: checked
15. 下拉框选中属性: selected
16. label标签是行内元素还是块级元素?如何判断的
行内元素
<lable for="">男</lable><input type="text" id="">
17. 图片标签中alt属性是什么意思?
规定图像的替代文本，当图片加载失败时显示。
```







