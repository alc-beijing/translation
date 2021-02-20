###
原文地址：https://infra.apache.org/licensing-howto.html

## 译文版

## 撰写 LICENSE 和 NOTICE 文件

这是 Apache 提交者为其项目产品撰写 LICENSE 和 NOTICE 文件的“操作方法”指南。

## 概述

LICENSE 文件传达 Apache 产品分发包中所有内容的许可。它始终包含 Apache 许可证的文本，有时还包含更多信息。

在 Apache 许可证版本2.0的[4.4节](https://www.apache.org/licenses/LICENSE-2.0.html#redistribution)中描述了 NOTICE 文件。这是[ ASF 政策](https://www.apache.org/legal/src-headers.html#notice)所要求的。

它提供了 LICENSE 和 NOTICE 文件的[完整要求](https://www.apache.org/legal/)。

## 指导原则

LICENSE 和 NOTICE 文件必须**准确表示**分发包中包含的内容。只有分发包中实际包含的组件和资源才对该分发的 NOTICE 和 LICENSE 的内容有影响。

## 位置

LICENSE 和 NOTICE 文件位于源代码树的顶层。ASF 倾向于文件使用裸名，但是 PMC 可以选择将它们命名为 LICENSE.txt 和 NOTICE.txt。

## 分步说明

要针对具有复杂要求的产品从头开始撰写 LICENSE 和 NOTICE 文件，请按照下列步骤操作：

- 将完整的[Apache 2.0许可证](https://www.apache.org/licenses/LICENSE-2.0.txt)文本复制到 LICENSE 文件中。
- 根据您的产品详细信息创建一个“NOTICE”文件，并遵守以下说明。[示例 NOTICE 文件](https://infra.apache.org/licensing-howto.html#example-notice)位于此页面的底部。
    * 添加专属于您产品 IP 的所有[强制性](https://infra.apache.org/licensing-howto.html#mod-notice)法律通知。
    * 对于任何[绑定](https://infra.apache.org/licensing-howto.html#bundled-vs-non-bundled)的依赖项，考虑是否需要修改 LICENSE 和 / 或 NOTICE。**不要**为非绑定的依赖项修改 LICENSE 或 NOTICE。

## 绑定许可的依赖关系

假设许可对依赖项中的所有文件都统一适用，那么根据以下许可之一发布的依赖项是很简单的:

- BSD (没有广告条款)
- MIT/X11

在 LICENSE 中，在发行版中添加一个指向依赖关系许可的指针，并简要说明其许可:

```$xslt
该产品绑定了 SuperWidget 1.2.3，可在“3-clause BSD”许可下使用。 相关详细信息，请参见 deps/superwidget/。
```

通常情况下，无需修改 NOTICE 即可提交绑定的依赖。

**注意**：它也可能包括你的产品的 LICENSE 文件中的第三方许可证的文本。最好为短期许可证保留。指定依赖项的版本很重要，因为许可证有时会随着产品版本的更改而更改。

ASF 法律事务委员会已[批准](https://www.apache.org/legal/resolved.html#category-a)使用其他许多“宽松”许可证。其中一些可能需要在 NOTICE 上添加一些内容 —— 如有疑问，[请寻求帮助](https://www.apache.org/legal/resolved.html#asking-questions)。

## 绑定 Apache 2.0许可的依赖项

假设绑定的依赖项本身在其他许可下不包含绑定的子组件，那么 ALv2 统一应用于所有文件，则无需修改 LICENSE。 但是，出于完整性考虑，列出产品及其版本是非常有用的，就像其他许可下列出的产品一样。

如果依赖项提供了 NOTICE 文件，则必须分析其内容，并将相关部分撰写到顶级 NOTICE 文件中。

## 绑定其他 ASF 产品

尽管必须考虑 ASF 版权和 NOTICE 的任何其他部分，但不必重复“此产品包括由 Apache 软件基金会开发的软件...”。

## 对 NOTICE 的修改

NOTICE 文件是为法律要求的通知的某些子集保留的，这些通知既不满足 LICENSE 文本的要求，也不满足嵌入在绑定依赖项中的许可证信息的存在。除了提供自己的 NOTICE 文件的 apache 许可依赖之外，很少有依赖需要添加 NOTICE。

在 NOTICE 中必须保留已从源文件中[重新定位](https://www.apache.org/legal/src-headers.html#headers)而不是删除的版权通知。但是，BSD 和 MIT 许可证中嵌入的版权通知之类的部分[不需要在 NOTICE 中重复](https://issues.apache.org/jira/browse/LEGAL-59)。您可以将这些通知留在其原始位置。

保持 NOTICE 尽可能简短和简单是很重要的，因为每次添加都会给下游消费者带来负担。

**不要**添加任何法律上没有要求的内容到 NOTICE 里。

## 绑定依赖与非绑定依赖

必须根据它们所在的特定发行版的内容来自定义 LICENSE 和 NOTICE 文件。不要把分发包中未包含的依赖项写进 LICENSE 和 NOTICE 里。 **只有绑定的才重要**。

例如：如果 Apache-FOO-1.0.tgz 和 Apache-FOO-1.1.tgz 之间的唯一区别是一个绑定了 SuperWidget 而另一个强制用户单独下载 SuperWidget，LICENSE 和 NOTICE 就需要修改以匹配不同的绑定项。

## 依赖关系的依赖关系

为了撰写 LICENSE 和 NOTICE，依赖关系的依赖关系（包括所谓的“传递性依赖关系”）与一阶依赖关系没有什么不同：**仅在它们部分被绑定在一起的情况下**，才需要修改 LICENSE 和 NOTICE 以符合它们。

## 二进制发行版

适用于规范的源代码分发的内容也适用于所有的再分配，包括二进制重新分配：

**所有重新分发都必须遵守内容的许可要求。**

撰写二进制发行版时，通常会引入并绑定未与源代码发行版绑定在一起的其他依赖项。必须在 LICENSE 和 NOTICE 中说明这些附加的依赖性。因此，二进制发行版的 LICENSE 和 NOTICE 文件可能与构建它的源代码发行版中的不同。

在任何情况下，原理都是一样的：LICENSE 和 NOTICE 必须**准确**表示它们所包含的分发内容。

## NOTICE文件示例

以下是 [Apache Royale](https://royale.apache.org/) 的 NOTICE 文件的内容：

```aidl
Apache Royale
Copyright 2020 The Apache Software Foundation

This product includes software developed at
The Apache Software Foundation (http://www.apache.org/).

The Initial Developer of some parts of the framework, which are copied from, derived from, or
inspired by Adobe Flex (via Apache Flex), is Adobe Systems Incorporated (http://www.adobe.com/).
Copyright 2003 - 2012 Adobe Systems Incorporated. All Rights Reserved.

The Initial Developer of the examples/mxroyale/tourdeflexmodules, 
is Adobe Systems Incorporated (http://www.adobe.com/).
Copyright 2009 - 2013 Adobe Systems Incorporated. All Rights Reserved.

The ping sound effect (ping.mp3) in 
examples/mxroyale/tourdeflexmodules/src/mx/effects/assets
was created by CameronMusic. (http://www.freesound.org/people/cameronmusic/sounds/138420/)
```