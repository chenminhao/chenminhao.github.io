---
title: css相关总结
categories:
- 前端
tags:
- 命令
---
CSS书写规范、顺序： http://www.admin10000.com/document/2979.html  
class命名规范：http://www.jb51.net/css/22091.html  
多屏复杂动画CSS技巧三则： http://www.cocoachina.com/webapp/20150316/11334.html  
无缝滚动： http://code.ciaoca.com/jquery/kxbdmarquee/   
纯CSS绘制三角形：http://www.jb51.net/article/42513.htm  

## background-size

>根据页面设计情况选择相应的参数，方法就是设计背景size参数
background-size：cover ，适用于上半部分背景图片，下半部分纯色
将背景图像等比缩放到完全覆盖容器，背景图像有可能超出容器。
background-size：contain 适用于一屏幕，缺点屏幕宽度高度不一致，会有缝隙
将背景图像等比缩放到宽度或高度与容器的宽度或高度相等，背景图像始终被包含在容器内。
background-size：100%  100%；
最简单粗暴的方法，缺点会给背景拉伸变形  
完美的背景图全屏css代码：http://huilang.me/perfect-full-page-background-image/  
背景：http://www.yangqq.com/jstt/css3/2013-08-02/541.html  

## box-shadow

>水平阴影为正值时，生成右边阴影，反之为负值时，生成左边阴影；垂直阴影为正值时，生成底部阴影，反之为负值时生成顶部阴 影
box-shadow属性中的阴影扩展半径（spread-radius）会是一个很关键的属性，要实现单边阴影效果，必须配上这个属性（除单边实影之外）。《设为负值是双倍收缩（为模糊距离的一半即可）》
单边阴影：box-shadow: 2px 0 5px -3px orange;
四周阴影：box-shadow:0 0 5px 3px orange;
水平阴影，垂直阴影，模糊距离，阴影尺寸，阴影颜色，内阴影(坐标相反)

## appearance
>允许您使元素看上去像标准的用户界面元素：有可能是单选框，多项框失效（bootstrap）  
appearance:radio;-moz-appearance:radio;-webkit-appearance:radio;

## -webkit-tap-highlight-color

>这个属性只用于iOS (iPhone和iPad)。当你点击一个链接或者通过Javascript定义的可点击元素的时候，它就会出现一个半透明的灰色背景。要重设这个表现，你可以设置-webkit-tap-highlight-color为任何颜色。(可以设置透明)

## hover 效果
```css
-webkit-box-shadow: 1px 4px 8px 0 rgba(25,119,173,0.4);
box-shadow: 1px 4px 8px 0 rgba(25,119,173,0.4);
-webkit-box-shadow: 1px 4px 11px 0 rgba(25,119,173,0.4);
box-shadow: 1px 4px 11px 0 rgba(25,119,173,0.4);
```
## text-indent
>属性规定文本块中首行文本的缩进 （允许使用负值。如果使用负值，那么首行会被缩进到左边）

## text-decoration
```css
text-decoration:none; //a标签下划线去除
```
## a标签href用法
```javaScript
 href="tel:139xxxxxxxx" // 一键拨打号码  
 href="sms:139xxxxxxx" //一键发送短信  
 href="wtai://wp/ap;1860;中国移动" //存储号码  
```
## 文字省略
``` css
/*单行文字超出文字省略*/   
overflow: hidden;
text-overflow:ellipsis;
white-space: nowrap; 

/*多行文字超出文字省略*/
display: -webkit-box;
-webkit-box-orient: vertical;
-webkit-line-clamp: 3;
overflow: hidden;
```
## 修改输入框placeholder
``` css
input::-webkit-input-placeholder,textarea::-webkit-input-placeholder{color:#fff;}
input:-moz-placeholder,textarea:-moz-placeholder{color:#fff;}
input::-moz-placeholder,textarea::-moz-placeholder{color:#fff;}
input:-ms-input-placeholder,textarea:-ms-input-placeholder{color:#fff;}
```
    
## 自定义radio按钮样式
``` css
input[type=radio]{position:relative;margin-right:4px;width:15px;height:15px;vertical-align:3px;}
input[type=radio]::after,input[type=radio]::before{position:absolute;display:block;border-radius:50%;content:'';transition:.3s all esae;}
input[type=radio]::before{top:0;left:0;width:23px;height:23px;border:1px solid #ddd;}
input[type=radio]::after{top:6px;left:6px;width:11px;height:11px;background-color:#fff;}
input[type=radio]:checked::after{background-color:#2aacfa;}
```