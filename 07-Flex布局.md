# Flex 布局 #

## 父级的排列方式 ##

###  设置父级属性     ` display: flex ` ###

### X 轴方向排列：` flex-direction: row `  默认 ###

```css
 /* 父级 */
  .box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* x轴方向排列    默认 */
    flex-direction: row;

  /* 子级 */
  .box span {
    width: 30px;
    height: 30px;
    border: 1px solid red;
    background-color: #fff;
    text-align: center;
  }
```

### Y轴方向排列：` flex-direction: column ` ###

```css
 /* 父级 */
  .box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* y轴方向排列 */
    flex-direction: column;

  /* 子级 */
  .box span {
    width: 30px;
    height: 30px;
    border: 1px solid red;
    background-color: #fff;
    text-align: center;
  }
```

### X轴方向的从右往左排列 ###

```css
flex-direction: row-reverse;
```

### Y轴方向的从下往上排列 ###

```css
flex-direction: column-reverse;
```

## 设置子级的排列方式 ##

### 父级设置    ` Justify-content `  属性 ###

```css
/* 父级 */
  .box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /*设置子级的排列方式*/
    justify-content: 属性值;
  }
```

### X轴方向   从左往右排列 ----默认 ###

```css
 .box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 从左往右排列 */
    justify-content: flex-start;
  }
```

### X轴方向   从右往左排列 ###

```css
 .box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 从右往左排列 */
    justify-content: flex-end;
  }
```

### X轴方向   居中排列 ###

```css
 .box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /*  居中排列 */
    justify-content: center;
  }
```

### X轴方向   平均分   ` 子元素外边距相等` ###

```css
.box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 平均分-外边距相等 */
    justify-content: space-around;

  }
```

### X轴方向   平均分     ` 子元素间隔相等 ` ###

```css
.box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 平均分-间隔相等 */
    justify-content: space-evenly;
  }
```



### X轴方向   两边贴边，中间平均分  ###

```css
.box {
    width: 300px;
    height: 90px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 两边贴边，中间平均分 */
    justify-content: space-between;
  }
```

### 如果想设置Y轴排列方式，需要将排列方式设置为    ` flex-direction: column ` ###

```css
  .box {
    width: 300px;
    height: 300px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 设置为纵向 Y 排列 */
    flex-direction: column;
    /* 纵向居中 */
    justify-content: center;
  }
```

## 设置子级换行 ##

**` 默认不换行 `**

` flex-wrap: nowrap `

```css
  /* 父级 */
  .box {
    width: 300px;
    height: 300px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 居中 */
    justify-content: center;
    /* 设置自动换行 */
    flex-wrap: wrap;
  }
```

## 设置子元素水平垂直居中 ##

```css
 /* 父级 */
  .box {
    width: 300px;
    height: 300px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 水平居中 */
    justify-content: center;
    /*侧轴居中*/
    align-items: center;
  }
```

## 设置侧轴的对齐方式 ##

### 单行-------多行没效果 ###

**` align-items `：属性值**    

**` align-items: flex-end `**    从下到上

**` align-items: flex-end`**   居中

**` align-items: stretch `**   拉伸   ---不设置元素高度

```css
  /* 父级 */
  .box {
    width: 300px;
    height: 300px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 居中 */
    justify-content: center;
    align-items: stretch;
  }
  /* 子级 */
  .box span {
      /*拉伸不设置高度*/
    width: 30px;
  /* height: 30px; */
    border: 1px solid red;
    background-color: #fff;
    text-align: center;
  }
```

### 多行  ----单行没效果 ### 

**` align-content: 属性值 `**

**``````**

```css
 /* 父级 */
  .box {
    width: 300px;
    height: 300px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    flex-wrap: wrap;
    /* 横向平均分 */
    justify-content: space-evenly;
    align-content: center;
  }
```

## align-items 和 align-content 的区别 ##

- ` align-items `适用于单行情况下，只有上对齐、下对齐、居中和拉伸
- ` align-content `适用于多行情况下（单行情况下无效），可以设置上对齐、下对齐、居中、拉伸以及平均分剩余空间
- 单行就写 ` align-items ` 多行就写 ` align-content ` 

### 复合属性 ###

**` flex-flow `**  相当于同时设置了 **` flex-direction `**  和 **` flex-warp `**属性

```css
.box {
    width: 300px;
    height: 300px;
    background-color: rgb(164, 173, 83);
    /* 设置flex布局 */
    display: flex;
    /* 纵向布局，换行 */
    flex-flow: column wrap;
  }
```

