## 目的和目标受众

本文档描述了 Apache 提交者和 PMC 成员应如何处理源文件许可和版权声明。
它并不适用于 ASF 以外的开发者在他们的工作中应用 Apache 许可证。[Apache 许可证](http://apache.org/licenses/LICENSE-2.0.html#apply)的[附录](http://apache.org/licenses/LICENSE-2.0.html#apply)描述了其他人如何将许可证应用于他们的工作。该页面没有描述与每个 Apache 产品发布时发布[的标准 LICENSE 文件中的内容的](http://apache.org/dev/apply-license.html#new)要求，也没有描述 [发布第三方组件](http://www.apache.org/legal/resolved.html)时[可接受的许可证](http://www.apache.org/legal/resolved.html)。

## 概述

Apache 产品是通过多个源文件中的许多代码组成，这些代码由不同的作者授权给 ASF，他们对自己的贡献拥有所有权。当 PMC 通过选择、协调和安排所有这些不同的贡献到一个产品中的过程时，这个集体作品也受到版权法的保护，并由AS F拥有——即使每一段代码仍然由贡献者拥有。Apache 产品还可能包括其他未直接提交给 ASF 的组件，但[以这种方式获得许可](http://www.apache.org/legal/resolved.html)，符合 ASF 的许可做法。

考虑到所有这些因素，本文档介绍了如何：- [标注贡献源的源头](http://www.apache.org/legal/src-headers.html#headers)， - [处理第三方作品的版权和许可](http://www.apache.org/legal/src-headers.html#3party)，以及 - [使用 NOTICE 文件收集版权声明和所需的归属](http://www.apache.org/legal/src-headers.html#notice)。

本文件还包括： - [常见问题解答](http://www.apache.org/legal/src-headers.html#faq)。

当[法律讨论](http://www.apache.org/foundation/mailinglists.html#foundation-legal)邮件列表中提出新的问题时，将对其进行更新。

## 该页面更新通知

该页面的更新将发送到[法律讨论](http://www.apache.org/foundation/mailinglists.html#foundation-legal)邮件列表。

## ASF 下开发的代码所适用的源文件头

0.本部分仅指版权所有者或所有者的代理人直接提交给ASF的作品。

1.如果提交的源文件中包含版权声明，则版权所有者（或所有者的代理人）必须：

​	a.删除此类声明，或

​	b.将它们移至与每个适用项目版本关联的 NOTICE 文件，或

​	c.提供书面的许可，让 ASF 可以删除或重新放置通知。

2.每个源文件都应包括以下许可证标题 -- -- 注意标题中不应有版权声明：  

     Licensed to the Apache Software Foundation (ASF) under one
     or more contributor license agreements.  See the NOTICE file
     distributed with this work for additional information
     regarding copyright ownership.  The ASF licenses this file
     to you under the Apache License, Version 2.0 (the
     "License"); you may not use this file except in compliance
     with the License.  You may obtain a copy of the License at
     
       http://www.apache.org/licenses/LICENSE-2.0
     
     Unless required by applicable law or agreed to in writing,
     software distributed under the License is distributed on an
     "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
     KIND, either express or implied.  See the License for the
     specific language governing permissions and limitations
     under the License.

## 第三方作品的处理办法

0.“第三方作品"指的是版权所有者或所有者的代理人没有直接提交给 ASF 的作品，这包括直接提交给 ASF 的作品的一部分，但提交者不是版权所有者或所有者的代理。

1.不要修改或删除第三方作品中的任何版权声明或许可。

2.请确保每个第三方作品都包含其相关的许可证，即使这需要将第三方下载网站的许可证副本添加到发行版中。

3.不要将标准的 Apache License 标头添加到第三方源文件的顶部。

4.为方便起见，通常应使用与其余第三方源文件相同的条款来许可对第三方源文件进行较小的修改/添加。

5.对第三方的重大修改/添加，应由 PMC 根据具体情况处理。

## 声明文件

0.每个 Apache 发行版都应该在顶部目录中包含一个 NOTICE 文件，以及标准的 LICENSE 文件。

1.每个 NOTICE 文件的顶部应该包括以下文本信息，并对其进行适当修改，以反映产品的当前和过去版本的产品名称和发布年份：

```
Apache [PRODUCT_NAME]
Copyright [XXXX-XXXX] The Apache Software Foundation

This product includes software developed at
The Apache Software Foundation (http://www.apache.org/).
```

2. NOTICE 文件的其余部分用于[所需的第三方通知](http://apache.org/legal/resolved.html#required-third-party-notices)。

     通知文件还可包括[从提交给 ASF 的源文件](http://www.apache.org/legal/src-headers.html#header-existingcopyright)移来的版权通知。

3.  另请参阅[对通知的修改](http://www.apache.org/dev/licensing-howto.html#mod-notice)。

## 常见问题解答

### 在哪里可以找到每个 ASF 发布中必须包含的 NOTICE 文件的示例？

请参阅[ httpd 项目 NOTICE 示例](http://www.apache.org/licenses/example-NOTICE.txt)或[ Boilerplate NOTICE 文件](http://www.apache.org/licenses/NOTICE-2.0.txt)

### 此政策是否适用于发行版中包含的文档文件？

是。

### 此政策是否也适用于我们网站上显示的内容？

不，我们的网站没有相关的 NOTICE 文件。作为替代，我们可能很快就会通过网页页脚的 "使用条款 "或 "法律信息 "链接来明确这些内容的条款。在这一点上，Apache 网站不需要采取任何措施。

### 如果我的项目在产品发布中包含其网站，该怎么办？

除了[少数例外](http://www.apache.org/legal/src-headers.html#faq-exceptions)，分发中包含的所有可供人阅读的 Apache 开发文件都必须包含[标题文本](http://www.apache.org/legal/src-headers.html#header-text)。文档，包括与发行版一起发布的网站文档，可能会在某种形式的元数据（如 HTML 注释）中包含标题文本，也可以在可见文档中包含标题或页脚。

### APACHE 发行版中哪些文件不需要许可证头信息？

在文字元素或结构上没有任何程度的创造性的文件，不受版权法的保护；因此，这样的文件不需要许可证头信息。如果对文件的创造性程度有疑问，请将许可证头信息添加到文件中。

其他文件没有许可证头信息也可能是合理的。三个示例是：

- 简短的信息文本文件，例如 README，INSTALL 文件。期望这些文件可以使它们明显了解与之相关的产品。
- 增加源头会导致测试失败的测试数据。
- 合并为较大文件的“片段”文件，其中较大文件将具有重复的许可标头。

PMC 应该根据自己的判断，优先选择使用完整的代码头，如果不确定，请联系legal-discuss@。

### 代码头的简短形式是否可用？

有时，文件出现以下情况并不建议使用 Apache 代码头。 例如图像，缩小的 JavaScript 或 PDF 文件中。 在这些情况下，可以使用以下较短的形式。

```
"Licensed to the Apache Software Foundation (ASF) under one or more contributor license agreements; and to You under the Apache License, Version 2.0. "
```

任何与文件相关的附加许可信息（即通常会在通知中出现的信息）应在使用简表时直接在文件中注明。

PMC 应该根据自己的判断，优先选择使用完整的代码头，如果不确定，请联系legal-discuss@。

### 此政策是否适用于 ASF 发行版中包含的第三方二进制/对象文件？

是的。即使发行版中没有源文件，LICENSE 文件和 NOTICE 文件仍然是每个 ASF 发行版中所需要的 -- -- 无论发行单元是：jar、.msi、.tar.gz、.zip、.exe 安装程序，还是任何其他用于发行的文件格式。例如，Windows .exe 文件不得用作分发单位，除非它们是安装程序，并在安装中包含 LICENSE 和 NOTICE 文件。

### 本政策是否适用于 ASF 发行版中包含的第三方底层/对象文件？

是的。请参阅政策的“[第三方作品](http://www.apache.org/legal/src-headers.html#3party)”部分，尤其是确保每个第三方作品都具有许可证的 [要求](http://www.apache.org/legal/src-headers.html#3party-addlicense)。

### 图像或其他媒体是否需要在 NOTICE 文件中添加版权行？ 

如果媒体是直接为 ASF 项目贡献的，则贡献者可以选择将其版权声明插入 NOTICE 文件，如[源文件所述](http://www.apache.org/legal/src-headers.html#header-existingcopyright)。如果媒体来自第三方（未直接贡献给项目），则任何明显与媒体相关的版权声明都应复制到 NOTICE 文件中。

### 为什么需要许可证头信息？

许可证头信息允许检查文件的人知道作品的条款，即使在没有分发其余内容的情况下进行分发也是如此。在没有许可通知的情况下，必须假定作者保留了所有权利，包括复制，修改和重新分发的权利。

### 此政策是否适用于 ASF 之外使用 APACHE 许可证的项目？

不可以。严格来说，这是一项 ASF 政策。使用 Apache 许可证的其他项目仍应参考 [许可证的附录，](http://www.apache.org/licenses/LICENSE-2.0.html#apply)以获取有关将标头应用于其源文件的指导。
