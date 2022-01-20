# HTML5

## HTML5与HTML4的区别

### HTML5推出的理由

解决Web上存在的问题:

web浏览器的兼容性低，在一个浏览器中可以运行的html，css，javascript,在另一个浏览器中不能运行

原因：各浏览器规范不统一，没有被标准化

解决方案：使各浏览器的功能符合通用标准

**文档结构不够明确 **：HTML4元素不能把元素结构表达清楚

解决方案：增加与结构相关的元素

**Web应用程序的功能得到限制**：HTML4对Web应用程序的贡献性小，比如：不允许上传多个文件

解决方案：提供应用程序使用的API

### HTML语法的改变

- **内容类型不变**

HTML5的文件扩展符(html或htm)与内容类型(tex/html)保持不变

- **DOCTYPE声明变化**

HTML4中需要指明html的哪个版本，HTML5不需要，只使用<!DOCTYPE html>即可

- **指定字符编码变化**

HTML4：

```javascript

```

HTML5

```javascript

```

* **可以省略元素的标记**

HTML5中很多元素标记可以省略

* **具有Boolean值的属性调整**

不指定属性值，属性名设定为属性值，字符串设定为空时表示属性值为true

不写该元素表示属性值为false

例如:

```javascript

```

- **可省略引号

HTML5可省略指定属性值时的引号

### 新增的元素和废除的元素

#### 新增的元素结构

**section:**表示页面中内容块，比如章节，页眉，页脚或页面中的其他部分，可与<h1>到<h6>结合使用表示文档结构

**article**:表示页面中一块与上下文不相关的独立内容，比如博客中的一篇文章或报纸中的一篇文章

**aside:**表示article内容之外，与 article内容相关的辅助信息

**header：**表示页面中的区域块，通常表示区域块的脚步或底部，用于承载作者的姓名，创作日期等与作者的元素

**nav**:表示页面中导航部分

**figuer**:表示一段独立的内容，一般表示主体流内容的一个独立单元

#### 新增的其他元素

**video**:定义电影的片段，视频流等视频

**audio:**定义音乐或音频流

**canvas**:画布，本身没有行为，仅提供一块画布，但它的API展现给JavaScript及脚本，能够把想绘制的东西绘制在canvas上

**embed Mark**

#### 新增的input元素的类型

**email:**表示必须输的邮箱地址

**url:**表示文本块输入的一个地址

**number**:表示数字

**range:**表示数字范围值

**DataPickers:**表示日历的日期，时间

#### 废除的元素

##### 能使用css代替的元素

basefont big center font s tt u 等

#### 不再使用fframe框架









# 第二章  HTML5拖放

## 怎么实现拖放

### 1.源元素

- 拖的文件，图片

- 事件

  - dragstart:当元素开始拖放

  - darg:拖放过程

### 2.目标元素

- 放的地方
- 事件
  -  dragenter:拖放事件投放到目标的事件
  - dragover:在目标区域移动
  - dragleave:离开当前目标区域
  - drop:在目标区域的投放事件

### 3.使用dataTransfer传递数据

- getData('放设置数据时的类型')
  - 获取数据
- setData('类型','值')
  - 设置数据
- files
  - 获取拖放文件的信息
  - type
    - 文件类型
  - size
    - 文件大小
  - name
    - 文件名

#### 4.设置源元素允许拖放

设置源元素的属性` draggable值为true` 







# 第三章 多媒体组件及API开发

### 音频(audio)

```html
 <!-- muted静音 -->
 <!-- controls -->
 <!-- loop重新播放 -->
 <!-- preload -->
<audio width="320px" height="240px" controls muted>
    <source src="地址" type="video/mp3">
    <source src="地址" type="video/ogg">
    <source src="地址" type="video/wav">
</audio>
```

### 视频(vedio)

```html
<video width="320px" height="240px" controls muted>
    <source src="地址" type="video/mp4">
    <source src="地址" type="video/ogg">
    <source src="地址" type="video/mpeg">
</video>
```

### 自定义多媒体

```html

```

# 第四章表单新功能解析及地理位置定位

##  HTML5新的input类型

### color拾色器中选择一个颜色

```html
<input type="color" />
```

### date选择一个日期

```html
<input type="data" />
```

### datetime选择一个日期（UTC时间）

