>本文作者为Toichi Tanaka. 本文参考资料已在文中给出。
如果你有任何疑问，请联系11911421@mail.sustech.edu.cn.
本文遵循MIT开源协议。
[toc]
# Requirements Engineering Framework 需求分析框架
>参考资料为Ryan的*Introduction to Systems Engineering*

## 需求与需要文档 Needs and Requirements Documentation
Gathering requirements in a formal sustematic way is referred to generically as **requirements engineering**.

我们需要知道，审视一个项目可以从几个不同的层级来看：
1. Enterprise view - enterprise leadership sets the enterprise strategies and concepts of operations
2. Business management view - 从商业管理的角度出发定义needs和constraints并且形成requirements
3. Business operations view - stakeholder利益相关方要求define their need and requirements
4. System view - 系统观点下确定概念系统和物理系统
需要说明，上述的前三个系统都是在problem domain也就是问题层，只有最后一个系统观点是在solution domian也就是解决方案层。
引用书中的话就是：
>The problem domain is generally considered to be the responsibility of those who have ownership of the problem to be solved, so the descriptions of the system are predominantly in the language of the customer's business management and business operations, focusing on **what the system needs to be able to do, how well it should be done, and why.**
上面的这个问题层描述都是logical/functional的descriptions.

对于解决方案层面(Solution domain)，考虑的则是implementing the solution，所以在engineering and physical terms（物理层）, **"focusing on how the problem is to be solved——that is, how it will look once it has been implemented."**

上面的这些层级都是vertical views of the process，还有每一个vertical views的horizontal views: **the Needs View** and **the Requirements View**. 这两个词在中文中的翻译似乎是一样的，但是在实际英语语境中是有不同的。
+ **Needs**是商业语境(in the language of the business at the business management or business operations levels)下对需求的描述(state capabilities)
+ **Requirements**是对needs的可验证的建构性描述。书中的原话是**"Requirements are formal structured statements that can be validated"**；需要说明的是：一个needs可以对应数个requirements.

我们在Business managment层级对应的是Business Needs and Business Requirements；在Business operations层级对应的是Stakeholder Needs and Stakeholder Requirements.我们下面逐level讲解从needs发展到requirements的process.
|层级|名称|介绍|
|:---|:---|:---|
|Business Management Level|**Business Needs and Requirements(BNR)** Definition Process|这个层级的定义过程出发点是组织的商业愿景(vision)，目标和目的(goals and objectives)以及Concept of Operations[(ConOps)](#ConOps).由此管理层面（管理者）定义了Business Needs，以Preliminary Life-cycle Concept Documents[PLCD]($#PLCD)展示。之后再从Business Needs发展、形成Business Requirements，一般会以形成文档的方式呈现，称为Business Requirements Specification[(BRS)](#BRS)或者叫做Business Requirement Document.|
|Business Operations Level|Stakeholder Needs and Requirements(SNR) Definition Process|在这一阶段，基于上一阶段所得到的ConOps和PLCD文档，需求工程师们(requirement engineers)和stakeholders一起通过一个structured process来确定利益相关方的需求，一般以refined OpsCon document和其他Life-cycle Concept Document[(LCD)](#LCD)来记录；然后再转化成Stakeholder Requirement，以Stakeholder Requirement Specification[(StRS)](#StRS)|
|System Level|System Requirements Definition Process|上一层级得到的StRS被需求工程师们转换成系统需求(System Requirements)，写成System Requirement Specification[(SyRS)](#SyRS)。由于在这一层次中产品被分解成数个systems，所以对于每一个system都可以发展出单独的[LCD](#LCD)|

|名词简写|名词全称|说明|
|:---|:---|:---|
|<span id = "ConOps">ConOps</span>|Concept of Operations||
|<span id = "PLCD">PLCD</span>|Preliminary Life-cycle Concept Documents早期生命周期概念文档|PLCD中一般要包括[Preliminary Acquisition Concept](#Acquisition_Concept), Preliminary Operational Concept[(OpsCon)](#OpsCon), [Preliminary Deployment Concept](#Deployment_Concept), [Preliminary Support Concept](#Support_Concept) and [Preliminary Retirement Concept](#Retirement_Concept)|
|<span id = "BRS">BRS</span>|Business Requirements Specification商业需要说明文档|从商业上的愿景、考量出发|
|<span id = "LCD">LCD</span>|Life-cycle Concept Documents生命周期概念文档|由[PLCD](#PLCD)发展而来，在business operations level加入了对stakeholder needs 安定requirements的考量|
|<span id = "StRS">StRS</span>|Stakeholder Requirements Specification利益相关方需要细则|在概念阶段对问题的延申(加入了对stakeholders的考虑)，但是仍然没有涉及具体的操作，是提出、发现、定义问题的加深过程|
|<span id = "SyRS">SyRS</span>|System Requirement Soecification系统需求细则|SyRS也可以简写成SS(System Specification)|
|<span id = "OpsCon">OpsCon</span>|Operational Concept 产品操作流程概念|试想产品如何交付给用户并被使用者使用；其在ConOps的背景(context)下得到并由business management level向business operations level的过程中由preliminary阶段实际考虑了stakeholders的需求，因此在businees operations level的definition结束以后contains Stakeholder Needs.|
|Null|<span id = "Acquisition_Concept">Preliminary Acquisition Concept</span>|描述了系统如何取得（获得），包括了利益相关者组织(stakeholder engagement)，项目需求定义(requirement definition)，资源募集与协约(soliciitation and contracting issue)，设计、生产与验收(design, production and verification)|
|Null|<span id = "Support_Concept">Preliminary Support Concept</span>|支持系统或者说是“售后”系统？它描述了为了支持系统部署后能够维持正常运转所需要的infrastructure and manpower。一个支持系统需要操作支持(operating support)比如机床代加工、engineering support工程师服务支持、维保支持(maintenance support)，supply support（补给支持）比如军队后勤支持以及技能培训支持(training support)比如一些软件推广时会有专人培训使用|
|Null|<span id = "Deployment_Concept">Preliminary Deployment Concept</span>|部署的概念描述了系统如何被证实可行(validated)，分发到使用者手中(delivered)，投入到实际使用(introduced into operations)|
|Null|<span id = "Retirement_Concept">Preliminary Retirement Concept</span>|描述了系统废弃后如何处理(be removed from operation and retired)，比如一些被使用的或被产出的有害材料如何处理|

##

