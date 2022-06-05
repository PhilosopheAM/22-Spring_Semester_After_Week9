>本文作者为Toichi Tanaka，参考了众多互联网资料，这些reference我会列举在相应位置。
如果您发现文章纰漏或是有任何想法、意见与建议，欢迎联系作者.
Email - 11911421@mail.sustech.edu.cn
本文遵从开源MIT协议。
# 半导体产业介绍、认识与基本了解
本文力图从一个宏观的角度讲述半导体产业的构成、商业合作与竞争模式、现状和未来发展，可能不会设计到具体的技术。另外，由于参考视频的youtuber是台湾人，中文有地方口音，他成功把我带跑了。下文中的“晶片”即是“芯片”。
$$Notion!!!:“晶片”=“芯片”$$
>参考youtube视频：[什么频道——半导体产业](https://youtu.be/kyFZMyavQJo)
[toc]

## [上游分类篇——晶片设计与应用|半导体产业的上游](https://youtu.be/kyFZMyavQJo)
### IP设计与设计服务
在晶片中有许多不同的小区块，这些小区块一般有不同的功能：比方说，A区块是做图形运算的，B区块是做AI加速的，它们被集成在一枚晶片上。每一个细分领域都有很高的技术门槛，因此不会有某一家公司“通吃”。更多的情况是细分领域中有专门做这个方向很NB的公司，它们设计了区块之后作为一个IP卖给别人（晶片需要这个区块来组成时）。这样的公司，自己不生产芯片，也不设计整个（完整的、独立的）芯片，而是提供区块设计服务，卖IP的，称为**IP设计公司**。

除了IP设计以外，还有一类公司称为芯片**设计服务公司**。这一类企业并不自己设计区块，而是整合区块（整合子系统来实现一个整体系统）来设计芯片然后交给生产商把芯片做出来。

## 概括图表

|产业链位置|公司名称|成立时间|所属国别|介绍|其他说明|
|---|---|---|---|---|---|
|IP设计|[ARM](https://www.arm.com/)|1990.11.27|英国、美国|ARM架构处理器，以IP核授权的方式向客户提供服务|N厂曾经试图收购ARM，但迫于监管压力而失败|
|IP设计|[Synopsys](https://www.synopsys.com/)|1986|美国|長期以來是全球排名第一的IC電子設計自動化（EDA）創新公司，并购不断，产业覆盖了半导体全链条|无|
|IP设计|[亿而得YMC](https://www.ymc.com.tw/)|2001.9|中国（台湾）|多次性读写的嵌入式非挥发性内存细分领域的顶尖设计公司|官网丑，而且简中写得看不懂，不走心|
|设计服务公司|[Faraday智原](https://www.faraday-tech.com/cn/content/index)|1993|中国（台湾）|提供[ASIC](#ASIC)专用芯片设计服务，客户提供芯片基本规格或已完成设计整合的GDS，智原接手后续工作项目直至量产|智原是联电分出来的，测试、量产阶段大多交给联发科来做，有时也交给三星来做|
|设计服务公司|[创意电子GUC](https://www.guc-asic.com/tw/)|1998.1.22|中国（台湾）|和智原一个性质的，只不过是台积电家的。需要最先进的制程时找GUC准没错|近年来像Google等互联网大厂对高速运算的需求增加，但在芯片设计领域底子薄或者没有专门团队，就会委托GUC用最先进的制程（大厂不缺钱呀）定制高性能处理器|
|设计服务公司|[芯原微](https://www.verisilicon.com/cn/AboutVeriSilicon)|2001|中国（大陆）|大陆第一家提供芯片标准单元库的公司，是非常典型的[fabless](#FAB)设计公司|最常见的集成电路设计代工公司，是各大[Foundry](#Foundry)厂的主要客户；A股上市|
|设计服务公司|[Alchip世芯电子](https://www.alchip.com/cn-home2/)|2003|中国（台湾）|由Simplex solutions的前员工创立，起初为Sony设计游戏机芯片发家|曾经参与为中国大陆的超级计算机提供芯片设计服务，后该项目被美国制裁，Alchip和台积电都暂停与大陆相关企业继续合作|
|CPU设计与制造|[Intel英特尔](https://www.intel.cn/content/www/cn/zh/homepage.html)|1968.7|美国加州硅谷|在和AMD打擂台赛以前被称作“牙膏厂”，是IDM设计制造一条龙；据我老师说内部的精英们都很老了|不像硅谷google的企业氛围那么随性，内部比较严格；多元化做得很好|
|CPU设计|[AMD超微半导体](https://www.amd.com/en)|1969|美国硅谷|曾经有Foundry，后来卖给阿拉伯人（Foundry独立出来就是GlobalFoundries）并且签了坑爹协议;16年和GF重新签订协议，允许AMD找TSMC等其他Foundries代工，AMD起飞|这几年发布的芯片几乎全方位地与Intel持平甚至超越；曾经也做过GPU(ATI公司)，但后来卖给NVIDIA了|
|CPU设计|[VIA威盛电子](https://zh.m.wikipedia.org/zh-sg/%E5%A8%81%E7%9B%9B%E9%9B%BB%E5%AD%90)|1987|中国（台湾）|曾经在2000年左右和Intel打擂台，后来G了|无|
|GPU设计|[英伟达nVIDIA](https://www.nvidia.cn/)|1993|美国加州|图形处理器的无厂设计公司|拒绝开源运动、自由软件运动；排他性竞争|
|FPGA设计|[Altera](https://www.intel.cn/content/www/cn/zh/products/programmable.html)|1983|美国加州|曾经牛逼，2015年被Intel收购后重组了，现在连渣都不剩了|无|
|FPGA设计|[Xlinx赛林斯](https://www.xilinx.com/)|1984|美国加州|发明了FPGA，可编程SoC与ACAP；世界上第一个Fabless公司|2020年末，正式被AMD收购马，已成功完成|
|通讯芯片设计|[华为海思](https://www.hisilicon.com/cn/)|1997|中国（大陆）|中国大陆最大的Fabless芯片设计公司。主要产品是无线通信芯片，具有5G芯片设计领先优势。20年在中国大陆销售已经超过高通领跑|因母公司华为受到美国政府无理打压，海思的芯片设计无法流片、制造|
|通讯、多媒体芯片设计|[联发科MTK](https://www.mediatek.cn/)|1997|中国（台湾）|全球第一大Fabless芯片设计公司，和海思的产品线重合比较大|是联华电子分出来的，官网不稳定...|
|显示、影像芯片设计|[联咏Novatek](https://www.novatek.com.tw/zh-CN/Home/Index)|1997|中国（台湾）|显示器驱动集成电路扛把子|联华电子分出来的|









## Terminology 专有词汇解释

#### <span id = "ASIC">ASIC</span>
什么是"[ASIC](https://zh.wikipedia.org/zh-cn/%E7%89%B9%E6%AE%8A%E6%87%89%E7%94%A8%E7%A9%8D%E9%AB%94%E9%9B%BB%E8%B7%AF)"?
ASIC这个词频繁在设计服务公司的官网中被提到。ASIC是Application&nbsp;Specific Integrated Circuit的简称，也就是专用集成电路。这一类集成电路的特点是用途专门、单一，出货量一般较小，单个芯片生产成本较高。做ASIC的原型阶段可以使用FPGA做设计验证、调试工作。

#### <span id = "IDM,">IDM</span>
什么是"IDM"? "IDM"是Integrated device manufacturer的缩写（垂直整合制造）.
简单来说，就是一个公司包办从设计、制造到销售的全部流程，需要雄厚的运营资本才能支撑此营运模式，如英特尔。

#### <span id = "FAB">FAB</span>
"FAB"是semiconductor fabrication plant的简写，诸如集成电路等半导体器件在fab中生产。具有fab的公司可以是晶圆代工厂，也可以是IDM. 
Fab所需的资金投入巨大，一般一家新建的Fab至少需要十亿美金。由于这个特性，集成电路行业逐渐从单一的IDM模式走出，出现fabless的纯设计公司与只提供代工能力的[foundry](#Foundry)

#### <span id = "Foundry">Foundry厂</span>
Foundry厂的[wiki定义](https://zh.wikipedia.org/zh-cn/%E6%99%B6%E5%9C%93%E4%BB%A3%E5%B7%A5)非常清楚：“接受其他无厂半导体公司（Fabless）委托、专门从事晶圆成品的加工而制造集成电路，并不自行从事产品设计与后端销售的公司”。
Foundry厂的出现对半导体行业是重大的变革——一方面，具备竞争优势的芯片设计中小企业无需再投入大量资金、人力研发先进制程工艺及建设厂房，从而可以专注半导体电路设计与研发，即成为无厂半导体公司；另一方面，晶圆代工厂可以专注于制造、研发先进制程工艺，将产能赋予多个用户，将市场波动（比如说GPU的横空出世等半导体产业黑天鹅事件）、产能供需失衡的风险（挖矿挖矿）压缩到最小。
注意：一些IDM厂商如Intel和Samsung，也会将自己设计的芯片交予其他Foundries生产以控制成本；IDM厂商也会开放自己的Foundries接受fabless设计公司的代工委托。




