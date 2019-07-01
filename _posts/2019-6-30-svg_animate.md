---
title: 多种皮皮svg汹涌来袭，准备好接招——animate元素
date: 2019-06-23
categories:
     - svg制作
tags:
  - svg
---

* 随着网络技术的发展，动画中占主流的已不再是SMIL动画，而是CSS动画和Web动画。
* 我们可以通过添加SVG动画元素，比如<animate>到SVG元素内部来实现动画。
* 上篇文章我们看到了小球简单的运动，这一次来看看他还能做些什么吧。

---

### animate

* 用来执行 CSS 属性集的自定义动画。
    该方法通过CSS样式将元素从一个状态改变为另一个状态。CSS属性值是逐渐改变的，这样就可以创建动画效果。

* 下面我们还是用一个方块来当例子。为了实现动画效果，我们添加了一个<animate>元素到<circle>元素的内部。
一开始当然还是要来认识一下**animate**较中为重要的属性

> * attributeName:需要动画的属性名称
> * from： 属性的初始值
> * to：终止
> * dur：动画的时间

* 接下来拿一段代码来进行演示：
```
<svg xmlns="http://www.w3.org/2000/svg" width="300px" height="100px">
    <circle cx="0" cy="50" r="15" fill="blue" stroke="black" stroke-width="1">
        <animate attributeName="cx" from="0" to="100" dur="0.5s" repeatCount="indefinite" />
    </circle>
</svg>
```

* 下面是他的动画效果:
<svg xmlns="http://www.w3.org/2000/svg" width="300px" height="100px">
    <circle cx="0" cy="50" r="15" fill="blue" stroke="black" stroke-width="1">
        <animate attributeName="cx" from="0" to="100" dur="0.5s" repeatCount="indefinite" />
    </circle>
</svg>

---

### animateTransform

* animateTransform元素可以执行变换属性的动画。旋转属性就像：rotation(theta, x, y)，theta是一个角度，x和y是绝对坐标。
* 下面来一个旋转的例子吧：
```
<svg xmlns="http://www.w3.org/2000/svg" width="300px" height="200px">
    <rect x="30" y="80" width="20" height="34" fill="pink" stroke="black" stroke-width="1" transform="rotation">
        <animateTransform attributeType="XML" attributeName="transform" begin="0s" dur="2s" type="rotate" from="20 60 60" to="360 100 60" repeatCount="indefinite" />
    </rect>
</svg>
```

<svg xmlns="http://www.w3.org/2000/svg" width="300px" height="200px">
    <rect x="30" y="80" width="20" height="34" fill="pink" stroke="black" stroke-width="1" transform="rotation">
        <animateTransform attributeType="XML" attributeName="transform" begin="0s" dur="2s" type="rotate" from="20 60 60" to="360 100 60" repeatCount="indefinite" />
    </rect>
</svg>

### animateMotion

* animateMotion中有几个例子，这里就给大家看两种： **Linear motion**和**Curved motion**

#### Linear motion

* 在这篇文章里的第一个动画中，小球从左到右重复着这个动画，却不会在碰到右侧边界后原路返回，有点机械。
* 但其实不难做到，只需要添加**Linear motion**元素 ，就像下面这样：

```
<svg xmlns="http://www.w3.org/2000/svg" width="300px" height="100px">
    <rect x="0" y="0" width="300" height="100" fill="yellow" stroke-width="1" stroke="red" />
    <circle cx="0" cy="50" r="15" fill="blue" stroke="black" stroke-width="1">
        <animateMotion path="M 0 0 H 300 Z" dur="3s" repeatCount="indefinite" />
    </circle>
</svg>
```

<svg xmlns="http://www.w3.org/2000/svg" width="300px" height="100px">
    <circle cx="0" cy="50" r="15" fill="blue" stroke="black" stroke-width="1">
        <animateMotion path="M 0 0 H 300 Z" dur="1s" repeatCount="indefinite" />
    </circle>
</svg>

#### Curved motion

* 这个元素能使图形沿着曲线和路径方向运动。
> * 就像这样：
<svg width="300px" height="100px">
    <rect x="0" y="0" width="20" height="20" fill="yellow" stroke="black" stroke-width="1">
        <animateMotion path="M 250,80 H 50 Q 30,80 30,50 Q 30,20 50,20 H 250 Q 280,20,280,50 Q 280,80,250,80Z" dur="1s" repeatCount="indefinite" rotate="auto">
    </rect>
</svg>

* 小小的animate元素，却能完成如此多的svg动画效果，这也太棒了吧！
* 如果想要是实现更多的动画效果还是需要我们自己多多查阅资料，多多练习，熟练掌握，才能给我们的网页增添色彩。
