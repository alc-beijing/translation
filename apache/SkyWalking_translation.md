# SkyWalking 8.2中的新特性:浏览器端监控;使用标签查询;仪表分析语言
* 作者:Zhenxu Ke， Sheng Wu， Hongtao Gao， and Tevah Platt. tetrate.io  
* 原始链接，[Tetrate.io blog](https://tetrate.io/blog/whats-new-with-apache-skywalking-8-2-browser-monitoring-and-more/)
* 2020年10月29日
![介绍图][overview_img]
Apache SkyWalking，一个可观测性平台，亦是一个开源的应用性能监视器（APM）项目，今日宣布 8.2 发行版全面可用。该发行版拓展了基础功能以及浏览器端的监控边界。

### 背景
SkyWalking是一个观测平台与APM工具。它可以与（或不与）Service Mesh协同工作，为微服务、云原生（Cloud Native）和基于容器的应用提供自动的仪表盘。该项目是全球社区支持的Apache顶级项目，阿里巴巴、华为、腾讯、百度、字节跳动和其它许多公司都在使用它。

### 浏览器端监控
APM可以帮助SRE和工程团队诊断系统故障，亦能在系统异常缓慢之前优化它。但它是否足以让用户总是满意呢？  

在 8.2.0 版本中， SkyWalking将它的监控边界拓展到了浏览器端， 比如Chrome， 或者Chrome和后端服务之间的网络。这样， 我们不仅可以像以前一样监控浏览器发送给后端服务的与请求，还能看到前端的渲染速度、错误日志等信息——这些信息是获取最终用户体验的最有效指标。（目前此功能尚未拓展到物联网设备中，但这项功能使得SkyWalking向着这个方向前进了一步）  

![监控展示图1][func_1]  

此外，SkyWalking浏览器监视也提供以下数据:
PV（page views，页面浏览量）， UV（unique visitors，独立访客数）， 浏览量前N的页面（Top N Page Views）等。这些数据可以为产品队伍优化他们的产品提供线索。  

![监控展示图2][func_2]  

### 按标签查询trace
在SkyWalking的Span数据模型中，已经有了许多被索引并可供用户查询的重要字段。但出于性能考虑，使用Span标签查询的功能至今尚未被支持。在SkyWalking 8.2.0 中， 我们允许用户查询被特定标签标记的trace，这非常有用。例如，在生产环境中运行测试的SRE工程师可以标记仿真（synthetic）流量并稍后通过该标签查找它。

### 仪表分析语言
在 8.2.0 中，仪表系统提供了一项名为MAL（Meter Analysis Language，仪表分析语言）的强大分析语言。该语言允许用户在OAP流系统中分析并聚合（aggregate）仪表数据。
表达式的结果可以被代理（agent）分析器或OpenTelemetry/Prometheus分析器获取。  

### 复合警报规则
警报是及时发现系统失效的有效方式。一个常见的问题是，为了避免错过任何可能的问题，我们通常会配置过多的触发器（triggers）。没有人喜欢半夜被警报叫醒，结果只是因为触发系统太敏感。这种警报很嘈杂并毫无帮助。  

在 8.2.0 版本中，用户选择可以配置考虑了多个度量维度的复合警报规则。使用复合报警规则，我们可以根据需要添加尽可能多的指标来更精确地判断是否存在真正的问题，或者只是一个偶发的小问题。  

一些常见的情况，如 `成功率  < 90%但只有 1~2个请求`现在可以被复合规则解决，如`traffic(calls per minute) > n && successful rate < m%`。  
### 其它值得注意的改进
1.现在代理工具箱公开了某些API，供用户发送自定义指标。
2.代理`exclude_plgins`允许您排除某些插件（plugins）;`mount`使您能够加载一套新的插件。
3.超过10个新的插件已经被贡献给代理。
4.报警系统原生支持发送消息到Slack，微信，钉钉。

### 附加资源
*阅读更多关于[SkyWalkng 8.2 发行版重点][e1]。  

*在[推特][tw]上获取更多关于SkyWalking的更新。

[overview_img]:https://skywalking.apache.org/assets/img/apache-skywalking.87a0b9b4.jpg
[func_1]:https://skywalking.apache.org/assets/img/apache-skywalking-web-app-monitoring.b6364269.png
[func_2]:https://skywalking.apache.org/assets/img/apache-skywalking-web-pages-monitoring.e6de5515.png
[e1]:https://github.com/apache/skywalking/blob/v8.2.0/CHANGES.md
[tw]:https://twitter.com/ASFSkyWalking

