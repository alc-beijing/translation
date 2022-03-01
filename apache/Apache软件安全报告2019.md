- **原文标题：** The Apache Software Foundation Blog
- **原文链接：** https://blogs.apache.org/foundation/entry/apache-software-foundation-security-report
- **提交路径：** translation/apache/securityreport/Apache软件安全报告2019.md

# Apache软件基金会博客
Apache 软件基础安全报告：2019 年

概要：本报告探讨了2019日历年所有Apache软件基金会项目的安全状况。我们回顾了关键指标、特定漏洞以及 ASF 项目用户受安全问题影响的最常见方式。

发布时间： 2020 年 1月 31日

作者：Mark Cox，Apache 软件基金会安全副总裁

## 背景
Apache软件基金会（ASF）的安全委员会负责监督和协调所有 300 多个Apache项目中漏洞的处理。我们成立于 2002 年，由所有志愿者组成，我们对如何处理问题有一个[标准流程](https://s.apache.org/cveprocess)，这个过程包括我们的项目必须如何披露安全问题。

在Apache项目中发现安全问题的人都可以将其报告给 security@apache.org，在那里它们被记录下来并传递给相关的[专门安全团队](https://apache.org/security/projects.html)或项目管理委员会（PMC）进行处理。安全委员会查看所有地址中报告的所有问题，并在整个漏洞生命周期中跟踪问题。

安全委员会负责确保问题得到妥善处理，并将积极提醒各项目其悬而未决的问题和责任。作为董事会委员会，我们有能力采取行动，包括阻止其未来的发布，或者在最坏的情况下，如果项目对处理其安全问题没有响应，则将项目归档。这与 Apache 软件许可证一起，是 ASF 围绕官方发布的一般治理功能的关键部分，使 ASF 能够保护个人开发人员，并让用户有信心部署和依赖 ASF 软件。

对所有安全报告的监督以及我们开发的工具使我们能够轻松创建有关问题的统计信息。

## 2019年统计数据

2019年，我们的安全地址总共收到了超过 18，000 封电子邮件。在垃圾邮件过滤和主题分组之后，会出现 620 个非垃圾邮件主题。不幸的是，许多安全报告确实看起来像垃圾邮件，因此安全团队会仔细检查所有邮件，以确保不会长时间错过真实的报告。
![img](https://blogs.apache.org/foundation/mediaresource/fa9b3fe8-0616-40ee-a93e-b96b5dce460f)

*图表 1：2019 年 ASF 安全电子邮件主题细分*

图 1 给出了这 620 个主题的细分。138个主题（22%）是 Apache 许可证使用困惑相关的问题。由于许多项目使用 Apache 许可证，而不仅仅是 ASF 保护伞下的项目，因此当用户看到 Apache 许可证并且他们不了解它是什么时，他们可能会感到困惑。这在手机上最常见，例如在设置菜单中显示许可证的手机上，通常是由于包含 Google 根据 Apache 许可证发布的软件。

接下来 620 个（26%）中，162个是电子邮件主题，它们不是垃圾邮件，但也不是新漏洞的报告。这些人通常会询问支持类型的问题或如何处理旧的漏洞。

剩下的 320 份关于 2019 年新漏洞的报告，这些报告涵盖了 84 个顶级项目。这 320 份报告是外部报告者和内部报告者的混合体;例如，如果项目自己发现了问题，并按照 ASF 流程为其分配了 CVE 名称并解决了它。请注意，我们不跟踪报告者隶属关系，并且 ASF 报告者经常使用非 ASF 电子邮件地址进行报告，因此我们不会对内部报告与外部报告进行细分。

下一步是相应的项目对报表进行分类，以查看它是否确实是一个问题。在此阶段，无效报告或实际上根本不是漏洞的内容会被拒绝返回给报告者。在接受的其余问题中，它们被分配了适当的 CVE 名称，并最终发布了修复程序。

截至 2020 年 1 月 1 日，这 320 份报告中有 19 份仍在分类中（即项目尚未确定该报告是被接受还是被拒绝）。分类和调查的过程在时间上有所不同，具体取决于项目、资源的可用性和要评估的问题数量。作为一般准则，我们努力确保项目在报告后的 90 天内对问题进行分类。解决问题的时间表取决于项目本身的时间表，而严重程度较低的问题通常保留到将来预先计划的版本中。

其余已关闭的 301 报告导致我们分配了 122 个 CVE 名称。某些漏洞报告可能包含多个问题，某些报告跨多个项目，并且某些报告是重复的，其中不同的报告者发现了相同的问题，因此所接受的报告与 CVE 名称之间并没有一个精确的一对一的映射。Apache 安全委员会负责处理 CVE 名称分配，并且是 Mitre 候选命名机构 （CNA），因此任何 ASF 项目中对 CVE 名称的所有请求都将通过我们来处理，即使报告者不知道，并直接与 Mitre 联系或在联系我们之前公开提出问题。

## 值得注意的事件

在2019年期间，有一些事件值得讨论;要么是因为它们是严重和高风险的，要么因为它们有现成的漏洞，要么是由于媒体的关注。其中包括：

2019 年 1 月：Securonix [发布了一份报告](https://www.securonix.com/resources/securonix-threat-research-detecting-persistent-cloud-infrastructure-hadoop-yarn-attacks-using-security-analytics-moanacroner-xbash/)，概述了尚未配置身份验证的 Apache Hadoop 实例的攻击增加。公共漏洞和Metasploit模块的存在是为了在未受保护的Hadoop YARN系统上执行远程代码执行。

2019 年 4 月：Apache HTTP Server 2.4 中的一个漏洞 （[CVE-2019-0211](https://httpd.apache.org/security/vulnerabilities_24.html#CVE-2019-0211)）。有权在 Web 服务器上编写脚本的用户可以将这些权限提升为 root。此问题有一个公共漏洞利用。

2019 年 4 月：旧版 Apache Axis 中的一个漏洞，该漏洞解析了[从过期域中不安全检索到的文件](https://rhinosecuritylabs.com/application-security/cve-2019-0227-expired-domain-rce-apache-axis/)，从而允许远程执行代码（CVE-2019-0227）。

2019 年 6 月：Jonathan Leitschuh 在发现许多 Java [构建依赖项通过不安全的路径](https://twitter.com/JLLeitschuh/status/1138116614623244288)（即 HTTP 而不是 HTTPS）下载后与我们联系。我们本身没有将这些漏洞归类为安全漏洞，因为利用它们需要在构建时进行MITM攻击。我们与ASF项目合作，包括报告者确定的项目，以确保我们使用安全的URL。现在，在2020年，许多存储库需要安全URL。

2019 年 8 月：Black Duck Synopsys 团队审查了较旧的 Struts 版本和公告，发现报告的受影响版本中存在一些差异。Struts团队仔细研究了他们的发现，并在需要时[发布了更正](https://cwiki.apache.org/confluence/display/WW/S2-058)。如果用户运行的是旧版本，而他们认为这些版本不受基于公告的问题的影响，但实际上确实如此，则这可能很重要。但是，这些相同的用户可能容易受到已修复的其他问题的影响，因此我们始终建议用户升级到最新版本的 Struts，以确保他们拥有的版本包含所有已发布的安全问题的修补程序。

2019 年 8 月：Netflix 发现了许多影响各种 HTTP/2 实现的拒绝服务漏洞。对包含 HTTP/2 实现的 ASF 项目进行了调查，并分析了报告的问题。Apache HTTP Server和Apache TrafficServer都[发布了](https://httpd.apache.org/security/vulnerabilities_24.html#CVE-2019-9517)[更新](https://lists.apache.org/thread/sv7wjbqsfcb7c2jm4ndxxls6j7lk63fr)，以解决影响它们的拒绝服务问题。Apache Tomcat还对HTTP / 2处理进行了性能改进，但这些问题[未被归类为拒绝服务](https://lists.apache.org/thread/shfnf6c86z82z2k5lgn934hy88rdp46o)。

2019 年 9 月：[RiskSense 报告](https://www.ivanti.com/lp/security/assets/s2/enterprise-ransomware-through-the-lens-of-threat-and-vulnerability-management?rsredirect=)强调了已知被勒索软件使用的漏洞，其中包括 ASF 项目中的四个漏洞。这四个漏洞在前几年都已修复，并且在任何勒索软件利用它们之前都有可用的更新和缓解措施。用户应始终确保他们关注他们使用的任何 ASF 项目中的安全更新，并优先针对任何远程或关键漏洞进行更新。这四个漏洞是：

- Apache ActiveMQ中的CVE-2016-3088。以 [XBash](http://blog.nsfocusglobal.com/threats/vulnerability-analysis/xbash-malware-security-advisory/) 的目标，这个问题很容易被利用。它在 Active MQ 5.14.0 中已修复，并且还提供了缓解措施。

- Apache Tomcat 中的 CVE-2017-12615。在列表中看到此问题令人惊讶，因为它会影响非默认且不太可能出现的缺陷。但是，这是 Lucky（“Satan”的变体）探讨的一个问题，因此如果有一个以这种方式配置的服务器，它将被暴露。此问题仅影响非默认配置的 Windows 平台，已在 Tomcat 7.0.81 中修复，并且还提供了缓解措施。请注意，Lucky 还将针对可访问的 Tomcat Web 管理控制台上的弱密码进行暴力攻击。

- CVE-2017-5638在Apache Struts中。已知此问题[在没有被人为的控制的情况被利用](https://blog.talosintelligence.com/2017/03/apache-0-day-exploited.html)，但是在发布咨询和修复后发现了第一个利用。由[ Lucky（“Satan”的变体）使用](https://blog.talosintelligence.com/2017/03/apache-0-day-exploited.html)。它在 Struts 2.3.32 和 2.5.10.1 中已修复，并且还提供了缓解措施。

- CVE-2018-11776在Apache Struts中。Lucky 也使用过这个问题。它在Struts 2.3.35，2.5.17中已修复，可以使用可能的缓解措施，但建议进行升级。

2019 年 12 月：Apache Olingo 中存在一个允许 XML 外部实体 （XXE） 攻击的漏洞 （[CVE-2019-17554](https://lists.apache.org/thread/lkpr8f4bgydjxx4dy5m8cxwshyxgylc5)）。例如，此问题可用于从服务器检索任意文件。此问题存在一个公共漏洞利用示例。

Apache Solr在这一年中存在许多缺陷，这些缺陷可能允许远程代码执行以及 Metasploit 模块存在公共漏洞。

欧盟委员会EU-FOSSA 2项目赞助了漏洞赏金计划，供用户在 Apache Kafka 和 Apache Tomcat 中发现安全问题。Apache Kafka 中没有修复任何问题。Apache Tomcat 中修复了两个问题：[CVE-2019-0232](https://tomcat.apache.org/security-9.html#CVE-2019-0232)（严重性高，影响 Windows 平台，公开漏洞（包括 Metasploit 模块可用）和 [CVE-2019-0221](https://tomcat.apache.org/security-9.html#CVE-2019-0221)（严重性低）。除了运行漏洞赏金外，EU-FOSSA 2还在 2019 年 6 月[赞助了一次成功的黑客马拉松](https://joinup.ec.europa.eu/collection/eu-fossa-2/news/eu-fossa-2-apache-hackathon)。

# 结论

Apache软件基金会的项目是高度多样化和独立的。它们具有不同的语言、社区、管理和安全模型。但是，每个项目的共同点之一是如何处理报告的安全问题的一致过程。

ASF 安全委员会与项目团队、社区和报告者密切合作，确保问题得到快速、正确的处理。这种负责任的监督是 The Apache Way 的一项原则，有助于确保Apache软件的稳定性和可信赖性。

该报告提供了 2019 年的指标，显示了我们从收到的 18，000 封电子邮件中分类了 300 多个漏洞报告，从而修复了 100 多个（CVE）问题。如果您有想要分享的漏洞信息或对此报告的评论，[请与我们联系](http://apache.org/security/#reporting-a-vulnerability)。
