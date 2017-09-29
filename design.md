交互设计规范
==========================

此为前端开发团队遵循和约定的**交互设计规范**，意在实现浪潮项目交互设计的一致性。



[TOC]
## 1 组件

### 1.1 布局

### 1.2 导航

导航菜单

面包屑

步骤

分页器

导航菜单根据级别设置样式标准。比如三级四级样式标准

### 1.3 表单

#### 1.3.1 对齐

##### 1.3.1.1 文案对齐

##### [建议] 标题和正文左对齐，使用一个视觉起点。

![image](https://github.com/jingqiu2180/styleguide/blob/master/images/1.png?raw=true)

##### [建议] 标题和正文使用了两个视觉起点，不推荐该种对齐方式，除非刻意强调两者区别

![image](https://github.com/jingqiu2180/styleguide/blob/master/images/2.png?raw=true)

##### 1.3.1.1 表单对齐
标题左对齐，居中对齐，有对齐
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/3.png?raw=true)
##### 1.3.1.1 数字对齐
为了快速对比数值大小，建议所有数值取相同有效位数，并且右对齐。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/4.png?raw=true)

错误示范
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/5.png?raw=true)

### 1.4 列表

1. 气泡显示：单个item内容过多使用省略号，同时加入tooltip气泡文字提示。

![image](https://github.com/jingqiu2180/styleguide/blob/master/images/6.png?raw=true)

2. 列表嵌入： 需要查看单行更多内容时，使用列表嵌入。用户可以不用打开新页面或者打开弹框，只要通过点击，就可以直接在上下文中查看该列表项的详情信息。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/7.png?raw=true)
3. 弹出层显示：用户通过点击，在弹出框中查看该列表项的详情信息，但是当前列表项的上下文关系会被打断。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/8.png?raw=true)
4. 双面板选择器：用户通过点击，在列表的一侧（一般为右侧）查看该列表项大量的详情信息。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/9.png?raw=true)
5. 对等网格：以网格或者矩阵的方式排列内容元素，其中每个元素都有相仿的视觉重量。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/10.png?raw=true)
6. 缩略图网格：以二维的形式来展现图片/Icon，具有强烈的视觉效果，可以吸引用户注意![image](https://github.com/jingqiu2180/styleguide/blob/master/images/11.png?raw=true)
7. 显示分类或者层级的列表![image](https://github.com/jingqiu2180/styleguide/blob/master/images/12.png?raw=true)
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/13.png?raw=true)

### 1.5 表格

#### 1.5.1 搜索区

select列表搜索change响应；

input框，通过点击查询进行关联搜索

#### 1.5.2 操作区

##### [建议] 列表中单行数据的操作事件放入列表区最后一列添加操作列，更加方便操作。

#### 1.5.3 表格区

1. 1.按钮组 2.搜索条件 3.排序 4.筛选 5.状态点 6.单行操作 7.分页器／无限加载![image](https://github.com/jingqiu2180/styleguide/blob/master/images/14.png?raw=true)
2. 更多操作：依次分别为：完整内容、暂时不可用、没有该权限。该项暂时不可用时，直接灰化该操作；用户没有该权限时，直接隐藏该操作。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/15.png?raw=true)
3. 跳转至详情页 常见要求：把 ID、名称等唯一性的表格项处理成文字链，点击后跳转至详情或增加查看按钮或查看列。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/16.png?raw=true)
4. 模块编辑：适用在易读性高于易编辑性时；适用在有一定数量的项需要编辑时。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/18.png?raw=true)

##### [建议] 启动和禁用要尽可能相似（对称性交互）；保证启用和禁用切换时，页面不在水平方向不错位。
5. 直接编辑：用户输入后，系统需要及时保存数据。适用在易编辑性高于易读性时。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/19.png?raw=true)
6. 悬浮编辑：悬浮层会遮挡部分页面，适用在上下文对编辑任务不那么重要时。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/20.png?raw=true)
7. 列宽配置：一般是根据栅格来排版，通过设定每一列的宽度比列，来保证一定尺寸之上。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/21.png?raw=true)

##### [建议] 表头不换行；
##### [建议] 固定字节长度的列尽量不换行（eg：创建时间、操作等）。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/22.png?raw=true)
8. 对齐方式
 
##### [建议] 数值右对齐（带小数则按小数点对齐），其余左对齐。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/23.png?raw=true)
### 1.6 复杂表格

1. 多列数据：可以固定表头／表尾，可以横向滚动
2. 带图表的表格：通过图表来强化信息的传递，适用在表达数据变化趋势。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/24.png?raw=true)
### 1.7 高级搜索

### 1.8 侧滑模板
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/25.png?raw=true)

## 2 设计原则

### 2.1 过渡原则

在界面中，适当的加入一些过渡效果，能让界面保持生动，同时也能增强用户和界面的沟通。
- 提供页面跳转的过渡动画
- 提供组件动态显示的过渡动画

### 2.2 即时响应原则

『过渡原则』的有用体现在它能够在交互期间为用户提供视觉反馈；『即时反应』的重要性体现在交互之后立即给出反馈。
- 进度指示：表格加载显示进度条，提交进度显示条， ztree加载数据进度显示条


### 2.3 重复原则

新的页面尽量使用通用的ui组件搭建，重复复用ui组件

### 2.4 足不出户原则

能在这个页面解决的问题，就不要去其它页面解决，因为任何页面刷新和跳转都会引起变化盲视（Change Blindness），导致用户心流（Flow）被打断。频繁的页面刷新和跳转，就像在看戏时，演员说完一行台词就安排一次谢幕一样。

