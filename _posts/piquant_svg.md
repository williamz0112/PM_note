---
title: 调皮的svg
categories:
     - svg制作
tags:
     - svg
---

上一篇文章带大家看了一些安静的svg图标，这一次，带大家看看会动的，比较皮的svg图像

### 实例：
> <svg width="800px"  height="500px"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"  class="lds-ball" style="background: yellow;"><circle cx="20" ng-attr-cy="{{config.cy}}" ng-attr-r="{{config.radius}}" ng-attr-fill="{{config.color}}" cy="50" r="20" fill="blue"><animate attributeName="cy" calcMode="spline" values="23;77;23" keyTimes="0;0.5;1" dur="5" keySplines="0.45 0 0.9 0.55;0 0.45 0.55 0.9" begin="0s" repeatCount="indefinite"></animate></circle></svg>

* 什么？这球太慢？一点也不皮？
* 别急嘛！这是可以改的啦

* 在修改之前，让我们来了解每一个元素的含义吧：
> * width和height分别指的是背景的宽度和高度，定义了这个svg图形的大小 
> * viewBox的四个参数分别代表：最小X轴数值；最小y轴数值；宽度；高度。且它是个正方形。
> * 中间的background则可以指定其颜色
> * dur则可以定义圆的移动速度  

> * **cs**：是用于标记图形的中心的横坐标值在什么位置
> * **cy**：是用于标记图形的中心的纵坐标值在什么位置
> * **r**：是指这个图形的半径
> * **stroke-width**：指的是图形的外边框的粗细大小
> * **stroke**：是注明外边框的颜色
> * **fill**：是注明填充图形内部的颜色



---

知道了这些，我们就可以着手改改这个图了！让他皮起来
<svg width="800px"  height="500px"  xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"  class="lds-ball" style="background: yellow;"><circle cx="20" ng-attr-cy="{{config.cy}}" ng-attr-r="{{config.radius}}" ng-attr-fill="{{config.color}}" cy="50" r="20" fill="blue"><animate attributeName="cy" calcMode="spline" values="23;77;23" keyTimes="0;0.5;1" dur="0.3" keySplines="0.45 0 0.9 0.55;0 0.45 0.55 0.9" begin="0s" repeatCount="indefinite"></animate></circle></svg>
 
 * 怎么样应该挺有趣的吧？我们可以在制作网页时多多利用，增加趣味性，吸引用户。