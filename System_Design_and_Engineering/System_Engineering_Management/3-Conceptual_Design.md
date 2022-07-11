# Conceptual Design 概念设计阶段
概念设计的产物是FBL(the Initial Functional Baseline). 这个baseline提供一个系统层级的逻辑架构(logical architecture). 由于概念设计还在问题层(problem domain)，因此它与用户（客户）联系紧密（一切从用户开始）.

为什么我们说概念设计是产品设计生命周期的最重要的一个环节？
1. 概念设计对系统的定义有很大的影响。随着项目的推进，系统的定义会从简短的商业需求(business needs)发展到几百页的系统层级的逻辑需求，好的概念设计将帮助完成这一定义的拓展。
2. FBL将作为后续的延申的系统设计的traced back base.所以在前期尽量不要犯错！任何error都会在拓展过程(expansion)中被放大。
3. 概念设计将问题域联系到解决方法域（transition from the problem domain into the solution domain).也是customer(the acquirer)和developer达成的一个联系、平衡的重要过程。所以概念设计的产物--FBL就代表了Business&Stakeholder的Needs&Requirements.

下面我们讲一下如何进行概念设计：五个步骤，一张图。需要说明的是，五个步骤是Iterative(迭代)的，当然设计也是迭代的。
![](source/img/3-Conceptual_Design-How_to_Conceptual_Design.png)

## C1 stage - Define business needs and requirements - BNR
在这一步，我们要做的工作是确定主要的Stakeholders和Constraints.需要注意的是，constraints和requirements总是联系在一起的。Constraints的类型有很多种，接下来会详细介绍。

### C1 - Who are the major stakeholders?
很多人在确定主要的利益相关者时会犯“列举”的错误，也就是将所有可能受到影响的人都假定是利益相关方。书中举了一个例子：
>银行所使用的ATM系统，运钞的安保人员算不算stakeholders?

尽管他们的requiremetents place considerable constraints on the design of the system, 但他们不会作为stakeholders被考虑。在类似的公共产品设计中，如果采用列举额的方法确定stakeholders，那几乎是无穷无尽的。
我们通常使用的确定原则是：一个stakeholders（组织或个人）必须有权利影响系统的输出(has a right to influence the outcome of the system)；而不是简单地以（可能会）受到系统影响来划分。

### C1 - What are the constraints?
限制、约束(constraints)是另外一种形式的需求。(Constraints are requirements that are imposed on the system in some way.)
对于约束的分析我们采用自顶向下的方式。
1. 商业约束(Business Constraints) - 包含管理指导、机构政策、机构标准、行业对于系统开发的指导准则。这一层面的约束主要是出于商业上的而非具体项目操作上的，涉及到公共关系、合同承包政策、人力资源情况、生命周期全流程考量(use of established life-cycle processes). 举一个例子，近期国内三大航空公司给空客下了：“世纪订单”。很多人问为什么不买国产的C919，理由是C919产能不足，且各个航司基本对空客、波音等老牌航空飞机manufacturer的飞机后勤保障体系建立得更好，短时间内无法为C919建立完善的后勤保障体系；而不买波音的理由就更简单了，政治对抗，这也是商业约束的一部分。
2. 项目约束(Project Constraints)一般指：预算限制、开发周期限制与技术标准限制。比如说，设计移动式房屋，需要满足一定的行业标准，安全性、移动性等等。
3. 外部约束(External Constraints) - 各国的法律法规、行业标准、道德风俗要求、此系统与其他系统进行交互的操作性要求、竞争对手的情况、市场上人力资源的情况、行业的特殊技能需求...一般来说，非具体项目操作的约束、不可控的约束，都是外部约束。
4. 设计约束(Design Constraints). 这个约束一般指辅助进行设计、开发、建造和生产的要素的约束。比方说新科技的引入、基础设施的升级与工人的技能提升。这些要素的特点是“直接地”与系统设计的实现与运转相关。

总体来说，进行约束分析时遵循的原则就是自上而下、由抽象到具体、从宏观到微观。其实没有必要严格地确定“什么什么是哪一类约束”，大致分类一下就可以了，有许多约束其实是重合在分类中地。

## C1 - 细致地确定Business Needs
确认了谁是stakeholders和存在什么constraints后，要考虑的事情就变成:确定利益相关方的考量(Elicit business intention)。
### C1 - 愿景、目的与目标 Mission，Goals, and Objectives
Mission（一般翻译为愿景）
