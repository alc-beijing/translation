###
原文地址：https://infra.apache.org/licensing-howto.html

## 译文版

## 撰写LICENSE和NOTICE文件

这是Apache提交者为其项目产品撰写LICENSE和NOTICE文件的“操作方法”指南。

## 概述

LICENSE文件传达Apache产品分发包中所有内容的许可。它始终包含Apache许可证的文本，有时还包含更多信息。

在Apache许可证版本2.0的[4.4节](https://www.apache.org/licenses/LICENSE-2.0.html#redistribution)中描述了NOTICE文件。这是[ASF政策](https://www.apache.org/legal/src-headers.html#notice)所要求的。

它提供了LICENSE和NOTICE文件的[完整要求](https://www.apache.org/legal/)。

## 指导原则

LICENSE和NOTICE文件必须**准确表示**分发包中包含的内容。只有分发包中实际包含的组件和资源才对该分发的NOTICE和LICENSE的内容有影响。

## 位置
LICENSE和NOTICE文件位于源代码树的顶层。ASF倾向于文件使用裸名，但是PMC可以选择将它们命名为LICENSE.txt和NOTICE.txt。

## 分步说明
要针对具有复杂要求的产品从头开始撰写LICENSE和NOTICE文件，请按照下列步骤操作：

- 将完整的[Apache 2.0许可证](https://www.apache.org/licenses/LICENSE-2.0.txt)文本复制到LICENSE文件中。
- 根据您的产品详细信息创建一个“NOTICE”文件，并遵守以下说明。[示例NOTICE文件](https://infra.apache.org/licensing-howto.html#example-notice)位于此页面的底部。
    * 添加专属于您产品IP的所有[强制性](https://infra.apache.org/licensing-howto.html#mod-notice)法律通知。
    * 对于任何捆绑的依赖性，请考虑是否需要修改许可和/或通知。**不要**为非捆绑的依赖项修改LICENSE或NOTICE。
