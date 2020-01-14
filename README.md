# CSS Flex 布局系统
在线可编辑示例 [flex-layout playground](https://shixianqin.github.io/flex-layout/playground)



## 安装
npm
```
npm install @shixianqin/flex-layout -S
```
bower
```
bower install https://github.com/shixianqin/flex-layout.git
```


## 导入
Module (npm install)
```javascript
import '@shixianqin/flex-layout';
```
Link (bower install)
```html
<link rel="stylesheet" href="./bower_components/flex-layout/index.css">
```


## 用法


#### 容器
+ 定义一个弹性布局盒子  
```html
<div class="d-flex"></div>
```

+ 排列方向
```html
<!-- 默认，从左到右 -->
<div class="d-flex flex-row"></div>

<!-- 从右到左 -->
<div class="d-flex flex-row-reverse"></div>

<!-- 从上到下 -->
<div class="d-flex flex-column"></div>

<!-- 从下到上 -->
<div class="d-flex flex-column-reverse"></div>
```

+ 换行方式
```html
<!-- 默认，从上到下自动换行 -->
<div class="d-flex flex-wrap"></div>

<!-- 不自动换行 -->
<div class="d-flex flex-nowrap"></div>

<!-- 从下到上自动换行 -->
<div class="d-flex flex-wrap-reverse"></div>
```

+ 主轴对齐方式，对齐方式与主轴的方向有关  
下面假设主轴方向为从左到右
```html
<!-- 默认，左对齐 -->
<div class="d-flex justify-content-start"></div>

<!-- 水平居中对齐 -->
<div class="d-flex justify-content-center"></div>

<!-- 右对齐 -->
<div class="d-flex justify-content-end"></div>

<!-- 两端对齐，项目之间的间隔相等 -->
<div class="d-flex justify-content-between"></div>

<!-- 每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍 -->
<div class="d-flex justify-content-around"></div>
```

+ 交叉轴对齐方式。对齐方式与交叉轴的方向有关  
下面假设交叉轴方向为从上到下
```html
<!-- 顶部对齐 -->
<div class="d-flex align-items-start"></div>

<!-- 垂直居中对齐 -->
<div class="d-flex align-items-center"></div>

<!-- 底部对齐 -->
<div class="d-flex align-items-end"></div>

<!-- 第一行文字的基线对齐 -->
<div class="d-flex align-items-baseline"></div>

<!-- 默认，如果项目未设置高度或设为 auto，项目高度将占满整个容器的高度 -->
<div class="d-flex align-items-stretch"></div>
```

+ 多轴对齐方式。如果项目只有一根轴线，该类不起作用。对齐方式与轴线的方向有关  
下面假设交叉轴方向为从上到下
```html
<!-- 交叉轴顶部对齐 -->
<div class="d-flex align-content-start"></div>

<!-- 交叉轴中点对齐（垂直居中） -->
<div class="d-flex align-content-center"></div>

<!-- 交叉轴底部对齐 -->
<div class="d-flex align-content-end"></div>

<!-- 交叉轴两端对齐，轴线之间的间隔平均分布 -->
<div class="d-flex align-content-between"></div>

<!-- 轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍 -->
<div class="d-flex align-content-around"></div>

<!-- 轴线占满整个交叉轴 -->
<div class="d-flex align-content-stretch"></div>
```


+ 组合对齐方式。通过将 justify-content, align-items, align-content 这三种对齐方式任意组合在一起，可实现各种各样的对齐效果  
例如：
```html
<!-- 水平垂直居中对齐 -->
<div class="d-flex justify-content-center align-items-center"></div>

<!-- 四周扩散效果 -->
<div class="d-flex justify-content-between align-content-between"></div>


<!-- 尝试更多组合... -->
```


#### 项目
+ 缩放比例
```html
<!-- 容器 -->
<div class="d-flex">

  <!-- 自动缩放比例，空间不足时缩小，空间足够时放大 -->
  <div class=“flex-fill”></div>

  <!-- 不自动放大比例 -->
  <div class=“flex-grow-0></div>

  <!-- 自动放大比例 -->
  <div class=“flex-grow-1></div>

  <!-- 不自动缩小比例 -->
  <div class=“flex-shrink-0></div>

  <!-- 自动缩小比例 -->
  <div class=“flex-shrink-1></div>

</div>
```

+ 对齐方式。覆盖父级的 align-items 属性
```html
<!-- 容器 -->
<div class="d-flex">

  <!-- 默认，继承父元素的 align-items 属性 -->
  <div class="d-flex align-self-auto"></div>

  <!-- 顶部对齐 -->
  <div class="d-flex align-self-start"></div>

  <!-- 垂直居中对齐 -->
  <div class="d-flex align-self-center"></div>

  <!-- 底部对齐 -->
  <div class="d-flex align-self-end"></div>

  <!-- 第一行文字的基线对齐 -->
  <div class="d-flex align-self-baseline"></div>

  <!-- 高度将占满整个容器的高度 -->
  <div class="d-flex align-self-stretch"></div>

</div>
```

#### 文本
+ 对齐方式
```html
<!-- 左对齐 -->
<div class="align-left"></div>

<!-- 水平居中对齐 -->
<div class="align-center"></div>

<!-- 右对齐 -->
<div class="align-right"></div>

<!-- 两端对齐 -->
<div class="align-justify"></div>

<!-- 垂直文本对齐方式，只对 table 有效 -->
<!-- 顶部对齐 -->
<div class="align-top"></div>

<!-- 垂直居中对齐 -->
<div class="align-middle"></div>

<!-- 底部对齐 -->
<div class="align-bottom"></div>
```

+ 文本裁剪
```html
<!-- 显示省略符号来代表被修剪的文本 -->
<div class="text-ellipsis"></div>

<!-- 显示多行 -->
<div class="text-ellipsis-2"></div>
<div class="text-ellipsis-3"></div>
<div class="text-ellipsis-4"></div>
<div class="text-ellipsis-5"></div>
<div class="text-ellipsis-6"></div>
```


#### display
+ 元素显示方式
```html
<div hidden></div>
<div class="d-none"></div>
<div class="d-inline"></div>
<div class="d-inline-block"></div>
<div class="d-block"></div>
<div class="d-table"></div>
<div class="d-table-row"></div>
<div class="d-table-cell"></div>
<div class="d-flex"></div>
<div class="d-inline-flex"></div>
```

## 查看阮一峰的 Flex 教程
[Flex 布局教程：语法篇](http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html)


## 参考 Bootstrap
部分 css 代码借鉴自 [bootstrap](https://github.com/twbs/bootstrap)  

