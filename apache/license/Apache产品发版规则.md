本页记录软件版本的 ASF 政策。本文档的内容针对 ASF 发版经理和 [PMC][uPMC] 成员。还提供了供 [最终用户][uend_user] 和 [分发镜像操作员][umirror] 使用的信息。


其他文档总结了该政策的 [发行过程][urelease] 和 [设计目标][udesign]。   
# 目录
  - [目录](# 目录)
- [**发行政策**](#发行政策)
  - [**“发行版” 的定义**](#发行版-的定义)
  - [**发行版的批准**](#发行版的批准)
  - [**出版物**](#出版物)
  - [**构件**](#构件)
    - [**源码包**](#源码包)
    - [**发行签名**](#发行签名)
    - [**已编译的包**](#已编译的包)
  - [**许可证（Licensing）**](#许可证licensing)
  - [**许可证文档**](#许可证文档)
    - [**LICENSE 文件**](#license-文件)
    - [**NOTICE 文件**](#notice-文件)
    - [**许可证头**](#许可证头)
  - [**发行版的分发**](#发行版的分发)
    - [**发行存档**](#发行存档)
  - [**发行政策管理**](#发行政策管理)
  - [**TODO 事项**](#todo-事项)
- [**发行常见问题**](#发行常见问题)
  - [**为什么我们需要一项基金会级别的政策？**](#为什么我们需要一项基金会级别的政策)
  - [**什么是发行版？**](#什么是发行版)
  - [**Apache 软件分发的类型有什么不同？**](#apache-软件分发的类型有什么不同)
  - [**发行管理问题**](#发行管理问题)
    - [**发行版到哪里去了？**](#发行版到哪里去了)
    - [**每个 ASF 发行版必须包含哪些内容？**](#每个-asf-发行版必须包含哪些内容)
    - [**ASF 对批准发行版有哪些要求？**](#asf-对批准发行版有哪些要求)
    - [**应该怎样发行发行版？**](#应该怎样发行发行版)
    - [**有最佳实践指南吗？**](#有最佳实践指南吗)
    - [**发行版必须在提交者控制的硬件上被构建吗？**](#发行版必须在提交者控制的硬件上被构建吗)
  - [**发行版分发和镜像问题**](#发行版分发和镜像问题)
    - [**我们在哪里可以托管测试包（每晚构建和候选发行版）？**](#我们在哪里可以托管测试包每晚构建和候选发行版)
    - [**我们可以在哪里托管公共（GA）发行版？**](#我们可以在哪里托管公共ga发行版)
    - [**发行版如何归档？**](#发行版如何归档)
    - [**旧的发行版应何时归档？**](#旧的发行版应何时归档)
    - [**如何上传发行版？**](#如何上传发行版)
    - [**在哪里可以发行候选版本？**](#在哪里可以发行候选版本)
    - [**分发某个发行版之前，我需要与基础设施进行沟通吗？**](#分发某个发行版之前我需要与基础设施进行沟通吗)
    - [**目录和发行版如何一一对应？**](#目录和发行版如何一一对应)
    - [**如何将旧版本移至存档库？**](#如何将旧版本移至存档库)
    - [**如何发行 Maven 构件？**](#如何发行-maven-构件)
  - [**发行版许可证问题**](#发行版许可证问题)
    - [**哪些文件必须包含 ASF 许可证文档？**](#哪些文件必须包含-asf-许可证文档)
    - [**所有源文件中都需要许可证的完整副本吗？**](#所有源文件中都需要许可证的完整副本吗)
    - [**属性声明的正确位置在哪里？**](#属性声明的正确位置在哪里)
    - [**NOTICE 文件适合什么内容？**](#notice-文件适合什么内容)
    - [**纯 ASF 代码是否需要属性文件？**](#纯-asf-代码是否需要属性文件)
    - [**如果文件包含多个许可证下的代码，它是否应该包含多个许可证文件？**](#如果文件包含多个许可证下的代码它是否应该包含多个许可证文件)
    - [**除了源代码包之外，分发其他文件还有什么要求？**](#除了源代码包之外分发其他文件还有什么要求)
  - [有关发行统计信息的问题](#有关发行统计信息的问题)
    - [有什么方法可以测量某软件包被下载了多少次吗？](#有什么方法可以测量某软件包被下载了多少次吗)


***(下面这一部分词打算加到术语表里，有的还没想好怎么加)，如果审查后没问题的话，我会单独再提一次术语表的 pull request***
nightly builds 是不是也不翻译更好  
artifact: 文件 (直译是 “文件” 的意思，特指组成项目的源文件，因为它们不具有独立的功能)
XYZ 直接翻译成软件包了 我觉得就是指代特定软件包 但不知道为啥不写清楚点  
nightly builds: 每夜构建版本
对 DISTRIBUTION 一词的翻译，可能是 “发行版” 或 “分发”，具体取决于语境。
对 release 一词一般直接译为 “发行版”。
assets 一词译为资产
tarball 一词译为原始文件
***end***
**问题**
They should not be mirrored; only blessed GA releases should be mirrored.
以及
prior to being, potentially, formally blessed as a GA release
上面两句中的‘blessed’如何理解，我译为 “获准”
**end**

## **发行政策**
### **“发行版” 的定义**
通常，“发行版” 是指由拥有者之外（的人）发行的任何东西。对于 Apache 项目，这意味着开发社区之外的任何发行版，都会定义为参与开发者或是出现在开发人员名单上个体的个人活动。

狭义地讲，Apache 的正式发行版是被 PMC 认可为 “基金会的行为”。

### **发行版的批准**
每个 PMC 在批准任何发行时都必须遵循 ASF 的要求。

一个发行版的通过至少需要三个赞成票，并且赞成票数多于反对票数。发行版可能不会被否决。PMC 成员的投票具有约束力。

在进行 + 1 约束力投票之前，**要求**个人将所有已签名的源代码包下载到自己的硬件上，验证它们是否符合 ASF 关于发行版的政策的所有要求：验证所有加密签名，按提供的方式进行编译，然后在自己的平台上测试结果。

发行投票至少应该开放 72 小时。

### **出版物**
项目**必须**发行官方发行版本，且**不得**发行未在开发社区发行的资料。

在开发软件和准备发行版时，开发社区将出于测试目的生产多种软件包。**项目必须将其他人引导到正式版本，而不是原始源代码仓库、每夜构建版本、快照、候选发行版本或任何其他类似软件包。**唯一应该了解此类开发人员资源的人是积极参与开发或遵循开发人员列表并因此了解未发行资料所处条件的个人。

### **构件**
#### **源码包**
每个 ASF 发行版**必须**包含一个或多个源代码包，只要用户能够访问适当的平台和工具，这些源代码包就足以让用户构建和测试版本。

#### **发行签名**
所有提供的软件包必须由发版经理使用分离的签名进行加密签名。对发行进行 + 1 投票的人们**可以**提供自己的加密签名，并在发行之前将其与分离的签名文件连接（由发版经理决定）。

#### **已编译的包**
ASF 生产开源软件。所有发行版都包含修改自身所需的源代码。

为了方便那些可能没有适当工具来构建源代码的编译版本的用户，**可以**将二进制 / 字节码包与官方 Apache 发行版一起分发。在所有这些情况下，二进制 / 字节码包**必须**与源版本具有相同的版本号，并且**必须**仅添加二进制 / 字节码文件，这些文件是该版本的源代码及其依赖项的编译结果。

### **许可证（Licensing）**
每个 ASF 发行版都必须遵守 ASF 许可政策。此要求极其重要，在创建任何完整版本之前都**应当**进行审核。特别地，根据 [Apache 许可政策][apache-licensing-policy]，每个 Apache 分发的文件都必仅包含适当许可的代码。

### **许可证文档**
每个软件包必须提供一个 LICENSE 文件和一个 NOTICE 文件，这些文件说明了该软件包的确切内容。 LICENSE 并且 NOTICE**不得**提供未与包内文件绑定的不必要信息，例如单独下载的依赖项。

对于源代码包，LICENSE 并且 NOTICE 必须位于发行版的根目录。对于其他软件包，它们必须位于特定分发格式中许可证的常规位置，例如 Java “jar” 文件的 META-INF 目录。

#### **LICENSE 文件**
该 LICENSE 文件必须包含 Apache License 2.0 的全文。

当软件包在多个许可证下捆绑代码时，LICENSE 文件必须包含所有这些许可证的详细信息。对于未经 Apache 许可的每个组件，必须将组件的详细信息附加到 LICENSE 文件中。组件许可证本身必须附加或存储在包中的其他位置，并带有从 LICENSE 文件指向它的指针，例如，如果许可证很长。

#### **NOTICE 文件**
NOTICE 文件必须符合 [Apache 许可政策][Apache-licensing-policy] 的要求。

另请参阅 Apache License 2.0 的 [4 (d) 小节][al20-4d]。

#### **许可证头**
如果源文件包含由版权所有者或所有者的代理人直接向 ASF 提交的代码，该源文件必须包含正确的 [ASF 许可证头][ASF-license-header]。

### **发行版的分发**
一旦发行被批准，所有文件必须上传到规范的 Apache 发行渠道中项目的子目录内，`downloads.apache.org`。

PMC 对项目分发目录负责，并且**必须**能够说明它的所有内容。目录中的所有发行文件**必须**由提交者（最好是 PMC 成员）签名。

在上传到规范的分发渠道之后，项目（或其他任何人）**可以**依照他们的许可证在其它渠道重新分发文件。

#### **发行存档**
所有正式发行版都必须在 archive.apache.org 上永久存档。

（上传到规范的分发渠道可满足此要求，因为存档会作为 “副作用” 自动进行。）

### **发行政策管理**
如果和任何建议或要求的政策指令有偏差，项目必须通知董事会。

更改发行政策必须得到法务部的批准。

### **TODO 事项**
正式制定其他官方政策，并从此政策中引用它们：

*ASF 许可政策（由法务部门策划，适用于已发行和未发行的代码）*

## **发行常见问题**

### **为什么我们需要一项基金会级别的政策？**

在像 Apache 这样的，实行志愿者责任有限制的传统开源开发方法学的组织中，有必要将 “开发中” 和 “适合多数人群消费” 的两种公共资源区分开来。明确区分的目的是告知我们为正式参与发行的参与者提供的法律保护政策 —— 这将在下一节中进行定义。“开发中” 的资产被看作为自识别的开发者开发项目而准备的的受控分发，这些开发者通过项目开发列表来注明。此政策文档旨在涵盖不受控制的分发（也称为发行版）。

如果我们不做这种区分，而是鼓励用户直接与源代码管理或每夜构建版本进行交互，那么组织将很难向 Apache 提交者和 PMC 成员提供法律保护。因为他们在进行软件修改时仅仅凭借自己的判断就批准将这些工件按原样分发给公众，而没有参考**授权商业决定**的帮助。Apache 的大部分 “官僚主义” 和项目治理结构都是为了促进该政策的目标，因此，此文档非常值得仔细研读。

偏离本政策可能会对法律保障的有效性产生不利影响，或影响 Apache 为保护高级成员和董事而支付的保险费用，因此在未经董事会事先明确批准的情况下，强烈建议不要这样做。但请注意，在组织上我们喜欢稳健、可审查的决策胜过高效的决策。因此，如果您正在考虑提出一个供董事会考虑的替代流程，请确保您的目标反映了这一点。

### **什么是发行版？**

根据定义，发行版是拥有该发行版的组织之外发行的任何内容。对于我们来说，这包括产品开发人员名单之外任何人的任何出版物。如果公众已经可以下载软件包，则该软件包已发行。每个 PMC 在批准任何发行时都必须遵守 ASF 的要求。而如何给发行包的标注标签则是次要问题，这将在下文讨论。

在开发软件和准备发行版的过程中，开发人员可以使用各种软件包进行测试。**不要在项目网站上包含任何可能鼓励非开发人员下载和使用的每夜构建版本、快照、候选发行版本或任何其他类似软件包的链接。**唯一应该了解此类软件包的人是关注开发人员列表（或搜索其存档）的人员，因为他们了解软件包上附加的条件。如果发现公众正在下载此类测试包，请删除它们。

在任何情况下，未经批准的构建都不适合做发行版。如果这样做不太方便，那就请更频繁的发行。适当的发行管理是 Apache 软件开发的关键。

Apache 软件基金会生产开源软件。所有发行版均以更改发行软件所需的原始资料的形式出现。在某些情况下，还会生成二进制 / 字节码包，便于那些可能没有适当工具来构建已编译产品的用户。在所有这些情况下，二进制 / 字节码软件包必须与源发行版具有相同的版本号，并且只能添加由该版本的源代码编译的二进制 / 字节码文件。

### **Apache 软件分发的类型有什么不同？**

-**测试软件包**不是 Apache 发行版。所有发行都需要经过适当程序和官方批准。测试包用于开发过程中，并且仅应在项目开发列表上进行讨论。

-**每夜构建版本**仅通过 Subversion/Git trunk/branch 构建，通常每天一次。这些软件包用于定期测试构建过程，并为自动测试人员提供用于回归测试的通用构建。它们不适合大众使用。

-**发行候选版**是已经申请批准为发行版但尚未得到项目批准的软件包。这些软件包供开发人员（和关注开发讨论的用户）测试，并就该发行版与先前发行版的质量的对比意见向项目报告。在发行批准之前，可能有许多候选发行。对开发测试不感兴趣的用户应等待，直到正式批准发行。

-**发行版(Releases)** 是已批准用于一般公众发行的程序包，通常伴随着不同程度的警告，包括已知的产品质量或潜在的改变。供非开发人员日常使用的发行版通常称为 “稳定版 (stable)” 或 “一般可用性（GA）” 发行版。对于另外一些发行版，它们可供项目外的测试和开发人员使用，但就功能或特性而言可能还不稳定，这些发行通常称为 “测试版 (beta)” 或 “不稳定版 (unstable)”。还有一些仅代表项目里程碑，并且仅面向在项目外部工作的前沿开发人员的发行版称为 “alpha” 版。

### **发行管理问题**
#### **发行版到哪里去了？**

直到发行版位于项目的分发目录（该目录是 `downloads.apache.org` 的子目录）中，才算是被 “发行” 了。除了发行目录外，使用 Maven 或相关构建工具的项目有时还会将其发行版放在 `repository.apache.org`，和一些方便使用的二进制文件放在一起。分发目录是必需的，而存储库系统是可选的便利措施。

#### **每个 ASF 发行版必须包含哪些内容？**
每个 ASF 版本**必须**包含一个源代码包，如果用户有权访问适当的平台和工具，则该源码包必须足以使用户构建和测试该版本。源代码包必须由 Release Manager 用分离的签名进行 [加密签名][cryptographically-sign]；并且源代码包及其签名必须先被测试，然后进行 + 1 进行投票来发行。对发行进行 + 1 投票的人们可以提供自己的加密签名，并在发行之前将其与分离的签名文件连接（由发版经理决定）。

注意：PMC 对其分发目录中的所有文件负责。分发目录是 `downloads.apache.org` 的子目录；放置目录中的所有构件必须由提交者（最好是 PMC 成员）签名。PMC 还必须确保源代码包足以构建与该发行版关联的任何二进制文件。

每个 ASF 版本都**必须**遵守 ASF 许可政策。此要求无比重要，并且任何完整发行版都应在创建之前被审核。特别地，分发的每个文件都必须仅包含 [适当][appropriately-][许可][licensed-] 的代码。可以在 [基金会网站][apache-index] 和 [发行许可常见问题][faq-relaese] 中找到更多信息。

#### **ASF 对批准发行版有哪些要求？**
投票决定是否准备好发行软件包，请使用 [少数服从多数][MajorityApproval]。即，至少三个 PMC 成员必须投肯定票，并且肯定票要多于否定票。发行可能不会被否决。在 PMC 成员进行 + 1 投票之前，他们必须下载签名的源代码包并按原样进行编译。之后在他们自己的平台上测试生成的可执行文件，并还要验证该包是否符合 ASF 发行政策的要求。

#### **应该怎样发行发行版？**
请确保您在上传新版本后至少等待 24 小时，然后再更新项目下载页面并发送公告电子邮件。这样一来，镜像服务器就有足够的时间同步。（对于时间紧迫的安全修复版本，下载页面脚本支持 [绕过][bypass-24h] 此要求。）

告知人们新版本的可用性很重要。公告必须包含指向源的相关下载页面的链接。至少，应该向所有适当的邮件列表发送电子邮件来宣布此消息。为此，许多顶级项目都有公告列表。还有一个适用于 [ASF 内][asf-wide] 的公告列表。

请注意，如果不使用 “apache.org” 邮件地址，则无法在 [ASF 内][asf-wide] 进行公告。另外，请确保已经放置了 3-5 行的项目简介。（因为大多数订阅了 announce.AT.apache.DOT.org 列表的用户通常不知道什么是 XX 项目）

建议将 SHA-1 OpenPGP 兼容的签名添加到公告邮件中。请确保您的公钥已经上传到知名度较高的 pgp 网站（例如 http://pgp.mit.edu/）。该密钥应该给发行版签名过，或是被给发行版签名过的密钥交叉签名过。

#### **有最佳实践指南吗？**
请参阅 [孵化器发布管理指南（草稿）][incubator-relaese-draft]。或者，请参阅任何已建立的 Apache 项目的 “如何发行” 开发人员文档。（该文章的作者对 [这个指南][best-practice] 比较熟悉，这来自他的项目。）

#### **发行版必须在提交者控制的硬件上被构建吗？**
严格来说，发行必须在提交者控制的硬件上进行 [验证][verify-build]。这意味着提交者在物理上拥有硬件、硬件控制权、以及完全的管理 / 超级用户访问权限。因为只有这样的硬件才有资格持有 PGP 私钥。并且应该在私钥所在的计算机上验证发行版是否可信。

实际上，当发行包含源代码控制标签的存档文件（例如 tarball 或 zip 文件）之外的任何内容时，验证该存档的唯一实用方法是在本地构建该存档。手动检查生成的文件（尤其是二进制文件）是不可行的。因此，基本上可以说，这个问题的答案是 “是”。

* 注意：此回答是指用于从源代码控制标签产生发行构建的过程。它不是指测试该文件的技术质量。*

### **发行版分发和镜像问题**

#### **我们在哪里可以托管测试包（每晚构建和候选发行版）？**

测试程序包仅供经同意的开发人员和感兴趣的社区成员使用，因此不应将其托管或链接到面向终端用户的页面。它们不应该被镜像；只有获准的 GA 版本应该被镜像。

项目应使用存储库的 [`dist` 仓库的 `dev` 目录][dist-dev] 或者 `repository.apache.org` 的暂存功能来托管候选发行版本，以供开发人员测试 / 投票（在将要潜在或正式获准发行 GA 版本之前）。

不是候选版本的每夜构建可以在 [ci.apache.org 项目区域](https://ci.apache.org/projects) 托管，只需提交 INFRA 票即可。

#### **我们可以在哪里托管公共（GA）发行版？**
目前必须通过 ASF 镜像系统来提供发行版。请将文件放在 `https://downloads.apache.org/` 下。（请参阅 [如何上载版本？][upload-release]）。

项目下载页面必须链接到镜像而非 Apache 主站。更多详细信息请参考 [创建下载页面的说明][create-download-page]。这些网站的软件文档必须包含指向源下载页面的链接。

项目网站（`http://{project}.apache.org`），VM（`http://{project}.zones.apache.org` 和 `http://{project}-vm.apache.org`）和源代码控制存储库（`svn.apache.org` 和 Git 存储库）不得用于分发发行版 —— 也就是说，不应从其中下载发行版。

#### **发行版如何归档？**

所有发行版本都必须归档在 [http://archive.apache.org/dist/](http://archive.apache.org/dist/) 上。

在发行首次出现在 [https://downloads.apache.org/](https://downloads.apache.org/) 大约一天后，自动化流程会将发行添加到存档中。一旦发行版被放在 [https://downloads.apache.org/](https://downloads.apache.org/) 后，发行版会被自动复制到 [http://archive.apache.org/dist/](http://archive.apache.org/dist/)。即使将其从 [https://downloads.apache.org/](https://downloads.apache.org/) 中删除，发行文件也会被永久保存。

如果您有（旧版？）从未存档的发行版，请要求基础设施将其复制到 `http://archive.apache.org/dist/`。

#### **旧的发行版应何时归档？**
`downloads.apache.org` 应该包含 * 正在开发的每个分支中的最新版本 *。当版本的分支不再开发时，应从项目的下载目录中删除该分支的发行版。

（如果项目使用 svnpubsub，则通过从中以下目录中删除文件来完成此操作 `https://dist.apache.org/repos/dist/release/<TLP name>/`。）

例如，如果 Apache Foo 1.2.x 是与 Foo 1.1.a 相同但更新一些的版本，则应在发行 1.2.x 时删除 1.1.a。请注意，所有版本都会自动存档，请参阅 [如何将旧版本移至存档][old-version-to-archives]。

如果 Apache Foo 1.2 是一个新的分支，并且 Foo 1.1.a 将继续并行开发，那么可以从 `/dist` 同时提供 1.1.a 和 1.2.x 的发行版。

#### **如何上传发行版？**
可以将发行版原始文件提交到 `https://dist.apache.org/repos/dist/release/` 存储库下相应的子目录中（即 TLP 名称）来完成上传。我们的同步过程将在 15 分钟内将文件推送到 [主镜像站点][master-mirror]。不过，仍然需要 24 小时等待镜像（因为 [镜像使用每天 1/N 的重同步][1/n-rsync] 来保持和 dist / 目录的同步）。

存储库目录 `https://dist.apache.org/repos/dist/release/<TLP name>/` 仅适用于**正式发行版**，即 PMC 已批准的存档（+ 签名，哈希）。因此，**默认情况下，只有 PMC 成员才能更新 dist/release 目录树。**

如果发版经理不是 PMC 成员，他们将需要请 PMC 成员来完成实际的发行版发布工作。

PMC 还可以投票让非 PMC 成员更新 dist/release 区域。要进行此设置，请在 [INFRA JIRA][INFRA-JIRA] 上打开一个引用 PMC 投票的工单。

#### **在哪里可以发行候选版本？**
还有一个开发区域在 `https://dist.apache.org/repos/dist/dev/<TLP name>/`，可用于开发目的的发行版本。例如，快照和候选版本可以存储在这里。需要注意的一个重要事项是，该目录不会通过 svnpubsub 发行到镜像中。它旨在充当正式发行前的准备发行目录。

项目上的所有提交者都可以写入该项目的 dist/dev 区域。

如果用于候选版本，则在成功投票后，可以将适当的文件从 dev/ 目录移动到 release/ 目录中以进行发行。

将邮件提交到 `dist/` 存储库将转到常规项目邮件列表。

#### **分发某个发行版之前，我需要与基础设施进行沟通吗？**
如前两个问题所述，大多数项目只能分发发行版。但是，可能会使镜像和下载资源紧张的发行版**必须**与基础结构协调。

发行超过 1GB 的文件需要提前了解基础架构。

来自其他 dist 政策的特定豁免（例如，可以 / 必须 / 禁止通过镜像分发的内容）也必须与基础架构进行协调。

#### **目录和发行版如何一一对应？**
| 类型	| 地址 |
|:-----:|:------:|
| 每晚构建 |	ci.apache.org/projects |
| 最新发行 |	downloads.apache.org |
| 旧版本	| archive.apache.org/dist |

#### **如何将旧版本移至存档库？**
`downloads.apache.org` 上的内容会自动存档。因此，存档中将已经存在一个正式发行版的副本。要将发行版移至存档，只需删除项目 dist 目录中的副本即可。记住要更新下载页面上的所有链接。

#### **如何发行 Maven 构件？**
请参阅 [Maven 发行指南][maven-publish]。

### **发行版许可证问题**
请阅读 [使用 Apache 许可证，2.0 版][use-apache-license-v2]，并查看 [Apache 许可证][Apache-License] 和 [Apache 法律信息][apache-legal] 页面以获取当前信息。

#### **哪些文件必须包含 ASF 许可证文档？**
每个源文件都必须包含适当的 ASF 许可证文档。

#### **所有源文件中都需要许可证的完整副本吗？**
简而言之，每个发行版仅需要一份许可证副本。完整的许可证文件应放在名为 LICENSE 的文件里，该文件应当位于发行版根目录下。对于由 ASF 开发的软件，每个源文件仅需包含 [范例声明][boilerplate]。

#### **属性声明的正确位置在哪里？**
新许可证允许包含此类属性声明（包括 Apache 属性声明）的 NOTICE 文件。阅读 [这里](http://apache.org/legal/src-headers.html#notice)。

现有源文件中包含的所有属性声明都应移入文件中。NOTICE 文件必须和 LICENSE 文件一同打包在发行版内。

确保在创建的任何新 NOTICE 文件中都包含标准的 ASF 属性通知。

#### **NOTICE 文件适合什么内容？**
阅读 [这里](http://apache.org/legal/src-headers.html#notice)。

只有产品许可证强制性要求的信息才需要放在这里。不适合放常规文档。

#### **纯 ASF 代码是否需要属性文件？**
是！NOTICE 文件必须包含标准的 ASF 属性，如下所示： 

    This product includes software developed at
    The Apache Software Foundation (http://www.apache.org/).  

注意：不幸的是，此文档在 2013-01-30（r1440650）之前的版本不正确，因为它们使用了短语：“developed by”(由 xx 开发) 而不是 “developed at”(在 xx 开发)。正式措辞在 2006 年 5 月 24 日的董事会会议记录第 6C 节中确定。

#### **如果文件包含多个许可证下的代码，它是否应该包含多个许可证文件？**
当文件包含多个许可证下的代码时，LICENSE 文件应包含所有这些许可证的详细信息。对于非 Apache 许可证的每个组件，应将组件的详细信息附加到 LICENSE 文件中。组件许可证本身可以被附加在文件后，或者存储在构建的其它地方，并在 LICENSE 文件中用指针指向它。例如，如果许可证文本太长。

[这里](https://svn.apache.org/repos/asf/httpd/httpd/trunk/LICENSE)
是一个附加许可证的示例。

#### **除了源代码包之外，分发其他文件还有什么要求？**
ASF 发行版通常包括源代码包及附加材料。附加材料可以包括有关该发行版的文档，但必须包含 LICENSE 和 NOTICE 文件。正如前文所述，如果要将这些文件放置在项目的分发目录中，则必须由提交者使用分离的签名进行签名。

同样，仅当这些构件包含 LICENSE 和 NOTICE 文件时，才可以分发它们。例如，Java 构件格式基于压缩的目录结构。那些希望分发 jar 的项目必须将 LICENSE 和 NOTICE 文件放置在 jar 的 META-INF 目录中。

本节中的所有内容都不能取代
[这里](https://www.apache.org/legal/release-policy.html#what)
和
[这里](https://www.apache.org/legal/release-policy.html#what-must-every-release-contain)
定义的要求：所有发行版都主要基于一个签名的源源代码包。

### 有关发行统计信息的问题

####  有什么方法可以测量某软件包被下载了多少次吗？

没有直接分发。文件是从镜像下载的。Apache 不需要镜像来收集有关下载的统计信息。

计算 [下载脚本][download-script] 的点击数 应该可以得出合理的估计。[Vadim Gritsenko][VG] 收集了各种类似的统计数据。

还有由 closer.cgi 记录的一些日志，存储在：

`https://www-eu.apache.org/dyn/stats/rocketmq.log https://www-us.apache.org/dyn/stats/rocketmq.log`

这些列显示：- 时间戳 - IP 地址的一部分 - 国家（估计）-URL

请注意，该日志仅记录对 CGI 脚本的访问。这样的访问可能不会导致下载，并且下载可能不会完成。

****

* 译者注：某些部分没有精确按字面翻译，因为英语和中文表达习惯并不相同，完全字字翻译会显得文章逻辑诡异、不通顺且令人费解。受译者水平所限，产生不恰当的翻译在所难免，还请批评指正。可以在 https://github.com/alc-beijing/translation/issues 提交改进意见，或发送电邮至 wwwwyccom at 163 . com*

[uPMC]:http://www.apache.org/foundation/governance/pmcs.html

[uend_user]:https://infra.apache.org/release-download-pages.html##best_practice

[umirror]:http://www.apache.org/info/how-to-mirror

[urelease]:http://www.apache.org/dev/release-publishing

[udesign]:http://www.apache.org/dev/mirrors

[apache-licensing-policy]:https://www.apache.org/legal/resolved

[Apache-licensing-policy]:http://apache.org/legal/src-headers.html#notice

[al20-4d]:https://www.apache.org/legal/licenses/LICENSE-2.0.html#redistribution

[ASF-license-header]:http://www.apache.org/legal/src-headers.html#headers

[cryptographically-sign]:https://www.apache.org/dev/release-signing.html

[appropriately-]:https://www.apache.org/legal/resolved#category-a

[licensed-]:https://www.apache.org/legal/resolved#category-x

[apache-index]:https://www.apache.org/

[faq-relaese]:https://www.apache.org/legal/release-policy.html#license

[MajorityApproval]:http://www.apache.org/foundation/glossary.html#MajorityApproval

[bypass-24h]:https://www.apache.org/legal/release-download-pages#less-than-24hr

[asf-wide]:http://www.apache.org/foundation/mailinglists.html#foundation-announce

[incubator-relaese-draft]:http://incubator.apache.org/guides/releasemanagement.html#best-practice

[best-practice]:http://subversion.apache.org/docs/community-guide/releasing#release-creating

[verify-build]:https://svn.apache.org/repos/private/committers/tools/releases/compare_dirs.pl

[dist-dev]:https://dist.apache.org/repos/dist/dev

[upload-release]:https://www.apache.org/legal/release-policy.html#upload-ci

[create-download-page]:https://www.apache.org/dev/release-download-pages

[old-version-to-archives]:https://www.apache.org/legal/release-policy.html#how-to-archive

[master-mirror]:https://downloads.apache.org/

[1/n-rsync]:https://www.apache.org/info/how-to-mirror

[INFRA-JIRA]:https://issues.apache.org/jira/browse/INFRA

[maven-publish]:http://www.apache.org/dev/publishing-maven-artifacts.html

[use-apache-license-v2]:https://www.apache.org/legal/apply-license

[Apache-License]:https://www.apache.org/licenses/

[apache-legal]:https://www.apache.org/legal/

[boilerplate]:http://www.apache.org/legal/src-headers.html#headers

[download-script]:https://www.apache.org/dev/release-download-pages.html#download-scripts

[VG]:http://home.apache.org/~vgritsenko/