
1. 学习目标
    1) 盒子模型分类

    2) 浮动布局

-------------------------------------------------------------

2. 盒子模型

    1) 分类
        1> 标准模式: html页面具有文档声明
        2> 怪异模式: 低版本IE中没有文档声明

    2) 理解: 
        1> 标准模式: 在内容之外绘制border和padding
        2> 怪异模式: 在内容之内绘制border和padding

    3) 计算方式: 
        1> 标准模式: 总宽度 = 设置width + 左右border + 左右padding + 左右margin
        2> 怪异模式: 总宽度 = 设置width + 左右margin

    4) 相互转换
        box-sizing: 
            content-box;  //标准模式  - 默认
            border-box;   //怪异模式  - 必须记住

    5) 项目中: 
        *{
            box-sizing: border-box;
        }

-------------------------------------------------------------

3. 浮动布局

    1) 浮动最初创建的目的: 文字环绕图片

    2) 原理: 浮动的元素会脱离文档流, 向左向右漂浮

    3) 浮动带来影响: 造成父级元素高度塌陷

    4) 解决浮动带来影响: 清除浮动

-------------------------------------------------------------

4. 清除浮动

    1) (不用)设置父元素高度
        缺点: 固定高度,难维护

    2) (不用)在浮动元素后,新建一个空白div,引入样式: clear: both;
        <div>
            <p class="fl"></p>
            <p class="fl"></p>
            <p class="fl"></p>
            <div style="clear: both"></div>
        </div>

        缺点: 增加了很多无用div, 影响后期js操作

    3) (不用)在父元素中引入样式: overflow: hidden;
        <div style="overflow:hidden">
            <p class="fl"></p>
            <p class="fl"></p>
            <p class="fl"></p>
        </div>

        缺点: 隐藏元素,不能和定位position一起使用

    4) (项目使用) 在父元素用伪元素清除
        .clearfix:after{
            content: '';        /*内容为空*/
            height : 0 ;        /*高度为0*/
            display: block;     /*转为块级元素*/
            clear: both;        /*清除两边浮动*/
        }

        <div class="clearfix">
            <p class="fl"></p>
            <p class="fl"></p>
            <p class="fl"></p>
        </div>

        缺点: 书写麻烦(忽略不计)

-------------------------------------------------------------

5. 溢出
    overflow: hidden; 溢出隐藏
    overflow: scroll; 溢出产生滚动条


-------------------------------------------------------------

6. display:呈现

    display: block;         以块元素方式显示        独占一行   可以设置宽高
    display: inline-block;  以行内块元素方式显示    共享一行   可以设置宽高
    display: inline;        以行内元素方式显示      共享一行   不能设置宽高
    display: none;          隐藏


-------------------------------------------------------------

7. 其他样式

    1) 清除列表前面样式: 
        ul{ list-style: none }

    2) 折叠表格的边框线
        table{ border-collapse: collapse; }

    3) 鼠标形态
        cursor: pointer;  手型