```html
<input type="datetime" />
```

### datetime-local 选择一个日期和时间(无时区)

```html
<input type="datetime-local" />
```

### email 邮箱

```html
<input type="mail" />
```

### month选择月份

```html
<input type="month" />
```

### number数字

```html
<input type="number" />
```

### range滑动条

```html
<input type="range" />
```

### search

```html
<input type="search" />
```

### tel

```html
<input type="tel" />
```

### time

```html
<input type="time" />
```

### url

```html
<input type="url" />
```

### week选择周和年

```html
<input type="week" />
```

## HTML5表单元素

### datalist下拉列表

```html
<input list="datalist">
<datalist id="datalist">
    <option value="重庆">
    <option value="成都">
    <option value="上海">
    <option value="北京">
</datalist>
```

### output文本框相加

```html
<form oninput="x.value=Number(a.value)+Number(b.value)">
    <input type="number" id="a">+
    <input type="number" id="b">=
    <output name="x" for="a b"></output>
</form>
```

## HTML5表单属性

### form新属性

- autocomplete

- Novalidate

### input新属性

- autocomplete  记住输入文字
  - on:保留
  - off:不保留

```html
<form action="http://www.baidu.com" autocomplete="on">
    姓名:<input type="text" /> 邮箱:
    <input type="email" autocomplete="off" />
    <input type="submit">
</form>
```



- atuofocus 自动获取焦点

  ```html
  <form action="http://wwww.baidu.com">
      姓名:<input type="text" autofocus/>
      <input type="submit" />
  </form>
  ```

- form 

  ```html
  <form action="http://www.baidu.com" id="form1">
      姓名:<input type="text" /> 邮箱:
      <input type="email" />
      <input type="submit" /> </form>
  <input type="text" form="form1" />
  ```

- formaction

- formenctype
- formmethod
- formnovalidate
- formtarget
- height与width
- list
- min与max
- multiple
- pattern(regexp)
- placeholder
- required
- step

## Geolocation(地理定位)

### 1.获取精确位置

```html
function geo() {
    var box = document.querySelector("#box1")
    //判断浏览器是否支持地理定位
    if (navigator.geolocation) {
        //如果支持，获取当前的经度，纬度
        navigator.geolocation.getCurrentPosition(function(p) {
            console.log(1)
            box.innerHTML = `当前位置的经度：${p.coords.longitude},
当前位置的纬度：${p.coords.latitude}`
        }, function(e) {
            switch (e.code) {
                case 1:
                    console.log('用户选择了不允许')
                    break
                case 2:
                    console.log('连不上gps')
                    break
                case 3:
                    console.log('连接超时')
                    break
                default:
                    console.log('未知错误')
                    break
            }
        }, {
            // 设置浏览器获取高精度的位置 默认为false
            enableHighAccuracy: true,
            //设置获取地理位置的超时时间，默认不超时，单位毫秒
            timeout: 5000,
            // 最长有效期，重复获取地理位置时，此参数指定多久再次获取位置
            maximumAge: 3000
        })

    } else {
        box.innerHTML = '当前浏览器不支持地理定位'
    }
}

```

### 2.监听实时位置

```html
// 监听实时位置        
;(function() {
    var w = navigator.geolocation.watchPosition(function(p) {
        console.log(1)
        console.log("实时位置纬度：" + p.coords.latitude)
        console.log("实时位置经度：" + p.coords.longitude)
        navigator.geolocation.clearWatch(w) // 清空实时位置
    })
    })()
```

### 3.百度地图

```html
<script src="http://api.map.baidu.com/api?v=1.0"></script>
<script>
    ;(function() {
        navigator.geolocation.getCurrentPosition(function(p) {
            var map = new BMapGL.Map("container"); // 创建地图实例 
            var point = new BMapGL.Point(p.coords.longitude, p.coords.latitude); // 创建点坐标 
            map.centerAndZoom(point, 15); // 初始化地图，设置中心点坐标和地图级别
            map.enableScrollWheelZoom(true); //开启鼠标滚轮缩放
            map.setHeading(64.5); //设置地图旋转角度
            map.setTilt(73); //设置地图的倾斜角度
        })
    })()
</script>
```

## Canvas路径和三角函数

### 1.SVG

- SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
- SVG 用于定义用于网络的基于矢量的图形
- SVG 使用 XML 格式定义图形
- SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
- SVG 是万维网联盟的标准

