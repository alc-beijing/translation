# 标题：在 ASF 版本中使用密码学技术

- [标题：在 ASF 版本中使用密码学技术](#标题在-asf-版本中使用密码学技术)
  - [本页面更新通知&para;](#本页面更新通知)
  - [总览&para;](#总览)
    - [检查出口管控分类编号（ECCN）&para;](#检查出口管控分类编号eccn)
    - [使用源码链接更新导出页&para;](#使用源码链接更新导出页)
    - [将新的发行版代码知照美国政府&para;](#将新的发行版代码知照美国政府)
    - [在 REMDME 文件里包含密码学技术提示以通知用户&para;](#在-remdme-文件里包含密码学技术提示以通知用户)
  - [常见问题&para;](#常见问题)

该页面为 PMC 成员提供了必备信息，以确保使用了密码学技术的 ASF 产品分发满足美国出口管控相关法律的要求。这些分发可能是一开始就被设计使用密码学技术，也可能是后来被修改以使用密码学技术来实现数据保密。

**此页面不适用于 Apache 产品的用户**。用户应咨询[我们产品的出口管控现状](https://www.apache.org/licenses/exports/)。

**注意**：由于美国加密软件相关的出口管控相关法律条款可能不定期更新，因而特此注明本页最后修改时间（即当前描述的法律适用时间）为：2019 年 5 月 24 日。

该页面描述了那些在`ASF 法务副总裁（ASF VP Legal Affairs）`批准更新版本之前必须完成的步骤。

## 本页面更新通知[&para;](#本页面更新通知 '永久链接')

本页面的更新通知显示在[法律讨论（legal-discuss）](https://www.apache.org/foundation/mailinglists.html#foundation-legal)邮件列表上。

## 总览[&para;](#总览 '永久链接')

美国政府对某些类型的软件产品设置了[出口限制](https://www.bis.doc.gov/index.php/regulations/commerce-control-list-ccl)，
其中包括采用了密码学技术的软件。幸运的是，出口管控条例（EAR）第 7​​42.15（b）条款适用于 ASF 所关注的大多数密码学技术。

考虑将密码学功能包含在其产品中或者设计其产品以使用具有密码功能的其他软件的 PMC，请在将此类代码放置在任何 ASF 服务器上（包括提交`subversion`或者`git`）**之前**采取以下步骤：

- 检查出口管控分类编号（ECCN）
- 使用源码链接更新导出页
- 将新的发行版代码知照美国政府
- 在 REMDME 文件里包含密码学技术提示以通知用户

### 检查出口管控分类编号（ECCN）[&para;](#检查出口管控分类编号eccn '永久链接')

[出口管控条例（EAR）](https://www.trade.gov/us-export-regulations)第 742.15（b）条款授权：加密软件源码和目标代码在满足以下条件的情况下，可不经二次审查进行出口或者再出口：

- 加密软件源码已由 ECCN 5D002 管控。
- 加密软件源码将公开可用（已发布并公开可用，同时不限制传播）。
- 在加密软件源码公开可用前，已知照美国政府工业与安全局（BIS）和 ENC 加密请求协调局（现行的 ASF 流程已满足“公开可用”的要求）。其中知照的具体要求见[下文](#将最新版本代码知照美国政府)。而重要的是确保所包含的密码学功能符合[ECCN D002 规范](https://cr.yp.to/export/ear2001/ccl5-pt2.pdf)，概要如下：
  - 为开发，生产或使用此列表中的任何其他软件而专门设计或修改的软件，或旨在对该列表中的其他软件进行认证的软件；或者
  - 使用“对称算法”且密钥长度超过 56 位的软件；或者
  - 使用“非对称算法”的软件，其中算法的安全性基于：分解超过 512 位的整数（例如 RSA），计算大小大于 512 位的有限域的乘法组中的离散对数（例如，基于有限循环群`Z/pZ`的 Diffie-Hellman 算法）或超过 112 位的组中的其他离散对数（例如，基于椭圆曲线的 Diffie-Hellman 算法）。
  - 为执行密码分析功能而设计或修改的软件。

若软件的密码学功能仅限于上述定义之一，应将其分类为 ECCN 5D002，并应采取剩余两个步骤（如下所述）。如果该发行版可能包含上述功能之外的加密功能，请联系[ASF 法务副总裁（ASF Vice President for Legal Affairs）](/foundation/)。

### 使用源码链接更新导出页[&para;](#使用源码链接更新导出页 '永久链接')

为了满足 BIS 的要求，使源代码可用于检查，同时最大程度地减少需要发送的[通知电子邮件](#将新的发行版代码知照美国政府)的数量，ASF 维护了 ASF 产品中的所有分类为 ECCN 5D002 的版本的源代码链接————[ASF 产品导出页](https://www.apache.org/licenses/exports/)。

为了使得此 ASF 产品导出页的更新尽可能简单且一致，用来生成导出页的[源 XML 文件](https://svn.apache.org/repos/asf/infrastructure/site/trunk/content/licenses/exports/index.page/eccnmatrix.xml)在`eccnmatrix`节点下包含了一棵 XML 树，并可以由具有`site-dev karma`相关权限的任何人（这其中包括所有 PMC 主席）进行编辑。

对导出页的所有修改均应使用网站构建过程（在提交任何改变前请查看`index.html`）和通过对添加/更改的产品运行`bisnotice.xsl`转换（请参见下文）进行测试。您可以通过遵循其他项目的示例并阅读页面来弄清楚 XML 字段应该包括什么内容。如果您对内容有任何其他疑问，或者不确定是否属于 BIS 知照要求范围，请先查看[常见问题列表](#常见问题)；若依然存疑，欢迎将问题带到`法律讨论（legal-discuss）`邮件列表中。请注意，仅当分类更改（例如，Apache HTTP Server 版本 1.3 与 2.0）或需要更改指向受控源代码的链接（例如，产品中包含的加密库用于以下用途）时，产品数据才应特定于版本来自不同制造商的不同版本。另外，可以在列表中同时包含受控产品和非受控产品（ECCN“ n / a”），但是 BIS 通知仅对于具有至少一个分类为 ECCN 5D002 的版本的产品是必需的。

### 将新的发行版代码知照美国政府[&para;](#将新的发行版代码知照美国政府 '永久链接')

在确保发行版的密码学技术符合第 742.15（b）条的豁免规定，并确保将可使用的源码链接置于 ASF 产品导出页后，请于**公开发布或公开提交受控代码之前**，使用以下模板发送电子邮件。

XSLT 转换器[bisnotice.xsl](https://svn.apache.org/repos/asf/infrastructure/site/trunk/content/licenses/exports/bisnotice.xsl)可以基于 XML 数据为产品生成 BIS 知照内容。以下是脚本示例（脚本文件应位于 site/trunk 的顶级目录；若`Windows`系统可命名为`bisnotice.cmd`，若`(Un\*x)`系统则命名为`bisnotice.sh`）:

```shell
$ cd {SVNROOT}/infrastructure/site/trunk/</li>
$ svn up</li>
$ cd content/licenses/exports/</li>
$ java -Xbootclasspath/p:../../../lib/xalan.jar org.apache.xalan.xslt.Process \
          -in index.page/eccnmatrix.xml -xsl bisnotice.xsl \
          -param product 'Apache HTTP Server'
```

以上操作将输出一个电子邮件纯文本模版，内容是以 PMC 主席的身份发送到政府知照指定地址的电子邮件。下面是一个通用示例。请注意，其中`-param product`参数将通过匹配产品名字符串的子串来选择要打印的产品；仅当匹配结果唯一时，模板才能输出正确。

```text
TO: crypt AT bis.doc.gov,
       enc AT nsa.gov,
       web_site AT bis.doc.gov
CC: {applicable project list}
SUBJ: Section 742.15 NOTIFICATION - Encryption</p>

SUBMISSION TYPE:      Section 742.15
SUBMITTED BY:         {PMC member sending email}
SUBMITTED FOR:        Apache Software Foundation
POINT OF CONTACT:     Secretary, Apache Software Foundation
MANUFACTURER(S)       {list of origin of all crypto code, e.g.
                         "OpenSSL Project" or "Apache Software Foundation."
                         If product includes multiple crypto items from
                         different origins, list all origins.}
PRODUCT NAME/MODEL #: {Apache product name(s) that include the source
                          code found at the URL below, or any binaries
                          that were created by compiling that source code
                          -- do not specify version numbers if the
                          future versions will use source code found at
                          the same URL (even if the source is updated at
                          that URL) }
<p>ECCN:                 5D002
NOTIFICATION:         http://www.apache.org/licenses/exports/
```

### 在 REMDME 文件里包含密码学技术提示以通知用户[&para;](#在REMDME文件里包含密码学技术提示以通知用户 '永久链接')

Should the software qualify for the Section 742.15(b) exemption, place the following notice into each distribution's README file:

```
   This distribution includes cryptographic software.  The country in
   which you currently reside may have restrictions on the import,
   possession, use, and/or re-export to another country, of
   encryption software. BEFORE using any encryption software, please
   check your country's laws, regulations and policies concerning the
   import, possession, or use, and re-export of encryption software, to
   see if this is permitted. See http://www.wassenaar.org for
   more information.
The Apache Software Foundation has classified this software as Export Commodity
   Control Number (ECCN) 5D002, which includes information security
   software using or performing cryptographic functions with asymmetric
   algorithms. The form and manner of this Apache Software Foundation
   distribution makes it eligible for export under the "publicly available"
   Section 742.15(b) exemption (see the BIS Export Administration Regulations,
   Section 742.15(b)) for both object code and source code.
The following provides more details on the included cryptographic
   software:
```

Be sure to add some information at the bottom of the notice about the components of the release including cryptography.

## 常见问题[&para;](#常见问题 '永久链接')

<h4 id="faq-productname">What is the "PRODUCT NAME/MODEL #" for my product?<a class="headerlink" href="#faq-productname" title="Permanent link">&para;</a></h4>

The product name is the name of the ASF product (e.g. "Apache Foo"), even if the notification is being made about another manufacturer's cryptography included in the ASF product. Do not list the ASF product's version number.

<h4 id="faq-manufacturer">What is the MANUFACTURER?<a class="headerlink" href="#faq-manufacturer" title="Permanent link">&para;</a></h4>The manufacture is the name of the individual/organization that built the crypto item included in the ASF product, whether that is the ASF itself or some other open source project or organization.

<h4 id="faq-notification">What is the NOTIFICATION?<a class="headerlink" href="#faq-notification" title="Permanent link">&para;</a></h4>

the notification is a URL that directly or indirectly points to the source code for the crypto item built by the listed <a href="#faq-manufacturer">manufacturer</a> that is
distributed within the ASF <a href="#faq-productname">product</a>. At the ASF, we indirectly point to the source code by having all products list `www.apache.org/licenses/exports/` as the NOTIFICATION url, and ensuring that this page is refreshed with the set of links to the crypto source code for the notifying product. If the product contains more than one crypto item, the exports page simply points to the source for each crypto item included in the product.

<h4 id="faq-firstnotification">When is the first time a notification email must be sent?<a class="headerlink" href="#faq-firstnotification" title="Permanent link">&para;</a></h4>

You must send the notification email prior to exporting/posting online. **Note**: this even includes distribution of code through publicly accessible servers/repositories before there has been any official release.

<h4 id="faq-public">What are examples of when a crypto item is publicly accessible through ASF servers?<a class="headerlink" href="#faq-public" title="Permanent link">&para;</a></h4>

The **obvious example** is including something like an OpenSSL binary within a product distribution from a /dist URL. The **less-obvious example** is the point at which a software repository starts to include code that is specially designed to work with any other 5D002 item, whether that item is ever to be included within a product distribution or not. In other words, a project should send out a notification email just after making the decision to include code that is specially designed to work with crypto APIs but
before actually committing such code. No need to worry about surprise Jira attachments with such code -- only the event of committing the code to the ASF product repository.

<h4 id="faq-publicemails">Are public contributions of crypto items to the mailing list, Jira or Bugzilla databases considered exports?<a class="headerlink" href="#faq-publicemails" title="Permanent link">&para;</a></h4>

No. We do not need to worry about surprise Jira attachments with such code -- only code committed to the ASF product repository. The actual poster of these attachments would be the one 'exporting' the crypto, since it would not be an act of the ASF project as it addressed <a href="#faq-public">above</a>.

<h4 id="faq-previouslyexported">If we distribute previously exported crypto items, must we still qualify the same item for export?<a class="headerlink" href="#faq-previouslyexported" title="Permanent link">&para;</a></h4>

Yes. The ASF is responsible for complying with the EAR, regardless of whether the item we are exporting has been previously exported under the Section 742.15(b) publicly available exemption or any license exception by another manufacturer/company/open source project.

<h4 id="faq-manyproducts">If the ASF distributes a particular crypto item within one product under the Section 742.15(b) publicly available exemption, must the same item requalify when distributed in a different ASF product?<a class="headerlink" href="#faq-manyproducts" title="Permanent link">&para;</a></h4>

Yes. Each product must qualify separately, which includes sending notifications for each.

<h4 id="faq-versions">If the ASF distributes/exports a crypto item after qualifying it under the Section 742.15(b) publicly available exemption, must the same product requalify for release of future versions?<a class="headerlink" href="#faq-versions" title="Permanent link">&para;</a></h4>

No. As long as the email's notification URL for the source location still (directly or indirectly) points to the applicable source for each version's crypto item, no additional process is required.

<h4 id="faq-notificationurl">Where must the email's notification URL point to?<a class="headerlink" href="#faq-notificationurl" title="Permanent link">&para;</a></h4>

The notification URL for all products should point to `https://www.apache.org/licenses/exports/`, which should be refreshed to include the project's cryptography data
before the email is sent.

<h4 id="faq-additionalemails">If the notification URL never changes, when are additional notification emails required?<a class="headerlink" href="#faq-additionalemails" title="Permanent link">&para;</a></h4>

Each product needs to send only one notification email until information previously submitted is no longer accurate, e.g. a change in the manufacturer.

<h4 id="faq-infousers">Is there any BIS requirement to tell users and/or redistributors of our products about the crypto within our products?<a class="headerlink" href="#faq-infousers" title="Permanent link">&para;</a></h4>

No, but it's a good idea to do so. See our self-imposed requirement to <a href="#inform">inform users</a>.

<h4 id="faq-twocryptos">When exporting a product that is not only designed to use some third-party crypto item, but also includes the third-party crypto item, does this require two notifications or one notification with two manufacturers?<a class="headerlink" href="#faq-twocryptos" title="Permanent link">&para;</a></h4>

When multiple crypto items exist within a single product, one email should be sent listing all manufacturers of encryption items in the product and the <a href="/licenses/exports/">standard notification URL</a> to the ASF-wide exports page with detailed information, including the location of the corresponding source code.

<h4 id="faq-nonasfsource">Can the ultimate link to the crypto item's source code point to a non-ASF web page?<a class="headerlink" href="#faq-nonasfsource" title="Permanent link">&para;</a></h4>

Yes, as long as the PMC is reasonably confident that the non-ASF location is likely to remain available for BIS inspection for the foreseeable future. If this is not the case at some point, the ASF should update the link to a location that will remain available.

<h4 id="faq-compilerswitch">What if the object/binary code being distributed was built with a particular compiler switch?<a class="headerlink" href="#faq-compilerswitch" title="Permanent link">&para;</a></h4>

It is fine to use whatever compiler switches you like. There is no need to provide compiler switch information, as long as the pointed source code is a superset of all the controlled source that ends up being distributed within the object/binary file.

<h4 id="faq-binaryurl">Do we need to notify the BIS of the location of object/binary files?<a class="headerlink" href="#faq-binaryurl" title="Permanent link">&para;</a></h4>

No, but whether we are distributing source or object/binary files, we must always make sure a notification has been made pointing (directly or indirectly) to the associated source.

<h4 id="faq-includedlibssl">If my project ships a binary that includes libssl/libcrypto, what notifications must be made?<a class="headerlink" href="#faq-includedlibssl" title="Permanent link">&para;</a></h4>

Within the single notification email (**sent prior to either hosting libssl/libcrypto or committing code that binds to it**), the ASF and the OpenSSL project should be listed as manufacturers, since both organizations produce encryption items included in the product. See the more generic <a href="#faq-twocryptos">Q&amp;A on this topic.</a>

<h4 id="faq-linkedtolibssl">If my project ships a binary that provides bindings to OpenSSL, but does not include its source or binaries, what notifications must be made?<a class="headerlink" href="#faq-linkedtolibssl" title="Permanent link">&para;</a></h4>

The only required notification for an Apache project that is specially designed to use, but doesn't include, such crypto, is the notification for the ASF product code.

<h4 id="faq-nonamerican">Why should I, who am not a U.S. citizen nor resident, be constrained by some U.S. law?<a class="headerlink" href="#faq-nonamerican" title="Permanent link">&para;</a></h4>

The ASF is a U.S.-based corporation and must comply with U.S. export controls. Incidentally, the U.S. is not the only country with controls on cryptography. Many other nations have similar restrictions, primarily driven by the <a href="https://www.wassenaar.org" target="_blank"> Wassenaar Arrangement</a>.

<h4 id="faq-digest">Do digest algorithms such as MD5 and SHA1 require notification?<a class="headerlink" href="#faq-digest" title="Permanent link">&para;</a></h4>
No. One-way algorithms such as MD5 or SHA1, or more sophisticated implementations, do not require notification. Only encryption algorithms do.