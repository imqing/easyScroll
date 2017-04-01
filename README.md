# easyScroll
简易滚动条，可以添加class和滚动到最下方，

# usage

 easyScroll($elem, settings);

# settings
  
# @param: className;
滚动条的样式

# @param: goToBottom;  
是否滚动到最下方


# 原理
主要使用当前容器，设为定位元素，绝对定位或者相对定位，基于原始的定位属性。
然后使当前元素overflow: hidden; 最后通过追加一个元素使容器中的子元素marginTop改变实现。
在计算高度的时候，是通过比对当前容器的高度和他的第一个子元素的高度来实现，所有对html结构有限制；

# html结构
```
<div class="con">
      <div class="child">这里放内容</div>
</div>

```
最后会生成一个和child同级的滚动条元素。


# 最终生成的html结构

```
<div class="con">
      <div class="child">这里放内容</div>
      <div class="easy-scroll" title="这是滚动条"></div>
</div>
```
