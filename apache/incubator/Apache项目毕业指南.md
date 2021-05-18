* **原文标题：** Guide :: Guide to Successful Graduation
* **原文链接：** http://incubator.apache.org/guides/graduation.html
* **提交路径：** translation/apache/incubator/Apache项目毕业指南.md

# Apache 项目毕业指南

## 目录

[一、什么是毕业](一、什么是毕业)

[二、毕业成为子项目还是顶级项目](二、毕业成为子项目还是顶级项目)

[三、毕业之前](三、毕业之前)

- [毕业检查清单](毕业检查清单)
- [检查状态文件](检查状态文件)

[四、确保合适的项目名称和产品名称](四、确保合适的项目名称和产品名称)

[五、创建 Apache 发行版](五、创建 Apache 发行版)

[六、创建一个开放和多样化的社区](六、创建一个开放和多样化的社区)

- [其他事宜](其他事宜)

[七、毕业流程](七、毕业流程)

- [毕业成为顶级项目](毕业成为顶级项目)
- [社区的毕业投票](社区的毕业投票)
- [准备章程](准备章程)
- [推荐投票](推荐投票)
- [向董事会提交决议](向董事会提交决议)
- [新顶级项目的新闻稿](新顶级项目的新闻稿)

[八、毕业成为子项目](八、毕业成为子项目)

- [社区的毕业投票](社区的毕业投票)
- [子项目验收投票](子项目验收投票)
- [毕业批准投票](毕业批准投票)
- [最后步骤](最后步骤)

