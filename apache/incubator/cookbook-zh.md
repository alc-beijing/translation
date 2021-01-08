### ASF孵化器指南
原文地址: https://incubator.apache.org/cookbook/
## 译文版
# Apache孵化器指南

该指南与[孵化器主页](http://incubator.apache.org/)为大家提供了在ASF孵化项目所需的必要信息。该指南汇集了所有孵化器的相关问题，给出了孵化器目标和过程的概述，并提供了更多详细信息的链接。

该指南内容按照项目从被接收孵化到毕业成为顶级项目（Top-Level Project，TLP）的时间顺序进行组织。

## 目录

[TOC]

## 一、我们的项目适合Apache孵化器吗？

正如ASF在[2018年的愿景声明](https://blogs.apache.org/foundation/entry/the-apache-software-foundation-2018)中所讲的那样，ASF为公共利益提供软件。

ASF的项目会遵循[Apache之道](http://www.apache.org/theapacheway/index.html)进行运转，Apache之道是一套指导原则和最佳实践。

ASF非常重视“社区重于代码”（Community Over Code）这一理念，ASF严格独立于公司和组织，并强调在工作各方面保持开放。

捐赠项目到ASF，意味着您将放弃对该项目以及项目商标（如果有）的控制。非常欢迎您参与该项目，但是除了成为PMC（Project Management Committee，项目管理委员会）成员之外，您没有其他特殊的地位。好消息是，由于ASF的独立性和对项目可持续性的重视，您的项目可以自己成长，并可能具有更广泛的影响力。

假设您的项目符合这种观念模式，我们不会根据项目功能来判断项目的接收情况，这是由ASF特意不设置技术策略所决定的。如果您的项目与[ASF已有项目](https://projects.apache.org/)非常相似，我们可能会要求你考虑加入该项目。尽管如此，我们仍然有一些项目具有相似的目标，但这并不一定是一个问题。

为了给“podlings”（incubating projects，孵化项目）带来最大的成功机会，我们通常要求他们进入孵化器，并至少有一个围绕现有代码库构建的社区的开端。

## 二、成为ASF顶级项目的步骤是什么？

孵化的目标是成为ASF的顶级项目。您可以通过[How the ASF works](https://www.apache.org/foundation/how-it-works.html)页面，了解孵化以及不同角色（提交者committers、PMC成员等）的内涵。

为此，孵化项目（incoming project，podling）需要执行以下步骤：

- 寻找接口人（champion）和孵化导师（mentor），讨论并准备孵化方案；
- 决定在ASF孵化；
- 与孵化器PMC讨论方案；
- 如果需要，完善方案中的初始提交者和导师列表；
- 如果需要，基于孵化器PMC的反馈，完善方案；
- 孵化器PMC对方案进行投票；
- 配置项目的基础设施；
- 围绕项目代码开始构建社区；
- 邀请新的提交者和PPMC成员；
- 发布项目并记录，完善代码和发布过程；
- 当准备毕业时，与导师一起评估项目的就绪情况；
- 准备将现有商标转让给ASF（如果情况符合）；
- 与孵化器PMC讨论毕业；
- 孵化器PMC开始毕业投票，这会使ASF董事会决议建立TLP。

以上描述的是乐观的情况，概述了典型的孵化流程，项目真正孵化的顺序可能会与该流程略有不同。以下是该流程的详细内容：

## 三、与孵化器沟通

孵化器PMC负责管理孵化器，帮助孵化项目完成孵化过程。

可以通过公开链接：https://lists.apache.org/list.html?general@incubator.apache.org [general@incubator.a.o]访问邮件列表，与孵化器PMC进行沟通。

## 四、寻找接口人和导师

为了进入孵化器，您的项目需要一名接口人和至少2-3名导师。这些人需要是孵化器PMC中的成员，ASF成员只需提出即可加入孵化器PMC。

接口人负责在创建方案过程中帮助孵化项目，他们在前面的步骤中（至少直到项目方案被接收）充当孵化项目与孵化器PMC之间的联络员，之后可能会继续担任导师。

导师则会在项目成长为顶级项目的道路上全程陪伴。

起点通常是寻找接口人，您可以在general@incubator.a.o邮件列表中提交项目的简短介绍，附上相关链接，并说明您正在寻找接口人，努力引起大家的兴趣。如果您认识任何ASF成员或孵化导师，可以直接询问他们是否愿意提供帮助。

## 五、创建孵化方案

接口人会帮助项目准备孵化方案，方案会对新项目进行描述，以便后续与孵化器PMC进行初步讨论。

方案需要包含若干标准段落，详情请参考[podling proposal template](https://cwiki.apache.org/confluence/display/INCUBATOR/New+Podling+Proposal).

ASF项目的孵化方案都保存在[Incubator wiki](https://cwiki.apache.org/confluence/display/INCUBATOR/Proposals)页面上，可以将它们作为示例进行参考，上一自然段中的链接给出的是方案的最新模板。

## 六、讨论孵化方案

方案准备好后，项目代表需将其发送至general@incubator.a.o进行讨论，主题行应如下，以引起孵化器PMC的注意。

`[DISCUSS] Foo Proposal`

该讨论通常会要求方案进行一些改动。

该讨论阶段没有规定讨论时长，通常会持续几天，直到所有讨论要点被解决。

以下是最近的讨论，请参考：

- [Nuttx proposal](https://lists.apache.org/thread.html/7ed194c45460a3941ae6713b20e742ec7af398c5414de7b17d188c3b@) (in progress)
- [StreamPipes proposal](https://lists.apache.org/thread.html/1cf79ef65888f695b4b925fd67ef8a2b845f6b0931c251a0ff1115e1@) (accepted)
- [Sparkr proposal](https://lists.apache.org/thread.html/ff9874f5353d319152f09aa9c1aa1a673b84acdaeb9932432d58d5ab@) (withdrawn)
- [TubeMQ proposal](https://lists.apache.org/thread.html/21c5453b40765cf1d5a06540fcf6d76c0d5b6b7df7ade5c29d31aa3e@) (accpeted)
- [MetaObjects proposal](https://lists.apache.org/thread.html/dbdbc6bd8e238d9dbf16604d5fa13500523d6e812fcd863444f99842@) (on hold)

## 七、孵化方案投票

讨论阶段一结束，接口人或项目代表就会在general@incubator.a.o邮件列表中创建[VOTE]进程。

投票过程依据[ASF投票规则](https://www.apache.org/foundation/voting)进行。简言之，投票发生在孵化器邮件列表中，持续至少72小时，由孵化器PMC成员进行投票，遵循多数投票法，也欢迎其他人进行投票。

## 八、配置基础设施

孵化器PMC投票决定创建该项目后，就可以为其配置基础设施。

通常，接口人或孵化导师会推动这一过程。但是，如果项目社区成员知道如何进行操作的话，也可以由社区成员推动这一过程。

详情请参考[Infra and the Incubator](https://infra.apache.org/infra-incubator.html)。

## 九、宣传和公告

在孵化器PMC接收该项目之前，项目不能发布有关加入ASF的新闻稿或其他公开声明。

关于项目如何为自己做广告方面也有一些限制，特别是在孵化项目的新闻稿方面。[Incubator Branding Guide](http://incubator.apache.org/guides/branding.html)和[Apache Podling Publicity/Media Guidelines](https://incubator.apache.org/guides/publicity.html)页面对项目宣传规则有更详细的解读。

## 十、导入初始代码

项目需遵循特定流程将代码捐赠给ASF，该流程基于[软件授权协议](https://www.apache.org/licenses/software-grant.txt)和/或[CCLA](https://www.apache.org/licenses/cla-corporate.txt)。

关于初始代码导入的更多信息，请参考[Initial Code Import](http://incubator.apache.org/guides/transitioning_asf.html)。

## 十一、社区构建

在孵化过程中，项目有望构建并扩大其社区，包括投票选拔新的提交者和PPMC成员。

候选者的讨论和投票过程都发生在项目的私有PPMC邮件列表中，这是该邮件列表为数不多的功能之一，因为通常所有的讨论都是公开的。

扩大社区，特别是重建项目社区是ASF治理的重要组成部分，因为社区可以提升项目的持续性。

## 十二、项目发布

在项目孵化过程中，我们期待项目可以发布多个软件版本，这些版本会朝着完全符合[ASF发布政策](http://www.apache.org/legal/release-policy.html)的方向逐渐发展。版本发布完全符合ASF发布政策是项目毕业的条件之一。

按照[孵化器发布指南](https://incubator.apache.org/guides/releasemanagement.html#choice_of_disclaimers)要求，项目发布版本时，任何发布文件名中必须包含“incubating”一词，并且必须要包含DISCLAIMER或DISCLAIMER-WIP免责声明，以避免混淆项目状态。由于孵化项目还不是真正的ASF项目，设置适当的期望值很重要。

请注意Apache版本发布仅包含源代码。为了给用户提供方便，项目通常也会一同分发[编译过的软件包](http://www.apache.org/legal/release-policy.html#compiled-packages)。但重点仍是实际发布的源码，所有分发的编译过的软件包都是基于这些正式发布的源码。

## 十三、关于项目版本发布的两轮投票

项目版本发布的投票分为两个阶段：

首先，在开发人员邮件列表（dev list）上对版本发布进行投票，该轮投票主要是为了让项目社区练习和学习版本发布的投票过程。只要PPMC成员给出至少三张赞成票（+1），并且赞成票多于反对票，就算投票通过。

如果第一次投票通过，则孵化器PMC在孵化器常规邮件列表上进行第二轮投票，与所有ASF版本发布一样，这是使投票成为基金会行为的规定动作。

在孵化器PMC的[VOTE]消息中，需明确将第一轮开发人员邮件列表中的投票情况报告给孵化器PMC，包括投票结果，以及指向项目投票记录的[lists.apache.org](http://lists.apache.org/)链接。这样，导师和其他孵化器PMC成员的投票将与孵化器PMC投票绑定，而不用投两次票。

项目和孵化器的投票都要遵循[ASF投票规则](https://www.apache.org/foundation/voting)：多数投票法；投票过程持续至少72小时；如果有人多次投票，以最后一次投票为准。

## 十四、孵化项目与顶级项目的区别是什么？

顶级项目是成熟的ASF项目，由自己的[PMC](http://www.apache.org/foundation/governance/pmcs)进行管理，并且向[ASF董事会](https://www.apache.org/foundation/board/)进行报告。

孵化项目是正在训练中的顶级项目。他们所做的大部分工作与顶级项目相同，特别是顶级项目在孵化过程中的工作。

主要的区别如下：

- 和PMC相反，孵化项目不能代表ASF做出正式决定，因为他们不是ASF架构的正式组成部分（比如，孵化项目没有在[ASF章程](https://www.apache.org/foundation/bylaws)中被提及）。这意味着孵化器PMC需要扮演孵化项目代理人的角色，使项目的操作（比如ASF发布）正式化，并使其成为[基金会的行为](https://blogs.apache.org/foundation/entry/success-at-apache-the-apache1)。
- 孵化项目会有一个PPMC（Podling Project Management Committee），像顶级项目PMC一样进行运转，但需要将一些事情委托给孵化器PMC执行，比如ASF版本发布的最终投票权。
- 提交者、PPMC成员的选拔与顶级项目中的做法类似。孵化项目可以直接选拔候选人进入PPMC，也可以先将候选人选为提交者，之后再将他们提为PPMC成员。提交者没有正式的决策权，所以通常采用“两步走”的流程，但这不是必需的。详情请参阅[How the ASF works](https://www.apache.org/foundation/how-it-works.html)。
- 顶级项目向[ASF董事会](https://www.apache.org/foundation/board/reporting)进行报告，而孵化项目向[孵化器PMC](https://cwiki.apache.org/confluence/display/INCUBATOR/Reports)进行报告。两种汇报最初都是每月一次，之后是每季度一次。
- 每个顶级项目都有一个[PMC主席](https://apache.org/dev/pmc.html)，PMC主席是顶级项目与董事会间的联络人。PMC主席不是项目的领导者，而是一个管理角色，即使他们在ASF组织架构中拥有VP（Vice President）的头衔。孵化项目中没有孵化导师的角色，导师是社区成员中的志愿者，在项目和孵化器PMC间充当联络员。
- 孵化项目的版本发布需要两轮投票。

ASF强烈鼓励项目有规律地成长和更新他们的名单，以促进项目可持续发展。孵化项目和顶级项目都应该留意社区中活跃的成员，积极选拔新的提交者和PMC成员。

## 十五、毕业就绪评估

当项目社区准备毕业时，应该先对就绪情况进行自评估。

ASF社区发展PMC（Community Development PMC）维护的[成熟度模型](https://community.apache.org/apache-way/apache-project-maturity-model.html)为此提供了一个很好的模板，可以帮助发现项目在孵化中忽略的事情。成熟度模型页面给出了项目毕业的案例。

## 十六、毕业讨论

基于就绪情况的自评估，当社区和导师认为项目已经准备好毕业了，导师或PPMC成员要在孵化器常规邮件列表中开始一个[DISCUSS]进程，提议毕业并请求孵化器PMC审查项目。

讨论中最好包含毕业方案，为接下来的投票做好准备。

## 十七、将商标转让给ASF

捐赠项目给ASF的个人或组织如果持有项目必需的商标，则需在项目毕业前将其转让给ASF。

## 十八、毕业投票

毕业方案讨论结束后，导师或PPMC成员在孵化器常规邮件列表中开始一个[VOTE]进程，孵化器PMC在该进程上对是否向董事会推荐项目进行投票。

该投票遵循标准的[ASF投票规则](https://www.apache.org/foundation/voting)，即多数投票法，持续至少72小时，如果重复投票，以最后一次投票为准。

## 十九、ASF董事会决议

一旦孵化器PMC投票通过项目毕业，孵化器PMC（IPMC）将会创建并向ASF董事会发送董事会决议进程，以供董事会进行投票。

董事会会在每月的第三个周三召开会议，并在例行会议上对此类决议进行投票。

董事会表决会立即生效，不过董事会会议的[公开会议记录](https://www.apache.org/foundation/board/calendar.html)相对较晚，但通常会在一个月之内。

## 二十、毕业后任务

项目毕业后，需要在孵化器状态页面上更新项目状态，并对其资源和流程进行一些更改。

[Life after Graduation](http://incubator.apache.org/guides/transferring.html)指南列出了相应的任务。
 
 
## 表格版
**成为ASF顶级项目的步骤**
步骤 | 内容 | 详情
-- | -- | --
1 | 与孵化器沟通 | 孵化器PMC管理孵化器，帮助项目孵化。
2 | 寻找接口人（champion）和孵化导师，讨论并准备孵化方案 | 项目要进入孵化器，需要一个接口人和至少2-3个导师，只有孵化器PMC中的成员可以担任这两种角色。
3 | 创建孵化方案 | 接口人会帮助项目准备孵化方案，该方案将用于下一步与孵化器PMC的讨论。方案可以根据模板编写，需要包含几个标准部分。
4 | 与孵化器PMC讨论孵化方案 | 方案准备好后，项目代表要将其发送至general@incubator.a.o邮箱，孵化器PMC会对该方案进行讨论。
5 | 如有需要，完善方案中初始提交者和导师列表 | -
6 | 如有需要，基于孵化器PMC的反馈完善方案 | -
7 | 孵化器PMC对方案进行投票 | 讨论阶段结束后，接口人或项目代表会在general@incubator.a.o邮件列表中启动【投票】进程，投票按照ASF的投票规则进行。
8 | 设置该项目的基础设施（JIRA等） | 如果孵化器PMC同意接受该项目，就可建立该项目的基础设施了，该过程通常由接口人或导师进行推动，如果社区成员熟悉该操作，也可由社区成员来推动。
9 | 导入初始代码 | 企业捐赠的项目，在导入初始代码前，需要提交软件授权协议（SGA）或企业贡献者许可协议（CCLA）；个人捐赠的项目，在导入初始代码前，需要主要贡献者提交个人贡献者许可协议（ICLA）或SGA。导入过程中，需要检查和报告代码中受美国出口管制法管制的密码技术。除此以外，代码还需要按照Apache模板，进行清理和重新打包。
10 | 围绕该项目的代码构建社区 | 包括投票产生新的提交者和PPMC成员（Podling Project Management Committee）。
11 | 发布项目，记录并完善发布过程 | 在孵化期间，预计将发布多个版本，这些版本将逐渐符合ASF发布政策。完全合规的发布是项目毕业的条件之一。孵化中的项目进行发布还必须在任何发布文件名中包含“incubating”一词，并根据孵化器发布指南包含免责声明或免责声明-WIP，以防止对项目状态产生任何混淆。由于孵化中的项目还不是“真正的”ASF项目，所以设定正确的期望值是很重要的。   孵化中的项目版本发布需要两次投票，一次是在开发者邮件列表上进行的投票，如果PPMC成员中至少有3个赞成票（+1），并且赞成票比反对票（-1）多就算通过了。第二次是在孵化器常规邮件列表上进行的投票，这次投票由孵化器PMC进行投票。   Apache发布仅包含源代码，但是项目通常也会分发一些编译过的软件包。软件源代码发布是发布重点，所有分发的编译过的软件包均基于这些发布的“正式”的源代码。
12 | 准备毕业，与导师一起评估项目的准备情况 | 准备毕业的项目需要根据ASF提供的成熟度模型进行自我评估，这可以帮助发现在孵化过程中被忽略的事务。
13 | 将商标转让给ASF | 将代码捐赠给ASF的企业或个人，如果持有该项目需要的商标，则需在项目毕业前，将商标转让给ASF。
14 | 与孵化器PMC讨论毕业 | 如果社区和导师根据自我评估认为项目已经做好准备，可以毕业，会在孵化器常规邮件列表上开始一个【讨论】进程，提议毕业并请求孵化器PMC审查该项目。
15 | 孵化器PMC进行毕业投票 | 毕业提议的【讨论】进程结束后，孵化器常规邮件列表上会开始一个【投票】进程，孵化器PMC对该项目进行投票，投票依据ASF投票规则进行。
16 | ASF董事会决议 | 孵化器投票通过后，将会创建董事会决议进程并发送给ASF董事会，供董事会投票。董事会每月第三个周三会召开会议，会上会对此类决议进行投票，投票结果即刻生效。
17 | 毕业后的任务 | 毕业后，项目需要在孵化器状态页面上更新状态，并对其资源和流程进行一些更改。
