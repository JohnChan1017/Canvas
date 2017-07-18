## 《HTML5 Canvas 基础教程》自学总结
*Foundation HTML5 Canvas : For Games and Entertainment* Self-study summary
**绘制矩形**
```html
$(document).ready(function() {
    var canvas = $("#myCanvas");
    var context = canvas.get(0).getContext("2d");
  
    //绘制填充矩形
    context.fillRect(40,40,100,100);
    //绘制一个从原点(40,40)宽100，高100的图形并填充

    //绘制矩形轮廓
    context.strokeRect(150,40,100,100);//绘制一个矩形轮廓
    
    
    //绘制线条
    context.beginPath();//开始路径
    context.moveTo(260,40);//设置路径原点
    context.lineTo(360,40);//继续连接
    context.lineTo(360,140);//设置路径终点
    context.closePath();//结束路径
    context.fill();//填充路径闭合的图形
    // context.stroke();//绘出路径轮廓
});
```
<br>
**解读：context.fillRect(x, y, width, height);**
--
> 创建一个矩形需要输入4个参数。前两个参数是矩形原点（左上角）的(x,y)坐标值，其余两个参数是矩形的宽度和高度。矩形宽度是(x,y)位置向右绘制的距离，而矩形高度是(x,y)位置向下绘制的距离。
词汇
- context:上下文
- fill:填充
- Rectangle:矩形
- Square:正方形  

需要注意的是，调用的方法是fillRect，而不是fillSquare。因为正方形形就是特殊的矩形啊！（正方形就是等边矩形）
**解读：context.strokeRect(x, y, width, height);**
--
> 和fillRect()类似，只是它绘制矩形并给它绘制边框

**解读：context.arc(x, y, radius, startAngle, endAngle, anticlockwise);**
--
> 创建一个圆弧需要使用6个参数：圆弧原点的(x,y)坐标值（也就是例子中的圆心）、圆弧半径、开始角度、结束角度和一个布尔值，如果圆弧按逆时针绘制，那么它为true，否则为false

**解读：context.fillText(text, x, y);**
--
> 