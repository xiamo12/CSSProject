CSS点亮灯泡

访问地址：https://xiamo12.github.io/CSSProject/bulb-lighting/index.html

# 点亮灯泡

将灯泡主体划分为四部分区域：

## 1、灯泡上半部分-圆形灯头：

- *制作圆形的代码*

```css
  width: 280px;
  height:280px;
  border-radius: 50%;
```

- *灯头的定位代码*

```css
margin: 0 auto; /*定宽块状元素的居中方式，在父盒子中居中显示*/
```

- *背景和过渡动画*

```css
background-color: #807d7d;
transition: 0.6s/*transition-property transition-duration transition-timing-function transition-deley的简写模式，其中过渡动画的持续时间transition-duration是必须的*/
```

## 2、灯泡下半部分[center]

- *过渡区域主体代码`.bulb-area2`：梯形*

```css
width: 142px;
height: 0;
border-left: 16px solid transparent;
border-right: 16px solid transparent;
border-top: 40px solid #807d7d;
```

- *过渡区域主体代码`.bulb-area2`：定位*

```css
position: relative;
margin: -12px auto 0 auto;
```

- *过渡区域主体代码`.bulb-area2`：过渡动画*

```css
transition: 0.6s
```

## 2、灯泡下半部分[top]

- 过渡区域代码上半部分`.bulb-area2:before`：梯形

```css
	content: "";
	width: 172px;
	height: 0;
	border-left: 32px solid transparent;
	border-right: 32px solid transparent;
	border-top: 54px solid #807d7d;
```

- *过渡区域代码上半部分`.bulb-area2:before`：定位*

```css
	margin: -93px auto 0 auto;
	position: absolute;
	left: -47px;
```

- *过渡区域代码上半部分`.bulb-area2:before`：过渡动画*

```css
transition: 0.6s;
```

## 3、灯泡下半部分[bottom]

- *灯头衔接区域代码下半部分`.bulb-area2:after`：矩形，下方圆角*

```css
	content: "";
	width: 144px;
	height: 55px;
	border-radius: 0 0 200px 200px;
	background: #728b4b; /*灯头浅绿色部分*/	
```

- *灯头衔接区域代码下半部分`.bulb-area2:after`：定位*

```css
	margin: -4px auto 0 auto;
	padding: 0;
	position: absolute;
	top: 0px;
	left: -1px;
```

## 4、灯头螺口[center]

- *螺口中间部分代码`bulb-neck1`：矩形*

```css
	width: 120px;
	height: 12px;
	background: #807d7d;
```

- *螺口中间部分代码`bulb-neck1`：定位*

```css
	margin: 32px auto 0;
	padding: 14px 0;
	position: relative;
```

## 5、灯头螺口[top/bottom]

- 螺口上、下部分代码：`.bulb-neck1:before, .bulb-neck1:after`：外形

```css
	content: "";
	width: 120px;
	height: 16px;
	background: #694b8b;
```

- *螺口上、下部分代码：`.bulb-neck1:before, .bulb-neck1:after`：定位*

```css
	position: absolute;
	left: 0;
	top: 0;
```

- 螺口下部分代码：`.bulb-neck1:after`：定位

```css
	top: auto;
	bottom: 0px;
```

## 6、灯头接触点[top]

- 灯头接触点上部分代码：`.bulb-neck2`:  梯形

```css
	width: 75px;
	height: 0;
	border-left: 25px solid transparent;
	border-right: 25px solid transparent;
	border-top: 25px solid #728b4b;
	border-radius: 10px;
```

- 灯头接触点上部分代码：`.bulb-neck2`:  定位

```css
	margin: -1px auto 0px;
	position: relative;
```

- 灯头接触点下部分代码：`.bulb-neck2:after`：外形

```css
	content: "";
	width: 0;
	height: 0;
	border-left: 36px solid transparent;
	border-right: 39px solid transparent;
	border-top: 20px solid #333;
```

- 灯头接触点下部分代码：`.bulb-neck2:after`：定位

```css
	margin: 0 auto;
	padding: 0;
	position: relative;
	top: 20px;
	left: 0;
```

## 7、整个灯泡

```css
.bulb-hover:hover .bulb-area1{
	background: #eaec68;
	box-shadow: 0 0 55px 25px rgba(255,255,0,0.4);
}
.bulb-hover:hover .bulb-area2,
.bulb-hover:hover .bulb-area2:before{
	border-top-color: #eaec68;
}
```

