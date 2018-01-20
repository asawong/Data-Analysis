作品[gist链接](http://bl.ocks.org/asawong/4b04cfc054f69da68855de8644f3060b)

### 总结

本可视化项目使用的数据，是根据"handedness"变量对棒球运动员数据集进行分组后计算的各组中位数。
每一行除"handedness"为分类变量外，其余几个变量包括"height"、"weight"、"avg"、"HR"和"Count"，
它们的值均为对应"handedness"各类别的中位数。

本可视化项目最终呈现出两幅作品，分别体现了惯用手不同的球员的赛场表现（avg和HR）及身体指标（height和weight）的差异。

#### Graph #1 (Performance based on handedness):
- Better performance are noted for Left handed players with higher median avg and HR

#### Graph #2 (Body Metrics based on handedness):
- Both handed players are found to have lower weight and height.

### 设计

本可视化作品改编自 Dimple.js library 中的示例 ["Vertical Bubble Lollipop"](http://dimplejs.org/examples_viewer.html?id=bubbles_vertical_lollipop)。

由于 x 轴为分类变量，所以使用了双 y 轴，从而能够在一副图表中呈现出三个变量。

添加了数据点的提示框。

为每个系列值各添加一条平滑曲线，作为视觉引导。

每幅作品的上方各添加了一句总结陈述。

### 反馈

[Version1](http://bl.ocks.org/asawong/54b95818ca76b3c5a5cdc359d05b1d4e)的反馈如下：

**反馈1：** 没有任何故事。大量的点重合造成过度绘制。可能需要重新构思一下到底想要呈现什么。

**改进1：** 完全推翻了过去希望从散点图中发现趋势的思路，在借鉴了 Dimple.js library 中的
示例后，想到使用各类别的中位数来避免发生过度绘制。然后我发现除"handedness"以外的变量实际
上可以分为两类：一类是"avg"和"HR"，表示球员的赛场表现；第二类是"height"和"weight"，表示
球员的身体指标。所以想到以"handedness"这个类别变量为x轴，通过双y轴，分两个图表来分别描述
这两类变量的关系。


**反馈2：** x轴和y轴代表的变量名称编码似乎错误。

**改进2：** 修改了代码，正确显示变量名称。

**反馈3：** 颜色使用不太恰当。

**改进3：** 借鉴了 dimple.js library 示例中的颜色。

### 资源

http://dimplejs.org/examples_viewer.html?id=bubbles_vertical_lollipop