### SVG优势

与其他图像格式相比（比如 JPEG 和 GIF），使用 SVG 的优势在于：

* SVG 图像可通过文本编辑器来创建和修改
* SVG 图像可被搜索、索引、脚本化或压缩
* SVG 是可伸缩的
* SVG 图像可在任何的分辨率下被高质量地打印
* SVG 可在图像质量不下降的情况下被放大

### SVG 与 Canvas两者间的区别

* SVG 是一种使用 XML 描述 2D 图形的语言。
* Canvas 通过 JavaScript 来绘制 2D 图形。
* SVG 基于 XML，这意味着 SVG DOM 中的每个元素都是可用的。您可以为某个元素附加 JavaScript 事件处理器。
* 在 SVG 中，每个被绘制的图形均被视为对象。如果 SVG 对象的属性发生变化，那么浏览器能够自动重现图形。
* Canvas 是逐像素进行渲染的。在 canvas 中，一旦图形被绘制完成，它就不会继续得到浏览器的关注。如果其位置发生变化，那么整个场景也需要重新绘制，包括任何或许已被图形覆盖的对象。

**五角星**

```html
<svg xmlns="http://www.w3.org/2000/svg" version="1.1" height="190">
    <polygon points="100,10 40,180 190,60 10,60 160,180"
             style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;"/>
</svg>

<svg xmlns="http://www.w3.org/2000/svg" version="1.1" height="190">
    <polygon points=""
             style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;"/>
</svg>
```

### 2.Canvas画布

* 获取画布

```html
var c = document.querySelector("div属性名")
```

* 创建画布

```html
var cxt = c.getContext("2d")
```

* 实例(使用 JavaScript 来绘制图像)

```html
<script>
    // <!-- 获取画图 -->
    var c = document.querySelector("#myCanvas")
    //创建画布
    var cot = c.getContext("2d")
    //填充颜色
    cot.fillStyle = "red"
    //rect 创建矩形
    cot.fillRect(0, 0, 150, 75)//x（横坐标），y（纵坐标） ，矩形的宽，矩形的高  
</script>
```

**注意：**

上面的 fillRect 方法拥有参数 (0,0,150,75)。

意思是：在画布上绘制 150x75 的矩形，从左上角开始 (0,0)。

### Canvas坐标

* Canvas是一个二维网格
* Canvas的左上角坐标是(0，0)

### Canvas - 路径

**在Canvas上画线，我们将使用以下两种方法：**

* moveTo(*x,y*) 定义线条开始坐标
* lineTo(*x,y*) 定义线条结束坐标

**实例**

```javascript
var a = document.querySelector("#mycanvas")
var ctx = a.getContext("2d")
ctx.moveTo(20, 20)
ctx.lineTo(20, 200)
ctx.stroke()
```

### canvas绘制圆形

**语法：**

* ```html
  arc(x,y,r,start,stop)
  ```

```javascript
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.beginPath();
ctx.arc(55, 50, 40, 0, 2 * Math.PI);
ctx.stroke();
```

### Canvas - 文本

* **font** - 定义字体
* **fillText**(**文字**,x,y) - 在 canvas 上绘制实心的文本
* **strokeText**(**文字**,x,y) - 在 canvas 上绘制空心的文本

```javascript
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.font="30px Arial";
ctx.fillText("Hello World",10,50);
```

**strokeText():**

```javascript
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
ctx.font="30px Arial";
ctx.strokeText("Hello World",10,50);
```

### Canvas 修饰线条

* **lineWidth** 线条宽度
* **lineCap = "square"** 方角
* **lineCap = "round"** 圆角
* **lineJoin = "round"**两条线段相交时创建的拐角----圆角
* **ineJoin = "square"** 两条线段相交时创建的拐角----方角
* **miterLimit** 最大斜接长度

**方角实例:**

```javascript
var a = document.querySelector("#mycanvas")
var ctx = a.getContext("2d")
ctx.lineWidth = "4"
ctx.lineCap = "square"
ctx.moveTo(20, 20)
ctx.lineTo(20, 200)
ctx.stroke()
```

**圆角实例:**

