# 与网格布局相关的CSS属性

## 定义在网格容器上的CSS属性
* display: 通过设置display的值为grid或者inline-grid来让一个元素成为网格容器
* grid-template-columns: 显示的定义列, 包括列的数量, 每一列的名称以及宽度. 可以通过repeat函数同时定义多个列. eg: `grid-template-columns: repeat(3, 1fr)`, 表示定义3列, 每列的宽度为1fr.
* grid-template-rows: 显示的定义行, 包括行的数量, 每一行的名称以及宽度. 
* grid-tempate-areas: 命名网格区域, 可以通过原点来占据某个单元格, 不放置其他元素. 
* grid-template: grid-template-column, grid-template-row和grid-template-areas的简写, 同时定义网格中行, 列和分区. 
* column-gap: 设置列与列之间的间距
* row-gap: 设置行与行之间的间距
* gap: row-gap和column-gap的简写
* grid-auto-columns: 定义隐式列的宽度. 当隐式的创建列的时候, 使用该值来作为列宽. 通常在只定义网格区域的情况会显示的定义列
* grid-auto-rows: 定义隐私行的高度. 当隐式的创建行的时候, 使用该值来作为行的高度. 常见的创建隐私行的情况有如下几种:
  * 定义了列, 没有定义行
  * 定义网格区域, 没有定义行
  * 显示定义的行, 不够放满网格项.
* grid-auto-flow: 如何排列网格元素. 取值如下:
  * row: 逐行排列元素. grid-auto-flow的默认值
  * column: 逐列排列元素. 
  * dense: 该关键字指定自动布局算法使用一种“稠密”堆积算法, 如果后面出现了稍小的元素, 则会试图去填充网格中前面留下的空白. 这样做会填上稍大元素留下的空白, 但同时也可能导致原来出现的次序被打乱. 如果省略它, 使用一种「稀疏」算法, 在网格中布局元素时, 布局算法只会「向前」移动, 永远不会倒回去填补空白. 这保证了所有自动布局元素「按照次序」出现, 即使可能会留下被后面元素填充的空白. 
* grid: grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns, grid-auto-flow, grid-column-gap, grid-row-gap的简写. 
* justify-items: 设置所有元素在容器中的主轴上的对齐方式
* align-items: 设置所有元素在容器中的侧轴上的对齐方式

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
* justify-self: 设置单个盒子在其布局容器主轴中的对其方式. 
* align-self: 设置单个盒子在其布局容器侧轴中的对其方式. 和flex布局的align-self类似