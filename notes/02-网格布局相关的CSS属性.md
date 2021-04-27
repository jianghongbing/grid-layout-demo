# 与网格布局相关的CSS属性

## 定义在网格容器上的CSS属性
* display: 通过设置display的值为grid或者inline-grid来让一个元素成为网格容器
* grid-template-columns: 显示的定义列, 包括列的数量, 每一列的名称以及宽度. 可以通过repeat函数同时定义多个列. eg: `grid-template-columns: repeat(3, 1fr)`, 表示定义3列, 每列的宽度为1fr.
* grid-template-rows: 显示的定义行, 包括行的数量, 每一行的名称以及宽度. 
* grid-tempate-areas: 命名网格区域
* grid-template: 
* column-gap: 设置列与列之间的间距
* row-gap: 设置行与行之间的间距
* gap: row-gap和column-gap的简写

## 定义在网格项上的CSS属性

* grid-column-start: 网格项在列方向上开始的列线号码. grid-column-start的可能的值如下:
  * 一个数字: eg: `grid-column-start: 1;`, 表示列线开始号码为1, 数字可以为负数, 此时计算为倒数列线号码. 
  * 字符串: eg: `grid-column-start: column-start`, 表示对应命名的列的号码. 
* grid-column-end: 网格项在列方向结束的列线号码, 取值可以参考grid-column-start. 
* grid-column: grid-column-start和grid-column-end的简写. grid-column有下面集中常见的写法: 
  * `grid-column: 1/2`: 表示该网格项放置在标号为1和2的列中间的区域. 
  * `grid-column: 1/span 2`: 表示该网格项从第一列开始放置, 占据2列. 
* grid-row-start: 网格项在行方向开始的行线号码
* grid-row-end: 网格项在行方向结束的行线号码
* grid-row: grid-row-start和grid-row-end的简写, 常见写法可以参考grid-column. 