```javascript
var a = document.querySelector("#mycanvas")
var ctx = a.getContext("2d")
ctx.lineWidth = "4"
ctx.lineCap = "round"
ctx.moveTo(20, 20)
ctx.lineTo(20, 200)
ctx.stroke()
```

**线段相交时创建的拐角**:

```javascript
var a = document.querySelector("#mycanvas")
var ctx = a.getContext("2d")
ctx.lineWidth = "4"
ctx.lineJoin = "round"
ctx.moveTo(20, 20)
ctx.lineTo(100, 50)
ctx.lineTo(20, 100)
ctx.stroke()
```

### Canvas 渐变

* **createLinearGradient(*x,y,x1,y1*) - 创建线条渐变**
* **createRadialGradient(*x,y,r,x1,y1,r1*) - 创建一个径向/圆渐变**

**注意:**

当我们使用渐变对象，必须使用两种或两种以上的停止颜色。

 addColorStop()方法指定颜色停止，参数使用坐标来描述，可以是**0**至**1**

使用渐变，设置fillStyle或strokeStyle的值为 渐变，然后绘制形状，如矩形，文本，或一条线。

**线性渐变**

```javascript
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");

// 创建渐变
var grd=ctx.createLinearGradient(0,0,200,0);
grd.addColorStop(0,"red");
grd.addColorStop(1,"white");

// 填充渐变
ctx.fillStyle=grd;
ctx.fillRect(10,10,150,80);
```

**径向渐变**

```javascript
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
 
// 创建渐变
var grd=ctx.createRadialGradient(75,50,5,90,60,100);
grd.addColorStop(0,"red");
grd.addColorStop(1,"white");
 
// 填充渐变
ctx.fillStyle=grd;
ctx.fillRect(10,10,150,80);
```

### Canvas 阴影

**shadowOffsetX** 设置或返回阴影与形状的水平距离

* shadowOffsetX=0 指示阴影位于形状的正下方
* shadowOffsetX=20 指示阴影位于形状 left 位置右侧的 20 像素处。
* shadowOffsetX=-20 指示阴影位于形状 left 位置左侧的 20 像素处。

**注意:**

请将**shadowColor**和**shadowBlur**一起使用

**实例:**

```javascript
var a = document.querySelector("#mycanvas")
var ctx = a.getContext("2d")
ctx.shadowBlur = 20
ctx.shadowColor = "black"//阴影颜色
ctx.fillStyle = "red"
ctx.fillRect(20, 20, 100, 80)
```

### Canvas 裁剪

* **clip()**方法从原始画布中剪切任意形状和尺寸

**注意:**

* 一旦剪切了某个区域，则所有之后的绘图都会被限制在被剪切的区域内（不能访问画布上的其他区域）
* 使用 save() 方法对当前画布区域进行保存，并在以后的任意时间对其进行恢复（通过 restore() 方法）

```javascript
var a = document.querySelector("#mycanvas")
var ctx = a.getContext("2d")
//绘制一个矩形
ctx.rect(20, 20, 300, 300)
ctx.fillStyle = "black"
ctx.fill()
ctx.stroke()
//裁剪
ctx.clip()
ctx.fillStyle = "red"
ctx.fillRect(30, 30, 100, 100)
```

### Canvas 图像

**把一幅图像放置到画布上**

* drawImage(*image,x,y*)

**实例:**

```javascript
var c=document.getElementById("myCanvas");
var ctx=c.getContext("2d");
var img=document.getElementById("scream");
ctx.drawImage(img,10,10);
```

### 圆弧和曲线的绘制

#### 二次贝塞尔曲线

**quadraticCurveTo** 方法通过使用表示二次贝塞尔曲线的指定控制点，向当前路径添加一个点

* 第一个点是用于二次贝塞尔计算中的控制点

* 第二个点是曲线的结束点

* 曲线的开始点是当前路径中最后一个点

  **注意:**

  如果路径不存在，那么使用 [beginPath()](https://www.runoob.com/tags/canvas-beginpath.html) 和 [moveTo()  ](https://www.runoob.com/tags/canvas-moveto.html) 方法来定义开始点。

  ```javascript
  var a = document.querySelector("#mycanvas")
  var ctx = a.getContext("2d")
  ctx.beginPath()
  ctx.moveTo(20, 20)
  ctx.quadraticCurveTo(20, 100, 200, 20)
  ctx.stroke()
  ```

  

  





