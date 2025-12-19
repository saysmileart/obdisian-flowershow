---
title: "如何在Excel中将一堆文本URL转换为可点击的超链接？"
source: "https://zh-cn.extendoffice.com/documents/excel/4321-excel-activate-hyperlinks.html"
author:
  - "[[xiaoyang]]"
published: 2016-12-09
created: 2025-11-11
description: "使用简单易懂的方法（如公式、VBA或Kutools）在Excel中将文本URL转换为可点击的超链接。快速高效的解决方案！"
tags:
  - "clippings"
---
[跳至主要内容](https://zh-cn.extendoffice.com/documents/excel/#tm-main)

[Kutools for Office — 一套工具，五种功能。 事半功倍。](https://zh-cn.extendoffice.com/product/kutools-for-office.html)

Author Xiaoyang Last modified

如果你有一系列纯文本格式的URL地址，如何将这些文本URL激活为如下截图所示的可点击超链接呢？

![convert text URLs to active hyperlinks](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-1.png)

**[使用公式将一堆文本URL转换为可点击的超链接](https://zh-cn.extendoffice.com/documents/excel/#a1)**

**[使用Kutools for Excel将一堆文本URL转换为可点击的超链接](https://zh-cn.extendoffice.com/documents/excel/#a2)**

**[使用VBA代码将一堆文本URL转换为可点击的超链接](https://zh-cn.extendoffice.com/documents/excel/#a3)**

---

#### 使用公式将一堆文本URL转换为可点击的超链接

逐个双击单元格以激活超链接会浪费大量时间。这里我可以为你介绍一些公式，请按照以下步骤操作：

在你想要输出结果的空白单元格中输入此公式： **\=HYPERLINK(A2, A2)** ，然后向下拖动填充柄以将此公式应用到其他需要的单元格中，所有文本URL都将被转换为可点击的超链接，见截图：

![use a formula to convert text URLs to active hyperlinks](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-2.png)

---

#### 使用Kutools for Excel将一堆文本URL转换为可点击的超链接

这里有一个方便的工具—— **Kutools for Excel** ，通过其“ **转换超链接** ”功能，你可以快速 **将一堆文本URL转换为可点击的超链接** ，并 **[从超链接文本字符串中提取真实的超链接地址](https://zh-cn.extendoffice.com/documents/excel/1177-excel-extract-hyperlink-from-cell.html)** 。

**Kutools for Excel** 提供了超过 300 种高级功能，简化复杂任务，提升创造力与效率。 **通过集成 AI 能力** ，Kutools 能够精准自动执行任务，让数据管理变得轻松简单。 **[Kutools for Excel 的详细信息...](https://zh-cn.extendoffice.com/product/kutools-for-excel.html)****[免费试用...](https://zh-cn.extendoffice.com/download/kutools-for-excel.html)**

安装 **Kutools for Excel** 后，请按以下步骤操作：

**1**. 选择包含要激活的文本URL的单元格。

**2.** 然后点击 **Kutools** > **链接** > **转换超链接** ，见截图：

![click Convert Hyperlinks feature of kutools](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-05.png)

**3**. 在“ **转换超链接** ”对话框中，在“ **转换类型** ”部分下选择“ **单元格内容转超链接地址** ”选项，如果你想将实际地址放入原始区域，请勾选“ **转换来源区域** ”，见截图：

![select Cell contents replace hyperlinks addresses option in the dialog box](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-6.png)

**4**. 然后点击“ **确定** ”按钮，文本URL将立即被激活，见截图：

[![the text URLs have been activated](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-4.png)](https://zh-cn.extendoffice.com/download/kutools-for-excel.html "点击免费下载")

**注意** ：如果你想将结果放到另一个单元格而不是原始单元格，请取消勾选“ **转换来源区域** ”，并从“结果区域”中选择一个你需要输出结果的单元格，如下图所示：

![put the result to another cell instead of the original cell](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-7.png)

**[立即点击下载Kutools for Excel并免费试用！](https://zh-cn.extendoffice.com/download/kutools-for-excel.html)**

---

#### 使用VBA代码将一堆文本URL转换为可点击的超链接

以下VBA代码也可以帮助你解决此任务，请按以下步骤操作：

**1**. 按住 **ALT + F11** 键打开 **Microsoft Visual Basic for Applications** 窗口。

**2**. 点击 **插入** > **模块** ，并将以下代码粘贴到模块窗口中。

**VBA代码：将一堆文本URL转换为可点击的超链接：**

```
Sub activateHyperlinks()
'Updateby Extendoffice
Dim Rng As Range
Dim WorkRng As Range
On Error Resume Next
xTitleId = "KutoolsforExcel"
Set WorkRng = Application.Selection
Set WorkRng = Application.InputBox("Range", xTitleId, WorkRng.Address, Type:=8)
For Each Rng In WorkRng
    Application.ActiveSheet.Hyperlinks.Add Rng, Rng.Value
Next
End Sub
```

**3**. 然后按 **F5** 键运行此代码，会弹出一个提示框，提醒你选择要转换为可点击超链接的单元格，见截图：

![ vba code to select the cells to convert to clickable hyperlinks](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-3.png)

**4**. 然后点击“ **确定** ”按钮，纯文本URL已被转换为可点击的超链接，见截图：

![the plain text URLs have been converted to active hyperlinks](https://cdn.extendoffice.com/images/stories/doc-excel/activate-hyperlinks/doc-activate-hyperlinks-4.png)

### 最佳Office办公效率工具

| 🤖 | [**Kutools AI 助手**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-excel-ai-assistant.html) ：以 [智能执行](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-excel-ai-assistant.html#ex1) 为基础，彻底革新数据分析 **\|** [代码生成](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-excel-ai-assistant.html#ex4) **\|** [自定义公式创建](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-excel-ai-assistant.html#ex2) **\|** [数据分析与图表生成](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-excel-ai-assistant.html#ex5) **\|** [调用Kutools函数](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-excel-ai-assistant.html#ex6) …… |
| --- | --- | --- | --- | --- | --- |
|  | 热门功能：查找、选中项的背景色或标记重复项 \| 删除空行 \| 合并列或单元格且不丢失数据 \| 四舍五入…… |
|  | **高级LOOKUP** ： [多条件VLookup](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-vlookup-multiple-criteria.html) **\|** [多值VLookup](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-one-to-many-lookup.html) **\|** [多表查找](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-vlookup-from-multiple-sheets.html) **\|** [模糊查找](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-fuzzy-lookup.html) …… |
|  | **高级下拉列表** ： [快速创建下拉列表](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-quick-drop-down-list.html) **\|** [依赖下拉列表](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-create-multiple-level-drop-down-list.html) **\|** [多选下拉列表](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-drop-down-list-multiple-selections.html) …… |
|  | **列管理器** ： [添加指定数量的列](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-add-columns.html) **\|** [移动列](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-list.html#a4) **\|** [切换隐藏列的可见状态](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-show-hidden-columns.html) **\|** [比较区域与列](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-compare-ranges,-rows-and-columns.html) …… |
|  | **特色功能** ： [网格聚焦](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-reading-view.html) **\|** [设计视图](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#design_protect) **\|** [增强编辑栏](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-display-whole-contents-of-cell.html) **\|** [工作簿及工作表管理器](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-list.html#a1) **\|** [资源库](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-auto-text.html) （自动文本） **\|** [日期提取](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-date-picker.html) **\|** [合并数据](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#combine_worksheets) **\|** [加密/解密单元格](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-encrypt-decrypt-cell-values.html) **\|** [按名单发送电子邮件](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-create-mailing-list-and-send-email.html#a2) **\|** [超级筛选](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-filter-data-multiple-criteria.html) **\|** [特殊筛选](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#special_filter) （筛选粗体/倾斜/删除线等）…… |
|  | **15大工具集** ： [12项](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#text) [**文本**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#text) [工具](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#text) （ [添加文本](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-add-same-text-to-multiple-cells.html) 、 [删除特定字符](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-remove-specific-characters-from-cells.html) 等） **\|** [50+种](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#charts) [**图表**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#charts) [类型](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#charts) （ [甘特图](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-create-gantt-chart.html) 等） **\|** [40+实用](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#Formula_helper) [**公式**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#Formula_helper) （ [基于生日计算年龄](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-calculate-age-by-birthday.html) 等） **\|** [19项](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#insert_tools) [**插入**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#insert_tools) [工具](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#insert_tools) （ [插入二维码](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-generate-qr-code.html) 、 [从路径插入图片](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-insert-display-image-from-url-path.html) 等） **\|** [12项](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#conversion_tools) [**转换**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#conversion_tools) [工具](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#conversion_tools) （ [小写金额转大写](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-convert-currency-to-text.html) 、 [汇率转换](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-convert-currency.html) 等） **\|** [7项](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#merge_split) [**合并与分割**](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#merge_split) [工具](https://zh-cn.extendoffice.com/product/kutools-for-excel/kutools-for-excel-all-features-list.html#merge_split) （ [高级合并行](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-combine-duplicate-rows.html) 、 [分割单元格](https://zh-cn.extendoffice.com/product/kutools-for-excel/excel-split-cell-by-delimiter.html) 等） **\|** …… |

Kutools支持多种语言——可选择英语、西班牙语、德语、法语、中文等40多种语言！

**通过Kutools for Excel提升您的Excel技能，体验前所未有的高效办公。** **Kutools for Excel提供300多项高级功能，助您提升效率并节省时间。 [点击此处获取您最需要的功能……](https://zh-cn.extendoffice.com/download/kutools-for-excel.html)**

 <video height="158" width="1197"><source src="//cdn.extendoffice.com/images/stories/kte-module/kte-tab-20240318-150.webm" type="video/webm"> <source src="//cdn.extendoffice.com/images/stories/kte-module/kte-tab-20240318-150.mp4" type="video/mp4"></video>

[Kutools for Excel更多详情……](https://zh-cn.extendoffice.com/product/kutools-for-excel.html) [免费下载……](https://zh-cn.extendoffice.com/download/kutools-for-excel.html)

---

#### Office Tab为Office带来多标签界面，让您的工作更加轻松

- 支持在Word、Excel、PowerPoint中进行多标签编辑与阅读 。
- 在同一个窗口的新标签页中打开和创建多个文档，而不是分多个窗口。
- 可提升50%的工作效率，每天为您减少数百次鼠标点击！
 [<video width="1140" height="157"><source src="//cdn.extendoffice.com/images/stories/kte-module/officetab-bottom-02.webm" type="video/webm"> <source src="//cdn.extendoffice.com/images/stories/kte-module/officetab-bottom-02.mp4" type="video/mp4"></video>](https://zh-cn.extendoffice.com/download/office-tab.html)

[Office Tab更多详情……](https://zh-cn.extendoffice.com/product/office-tab.html) [免费下载……](https://zh-cn.extendoffice.com/download/office-tab.html)

---

#### 所有Kutools加载项，一键安装

**Kutools for Office** 套件包含Excel、Word、Outlook和PowerPoint的插件，以及Office Tab Pro，非常适合跨Office应用团队使用。

![Excel](https://cdn.extendoffice.com/images/stories/Kutools-for-office/excel.png) ![Word](https://cdn.extendoffice.com/images/stories/Kutools-for-office/word.png) ![Outlook](https://cdn.extendoffice.com/images/stories/Kutools-for-office/outlook.png) ![Tabs](https://cdn.extendoffice.com/images/stories/Kutools-for-office/tab.png) ![PowerPoint](https://cdn.extendoffice.com/images/stories/Kutools-for-office/powerpoint.png)
- **全能套装** ——Excel、Word、Outlook和PowerPoint插件+Office Tab Pro
- **单一安装包、单一授权** ——数分钟即可完成设置（支持MSI）
- **协同更高效** ——提升Office应用间的整体工作效率
- **30天全功能试用** ——无需注册，无需信用卡
- **超高性价比** ——比单独购买更实惠

[Kutools for Office更多详情……](https://zh-cn.extendoffice.com/product/kutools-for-office.html) [免费下载……](https://zh-cn.extendoffice.com/download/kutools-for-office.html)