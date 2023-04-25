---
title : 新 Committer
原文 : 'https://community.apache.org/newcommitter.html'
翻译 : @L-Y-L/87
校对 : @tuohai666, @ShawnJim, @6freeair2016, @willemjiang
---

发现潜在的新 Committer，发起提名他们是 Committer 的投票并处理相关文档，是整个社区成员可以致力的任务。

每个项目都有不同的方法来管理 Committer。本页面描述了在许多 Apache 项目中常见的过程，同时还提供了各种必要的沟通模板。

{{% toc %}}

## 评估新候选人是否适合成为提交者的指南

在投票时，所有 PMC 成员都需要自己决定是否批准候选人成为 committer。他们可能会搜索邮件列表和 JIRA，以查看候选人如何与他人互动，以及他们所做的贡献（代码或文档补丁、建议、参与对话）。

所有新提交者都**必须**遵守[Apache 行为准则](https://www.apache.org/foundation/policies/conduct.html)。

每个 PMC 可能希望创建自己的补充提交者指南；这是[Apache Forrest 提交者指南](https://forrest.apache.org/committed.html)。

以下是在评估候选人的 Committer 资格时需要考虑的一些要点。

### 与同行合作的能力。

我们如何评估？

-   通过他们通过电子邮件进行的互动。
-   通过他们如何回应批评。
-   通过他们如何参与群体决策。

### 有能力成为导师。

我们如何评估？

-   通过他们通过电子邮件进行的互动。
-   通过他们的清晰程度以及他们识别甚至创建适当的背景材料的意愿。

### 社区

我们如何评估？

-   通过他们通过电子邮件进行互动情况。
-   他们是否帮助回答邮件列表中提出的问题？他们是否表现出乐于助人的态度，是否尊重他人的想法？

### 投入

我们如何评估？

-   按已经给项目的时间。
-   通过他们如何坚持这个过程来解决棘手的问题。
-   通过他们如何帮助完成不那么有趣的任务。

### 个人技能/能力

我们如何评估？

-   对项目有扎实的总体了解。
-   电子邮件中讨论的质量。
-   他们的补丁（如适用）是否仅需粗略审查即可轻松应用。

## 新提交者过程

本节描述了一个典型的 Apache 项目处理投票以添加新提交者的过程。该过程中提到的模板出现在本文档的后面。

### 概括

1.  讨论提议的 Committer/PMC 成员。如果是肯定的，请进行投票（templates/committerVote.txt）
2.  关闭投票 (templates/closeVote.txt)
3.  如果结果是肯定的，请邀请新的提交者 (templates/committerInvite.txt)

如果他们接受，那么：

1.  如果他们已经有一个 Apache id，授予适当的提交权限。使用 Whimsy 工具通过[https://whimsy.apache.org/roster/committee/](https://whimsy.apache.org/roster/committee/)或[https://whimsy.apache.org/roster/ppmc/](https://whimsy.apache.org/roster/ppmc/)更新名册。
2.  如果他们已经提交了 ICLA，请求创建提交者帐户。如果他们需要更改之前提交的 ICLA 中的任何内容，请等待新的 ICLA 提交，然后申请帐户。
    1.  等 root 确认完成
    2.  PMC Chair 更新 LDAP 组成员资格，启用 svn、gitbox 和其他访问。如果提交者使用 GitHub，他们有责任将其链接到他们的 ASF 帐户。
    3.  将提交者添加到 JIRA 和 CWiki 中的相应分组
3.  通知提交者完成（template/committerDone.txt）
4.  如果提交者也将成为 PMC 成员，PMC 主席将发送电子邮件至 board@ 请求确认新的 PMC 成员 (templates/email-member-ack.txt)
5.  宣布新的提交者（template/committerAnnounce.txt）

### 讨论

我们在邮件列表上进行讨论和投票，`private@`以进行坦率的讨论。

我们邀请人们以提交者/PMC 成员的身份加入，而不是 github id。可以参考候选人的 github id 来了解上下文，但是应该用他们的名字来称呼这个人。没有必要提供他们的法定全名（这将被保密），但使用他们的名字很重要，因为他们在电子邮件中是这样称呼自己的。如果一个人只知道他们的 github id，那么可以在举行投票之前询问他们的真实姓名。

为每个新人启动一个单独的 \[VOTE\] 线程。这会使查看电子邮件存档变得更容易。

我们需要确保他们是忠诚的人，我们可以与之共事。他们将是我们的同龄人。我们已经观察到他们致力于项目并且对用户和其他开发人员很友善。

提议不要拖太久，也不能过于匆忙，需要考虑时效性的问题。时机来临，很显然我们应该邀请他们，这会鼓舞他们，令之保持热情。如果我们拖得太久，就有可能让他们感到失望。

在`private@`名单上，我们每个人都可以毫无保留地准确地说出我们对每个人的感受。保持讨论简洁。表扬部分可以稍后公开进行。但是请记住，如果该成员以后成为 PMC 成员，他们将有权访问此讨论。

让投票线程运行一周。

**共识批准**取得了积极的结果：至少 3 +1 票且没有否决权。

任何否决都必须附有理由，并且否决者必须准备好为其辩护。其他成员可以尝试鼓励他们改变主意。

新提交者可以选择安静或活跃。如果我们发现某些人失效并且从未做出贡献，那么该项目可以采取措施让他们退休。

获得肯定结果后，将结果记录在 PMC 列表中，主题为 \[RESULT\]\[VOTE\]，然后邀请候选人。我们让候选人有机会私下拒绝提交者身份。他们可以回复 PMC 邮件列表。

在我们对列表做出决定`private@`并完成上述步骤后，我们会在列表中宣布新的提交者`dev`。然后我们每个人都可以在公开场合进行称赞。

[有关该过程的其他说明可在Apache](https://www.apache.org/dev/pmc.html#newcommitter)主站点上找到。

## 电子邮件模板

### 提交者投票模板

这是开始对新提交者进行投票的电子邮件。一些项目自动使提交者成为 PMC 成员。如果是这种情况，请将此模板与以下模板（PMC 投票模板）合并。

```
------------------------------------------------------------
To: private@[PROJECT].apache.org
Subject: [VOTE] New committer: Jo Bloggs

[ add the reasons behind your nomination here ]

Voting ends one week from today, i.e. midnight UTC on YYYY-MM-DD
https://www.timeanddate.com/counters/customcounter.html?year=YYYY&month=MM&day=DD

See voting guidelines at
https://community.apache.org/newcommitter.html

------------------------------------------------------------
```

### PMC 投票模板

**这是开始对新的PMC 候选人**进行投票的电子邮件。新的 PMC 成员需要由现有的 PMC 成员投票选出，然后由董事会（或用于孵化项目的孵化器 PMC）批准。

```
------------------------------------------------------------
To: private@[PROJECT].apache.org
Subject: [VOTE] New PMC candidate: Jo Bloggs

[ add the reasons behind your nomination here ]

Voting ends one week from today, i.e. midnight UTC on YYYY-MM-DD
https://www.timeanddate.com/counters/customcounter.html?year=YYYY&month=MM&day=DD

See voting guidelines at
https://community.apache.org/newcommitter.html
```

### 关闭投票

此邮件结束投票并将结果报告给项目。

```
------------------------------------------------------------
To: private@[PROJECT].a.o
Subject: [RESULT] [VOTE] New committer (or PMC candidate): Jo Bloggs

The vote has now closed. The results are:

Binding Votes:

+1 [TOTAL BINDING +1 VOTES]
 0 [TOTAL BINDING +0/-0 VOTES]
-1 [TOTAL BINDING -1 VOTES]

The vote is ***successful/not successful***
```

### 通知董事会新的 PMC 成员

请参阅[https://www.apache.org/dev/pmc.html#newpmc](https://www.apache.org/dev/pmc.html#newpmc)

### 提交者邀请模板

这是建议发送给新当选的提交者的邀请电子邮件，在新提交者投票获得积极结果后发送。

```
------------------------------------------------------------
To: JoBloggs@foo.net
Cc: private@[PROJECT].apache.org
Subject: Invitation to become [PROJECT] committer: Jo Bloggs
    
Hello [invitee name],

The [Project] Project Management Committee (PMC) 
hereby offers you committer privileges to the project 
[as well as membership in the PMC]. These privileges are
offered on the understanding that you'll use them
reasonably and with common sense. We like to work on trust
rather than unnecessary constraints. 

Being a committer enables you to more easily make 
changes without needing to go through the patch 
submission process. [Being a PMC member enables you 
to guide the direction of the project.]

Being a committer does not require you to 
participate any more than you already do. It does 
tend to make one even more committed.  You will 
probably find that you spend more time here.

Of course, you can decline and instead remain as a 
contributor, participating as you do now.

This personal invitation is a chance for you to accept or decline in private.
Please let us know in reply to this message whether you accept or decline.

If you accept, you will need an Apache account (id) with privileges.
Please follow these instructions.

A. If you already have an ICLA on file:

    1. If you already have an Apache account, let us know your id and we
will grant you privileges on the project repositories.

    2. If you have previously sent an ICLA, let us know the email address
and public name used on the ICLA and your preferred Apache id, and
we will request your account. 

    3. If the email address on the previously submitted ICLA is no longer
valid, let us know the email address and public name used on the new ICLA,
and your preferred Apache id. Continue to step B below and file your new ICLA.

Look to see if your preferred ID is already taken at 
https://people.apache.org/committer-index.html

B. If there is not already an ICLA on file, you need to submit an ICLA:

    1. Details of the ICLA and the forms are found 
    through this link: https://www.apache.org/licenses/#clas

    2. Instructions for its completion and return to 
    the Secretary of the ASF are found at
    https://www.apache.org/licenses/contributor-agreements.html#submitting

    Do not copy the project or any other individual on your message
    to Secretary, as the form contains Personally Identifiable Information
    that should be kept private.

    3. When you complete the ICLA form, be sure to include in the form
    the Apache [Project] project and choose a 
    unique Apache ID. Look to see if your preferred 
    ID is already taken at 
    https://people.apache.org/committer-index.html
    This will allow the Secretary to notify the PMC 
    when your ICLA has been recorded.

When recording of your ICLA is noted, you will 
receive a follow-up message with the next steps for 
establishing you as a committer.
```

### Committer 帐户创建

[按照此处的](https://www.apache.org/dev/pmc.html#newcommitter)说明进行操作 。

总之：

如果 ICLA 标识了项目和有效的 Apache ID，并且 [RESULT][VOTE] 消息已发布到 PMC 私有邮件列表，则帐户创建请求由提交 ICLA 的秘书或助理提出。

否则，新帐户请求应由 PMC 主席（如果主席不在，则由任何[ASF 成员提出）。](https://www.apache.org/foundation/glossary.html#Member)

PMC 主席需要使用[ASF 新账户申请](https://id.apache.org/acreq/pmc-chairs/)表来发送新账户申请。会员可以使用[ASF 新帐户请求](https://id.apache.org/acreq/members/)页面。

对于在公共列表上举行的选举，请提供 [mail-archives.apache.org](https://mail-archives.apache.org/) url。对于私人列表，您可以使用[邮件搜索工具](https://mail-search.apache.org/)找到合适的 url。

### Committer 公告模板

`[PROJECT]-dev`这是在创建帐户后向其宣布新 Committer 的电子邮件。

```
------------------------------------------------------------
To: dev@[PROJECT].apache.org
Subject: new committer: ###Jo Bloggs

The Project Management Committee (PMC) for Apache [PROJECT]
has invited Jo Bloggs to become a committer and we are pleased 
to announce that they have accepted.

### add specific details here ###

Being a committer enables easier contribution to the
project since there is no need to go via the patch
submission process. This should enable better productivity.
A PMC member helps manage and guide the direction of the project.
```

### Committer 账号创建完成模板

Committer 账户建立后。
```
------------------------------------------------------------
To: private@[PROJECT].a.o, ###JoBloggs@foo.net
Subject: account request: ###Jo Bloggs

####, as you know, the ASF Infrastructure has set up your
committer account with the username '####'.

Please follow the instructions to set up your SSH,
svn password, svn configuration, email forwarding, etc.
https://www.apache.org/dev/#committers

[If your project automatically adds committers to the PMC]
Please subscribe to the [PROJECT] Project Management 
Committee mailing list private@[PROJECT].apache.org.
[/If]

You have commit access to specific sections of the
ASF repository, as follows:

[PROJECT] has various resources at:
  https://svn.apache.org/repos/asf/[PROJECT]
  https://gitbox.apache.org

The general "committers" at:
https://svn.apache.org/repos/private/committers

If using svn, you will probably need to 'svn switch" previous checkouts to now use https, 
for example:

svn switch --relocate https://svn.apache.org/repos/asf/[PROJECT] https://svn.apache.org/repos/asf/[PROJECT]
    
The developer section of the website describes roles within the ASF and provides other
resources:
  https://www.apache.org/foundation/how-it-works.html
  https://www.apache.org/dev/

The incubator also has some useful information for new committers
in incubating projects:
  https://incubator.apache.org/guides/committer.html
  https://incubator.apache.org/guides/ppmc.html

Just as before you became a committer, participation in any ASF community
requires adherence to the ASF Code of Conduct:
  https://www.apache.org/foundation/policies/conduct.html

[PROJECT should insert its own guidelines here; if none are available,
 the Apache Forrest guidelines are available as a template.]
  https://forrest.apache.org/guidelines.html

If you have any questions during this phase, then please
see the following resources:

Apache developer's pages: https://www.apache.org/dev/
Incubator committer guide: https://incubator.apache.org/guides/committer.html

Naturally, if you don't understand anything be sure to ask us on the [PROJECT] dev mailing list. 
Documentation is maintained by volunteers and hence can be out-of-date and incomplete - of course
you can now help fix that.

A PMC member will announce your election to the dev list soon.
```
