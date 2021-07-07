<center><h1>css-day2</h1></center>

# 1. 字体样式

```javascript
#1.字体名称
font-family: '微软雅黑';

#2.字体大小
font-size: 16px;//网页默认字体大小 - pc端
font-size: 2em; //相对值 相对于当前框内字体大小
font-size: 3rem;//相对值 相对于HTML标签字体大小 - 移动端

#3.字体粗细
font-weight: bold;    //加粗
font-weigth: normal; //正常大小

#4.行高
line-height: 30px;
line-height: 2; 		//当前字体大小的2倍
line-height: height值; //单行文本垂直居中

#5.字体颜色
color: red;
color: #000;
color: rgb(200,100,0);
color: rgba(100, 150, 200, .5) //透明度取值范围0-1
```



# 2. 文本样式

```javascript
#1.文本修饰
text-decoration: none; 		//去掉下划线
text-decoration: underline; //添加下划线

#2.文本缩进
text-indent: 2em;   //缩进2个字体大小
text-indent: 30px; //缩进30px

#3.水平对齐
text-align: left; 	//左对齐
text-align: center; //居中对齐
text-align: right; //右对齐

#4.垂直对齐
vertical-align: top; //顶部对齐
vertical-align: middle; //居中对齐
vertical-align: bottom: //底部对齐

小结: 通常用于 清除图片底部4px间距

#5.文本溢出
	1) 单行文本溢出产生省略号
		white-space: nowrap;            /* 不换行 强制在一行显示 */
        overflow: hidden;               /* 溢出隐藏 */
        text-overflow: ellipsis;        /* 文本溢出产生省略号 */

	2) 多行文本溢出产生省略号
        display: -webkit-box;           /* 转为弹性盒子 */
        -webkit-box-orient: vertical;   /* 设置文本为垂直排列 */
        -webkit-line-clamp: 3;          /* 排列行数 */
        overflow: hidden;               /* 溢出隐藏 */

```



# 3. 继承与优先级

```javascript
#1.能够继承的属性: 
    font-family font-size font-weight line-height color text-align text-indent

    小结: a标签不能继承颜色

#2.优先级
    1) 如何计算: 
    	1> 作用在不同标签上: 就近原则

    	2> 作用在相同标签上: 比较权值大小

            style   : 1000 - 行间
            ID      : 100
            class   : 10
            标签    : 1 

    2) 如何提高优先级 - 项目中如何使用
        a. 在值后面加: !important  - 正无穷大
        b. 加选择器层级
```