#### 2.4.1 二次覆盖层： 删除这种谨慎操作统一『二次确认』

二次确认包含强确认和弱确认，强确认要求必须输入yes，弱确认要求用户点击即可。

#### 2.4.2	输入覆盖层：在覆盖层上，让用户直接进行少量字段的输入
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/25.jpg?raw=true)
## 3 色彩

设计中对色彩的运用不仅应考虑品牌的识别性，还需达到信息传递、操作指引、交互反馈，或是强化和凸显某一个元素的目的。基于操作系统更注重高效、清晰等特点。
##### [建议] 界面用色建议不超过三种（数据图表和图形类插画除外）。

品牌色的应用
中性色的应用
	灰色作为中性色。这类色彩主要体现在导航框架、背景底色、描边、或次级操作等等。
功能色的应用
	提供几种功能色的标准：消息通知，反馈提醒，表单校验，默认色，提示，成功，警告，严重警告，失败等
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/26.png?raw=true)

## 4 图标

采用webfont来减少请求数和体积；
图标尺寸的标准： 如y = 8+n*8

## 5 字体

字体类型

字体大小

字体行高

	行高公式 字体行高绝对值为『字号 x 1.5倍』。例如：12 号字体的行高为 18px，14 号字体的行高为 21px。

## 6 文案

在界面中，我们需要通过对话的方式与用户产生共鸣。精准、清晰的语言会更容易让用户理解，合适的语气更容易让用户建立信任感。因此在界面设计时，文案也应当被重视。 在使用和书写文案时有以下几点需要注意：
- 从用户角度出发
- 表述一致
- 重要的信息放在显著位置
- 专业、精准、完整
- 精简、友好、正面

### 语言

- 明确表述立足点
- 精简语句
- 使用用户熟悉的语言
- 表述一致
- 重要的信息放在显著位置
- 完整、直接得阐述信息
- 用词精准完整

### 语气

- 拉近彼此的距离
- 友好、尊重用户
- 表述不应过于极端

### 大小写和标点符号

- 英文名词大小写规范
- 统计数据使用阿拉伯数字
- 省略不必要的标点
- 谨慎使用感叹号
- 基本标点规范

## 7 数据录入

数据录入是获取对象信息的重要交互方式，用户会频繁的增加、修改或删除信息。多种多样的文本录入和选择录入方式帮助用户更加清晰和高效的完成这项体验。

### 7.1 文本录入

##### [建议] 文本框（Input）： 输入较少的字符总数，使用单行的输入形式

##### [建议] 文本域（Textarea）：录入长篇幅的单一的文本使用多行的文本区域

    为提升数据录入效率，通常可以在输入框内增加暗提示以帮助提醒用户

    当说明文案较长时，你可以使用一个『信息』图标或者提示工具。

    对于那些短的输入提醒（短于一句），你可以将其放置在输入框的下方。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/27.png?raw=true)
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/28.png?raw=true)
### 7.2 选择录入
让用户在一个预定的范围中进行选择。

#### 7.2.1 单选
单选按钮允许用户从多个选项中选择一个选项。Radio 所有选项默认可见，方便用户在比较中选择，因此选项不宜过多。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/29.png?raw=true)
#### 7.2.2 复选
复选框用于在一组可选项中进行多项选择时。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/30.png?raw=true)

    1. 复选框（Checkbox）一般用于状态标记，需要和提交操作配合；
    2. 单个复选框可以表示两种状态之间的切换。
#### 7.2.3 开关
用于切换单个选项的状态。『开关』的内联标签应该显示清楚，例如：禁用/启用，不允许/允许等。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/31.png?raw=true)
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/32.png?raw=true)
错误示范
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/33.png?raw=true)
#### 7.2.4 滑块
滑块选择可以在连续或间断的区间内，通过滑动锚点来选择一个合适的数值。这种交互特性使得它在设置诸如音量，亮度，色彩饱和度等需要反映强度等级的选项时是一种极好的选择。![image](https://github.com/jingqiu2180/styleguide/blob/master/images/34.png?raw=true)
在不要求精准数值的场景下用户使用『连续滑块』可得到更灵活便捷的操作；在用户需要精确数值时，可与『数字输入框』搭配使用。
![image](https://github.com/jingqiu2180/styleguide/blob/master/images/35.png?raw=true)

## 8 数据展示
合适的数据展示方式可以帮助用户快速地定位和浏览数据，以及更高效得协同工作。在设计时有以下几点需要注意：
- 依据信息的重要等级、操作频率和关联程度来编排展示的顺序。
- 注意极端情况下的引导。如数据信息过长，内容为空的初始化状态等

## 9 反馈

为了帮助用户了解应用当前要做什么，也给用户的下一步行为做参考，以及了解操作后所产生的结果 ，当用户和系统需要交互时，使用不同的模式来反馈信息或结果。当设计者使用反馈或者自定义一些反馈时，请注意：
- 为用户在各个阶段提供必要、积极、即时的反馈；
- 避免过度反馈，以免给用户带来不必要的打扰，能够及时看到效果的、简单的操作，可以省略反馈提示。

1.	提示信息
> 	警告
	通知提醒
徽标数（Badge）
帮助－气泡卡片（popover） 文字提示（ToolTip）

2.	过程反馈
> 	加载状态进度反馈	录入反馈－form表单校验	气泡确认框（Popconfirm）
3.	结果反馈

> 顶部全局提示反馈（Message）
对话框反馈

## 10 参考
