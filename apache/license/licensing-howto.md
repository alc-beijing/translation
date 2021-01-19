## 组装LICENSE和NOTICE文件

这是Apache提交者为其项目产品组装LICENSE和NOTICE文件的“操作方法”指南。

## 概述

LICENSE文件传达Apache产品分发中所有内容的许可。它始终包含Apache许可证的文本，有时还包含更多信息。

在Apache许可证版本2.0的4.4节中描述了NOTICE文件。这是ASF政策所要求的。

提供了LICENSE和NOTICE文件的完整要求。

## 指导原则

LICENSE和NOTICE文件必须准确表示它们所驻留的分发的内容。只有分发中实际包含的组件和资源才对该分发的NOTICE和LICENSE的内容有影响。

## 位置
LICENSE和NOTICE文件位于源代码树的顶层。ASF更喜欢文件使用裸名，但是PMC可以选择将它们命名为LICENSE.txt和NOTICE.txt。

## 分步说明
要针对具有复杂要求的产品从头开始组装LICENSE和NOTICE文件，请按照下列步骤操作：

将完整的Apache 2.0许可证文本复制到LICENSE文件中。
根据您的产品详细信息创建一个“NOTICE”文件，并遵守以下说明。示例NOTICE文件位于此页面的底部。
添加特定于您产品IP的所有强制性法律通知。
对于任何捆绑的依赖性，请考虑是否需要修改许可和/或通知。不要为非捆绑的依赖项修改LICENSE或NOTICE。

Bundling permissively-licensed dependencies