本文档的目的是帮助正在孵化的项目了解毕业流程，并提供一些关于如何实现毕业的看法。它还与孵化器[退出政策](http://incubator.apache.org/incubation/Incubation_Policy.html#Graduating_from_the_Incubator)有关。这不是一个僵化的标准，但代表了孵化器 general 邮件列表上以往讨论中凝结的共识。它还描述了毕业后应该如何迈出第一步。

本文只是一个指南。更具体的政策[在此](http://incubator.apache.org/policy/incubation.html)说明。

通过在 JIRA 的 Incubator 部分发布本文件的补丁或在孵化器的[general](http://incubator.apache.org/guides/lists.html#general_at_incubator.apache.org)邮件列表中发表评论来帮助改进本文。

## 一、什么是毕业

毕业是指一个正在孵化的项目成为已经存在的 Apache 项目下的一个子项目，或者成为一个顶级 Apache 项目的行为。毕业是一个民主的过程：最终要通过[投票](http://www.apache.org/foundation/voting.html)来决定。请注意，在你加入孵化器期间，你已经在忙于毕业的过程了：采用 Apache 的步骤、培养你的社区使之成长、就代码风格（制表符和空格）进行（有礼貌的）争论和创建发行版等等。所有这些行为都会对项目的毕业产生影响。

通往毕业的道路是非常清晰的：根据你的项目是想成为一个顶级项目，还是作为一个已经存在的项目下的子项目加入进去，步骤相当简单，但确实需要时间和努力。本文提供了使这个过程能够顺利进行的指南。

本文件仅用于指导和教育。实际政策记录在[孵化政策指南](http://incubator.apache.org/incubation/Incubation_Policy.html)中[这个](http://incubator.apache.org/incubation/Incubation_Policy.html#Graduating_from_the_Incubator)章节。关于毕业的任何问题，请在[孵化器 general 邮件列表](http://incubator.apache.org/guides/lists.html#general_at_incubator.apache.org)中发布。

## 二、毕业成为子项目还是顶级项目

每个提案都有一个[发起人](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#Sponsor)。发起人的身份表明了项目的目的地。对于由[董事会](http://incubator.apache.org/guides/roles_and_responsibilities.html#the_board)或[孵化器项目管理委员会（IPMC）](http://incubator.apache.org/guides/roles_and_responsibilities.html#incubator_project_management_committee_ipmc)发起的提案，这是一个顶级项目。对于其他提案，则作为发起项目的一个子项目。然而，目的地只在毕业时固定下来，而不是刚孵化的时候。项目在毕业过程中不断成长和发展。随着毕业的临近，应该根据项目当前的情况来重新审视最初的目标。

只有当子项目仍然属于某项目的范围并需要该项目[PMC](http://www.apache.org/foundation/how-it-works.html#structure)的同意时，才有可能作为子项目毕业。而作为一个顶级项目毕业，则需要[董事会](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#board)来组建新的项目。

[IPMC](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#Incubator_Project_Management_Committee_IPMC)也将发表民主意见。对于那些寻求毕业为子项目的人来说，这些意见是为了批准项目迁移。对于那些寻求毕业成为顶级项目的人来说，这些意见将是对[董事会](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#board)的建议。我们期待 IPMC 成员提出关于项目的问题，包括目的地的选择。这也是正常程序的一部分。

## 三、毕业之前

在开始考虑毕业之前，你需要确保已经准备好了，并且符合 Apache 对项目提出的要求。本节将为正在孵化的项目提供一个简短清单，以确定他们是否符合毕业标准。

### 毕业检查清单

以下是一个简短的检查清单，给出了一个总览，不能代替阅读之后的内容。

- 准备工作

  - 完成（并签收）[状态文件](http://incubator.apache.org/guides/graduation.html#notes-status)中记录的任务
  - 确保项目和产品的[合适名称](http://incubator.apache.org/guides/graduation.html#notes-names)
  - 展示[创建 Apache 发行版](http://incubator.apache.org/guides/graduation.html#releases)的能力
  - 展示[社区的准备情况](http://incubator.apache.org/guides/graduation.html#community)
  - 确保[导师](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#Mentor)和[IPMC](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#Incubator_Project_Management_Committee_IPMC)没有[遗留问题](http://incubator.apache.org/guides/graduation.html#notes-issues)

- 决定项目的[目的地](http://incubator.apache.org/guides/graduation.html#subproject-or-top-level)

- 准备一份[决议](http://incubator.apache.org/guides/graduation.html#tlp-resolution)（只限于候选的顶级项目）

- 目的地项目的[验收投票](http://incubator.apache.org/guides/graduation.html#subproject-acceptance)（只限于候选的子项目）

- 孵化器项目管理委员会（IPMC）：

  - 对于候选的顶级项目，这是一个[建议投票](http://incubator.apache.org/guides/graduation.html#ipmc-top-level-recommendation)
  - 对于候选的子项目，这是一个[毕业批准投票](http://incubator.apache.org/guides/graduation.html#subproject-graduation)

- 最后[交接](http://incubator.apache.org/guides/graduation.html#notes-on-hand-over)

- 考虑毕业后的[任务](http://incubator.apache.org/guides/graduation.html#project-first-steps)

### 检查状态文件

状态文件记录并总结了项目孵化的相关信息。[PPMC](http://incubator.apache.org/guides/ppmc.html#Incubator_ASF_Board_Reports)负责保持该文件的最新状态。在你能够毕业之前，所有的任务都需要完成。

状态文件是一个很好的方法，可以随时了解你的项目是如何进行的，以及为达到毕业标准需要做什么。[孵化器项目管理委员会](http://incubator.apache.org/guides/ppmc.html#Incubator_ASF_Board_Reports)将在投票决定你的项目是否毕业时检查这个文件。一旦所有的任务都完成了，并且符合标准，你的项目就可以毕业了。

JUDDI 项目的状态文件就是一个[例子](http://incubator.apache.org/projects/juddi.html)。

## 四、确保合适的项目名称和产品名称

请阅读这个[文档](http://www.apache.org/foundation/marks/naming.html)。"确保合适的项目和产品名称的过程 "是每个想毕业的正在孵化的项目的必修课。

## 五、创建Apache发行版

> 早发布，多发布

> — Eric Steven Raymond

> http://catb.org/esr/writings/cathedral-bazaar/cathedral-bazaar/ar01s04.html

项目需要创建发行版。Apache 项目需要了解如何进行版本发布。因此，在孵化器中展示发版能力是一个重要步骤。

当你要创建 Apache 发行版时，那么请阅[读孵化器发布管理指南](http://incubator.apache.org/guides/releasemanagement.html)，以了解发布一个能获得[IPMC](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#Incubator_Project_Management_Committee_IPMC)批准的版本的提示、技巧和指南。

## 六、创建一个开放和多样化的社区

毕业的一个主要标准是发展一个开放和多样化的[由精英管理的](http://www.apache.org/foundation/glossary.html#Meritocracy)社区。时间已经证明，这类社区比封闭的社区更加强大和富有成效。

Apache 项目是自我维持和自我管理的社区。长期的成功和良性发展，需要社区了解如何：

- 招募用户、开发者、提交者和 PMC 成员
- 开展尽责的集体活动
- 在不破坏人际关系的情况下，在公开场合就技术问题提出不同意见
- 在邮件列表中创造一个开放、积极和包容的氛围

毕业需要评估（IPMC 角度）一个正在孵化的项目是否学到了足够的知识，是否有足够的责任感来维持这样一个社区。

可以在[社区指南](http://incubator.apache.org/guides/community.html)中阅读如何为你的孵化项目建立一个开放和多样化的社区。

随着项目的发展，社区需要通过接受新的提交者来提高活力。一个项目需要学习如何招募新的开发者和提交者进入社区。接受新的提交者通常会增强项目的多样化。所以，这个过程是非常有益的。[社区建设](http://incubator.apache.org/guides/community.html)需要耗费精力，这些精力本可以用在代码开发上，但这一成本对项目的未来来说是一项重要的投资。

社区的开放性不仅仅是由贡献者的数量来衡量的。在邮件列表上的开放和互相尊重的讨论是至关重要的。必须学会在不破坏人际关系的情况下解决技术冲突。学习如何有效地使用邮件列表是非常重要的。如果能做到这一点，那么你们已经展现出一个活泼、活跃和成功的社区。未来将会很光明。

当项目不高度依赖任何一个贡献者（至少有 3 个法律上独立的提交者，并且没有某一个公司或实体单独掌控项目的命脉）时，该项目被认为有一个多样化的社区。基本上，这意味着当一个项目主要由一个公司的贡献者组成时，这是一个不够多样化的信号。你可以通过接纳更多的外部贡献者来满足这一要求。

培养一个开放的、多样化的、精英管理的社区不可能一蹴而就，我们需要努力。请阅读[社区建设指南](http://incubator.apache.org/guides/community.html)，了解实现这一目标的指南、提示和技巧。

### 其他事宜

孵化器更多的是依靠人而不是规则：并不试图创造规则来涵盖所有情况，而是根据需要制定和编写规则。在优化流程和政策的时候，人是可信的。本指南只能记录最常见的问题，有可能还有其他需要解决的问题没有被包括在内。

不确定是否准备好毕业的孵化项目可以参考[Apache 项目成熟度模型](http://community.apache.org/apache-way/apache-project-maturity-model.html)。当你评估社区的各种细节时，你可能会发现这是个有用的指南。

## 七、毕业流程

### 毕业成为顶级项目

顶级项目是由董事会创建的。因此，孵化器项目管理委员会（IPMC）只能向董事会建议该项目已经准备好毕业成为顶级项目。

毕业成为顶级项目需要：

- 项目的章程
- 一个正向的毕业[投票](http://www.apache.org/foundation/voting.html)
- 一个正向的 IPMC 建议[投票](http://www.apache.org/foundation/voting.html)
- 董事会接受的[决议](http://incubator.apache.org/guides/graduation.html#tlp-resolution)

这个过程可能需要一些时间，因为它通常会在社区内引起一些讨论，也可能在 IPMC 中引起讨论。

下面是一个毕业过程的大概时间表。它应该能帮助你了解你应该什么时候开始加强你的社区，以获得及时的毕业，并使这个过程顺利进行。

[![](http://incubator.apache.org/images/graduation-timeline.png)](http://incubator.apache.org/images/graduation-timeline.png)

对于每个事件，我们都安排了一到两周的时间。即使投票通常被限制在 72 小时内，你也应该为讨论和修改提案后的重新投票做准备。

### 社区的毕业投票

成为一个顶级项目之前，社区需要有自我管理的意愿。证明这一点的一个好方法是，由社区对毕业提案自由投票。

这个投票并不是一个要求，而是建议。除非[导师](http://incubator.apache.org/incubation/Roles_and_Responsibilities.html#Mentor)和社区积极地表达他们对毕业的准备，否则 IPMC 成员不太可能投票批准毕业。明智的做法是通知[孵化器 general 邮件列表](http://incubator.apache.org/guides/lists.html#general_at_incubator.apache.org)，社区内部投票正在开始。请不要将投票抄送至孵化器 general 邮件列表，因为这样会造成混乱。相反，你可以： 转发投票邮件到孵化器 general 邮件列表，或者向孵化器 general 邮件列表发送一份不同的副本，表明毕业社区投票正在进行中。

### 准备章程

因此，在这种情况下，应该由社区在导师的建议下起草一份合适的董事会决议。提交者可以在[提交者 svn 仓库](https://svn.apache.org/repos/private/committers/board/templates/podling-tlp-resolution.txt)中访问孵化项目决议模板。你的[花名册](https://whimsy.apache.org/roster/ppmc/)也包括起草决议的功能。此外，决议还包括在董事会会议记录中，这些会议记录在[这里](http://www.apache.org/foundation/board/calendar.html)公开发布，这里包含了许多例子。

在创建这个文件时，应该参考原始提案和状态文件。项目随着时间的推移而发展，与原始提案的一些偏差很可能是可以接受的。董事会决议将对 Apache 项目范围做最终定义。因此，重要的是，它要反映出项目在毕业前夕的愿景。

一个好的决议既不能太窄也不能太宽。如果项目的范围太窄，那么其活力就会受到不必要的限制。如果一个项目的范围太广，那么它可能缺乏重点，并遭受不容易治理的困扰。

如果你阅读了这些决议，你还会发现你需要为你的项目任命一个[主席](http://www.apache.org/foundation/glossary.html#Chair)。由[PPMC](http://incubator.apache.org/guides/ppmc.html)来选择一个人在毕业后担任主席。

### 推荐投票

在开始投票之前，应在[孵化器 general 邮件列表上](mailto:general@incubator.apache.org)提出决议，以允许反馈。一旦达成共识，就应该由 PPMC 的一名成员在孵化器 general 邮件列表中开始投票，提议 IPMC 向董事会推荐该决议。

### 向董事会提交决议

顶级项目是由董事会的一项[决议](http://incubator.apache.org/guides/graduation.html#tlp-resolution)创建的。一旦决议定稿并达成共识，应提交给董事会。为了列入下一次会议的议程，该决议应在会议前至少 72 小时提交。可提供一份[会议日程](http://www.apache.org/foundation/board/calendar.html)。

董事会的事务应该通过董事会的邮件列表提交。建议使用Apache邮箱发送邮件。不建议在一个主题中混合公开的和私有的邮件列表地址。

董事会邮件列表是私有的。应该遵守 Apache 私有邮件列表的一般[网络礼仪](http://www.apache.org/foundation/how-it-works.html#management)。因此，建议只抄送孵化项目和 IPMC 的私有邮件列表（而不是孵化器 general 邮件列表）。请以适当的保密性对待回复。

提交的内容应包括：
- 一个明确的主题（例如建立 Foo 顶级项目） 
- 一个简短的介绍 
- 拟议的 VP 的名字 
- 投票历史邮件的链接 
- 投票结果的摘要 
- [决议文本](http://incubator.apache.org/guides/graduation.html#tlp-resolution)

例如：

```
From: <you _at_ apache dot org>
To: <board _at_ apache dot org>
CC: <<project>-private _at_ incubator dot apache dot org>
Subject: Proposed Resolution: Establish <project> TLP

Dear Apache Board,

<Project> is ready for graduation out of the incubator. So, please
consider the draft resolution below at your next meeting.

<thank you, best regards, personal note if you wish, etc etc>

<your name>

--
References:

Home: <project home page>
Vote by project: <link to vote thread on project list>
Vote by incubator: <link to vote thread on general list>

Resolution draft:

<<resolution goes here, 72 characters wide,
indent with 4 spaces>>

--
<your e-mail sig, if you have one>
```

请尽量保持董事会邮件列表低流量。不要在列表中提醒或询问是否已经收到信息。[Apache 成员](http://www.apache.org/foundation/members.html)可以访问董事会档案，并可以查看董事会会议。如果想了解某个决议的进展情况，请询问友好的导师、Apache 成员或[董事](http://www.apache.org/foundation/board/)。

### 新顶级项目的新闻稿

一旦有了明确的共识，推荐就会水到渠成，PPMC 的成员应该联系 ASF 市场和宣传部，如果你对宣布项目毕业的正式新闻稿感兴趣，请联系 press(at)apache(dot)org。在董事会决议发布的同时，你就可以着手进行了。

## 八、毕业成为子项目

子项目是由项目管理委员会接受的。IPMC 将会批准孵化项目毕业为一个子项目。

### 社区的毕业投票

成为子项目是一个自愿的过程，社区应该接受该项目成为一个子项目。孵化项目的 PPMC 和提交者应该清楚新的子项目的结构，例如，谁将成为 PMC，谁将成为提交者。由于这种性质，重要的是，孵化项目要经过投票来成为一个子项目。这个投票应该发生在公开的开发者邮件列表中。

### 子项目验收投票

为了接受孵化项目为子项目的一个先决条件是，由项目[PMC](http://www.apache.org/foundation/how-it-works.html#structure)发起正式投票。有时，项目可能会觉得孵化项目的规模太大，作为一个顶级项目会更好。遇到这种情况，请联系项目的主席。

### 毕业批准投票

一旦一个顶级项目投票接受孵化项目并成为一个子项目，应通过孵化器 general 邮件列表向 IPMC 发送通知，表明孵化项目将成为一个子项目。如果在 72 小时后没有提出任何问题，那么孵化项目可以被认为成功的成为了一个子项目。同样的，如果任何 IPMC 成员提出问题，就需要进行讨论。如果问题得到解决，提出问题的人应表示收回他们的顾虑，或以其他方式表示问题已经解决。

### 最后步骤

请阅读[《孵化器资源迁出指南》](http://incubator.apache.org/guides/transferring.html)
