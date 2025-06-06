# ASF 项目安全指南（针对提交者）
>原文地址 : https://www.apache.org/security/committers.html
>
>翻译 : @CaoZhen
>
>校对 : @willemjiang

## 引言

以下是针对 Apache 提交者处理安全漏洞的指导原则。[Apache 安全团队](security@apache.org)可为需要协助的 Apache 项目提供支持与建议。

- [已知漏洞](https://www.apache.org/security/committers.html#known)
- [项目专用安全邮件列表](https://www.apache.org/security/committers.html#lists)
- [处理潜在漏洞](https://www.apache.org/security/committers.html#possible)
- [CVE IDS](https://www.apache.org/security/committers.html#ids)

## 已知漏洞

存在已知且已公开漏洞的项目应在如 [httpd 安全页面](https://httpd.apache.org/security_report.html)的相关页面上提供这些漏洞的详细信息。在项目主页上提供指向安全信息页面的清晰链接。

除非已实施必要配置来限制对该问题的访问权限为仅限于报告者和项目团队，否则不得在项目的公开漏洞跟踪系统中输入安全漏洞的详细信息。

## 项目专用安全邮件列表

项目可能希望创建一个[项目专用安全邮件列表](https://security.apache.org/projects/)。这些列表的名称采用 `security@project.apache.org` 的格式，例如 `security@tomcat.apache.org`。

当基础设施团队创建项目专用安全邮件列表时，会将其配置为自动将所有消息抄送至 `security@apache.org`，因此您在向该列表发送邮件时无需手动抄送 `security@apache.org`。

我们预计项目 PMC 成员和提交者中的一部分将订阅项目专用安全邮件列表。请勿将该列表用作第三方通知系统；非提交者不应订阅该列表。

## 处理潜在漏洞

以下是处理潜在安全漏洞的默认流程。需要采用不同流程的项目**必须**联系 `security@apache.org` 寻求建议，并应明确且公开地记录其流程。

### 私下处理

在该流程正式结束并公开宣布前，**切勿**将漏洞相关信息对外披露。例如，**不应**创建公开的 Jira工单或GitHub问题跟踪，因为此类操作会使问题公开化。与任何提交相关的消息**均不得**提及该提交的安全性质。

### 报告

1. 发现问题的报告者需确定用于报告的邮件列表。若相关项目在安全项目列表中列出了 security@[project].apache.org 邮件列表，请使用[该列表](https://security.apache.org/projects/)。否则，请使用 `security@apache.org`。

2. 需注意，安全团队将忽略所有与报告或管理 Apache 软件中未公开安全漏洞无关的消息。

3. 如果报告发送到 `security@apache.org`，安全团队会将其转发至该项目的安全邮件列表，如果项目没有安全邮件列表，则转发至该项目的私人（PMC）邮件列表。安全团队会回复原始报告者，告知已完成转发。

如果该项目没有专门的 `security@project.apache.org` 邮件列表，所有与该漏洞相关的后续沟通都应抄送至 `security@apache.org`。对于发送到 `security@project.apache.org` 的消息无需进行此操作，因为这些消息会自动抄送至 `security@apache.org`。

### 确认

4. 项目团队向原始报告人发送一封电子邮件以确认该报告，并抄送至相关安全邮件列表。

5. 项目团队对报告进行调查，并决定是否接受或拒绝该报告。项目团队成员可在项目安全团队的授权下，与领域专家（包括其雇主处的同事）分享有关漏洞的信息，但需明确说明该信息不得公开披露。

6. 如果项目团队**拒绝**该报告，团队将致函报告人说明原因，并抄送相关安全邮件列表。

7. 如果项目团队**接受**该报告，团队将致函报告人告知已接受报告并正在修复中。若将此步骤与步骤8、9结合，可向报告人分享 CVE ID。

8. 项目团队可通过内部门户 `https://cveprocess.apache.org` 申请 CVE（[通用漏洞与暴露](https://cve.mitre.org/)）ID；或发送主题为“CVE 请求...”的邮件至 `security@apache.org`，并提供漏洞的简短（一行）描述。`security@apache.org` 可协助判断报告是否需要多个 CVE ID，或是否应将多个报告合并到单个 CVE ID 下。

9. 若未使用 `https://cveprocess.apache.org`，ASF 安全团队将分配 CVE ID，并向项目团队发送内部门户链接，以便其输入漏洞详细信息。

### 解决
10. 项目团队在内部列表中对修复方案达成一致。

项目团队在内部门户上记录了漏洞的详细信息和修复方案。门户会生成草稿公告文本。有关公告示例，请参阅[Tomcat对CVE-2008-2370的公告](https://lists.apache.org/thread/smbdmck5m48rbh6tw9bbfszf64oh591y)。报告中包含的详细程度取决于判断。通常，报告应包含足够的信息，使人们能够评估该漏洞对其自身系统构成的风险，但不应包含更多内容。公告通常不包含重现漏洞的步骤。

可选地，您可以将 CVE 置于 `REVIEW` 状态以请求安全团队进行审查。您可以通过“评论”功能讨论披露事宜，该功能也会将评论发送至相关私人邮件列表。

12. 项目团队向报告者提供修复方案和漏洞公告草稿以供评论。

13. 项目团队与报告者就修复方案、公告内容及发布计划达成一致。若报告者在合理时间内未予回应，这不应阻碍项目团队推进后续步骤，尤其当问题具有高严重性或重大影响时。

14. 项目团队提交修复方案。提交时**不得**提及该提交与安全漏洞相关。

15. 项目团队创建包含修复方案的发布版本。

### 公告

16. 在发布公告之后（或与发布公告同时），项目团队将公布漏洞及修复方案。在[内部门户](https://cveprocess.apache.org/)中将 CVE 状态设置为“就绪”。随后可通过该门户发送邮件。漏洞公告应发送至以下收件人：

    a. 与发布公告相同的收件人

    b. 漏洞报告人

    c. 项目的安全列表（如果项目没有专门的安全列表，则发送至 `security@apache.org`）

    d. `oss-security@lists.openwall.com`（[无需订阅](https://oss-security.openwall.org/wiki/mailing-lists)）。

这是有关漏洞的任何信息首次公开的节点。

### 完成

17. 项目团队更新项目的安全页面。

18. 将邮件列表中的公开公告链接添加到 CVE 的“参考”部分。这将通知安全团队，他们将把信息提交给 CVE 项目。

19. 如果项目仓库使用 Subversion，请在应用修复的提交日志中添加 CVE ID。如果项目使用 Git 仓库，**请勿**尝试此操作，因为编辑已推送的提交会引发各种问题。

## CVE IDS

CVE ID 是分配给安全漏洞的唯一标识符。Apache 安全团队是负责所有 Apache 项目的 [CVE 编号授权机构（CNA）](https://www.cve.org/ProgramOrganization/CNAs)，也是唯一有权为 Apache 软件基金会项目问题分配 ID 的团队。

如果您认为某个问题的描述存在错误，请联系 `security@apache.org`。
 
