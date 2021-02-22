###
原文地址：https://www.apache.org/legal/resolved.html

## 译文版

- [目的](#目的)

    - [许可标准](#许可标准)
    
    - [高层次](#高层次)
    
- [A 类：我们可以把什么写进 ASF 项目中？](#a-类我们可以把什么写进-asf-项目中)

    - [处理公共领域“授权”的作品](#处理公共领域授权的作品)
    
- [B 类：我们可能把什么写进 ASF 项目中？](#b-类我们可能把什么写进-asf-项目中)

    - [适当标记的条件](#适当标记的条件)
    
    - [仅二进制包含条件](#仅二进制包含条件)
    
    - [“较低的公共版权”许可证](#较低的公共版权许可证)
    
    - [包括知识共享署名内容](#包括知识共享署名内容)
    
    - [知识共享署名-相同方式共享许可未经修改的媒体](#知识共享署名-相同方式共享许可未经修改的媒体)
    
    - [我可以从 Stack Overflow 复制代码并将其贡献给 ASF 项目吗？](#我可以从-stack-overflow-复制代码并将其贡献给-asf-项目吗)
    
    - [Doug Lea 的并发库](#doug-lea-的并发库)
    
    - [将 OSGi 元数据添加到较低的公共版权二进制文件中](#将-osgi-元数据添加到较低的公共版权二进制文件中)
    
    - [Cobertura 报告](#Cobertura-报告)
    
    - [处理禁止修改的许可证](#处理禁止修改的许可证)
    
    - [在 ASF 项目中包含构建工具](#在-ASF-项目中包含构建工具)
    
    - [创建动态加载的 XS 模块时包含 Perl 许可的头文件](#创建动态加载的-XS-模块时包含-Perl-许可的头文件)
    
    - [包括 Doxygen 生成的配置文件](#包括-Doxygen-生成的配置文件)
    
    - [Apache 项目可以对 Ruby 许可的作品具有外部依赖性吗？](#Apache-项目可以对-ruby-许可的作品具有外部依赖性吗)
    
- [X 类：我们不能把什么写在 ASF 项目中？](#X-类我们不能把什么写在-ASF-项目中)

    - [可能没有被分发的东西](#可能没有被分发的东西)
    
    - [当支持一个可选的特性时，可能会被依赖的东西](#当支持一个可选的特性时可能会被依赖的东西)

- [常见问题与解答](#常见问题与解答)：

   - [创建 Apache 项目用于什么平台有关系吗？](#创建-Apache-项目用于什么平台有关系吗)
   
   - [如果可以选择许可，我应该如何处理作品？](#如果可以选择许可我应该如何处理作品)
   
   - [是否需要对库依赖进行 IP 清除？](#是否需要对库依赖进行-IP-清除)
   
   - [需要哪些第三方通知？](#需要哪些第三方通知)
    
## 目的
    
该政策为 Apache 软件基金会项目提供了许可指南。它确定了在 Apache 软件基金会项目中包含第三方开放源代码组件的可接受许可。

如果他们有许可证问题，产品会被要求向法律事务委员会 JIRA 空间提交问题。

#### 许可标准

以下标准作为本页类别的指南。

- 1、许可证必须符合[开源定义](https://opensource.org/osd-annotated)₁。

- 2、在实践中应用的许可证不得施加超出 Apache 许可证2.0所规定的重要限制。

₁.（审阅日期：2019-02-16）

#### 高层次

在较高层次上，此政策将许可证分为三类。

   - **A 类**：A 类许可证可能包含在 Apache 软件基金会项目中。据说他们是“Apache 式的”。

   - **B 类**：在某些条件下，B 类中的许可证可能包含在 Apache 软件基金会项目中。它们“可能”包含在内。

   - **X 类**：X 类中的许可证可能**不**包含在 Apache 软件基金会项目中。

## A 类：我们可以把什么写进 ASF 项目中？

为了成为 Apache 软件基金会项目的一部分，以下许可证在条款上应该与Apache 许可证2.0相似。：

   - [Apache 许可证2.0](http://apache.org/licenses/LICENSE-2.0)
    
   - [Apache 软件许可证1.1](http://apache.org/licenses/LICENSE-1.1)，包括变体：
   
       - [PHP 许可证3.01](http://www.php.net/license/3_01.txt)
       
       - [MX4J 许可证](http://mx4j.sourceforge.net/docs/ch01s06.html)
       
   - BSD（无广告条款）。包括变体：
   
       - [BSD 2-条款](http://opensource.org/licenses/bsd-license.php)
       
       - [BSD 3-条款](https://opensource.org/licenses/BSD-3-Clause)
       
       - [DOM4J 许可证](http://dom4j.sourceforge.net/dom4j-1.6.1/license.html)
       
       - [PostgreSQL 许可证](https://opensource.org/licenses/postgresql)
       
       - [Eclipse 发行许可证1.0](http://www.eclipse.org/org/documents/edl-v10.php)
   
   - [MIT / X11](https://opensource.org/licenses/mit-license.php)
   
       - [ISC](https://opensource.org/licenses/ISC)
       
       - [新泽西州标准 ML](https://www.smlnj.org/license.html)
       
       - [杯形语法分析器产生程序](http://www2.cs.tum.edu/projects/cup/licence.php)
       
   - [ICU](http://source.icu-project.org/repos/icu/icu/trunk/LICENSE)
       
   - [伊利诺伊大学/ NCSA](https://opensource.org/licenses/UoI-NCSA.php)
       
   - [W3C 软件许可](https://opensource.org/licenses/W3C.php)
       
   - [W3C 社区贡献者许可协议](https://www.w3.org/community/about/agreements/cla/)-如果发布,至少45天之后
       
   - [X.Net](https://opensource.org/licenses/xnet.php)
       
   - [zlib/libpng](https://opensource.org/licenses/zlib-license.php)
       
   - FSF Autoconf 许可证
       
   - [DejaVu 字体（Bitstream Vera / Arev 许可）](https://dejavu-fonts.org/)
       
   - [学术免费许可证3.0](https://opensource.org/licenses/afl-3.0.php)
       
   - [服务+组件+建筑+规格](http://web.archive.org/web/20080704184203/http://www.osoa.org/xmlns/sca/1.0/license.txt)
       
   - OOXML XSD ECMA 许可证
       
   - [Microsoft 公共许可证（MsPL）](https://opensource.org/licenses/ms-pl.html)
       
   - [知识共享组织仅限于版权贡献](https://creativecommons.org/licenses/publicdomain/deed.zh)
       
   - [Python 软件基金会许可证](http://www.opensource.org/licenses/PythonSoftFoundation.php)
       
   - [Python Imaging Library 软件许可](https://github.com/python-pillow/Pillow/blob/master/LICENSE)
       
   - [Adobe Postcript（R）AFM 文件](https://spdx.org/licenses/APAFML.html)
       
   - [Boost 软件许可版本1.0](https://opensource.org/licenses/BSL-1.0)
       
   - [COLT 中 CERN 软件包的许可](https://dst.lbl.gov/ACSSoftware/colt/license.html)，但请注意，这**仅**适用于COLT中的CERN软件包，**不**适用于其他
       
   - [英国开放政府许可证](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)。该许可允许许可方提供自定义归属通知。如有，请在NOTICE中注明。如果没有提供，那么在NOTICE上注明“包含根据开放政府许可证v3.0许可的公共部门信息”。
       
   - [WTF 公共许可证](http://www.wtfpl.net/)
       
   - [浪漫 WTF 公共许可证](https://github.com/pygy/gosub/blob/master/LICENSE)
       
   - [UNICODE 公司许可协议-数据文件和软件](http://www.unicode.org/copyright.html#Exhibit1)
       
   - [Zope 公共许可证2.0](https://opensource.org/licenses/ZPL-2.0)
       
   - [ACE 许可证](http://www.cs.wustl.edu/~schmidt/ACE-copying.html)
       
   - [Oracle 通用许可许可证（UPL）1.0版](https://oss.oracle.com/licenses/upl/)
       
   - [开放网格论坛许可证](https://www.ogf.org/ogf/doku.php/about/copyright)
       
   - [谷歌“附加知识产权授权(专利)”](https://chromium.googlesource.com/external/webrtc/+/master/PATENTS)
       
   - [非授权许可证](https://chromium.googlesource.com/external/webrtc/+/master/PATENTS)
       
   - [历史许可声明和免责声明](https://opensource.org/licenses/HPND)
       
   - [木兰宽松许可证, 第2版](https://license.coscl.org.cn/MulanPSL2/)
       
其中许多许可证都有特定的归属条款需要去遵守，通常是将其[包含到 NOTICE 文件中](https://www.apache.org/dev/licensing-howto.html)。当收录这些作品时，请确保您正在执行此操作。     
   
#### 处理公共领域“授权”的作品

Apache 项目中可能包含公共领域的作品（或受到类似处理的许可所涵盖的作品）。必须提供出处（与“A 类”列表类似）。

符合以下条件之一的作品应被视为属于公共领域：

  - 作品涵盖
  
    - 知识共享[公共领域标识](https://creativecommons.org/publicdomain/mark/1.0/deed.zh)，或
    
    - 作者(对公共领域)的适当奉献;或
    
  - 有明确的证据表明美国拥有该作品的版权
  
    - 已经过期，或
    
    - 无法被认领。
   
应被视为类似于公共领域的许可证：

  - 知识共享 [CC0 “不保留任何权利”](https://creativecommons.org/about/cc0)
  
  - 知识共享[公共领域认证](https://creativecommons.org/licenses/publicdomain/)
  
**要注意的是**判断作品是否属于公共领域可能是一件[困难](http://fairuse.stanford.edu/Copyright_and_Fair_Use_Overview/chapter8/)的事情。确定一部作品的版权是否已经过期似乎是非常重要的，而且在不同的司法管辖区可能会有所不同。如果你对某件作品是否属于公共领域有疑问，可以通过“法律讨论”或“JIRA 问题”提出这个话题。

## B 类：我们可能把什么写进 ASF 项目中？

为了成为 Apache 软件基金会项目的一部分，**如果**满足指定条件，则可以涵盖本节中描述的许可和/或项目。

#### 适当标记的条件

所有 B 类案件，我们的用户都不应该对其被纳入我们的项目感到惊讶。通过给发行版添加适当且突出的标签，用户就可能知道与 Apache 许可证显著不同的限制。一个合适且突出的标签是用户在了解发行版时将阅读的标签——例如在自述文件中，它应该能识别第三方产品、其授权，以及到其主页的 url。同时，请确保遵守相关许可证中的任何归属/通知要求。

#### 仅二进制包含条件

除非另有说明，否则所有 B 类许可的作品都应以纯二进制形式包括在 Apache 软件基金会项目便利二进制文件中（而不是源代码）。

#### “较低的公共版权”许可证

本节中的每个许可证都需要一定程度的对等。这可能意味着需要采取额外的措施，以最大程度地减少 Apache 项目用户在不了解适用要求的情况下创建 Apache 项目不同许可部分的衍生作品的机会。

如果包含的软件有适当的标签，则以下许可协议中的软件可以以二进制形式包含在 Apache 项目中（见上文）：

  - 通用开发和发行许可证：[CDDL 1.0](https://opensource.org/licenses/CDDL-1.0)和[CDDL 1.1](https://spdx.org/licenses/CDDL-1.1.html)
  
  - 通用公共许可证：[CPL 1.0](https://opensource.org/licenses/cpl1.0.php)
  
  - Eclipse 公共许可证：[EPL 1.0](http://www.eclipse.org/legal/epl-v10.html)
  
  - IBM 公共许可证：[IPL 1.0](http://www.opensource.org/licenses/ibmpl.php)
  
  - Mozilla 公共许可证：[MPL 1.0](https://website-archive.mozilla.org/www.mozilla.org/mpl/mpl/1.0/)，[MPL 1.1](https://www.mozilla.org/en-US/MPL/1.1/)和[MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/)
  
  - Sun 公共许可证：[SPL 1.0](https://opensource.org/licenses/SPL-1.0)
  
  - [开放软件许可3.0](https://opensource.org/licenses/OSL-3.0)
  
  - [Erlang 公共许可证](https://www.erlang.org/EPLICENSE)
  
  - [UnRAR 许可证](https://github.com/jukka/java-unrar/blob/master/license.txt)（仅用于取消存档）
  
  - [SIL 开放字体许可](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL)
  
  - [Ubuntu 字体许可版本1.0](https://ubuntu.com/legal/font-licence)
  
  - [IPA 字体许可协议v1.0](https://fedoraproject.org/wiki/Licensing/IPAFontLicense)
  
  - [Ruby 许可证](https://www.ruby-lang.org/en/about/license.txt)（包括 GPLv2 是列出的替代[Ruby 1.9.2许可证](https://svn.ruby-lang.org/cgi-bin/viewvc.cgi/tags/v1_9_2_320/COPYING?view=markup)时的旧版本）
  
  - Eclipse 公共许可证2.0：[EPL 2.0](https://www.eclipse.org/legal/epl-2.0/)
  
通过仅包括对象/二进制形式，第三方作品的暴露表面积较少，因此可以衍生作品；这涉及本政策的第二个指导原则。

对于 ASF 项目在运行时以源代码形式直接消耗的少量源代码，并且该源代码未经修改且无论如何都不可能更改（例如，通过标准指定），也允许包含适当标记的源代码。这方面的一个例子是 web-facesconfig_1_0.dtd，jsr127：JavaServer Faces 规范要求其包含在内。

#### 包括知识共享署名内容

[知识共享署名（CC-BY）](https://creativecommons.org/licenses/by/4.0/deed.zh)许可证（2.5、3.0和4.0）下的作品包含与“有效技术措施”相关的术语，这可能会让用户感到意外。因此，其包含物应适当标记，且仅以二进制形式。

#### 知识共享署名-相同方式共享许可未经修改的媒体

Apache 项目中可能包含[知识共享署名相同方式共享2.5](https://creativecommons.org/licenses/by-sa/2.5/deed.zh)、[知识共享署名相同方式共享3.0](https://creativecommons.org/licenses/by-sa/3.0/deed.zh)[和知识共享署名相同方式共享4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.zh)的不可修改媒体，但可能需要修改 LICENSE/NOTICE/README。对于任何其他类型的 CC-SA 许可作品，请联系合法的 PMC。

注意，media 指的是我们文档中使用的二进制视觉/视频/音频元素。这并不意味着会包含在我们的源代码中。

#### 我可以从 Stack Overflow 复制代码并将其贡献给 ASF 项目吗？

不行，如果没有联系原始作者并获得他们的许可，就不能在 Apache 许可证2.0下的 Apache 项目中使用代码。

#### Doug Lea 的并发库

Doug Lea 的并发库是公共领域的，但是包含一些非公共领域的 Sun 文件。这可能包含在 ASF 项目中，就像上面的“较低的公共版权”列表一样。“如果适当地标记了包含内容，则它可以二进制形式包含在 Apache 项目中”。如果使用了源代码，请删除 Sun 授权给 Doug 的文件并将其视为 A 类（或从 [Harmony](http://svn.apache.org/repos/asf/harmony/standard/classlib/trunk/modules/concurrent/src/main/java/java/util/concurrent/) 获取文件）。

#### 将 OSGi 元数据添加到较低的公共版权二进制文件中

允许将 OSGi 元数据插入到“B 类”许可的 jar 中，前提是 jar 的突出标注中包含发生这种情况的注释。

#### Cobertura 报告

Cobertura 报告可能包含在 ASF 分发包中。

#### 处理禁止修改的许可证

有些许可证赋予了重新分发**未修改**副本的广泛权利。这些许可证不是开源的，但它们确实满足上述第二和第三条指导原则。

Apache 项目不得在版本控制或已发布的源代码包中包含此类许可证下的材料。但是，构建过程可以自动下载字体和标准化数据等非软件材料，并将它们包含在生成的二进制文件中。这种用法清楚地表明，这些依赖项不是项目开放源代码的一部分。

可如上所述使用以下许可证下的材料：

   - [PDF CJK 字体的 CMAP](https://www.adobe.com/devnet/font.html#pcfi)
   
   - JCR API jar（[日规范许可证](http://www.day.com/maven/jsr170/licenses/day-spec-license.htm)+[附加许可证](http://www.day.com/maven/jsr170/jars/LICENSE.txt)）
   
   - [WSDL（2004）模式文件许可证](https://issues.apache.org/jira/browse/LEGAL-385)

#### 在 ASF 项目中包含构建工具

许多语言已经开发了一个相关工具的生态系统，帮助构建分发的工件。虽然这些工具可能并不总是在其他兼容的许可证下可用，但特定的工具在用于特定目的时可以包含在 Apache 发行版中。

请注意，该工具不得影响产品源代码的许可。我们使用该工具来构建源代码也是它的典型用途。

迄今为止，以下工具已获准用于此类用途：

   - Autotools 系列产品，特别是：
        - [自动配置](http://www.gnu.org/software/autoconf/)
        - [自动制造](http://www.gnu.org/software/automake/)
        - [Libtool](http://www.gnu.org/software/libtool/)
        - [mkinstalldirs.sh](http://www.gnu.org/software/hello/manual/gettext/mkinstalldirs.html)
   - [OCamlMakefile](http://hg.ocaml.info/release/ocaml-make/)
        - [setup.rb](https://i.loveruby.net/en/projects/setup/)

#### 创建动态加载的 XS 模块时包含 Perl 许可的头文件

开发链接已编译的 C 代码以创建动态加载的 XS 模块的 Perl 绑定，需要包括获得 Perl 许可（http://dev.perl.org/licenses/ -GPL-any/Artistic1, with exceptions 除外）许可的头文件。

您可以包括这些头文件 - XSUB.h，perl.h 和 EXTERN.h（请参阅：[LEGAL-79](https://issues.apache.org/jira/browse/LEGAL-79)）。

#### 包括 Doxygen 生成的配置文件

只要从 Doxygen 生成的文件中删除生成的注释，就可以使用这些文件。

#### Apache 项目可以对 Ruby 许可的作品具有外部依赖性吗？

以 Ruby 为主要语言编写的产品可以依赖 Matz 的 Ruby 解释器（MRI），也可以依赖于 [Ruby 许可](http://www.ruby-lang.org/en/LICENSE.txt)下许可的任何 Gem。

当然，根据其他许可证（如 MIT）编写的 Gems 也可以，这取决于许可证。

另外请注意，对于二进制用法，Ruby 许可证列在上面的“B 类”较低的公共版权列表中（例如 JRuby）。

## X 类：我们不能把什么写在 ASF 项目中？

以下许可证可能不包含在 Apache 项目中：

   - 不符合 OSD：
   
        - 二进制代码许可证（BCL）
        
        - 英特尔简化软件许可证
        
        - [JSR-275 许可证](https://software.intel.com/content/www/us/en/develop/articles/end-user-license-agreement.html#inpage-nav-3)
        
        - 使用领域限制：
        
            - [Microsoft 有限公共许可证](https://www.openhub.net/licenses/mslpl)
            
            - [亚马逊软件许可证（ASL）](https://aws.amazon.com/cn/asl/)
            
            - [Satori RTM 许可证的 Java SDK](https://aws.amazon.com/cn/asl/)
            
            - [Redis 源可用许可证（RSAL）](https://redislabs.com/legal/licenses/)
            
            - [博思艾伦公共许可证](http://boozallen.github.io/licenses/bapl)

        - 非商业许可证：
        
            - [知识共享非商业](https://en.wikipedia.org/wiki/Creative_Commons_license#Non-commercial_licenses)变体

            - [Sun 社区源代码许可证3.0](http://jcp.org/aboutJava/communityprocess/SCSL3.0.rtf)
            
   - 对大型工程进行限制：

        - [GNU GPL 1、2、3](http://www.opensource.org/licenses/gpl-license.php)

            - GNU GPL 的特殊例外（如 GNU 类路径），除非本页其他地方另有允许。

        - [GNU 阿费罗 GPL 3](http://www.opensource.org/licenses/agpl-v3.html)

        - [GNU LGPL 2、2.1、3](http://www.opensource.org/licenses/lgpl-license.php)

        - [QPL](https://opensource.org/licenses/QPL-1.0)

        - [Sleepycat 许可证](http://www.opensource.org/licenses/sleepycat.php)

        - [服务器端公共许可证（SSPL）版本1](https://www.mongodb.com/licensing/server-side-public-license)

        - [代码产品开放许可证（CPOL）](http://www.codeproject.com/info/cpol10.aspx)
        
   - 其他问题：
   
        - [BSD-4条款](https://spdx.org/licenses/BSD-4-Clause.html) / [BSD-4条款（加州大学专用）](https://spdx.org/licenses/BSD-4-Clause-UC.html)
   
        - [Facebook BSD+ 专利许可证](https://code.facebook.com/pages/850928938376556)
   
        - [NPL1.0](https://spdx.org/licenses/NPL-1.0.html) / [NPL1.1](https://spdx.org/licenses/NPL-1.1.html)
   
        - 无厘头许可证：
   
            - Solipsistic Eclipse 公共许可证
   
            - [“不要做个鸟人”公共许可证](https://dbad-license.org/)
   
            - [JSON 许可证](http://www.json.org/license.html)
            
“其他问题”的详细信息：

**Facebook BSD + 专利许可证**

Facebook BSD+ 专利许可证包含一个专利文件规范，该规范将风险传递给我们软件的下游消费者，这种不平衡有利于许可方，而不是被许可方，从而违反了作为[通用捐赠者](http://www.apache.org/legal/ramblings.html#head-62def7ee9e2cb64eb757533133a99da472b1e88a)的 Apache 法律政策。Facebook BSD+ 专利许可证的条款不是 ALv2 中的条款的子集，它们不能作为 ALv2 的再许可。

**NPL**

Netscape 公共许可证是 Mozilla 的原始许可证，包含特定于 Netscape 的修改。这些修正案允许“网景”（现在是美国在线的一部分）避免所有其他许可证持有人必须遵守的互惠要求。这将取消许可证满足开源定义#5（“不歧视个人或团体”）的资格。

**无厘头许可证**

这些许可证虽然对它们的创造者来说很有趣，但在法律上是有问题的。它们通常包括主观的使用领域限制，例如“不要作恶”，没有定义主观限制的仲裁者。在某些情况下，他们甚至可能没有授予足够的权限来符合 OSI 开源定义。由于我们不想让下游消费者感到惊讶，我们禁止使用此类许可证。

JSON 许可证

从2016年11月3日起，JSON 许可证被移至“X 类”许可证列表。在此之前，允许使用[Json Java 库](https://github.com/stleary/JSON-java)。请参阅 Debian 的页面以获取[备选方案列表](https://wiki.debian.org/qa.debian.org/jsonevil)。

#### 可能没有被分发的东西

Apache 项目可能不以源代码或二进制形式分发 X 类许可的组件。并包含在 ASF 源代码或便捷二进制文件中。与前面关于平台的问题一样，如果组件的许可条款不影响 Apache 项目的许可，那么可以依赖组件。例如，在构建过程中使用 GPL 版本的工具是可以的，但是不能包含 GPL 版本的源代码。

#### 当支持一个可选的特性时，可能会被依赖的东西

如果组件仅用于可选功能，Apache 项目可以依赖被禁止的许可证下的组件。在这样做时，项目应向用户提供如何获取和安装未包含作品的说明。可选是指该组件不是项目标准使用或项目达到理想质量层次所必需的。在这种情况下要问自己的问题是:

   - “大多数用户会在不添加可选组件的情况下使用我的项目吗?” 

## 常见问题与解答：

#### 创建 Apache 项目用于什么平台有关系吗？

没关系，除非该平台的条款影响 Apache 项目的许可。例如，创建一个运行在 Windows 或 Java 上的项目，使用 Google Services 或 Yahoo Search 等 web 服务，或者是 JBoss 或 JIRA 等项目的插件都可以，而创建 Linux 内核模块则不行，因为 Apache 项目本身必须获得 Apache 许可证2.0版以外的许可。

请注意，这并不意味着平台代码本身可以重新分发。当然，这将取决于上述代码的许可。此外，如果您对平台的许可是否会影响 Apache 代码有任何疑问，我们建议您检查 legal discuse@归档文件，看看它以前是否出现过，如果没有，请通过电子邮件 legal discuse@来了解。

#### 是否需要对库依赖进行 IP 清除？

不用。

IP 许可用于从 Apache 外部导入代码库，以便将来在这里进行开发。

#### 如果可以选择许可，我应该如何处理作品？

当包含该作品的许可证时，请说明正在使用的许可证，并且只包含您选择的许可证。与 B 类和 X 类相比，A 类更可取。例如，如果作品在源标题中提到了各种许可选项，则不需要修改作品本身。

#### 需要哪些第三方通知？

当发行版包含第三方作品时，涵盖这些作品的许可证可能会要求以某些特定方式通知消费者。这些第三方通知因许可证的不同而不同。Apache 发行版应包含每个许可证的副本，通常包含在 LICENSE 文档中。对于许多许可证来说，这些通知足够了。对于某些许可证，需要一些额外通知。在许多情况下，这将包含在依赖工件中。

必要的第三方通知是指上述情况不包括的任何第三方通知。

当一个版本包含了另一个 Apache 项目时，请参阅[**绑定其他 ASF 项目**](https://infra.apache.org/licensing-howto.html#bundle-asf-product)，了解需要注意的事项。
