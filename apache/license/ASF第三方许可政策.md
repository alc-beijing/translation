###
原文地址：https://www.apache.org/legal/resolved.html

## 译文版

- [目的](#目的)

    - [许可标准](#许可标准)
    
    - [高水平](#高水平)
    
- [A类：我们可以把什么写进ASF项目中？](#A类：我们可以把什么写进ASF项目中？)

    - [处理公共领域“授权”的作品](#处理公共领域“授权”的作品)
    
- [B类：我们可能把什么写进ASF项目中？](#B类：我们可能把什么写进ASF项目中？)

    - [适当标记的条件](#适当标记的条件)
    
    - [仅二进制包含条件](#仅二进制包含条件)
    
    - [“较低的公共版权”许可证](#“较低的公共版权”许可证)
    
    - [包括知识共享署名内容](#包括知识共享署名内容)
    
    - [知识共享属性-共享许可未经修改的媒体](#知识共享属性-共享许可未经修改的媒体)
    
    - [我可以从Stack Overflow复制代码并将其贡献给ASF项目吗？](#我可以从Stack Overflow复制代码并将其贡献给ASF项目吗？)
    
    - [Doug Lea的并发库](#Doug Lea的并发库)
    
    - [将OSGi元数据添加到较低的公共版权二进制文件中](#将OSGi元数据添加到较低的公共版权二进制文件中)
    
    - [Cobertura报告](#Cobertura报告)
    
    - [处理禁止修改的许可证](#处理禁止修改的许可证)
    
    - [在ASF产品中包含构建工具](#在ASF产品中包含构建工具)
    
    - [创建动态加载的XS模块时包含Perl许可的头文件](#创建动态加载的XS模块时包含Perl许可的头文件)
    
    - [包括Doxygen生成的配置文件](#包括Doxygen生成的配置文件)
    
    - [Apache项目可以对Ruby许可的作品具有外部依赖性吗？](#Apache项目可以对Ruby许可的作品具有外部依赖性吗？)
    
- [X类：我们不能把什么写在ASF项目中？](#X类：我们不能把什么写在ASF项目中？)

    - [可能没有被分发的东西](#可能没有被分发的东西)
    
    - [当支持一个可选的特性时，可能会被依赖的东西](#当支持一个可选的特性时，可能会被依赖的东西)

- [常见问题](#常见问题)：

   - [创建Apache产品用于什么平台有关系吗？](#创建Apache产品用于什么平台有关系吗？)
   
   - [如果可以选择许可，我应该如何处理作品？](#如果可以选择许可，我应该如何处理作品？)
   
   - [是否需要对库依赖进行IP清除？](#是否需要对库依赖进行IP清除？)
   
   - [需要哪些第三方通知？](#需要哪些第三方通知？)
    
## 目的
    
该策略为Apache软件基础产品提供了许可指南。它确定了在Apache软件基础产品中包含第三方开放源代码组件的可接受许可。

如果他们有许可证问题，项目会被要求向法律事务委员会JIRA空间提交问题。

#### 许可标准

以下标准作为本页类别的指南。

- 1、许可证必须符合[开源定义](#https://opensource.org/osd-annotated)₁。

- 2、在实践中应用的许可证不得施加超出Apache许可证2.0所施加限制的重要限制。

₁.（审阅日期：2019-02-16）

#### 高水平

在较高级别上，此策略将许可证分为三类。

**A类**：A类许可证可能包含在Apache软件基础产品中。据说他们是“Apache式的”。

**B类**：在某些条件下，B类中的许可证可能包含在Apache软件基础产品中。它们“可能”包含在内。

**X类**：X类中的许可证可能不包含在Apache软件基础产品中。

## A类：我们可以把什么写进ASF项目中？

如果要成为Apache软件基础产品的一部分，下列许可证都是相似的，特别是Apache许可证2.0：

   - [Apache许可证2.0](#http://apache.org/licenses/LICENSE-2.0)
    
   - [Apache许可证1.1](#http://apache.org/licenses/LICENSE-1.1)，包括变体：
   
       - [PHP许可证3.01](#http://www.php.net/license/3_01.txt)
       
       - [MX4J许可证](#http://mx4j.sourceforge.net/docs/ch01s06.html)
       
   - BSD（无广告条款）。包括变体：
   
       - [BSD 2-条款](#http://opensource.org/licenses/bsd-license.php)
       
       - [BSD 3-条款](#https://opensource.org/licenses/BSD-3-Clause)
       
       - [DOM4J许可证](#http://dom4j.sourceforge.net/dom4j-1.6.1/license.html)
       
       - [PostgreSQL许可证](#https://opensource.org/licenses/postgresql)
       
       - [Eclipse发行许可证1.0](#http://www.eclipse.org/org/documents/edl-v10.php)
   
   - [MIT / X11](#https://opensource.org/licenses/mit-license.php)
   
       - [ISC](#https://opensource.org/licenses/ISC)
       
       - [新泽西州标准ML](#https://www.smlnj.org/license.html)
       
       - [杯形语法分析器产生程序](#http://www2.cs.tum.edu/projects/cup/licence.php)
       
       - [ICU](#http://source.icu-project.org/repos/icu/icu/trunk/LICENSE)
       
       - [伊利诺伊大学/NCSA](#https://opensource.org/licenses/UoI-NCSA.php)
       
       - [W3C软件许可](#https://opensource.org/licenses/W3C.php)
       
       - [W3C社区贡献者许可协议](#https://www.w3.org/community/about/agreements/cla/)-如果发布,至少45天之后
       
       - [X.Net](#https://opensource.org/licenses/xnet.php)
       
       - [zlib/libpng](#https://opensource.org/licenses/zlib-license.php)
       
       - FSF Autoconf许可证
       
       - [DejaVu字体（Bitstream Vera / Arev许可）](#https://dejavu-fonts.org/)
       
       - [学术免费许可证3.0](#https://opensource.org/licenses/afl-3.0.php)
       
       - [服务+组件+建筑+规格](#http://web.archive.org/web/20080704184203/http://www.osoa.org/xmlns/sca/1.0/license.txt)
       
       - OOXML XSD ECMA许可证
       
       - [Microsoft公共许可证（MsPL）](#https://opensource.org/licenses/ms-pl.html)
       
       - [知识共享组织仅限于版权贡献](#https://creativecommons.org/licenses/publicdomain/deed.zh)
       
       - [Python软件基金会许可证](#http://www.opensource.org/licenses/PythonSoftFoundation.php)
       
       - [Python Imaging Library软件许可](#https://github.com/python-pillow/Pillow/blob/master/LICENSE)
       
       - [Adobe Postcript（R）AFM文件](#https://spdx.org/licenses/APAFML.html)
       
       - [Boost软件许可版本1.0](#https://opensource.org/licenses/BSL-1.0)
       
       - [COLT中CERN软件包的许可](#https://dst.lbl.gov/ACSSoftware/colt/license.html)，但请注意，这**仅**适用于COLT中的CERN软件包，**不**适用于其他
       
       - [英国开放政府许可证](#https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/)。该许可允许许可方提供自定义归属通知。如有，请在NOTICE中注明。如果没有提供，那么在NOTICE上注明“包含根据开放政府许可证v3.0许可的公共部门信息”。
       
       - [WTF公共许可证](#http://www.wtfpl.net/)
       
       - [浪漫WTF公共许可证](#https://github.com/pygy/gosub/blob/master/LICENSE)
       
       - [UNICODE公司。许可协议-数据文件和软件](#http://www.unicode.org/copyright.html#Exhibit1)
       
       - [Zope公共许可证2.0](#https://opensource.org/licenses/ZPL-2.0)
       
       - [ACE许可证](#http://www.cs.wustl.edu/~schmidt/ACE-copying.html)
       
       - [Oracle通用许可许可证（UPL）1.0版](#https://oss.oracle.com/licenses/upl/)
       
       - [开放网格论坛许可证](#https://www.ogf.org/ogf/doku.php/about/copyright)
       
       - [谷歌“附加知识产权授权(专利)”](#https://chromium.googlesource.com/external/webrtc/+/master/PATENTS)
       
       - [非授权许可证](#https://chromium.googlesource.com/external/webrtc/+/master/PATENTS)
       
       - [历史许可声明和免责声明](#https://opensource.org/licenses/HPND)
       
       - [木兰宽松许可证, 第2版](#https://license.coscl.org.cn/MulanPSL2/)
       
其中许多许可证都有特定的归属条款需要去遵守，通常是将其[包含到NOTICE文件中](#https://www.apache.org/dev/licensing-howto.html)。当完成这些作品时，请确保您正在执行此操作。     
   
#### 处理公共领域“授权”的作品

Apache产品中可能包含公共领域的作品（或受到类似处理的许可所涵盖的作品）。必须提供出处（与“A类”列表类似）。

符合以下条件之一的作品应被视为属于公共领域：

  - 作品涵盖
  
    - 知识共享[公共领域标识](#https://creativecommons.org/publicdomain/mark/1.0/deed.zh)，或
    
    - 作者(对公共领域)的适当奉献;或
    
  - 有明确的证据表明美国拥有该作品的版权
  
    - 已经过期，或
    
    - 无法声明。
   
应被视为类似于公共领域的许可证：

  - 知识共享CC0“不保留任何权利”
  
  - 知识共享公共领域认证
  
要注意的是判断作品是否属于公共领域可能是一件困难的事情。确定一部作品的版权是否已经过期似乎是非常重要的，而且在不同的司法管辖区可能会有所不同。如果你对某件作品是否属于公共领域有疑问，可以通过“法律讨论”或“JIRA问题”提出这个话题。

## B类：我们可能把什么写进ASF项目中？

为了包含在Apache软件基础产品中，如果满足指定条件，则可以涵盖本节中描述的许可和/或项目。

#### 适当标记的条件

所有B类案件，我们的用户都不应该对其被纳入我们的产品感到惊讶。通过给发行版添加适当且突出的标签，用户就可能知道与Apache许可显著不同的限制。一个合适且突出的标签是用户在了解发行版时将阅读的标签——例如在自述文件中，它应该能识别第三方产品、其授权，以及到其主页的url。同时，请确保遵守相关许可证中的任何归属/通知要求。

#### 仅二进制包含条件

除非另有说明，否则所有B类许可的作品都应以纯二进制形式包括在Apache软件基础产品便利二进制文件中（而不是源代码）。

#### “较低的公共版权”许可证

本节中的每个许可证都需要一定程度的对等。 这可能意味着需要采取额外的措施，以最大程度地减少Apache产品用户在不了解适用要求的情况下创建Apache产品不同许可部分的衍生作品的机会。

如果包含的软件有适当的标签，则以下许可协议中的软件可以以二进制形式包含在Apache产品中（见上文）：

  - 通用开发和发行许可证：[CDDL 1.0](#https://opensource.org/licenses/CDDL-1.0)和[CDDL 1.1](#https://spdx.org/licenses/CDDL-1.1.html)
  
  - 通用公共许可证：[CPL 1.0](#https://opensource.org/licenses/cpl1.0.php)
  
  - Eclipse公共许可证：[EPL 1.0](#http://www.eclipse.org/legal/epl-v10.html)
  
  - IBM公共许可证：[IPL 1.0](#http://www.opensource.org/licenses/ibmpl.php)
  
  - Mozilla公共许可证：[MPL 1.0](#https://website-archive.mozilla.org/www.mozilla.org/mpl/mpl/1.0/)，[MPL 1.1](#https://www.mozilla.org/en-US/MPL/1.1/)和[MPL 2.0](#https://www.mozilla.org/en-US/MPL/2.0/)
  
  - Sun公共许可证：[SPL 1.0](#https://opensource.org/licenses/SPL-1.0)
  
  - [开放软件许可3.0](#https://opensource.org/licenses/OSL-3.0)
  
  - [Erlang公共许可证](#https://www.erlang.org/EPLICENSE)
  
  - [UnRAR许可证](#https://github.com/jukka/java-unrar/blob/master/license.txt)（仅用于取消存档）
  
  - [SIL开放字体许可](#https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL)
  
  - [Ubuntu字体许可版本1.0](#https://ubuntu.com/legal/font-licence)
  
  - [IPA字体许可协议v1.0](#https://fedoraproject.org/wiki/Licensing/IPAFontLicense)
  
  - [Ruby许可证](#https://www.ruby-lang.org/en/about/license.txt)（包括GPLv2是列出的替代[Ruby 1.9.2许可证](#https://svn.ruby-lang.org/cgi-bin/viewvc.cgi/tags/v1_9_2_320/COPYING?view=markup)时的旧版本）
  
  - Eclipse公共许可证2.0：[EPL 2.0](#https://www.eclipse.org/legal/epl-2.0/)
  




#### 包括知识共享署名内容

#### 知识共享属性-共享许可未经修改的媒体

#### 我可以从Stack Overflow复制代码并将其贡献给ASF项目吗？

#### Doug Lea的并发库

#### 将OSGi元数据添加到较低的公共版权二进制文件中

#### Cobertura报告

#### 处理禁止修改的许可证

#### 在ASF产品中包含构建工具

#### 创建动态加载的XS模块时包含Perl许可的头文件

#### 包括Doxygen生成的配置文件

#### Apache项目可以对Ruby许可的作品具有外部依赖性吗？

## X类：我们不能把什么写在ASF项目中？

#### 可能没有被分发的东西

#### 当支持一个可选的特性时，可能会被依赖的东西

## 常见问题：

#### 创建Apache产品用于什么平台有关系吗？

#### 是否需要对库依赖进行IP清除？

#### 如果可以选择许可，我应该如何处理作品？

#### 需要哪些第三方通知？
