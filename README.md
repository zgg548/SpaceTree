## 基本要求

### 用户兴趣度

1、DOI

​	1.1、DOI的计算方式

​		DOI = -1 * （该node到root的距离 + 该node到focus的距离）。[1]

​	1.2、DOI排序

​		对DOI由大到小进行排序（如果DOI相同则按照depth从小到大排序），然后遍历每一个结点的DOI，判断其是否可以展开。

​	1.3、关于是否可以展开的判断

​		使用了d3的树布局算法，判断当前的树的布局是否在给定的区域内能放的下。分为两部分：

​		(1) 判断树的宽度是否超过区域的宽度。

​		(2) 判断每个node的children x坐标之间的距离是否大于某个阈值k。

2、树布局算算法

​	d3的树布局算法。

3、点击展开

​	支持点击展开，并且会点亮从root到focus的路径上的节点。

### 节点动态展示DOI数值

每个node的text为"name(doi)"，支持动态显示。

## 加分项

实现了动态编辑树结构，用拖拽的方式即可。

## 其他

可以实现缩放（保留了该功能）。

## 致谢

谢谢长建学长的两个提示。

## 引用

[1]  G. W. Furnas, "The FISHEYE view: a new look at structured files," in Readings in Information Visualization: Using Vi- sion to Think, S. K. Card, J. D. Mackinlay, and B. Shnei- derman, Eds. San Francisco: Morgan Kaufmann Publishers, Inc., 1981, pp. 312-330. 