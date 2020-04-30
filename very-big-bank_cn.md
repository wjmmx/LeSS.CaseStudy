# 在大型投资银行中采用LeSS 的步骤

## 背景

（VBB是个代称，公司政策不允许我们使用真实的公司名称。本案例研究中的所有个人名称也是化名。

此报告是关于VBB在2015-2016年大规模Scrum（LeSS）的应用经验，由两名敏捷教练Sean和Gene分享，他们被VBB雇用帮助其实行敏捷转换。教练们事先对VBB的内部动态有一定的了解。

此LeSS应用所涉及的产品范畴是一个文件管理系统，用于法律和财务文件的获取，传输和存储。

## 之前的组织结构

VBB具有传统的组织结构，有多层汇报关系和各种中间人。例如：

开发团队：在负责整体管理的VBB CIO和实际动手的开发人员之间平均有5-6层汇报关系。

[业务团队](http://www.keystepstosuccess.com/wp-content/uploads/2018/09/vbb_case_study_org_design_Biz.jpg): ): 在软件的最终实际用户和做事儿的开发人员之间，存在多层级的“传话人”和“代理人”，比如BA，PMO和各种项目经理。

在采用LeSS之前，开发团队被分成了不同的组件团队。

一般来说，需求获取的工作是由开发团队的业务分析师对接业务团队的业务分析师，然后再对接其他中间人或实际用户来完成。

### 组件团队和产品

在采用LeSS之前，文档管理解决方案是由几个定义狭隘的所谓产品组成的。而这些“产品”实际上只是组件，有固定的组件团队来负责，自然也就没有哪个组件团队能够独立完成跨组件的以客户为中心的端到端特性。

组件团队与其负责的软件“产品”，**见图1**：

<figure>
<img src="img/case-studies/very-big-bank/component-teams-on-fake-products.png" alt="Component Teams as Products">
  <figcaption>Figure 1: Component Teams as Products</figcaption>
</figure>

* CAP - 一个较新的组件，用来获取数据，三种渠道：另一个上游系统，外部data-feed，人工输入
* COM - 一个较新的组件，用来在系统间传输获取的数据，最终将其存为文档
* CAR - 一个遗留组件，用来记录所有文档

### 应用“伪Scrum”

最初曾尝试过使用"伪Scrum". 每个团队成员仍然只是某一个职能的专家。他们的职称是“业务分析师”，“测试人员”，“前端开发人员”，“经理”，“架构师”等等，所以他们几乎没有兴趣去学习别的职能领域知识或技术技能，这也是受到由直线经理强制执行的个人目标设定和绩效评估流程所影响。每个人的年终绩效和discretionary incentives（奖金，晋升）都是基于对个体能力的评估，个人要证明他们是按照最初的岗位描述交付了成果（并且比同事做得更好）。例如，要度量业务分析师“编写故事”的效率，要度量测试人员发现错误的数量，依此类推。这也导致了每个职能的 *局部优化* ，以及整个组织系统的 *次优化*

因此，每个人都会规避风险，并且不愿意去尝试新的或创新的东西，因为这会使他们看起来“效率低下”。这是【拉曼组织行为法则的第5条】（“文化遵循结构”）的一种经典表现，其中指出我们不能在实际中期望人们的举止与组织系统背道而驰，特别是当它涉及工资和职业晋升时。

自然地，这种具有组件团队、单一职能专家、传统的经理角色的“Scrum”应用，以及对应的策略，对增加适应性没有任何效果，也没有加速端到端高质量功能的交付，反而显示出巨大的浪费。

### 有利于LeSS实施的前提条件

以下是在教练入场之前，开发内部有利于LeSS指南和实验的前提条件:

* PMO，作为一个组织单位已经被解散。一些剩余的类似于PMO的职能（例如：排期，预测，工作分配，进度监视）被开发团队和业务人员吸收。（LeSS实验：*避免... 项目管理办公室*, *避免... 所谓的敏捷PMO*）
* 大家有清楚的认知，认为让Scrum Masters对团队成员进行绩效评估会带来严重的功能障碍。(LeSS实验: *避免... Scrum Masters 做绩效评估*)
* 即使在最初采用”伪Scrum“时，团队已经开始定义并遵守每个Sprint的（非常不完善）完成的定义。 (LeSS指南: *创造完成的定义，完善完成的定义*)
* 开发团队每个人都明白将“假”团队成员（例如项目经理，“powerpoint架构师”）添加到团队中无济于事，相反，这只会创造一种”大团队“的假象。(LeSS实验: *避免... 假的团队成员*)
* 资深经理们很乐意被称为并提供“障碍消除服务”，而不是“变革管理团队”。(LeSS实验: *尝试... 障碍服务而不是变革管理*). 例如，某个资深经理接到团队成员的关于某个问题的电话或邮件，他不会委托下属处理，而是召集一个会议。
* 通过利用一些简单的工具和视频设备，多站点的计划扑克已经有效运作（LeSS实验：*尝试...眼见为实-无处不在的廉价视频技术和视频文化。* *尝试...多站点计划扑克（估算扑克）* ）。 例如，每个团队的个人公共区域都配备了摄像机，扬声器和小白板。 这使得可以使用物理计划扑克卡（无需用更复杂的软件乱搞），因为每个团队成员都可以将其物理表决卡展示给房间里的人，也可以给摄像头对面的人。 白板用来做快速笔记，以便房间里的人和通过摄像头参会的人都可以看到信息。
* [中央（组织）教练部门](https://www.infoq.com/articles/centralized-decentralized-coaching)（例如，所谓的“敏捷卓越中心”）和中心化的敏捷/精益指南已被视为一种伪造的迹象，重新标榜既有现状以及局部优化，最终将导致打造出孤立的孤岛和特权的教练（LeSS实验：*请尝试...偏爱去中心化解决方案胜于中心化解决方案。避免...有正式权威的中央教练组。避免...内部敏捷/精益指南*）。 该组织看到了与团队、业务或产品人员密切合作的深层嵌入式教练的价值。 人们偏爱和嵌入式教练在一个社区里共同努力（右图），胜于隐秘的“首席教练”权力结构。 **见图2**.

<figure>
<img src="img/case-studies/very-big-bank/centralized-vs-decentralized-coaching.jpg" alt="Centralized vs Decentalized Coaching">
  <figcaption>Figure 2: Centralized vs Decentralized Coaching</figcaption>
</figure>

## LeSS应用的初始步骤 Initial Steps for the LeSS Adoption

教练限制了初始采用LeSS的人数，开发大概50人，业务人员20人。

这与[三项LeSS采用原则](https://less.works/less/adoption/three-principles.html)之一一致，该原则指出，为了成功进行组织的LeSS采用，必须要“*深而窄优于宽而浅*”。进一步，LeSS指南之一还建议组织在采用LeSS时必须“ .. *将采用LeSS的工作重点放在某一个产品团队上，为他们提供所需的所有支持，并确保他们工作得很好* .... ”

### 扩展产品定义 Defining a Broader Product Definition

符合LeSS尽可能扩大软件产品定义范围的规则，CAP，COM和CAR组件被合并成一个更宽泛的产品定义。 为什么没有定义更宽的范围？ 这是受到参与到本次LeSS采用中的管理层其影响范围的限制。

教练们意识到，将CAP，COM和CAR组件合并到一个更广泛的产品定义中，仍然不能创造完整端到端客户体验的软件产品。 为了使该软件成为完整的端到端软件，它实际上必须包括银行系统中的其它软件组件（和团队），例如：

* **监管**组件
* **客户登入**组件
* **法律**组件
* **人力资源和招聘**组件
* **采购**组件

然而，目前还做不到。

### 向特性团队迈进

由于组件团队的存在与提高全局适应性、从最高价值入手、缩短端到端的响应时间的目标不一致，因此必须换成跨组件的特性团队，这反映了LeSS规则，即“大多数团队都是端到端特性团队*。

在教练的引导下，代表了三个组件的高级管理人员和利益相关者一起进行了“工作坊前的准备活动”。他们使用了几种可视化技术（业务价值流，用户体验地图，用户故事地图）来吸引参与者进入对话和一系列用例模拟，这些用例模拟揭示了，没有哪个组件能代表完整的端到端客户或用户特性。

在准备创建特性团队的这个步骤中，最重要的教育活动可能是：

**经理必须学会明白组件团队的发展是集成问题和过多的跨团队协调问题的根本原因。**

他们能够了解一些从组件团队到特性团队的组织影响，这是很重要的。具体来说，随着特性团队的发展，需要消除现有VBB“组件所有者”的控制权。正如后面将要探讨的那样，这个事情将成为这次应用紊乱的一个问题来源。

最初的CAR组件团队在一家外部（且非常远程）的供应商公司中。它增加了额外的复杂度：时区，供应商中间商，移交，尤其是影响内部行为“合同”功能失调的商业合同。作为向功能团队迈进的一部分，决定将供应商开发人员与内部开发人员混合使用，从而不再强调属于不同公司并强调属于同一功能团队。与VBB和供应商经理举行了一系列会议，讨论以支持敏捷工作方式的方式编写法律合同的重要性。在了解了现有组织动态的背景下，介绍并讨论了一些LeSS实验：

* *尝试...律师研究由筒仓心态和缺乏系统思维引起的问题*
* *尝试...律师学习敏捷、迭代和系统思考的概念*

教练还建议应邀请公司律师参加未来的培训和辅导课程。

教练还组织了**<u>全体培训工作坊</u>。** 教练们介绍了Scrum和LeSS的基本原理。 就角色，事件和工件方面，特别聚焦在Scrum和LeSS之间的区别。 在培训中，每桌由开发人员与业务人员、经理们混合组成，以实现更好的协作和学习（没有“仅开发人员使用”表或“仅管理人员使用”表）。 在研讨会期间，教练们介绍了LeSS的所有规则和原则。 他们还讨论了LeSS指南，并提供了已记录的LeSS实验的案例。 还向听众介绍了LeSS Huge，但显然这次不会采用（因为少于“8”个特性团队）。

#### 自设计团队会议 Self-Designing Teams Meeting

在引导自设计团队会议之前，两个教练学习了[之前的一个案例研究](https://less.works/blog/2018/12/27/how-to-form-teams-a-story-of-self-designing-teams.html)，它描述了在另一家大型银行金融公司的类似事件. This was helpful as the coaches got to read about some practical techniques that could be used with the teams.

这很有帮助，因为教练了解到一些可以在团队应用的实用技术。

新产品团队的关键元素在在巨型白板上用图形可视化的方式进行展示，包括：组件、组外的其他支持应用，所需的个人技能和领域专业知识，以及地理位置。另外几个白板纸上画了一些插图，展示了从历史教训中学到的仓筒工作模式的缺点，来提醒人们该实践背后的“原因”。

在会议期间，一些经理随时待命，解决出现的组织问题。 具体来说，在参加本次会议时，有一些担忧：

* 前面设计团队的尝试会影响后面的决定
* 按照现有的汇报关系或者单组件（比如，UI或DB团队）来构建团队
* 人们不想和不喜欢的人在一个团队，等等

经理们被明确要求不要参与自设计团队会议，除非这些担忧成为现实。幸运的事，唯一需要经理参与的工作是提供有关几个最新招聘的开发人员的信息，他们几周内会加入团队中。 另一个管理层的输入是，新成立的团队将长期存在。

当然，会议的关键活动是人们自组织成新的团队。 这是通过所有人聚在一起讨论最佳的方法来组建可以交付端到端特性的团队来完成的。 这里使用了LeSS“使用志愿服务”的采用原则。 一开始，通过确保每个团队在同一地点，跨职能，熟悉多个组成部分，使每个人都意识到产品和研讨会的目标，以及组建结构合理的团队的含义， 自我管理，可容纳3至9人，寿命长。

最后，形成了三个在同一地点的特性团队，做同一产品，并共享一个产品待办事项列表。

### 初始PBR工作坊

在开始Sprint 1之前，产品组决定遵循LeSS指南之一，举行一个*“初始” *产品待办事项列表梳理（PBR）工作坊，期间澄清了产品的范围和愿景，选择了工作所需的关键人员，识别出了最高优先级的特性，并阐明了初始“完成的定义”。

以下是CAPCOMCAR愿景声明的例子：

>“ VBB员工和外部客户将更喜欢使用我们的文档捕获平台作为最有效的解决方案，该解决方案能够及时设置和管理产品和帐户，并符合全球，法律，法规和控制要求。该过程将包括信息捕获，通信和存储”。

在研讨会上，业务和开发利益相关者都同意了高层的产品主题和战略，和长期目标。在教练的协助下，这是通过结合用户旅程识别和故事地图绘术来完成的，并有助于可视化具有战略意义的“大工作”。将来的所有工作都记录在一个共享的产品待办事项列表中。

### 找到一个产品负责人和领域专家

确定谁来担任产品负责人的角色是有难度的。实践中几乎不可能找到一个具有足够战略眼光并能得到足够的组织授权来为多个团队设定优先级的人。最后，在业务组中找到了这样的人。

但是随后面临另一个挑战：她不了解基本的Scrum（更不用说LeSS），所以也不了解产品负责人这个角色。这个问题通过让她参加Scrum培训然后安排一位教练提供持续的个人辅导来解决的。

最后，给产品组直接引荐了*实际上手的内部用户*，并要求他们安排时间为团队澄清需求，提供详细信息。我们特别小心地选择这些人，确保他们不是中间人、代表或代理人。确定了三个人，他们对前面提到的三个组件（以及文档管理过程中的相关步骤）都具有丰富的实践知识：CAP、COM、CAR。

### 形成社区

根据LeSS指南和实验，创建了几个社区。 （*LeSS实验：尝试...培养实践社区。尝试...使用CoP促进技能学习。*）

首先是“ Scrum Master社区”。重点是提高Scrum Master的引导技能及其区分团队级别（内部）障碍和组织（外部）障碍的能力。通过观察其社区参与情况，很容易识别哪些人可以成为Scrum Master角色的优秀候选人，哪些人不能。通过社区，Scrum Masters能够进一步成长。

自动化测试的成熟度较低。 为了对此进行补救，创建了一个**测试自动化社区**。 这样可以共享经验，提高测试实践水平。 这催生了将测试自动化活动逐渐吸收到团队中的过程。

### 使组织结构和沟通扁平化

(*LeSS实验: 尝试... 尽可能使组织扁平化*)

经常向管理层传递的一个关键信息是：影响组织文化和个人行为以及整个组织系统行为的*首要因素是组织设计*。人们使用了各种辅导工具和技术来帮助大家了解这一点：因果关系图，问卷调查，讨论会。因此，采用了以下措施来改善开发团队的情况：

* 高级管理层向大家传达了强烈的信息，成为“直线经理”（按职称）、增加下属数量并不能确保晋升或加薪
* 建议每位经理的汇报人数上限提高到20-25。
* 鼓励个人*不要*将其直线经理视为不可逾越的层级，*不要*将接触更上级的经理视为禁忌。相反，管理者发起了一系列员工与跨级经理的会议。
* 为了强化说明直线经理*不是*唯一的沟通渠道，更多的高级管理人员（在教练的建议下）建立了障碍清除服务（“IRS”），以便任何团队成员都可以升级他们的问题。

下图（**图3**）是用来向组织讲解，组织扁平化的概念是规模化组织适应性所需的：

<figure>
<img src="img/case-studies/very-big-bank/organizational-flattening.png" alt="Organizational Flattening">
  <figcaption>Figure 3: Organizational Flattening</figcaption>
</figure>

## 早期迭代

### 运行LeSS的Sprint

这些团队实施了以下内容：

* 迭代计划会 - 多个团队全体参与。
* PBR - *总体*产品待办事项列表梳理（PBR）会议之后是*多团队* PBR，团队讨论了底层实施细节。教练明确指出，采用单团队PBR是不可取的，因为这将导致每个团队分别创建“隐式”产品待办事项列表和本地优化。
* 迭代评审 - 所有团队、产品负责人、用户以及利益相关者一起参加。
* 回顾会议 - 有仅需要Scrum Master和团队参加的团队回顾会议；也有全体回顾会议，需要产品负责人，团队成员和开发经理都参加。开发经理被邀请来学习并承担消除组织级障碍的责任。

### 早期成果和业务感知

采用LeSS的第一步是扩展产品定义和打造特性团队，这给用户留下了深刻的印象，并要求*更多*。简而言之，他们说：“*我们真的很喜欢你们这些产出，我们想要更多。需要做哪些事情才能够让你们更频繁地交付更多功能*？

用户为什么对采用LeSS的*初始*结果感到满意？

* 首先，他们能够在每个Sprint的末尾看到更完整的功能，而不仅仅是需要进一步集成的相互分离的组件。
* 其次，由于团队改进了设计和稳定性，交付的一致性得到了提高。从而，进一步提高了向用户交付功能的预测能力。
* 第三，由于前两点，业务和技术之间的整体关系得到了改善。 信任和尊重开始建立。
 
### 特性团队从三个扩展为五个

由于这些益处以及对更多特性的渴望，又新组建了两个特性团队，成员是来自于同一技术领域的开发人员。然后进行了一些的初始准备工作。

这些工作包括：关于基础Scrum的进修培训，LeSS简介，使新团队熟悉产品待办事项列表，优先级和战略目标，然后将他们纳入LeSS产品组加入下一个Sprint。

前面三个团队中有一位经验丰富的Scrum Master被要求服务新团队，另一位Scrum Master则为最初的三个团队服务。现在，由五个团队组成的产品组拥有两个Scrum Master。这符合LeSS规则：“*Scrum Master是专注的全职工作。一个Scrum Master可以为1-3个团队服务*”。

前三个团队的几位高级开发人员被要求暂时扮演<u>开发人员-旅行者</u>的角色（*LeSS 实验：尝试...旅行者*），并加入新的团队，以身作则，提供一些指导。旅行者通过不仅向新成员传授LeSS动态，还教授新团队所不知道的不同组件的某些细微差别，从而暂时成为每个新创建的团队的"支点"。

为了加快与更有经验的团队的同化进程，所有团队都同意，两个*新*团队*全体*参加多团队LeSS活动（Sprint计划一，多团队PBR），而三个经验丰富的团队将只派代表参加。此外，对于最初几个Sprint，两个新团队至少与最初的三个团队中的一个团队进行多团队Sprint计划二。这种方法使用了几个Sprint，直到每个人都确信新加入的团队已经对LeSS事件的流程感到足够舒适。

#### 在运行五个团队Sprint时的调整 Changes in Running a Sprint with Five Teams

Sprint计划一（”做什么“）二（“怎么做”）在目的和出席人员的方面区分得更清楚了。出席计划一的，只有三个成熟团队的代表，以及所有新增加的团队的*全体成员*。让所有新团队成员参加是有意义的：只要计划会议现场不过于拥挤，新人就会从参与和共同学习中受益。

在Sprint计划会第二部分中，团队的目标是定义自己的Sprint待办事项列表。 考虑到工作的性质以及一起讨论技术解决方案的偏好（这将提高大家的领域知识以及对工作的彼此了解，也就使将哪个团队来选择哪个代办事项的决定推迟到最后一刻成为可能），这5个团队通常会*一起*进行计划（* LeSS指南：多团队参加的Sprint计划二*）。 而很少将团队分为2+3的小组来做计划。

## 限制改进的组织元素

### 财务和预算政策

(**LeSS实验**: *尝试... 超越预算*)

At VBB, there is a strong belief that “*everyone must follow the plan and say on-budget*”, as opposed to “*everyone needs to be able to respond to changes, and take advantage of newly raising opportunities*”. As such, budgeting is still done traditionally by once-a-year allocating a fixed amount to new projects (with fixed timeline and scope), basing decisions on a prior year’s expenditures and coarse-grained estimates from hands-off Development managers.

在VBB，人们坚信“每个人都必须遵循计划并在预算内”，而不是“每个人都必须能够应对变化并抓住新的机会*”。因此，按照惯例，预算仍然是每年进行一次，即每年将一个固定金额分配给新项目（具有固定的时间表和范围），然后根据前一年的支出做出决定，并由不负责任的开发经理进行粗粒度的估算。

采用这种方法，不断面临以下挑战：

* 当然，由于采用的是项目模型而不是产品模型，普遍存在交付错误的情况，以及对变化和学习没有反应
* 由开发经理而不是业务端的产品负责人决定要做什么。
* 预算估计的不准确会导致意料之外的关键功能范围缩减，从而使用户不满意。
* 急于在没有进行适当测试的情况下快速交付产品，从而损害了产品质量
* 终止优秀但更贵的开发人员，雇用廉价的低水平开发人员
* 与上述所有情况相关，流程复杂的的增加预算的申请经常伴随着开发与业务之间的相互指责，从而导致关系恶化。
* 开发人员没有能力进行试验和创新，因为试验和创新未列入预算。
* 在某些情况下，如果分配的预算到年底仍未完全用完，则将其“消耗”在不重要的事情上。否则，第二年就有可能得不到相同的金额。

教练们组织了一个工作坊来教育管理人员，内容涉及：
* 自适应预算计划
* 在具有连续自适应交付功能的*产品*上工作，而不是*项目*
* 产出与结果之间的差异

通过Bjarte Bogsnes的“实施超越预算”中所述的行业案例（讨论学习了书中部分<u>摘录</ u>），引入了LeSS实验之一的“ *尝试...超越预算” *。

尽管教练*能够*在这些想法上赢得管理层的赞赏，但不幸的是，在LeSS采用的过程中，会计年度计划仍然是采用了官方既定的常规的自上而下方法来做预算。

而教练的“有限胜利”是，说服了管理层在预算预测层面与团队更频繁地直接协商，在新需求和（重新）设定优先级方面与产品负责人协商。这些对话每个月（每隔一个Sprint）有一次。

### 保证投入 Availability

有个问题是：某个重要的利益相关人一直没有时间，他的输入对产品负责人和团队至关重要。此人一直在出差，并不热衷于参加Sprint评审会。 相反，她会派代表参加“*代表她的观点*”，这是不够的，因为信息在传递中经常被歪曲和扭曲。资深管理层采取了必要步骤，以确保必要的人员能参加未来的Sprint评审会。

### 现有的汇报结构

尽管LeSS结构占了上风，并且自组建的团队也进行了自我管理，没有一线管理人员的明显干预，但是正式的传统报告关系并未*正式被消除。 这主要是由于人力资源部门强制的每年两次的绩效评审流程。这导致了各种浪费和一些冲突。.

### 产品负责人身边的经理们

即使在正确定义了CAPCOMCAR产品、合理安排了团队结构，选出了产品负责人后，仍然存在一个问题：*沟通*。

在LeSS产品组之外的开发技术经理仍在尝试要求团队做一些技术改进和"编外工作"，而没有事先和产品负责人协调（并用感知到的紧迫性为其行为辩护）。这种情况持续了一段时间，尽管教练们强烈建议不要这样做，而且LeSS"入门"指南中建议的是："*只有产品负责人为团队提供工作*"和"*让项目经理远离团队*"。

鉴于拒绝遵守上下级汇报关系对开发人员可能产生令人不快的影响（例如，指责他们不尊重下属的边界，导致低绩效评估），团队尝试了一项实验，他们向产品负责人通报了此类管理"紧急变更"。这是隐式而不是显式进行的，以避免陷入尴尬的局面，具体如下：

鉴于拒绝遵守上下级汇报关系对开发人员可能产生令人不快的影响（例如，指责他们不尊重下属的边界，导致低绩效评估），团队尝试了一项实验，他们向产品负责人通报了此类管理"紧急变更"。这是隐式而不是显式进行的，以避免陷入尴尬的局面，具体如下：

有几次PBR会议，直线经理被邀请作为客人，在产品负责人和一些关键利益相关人面前明确、坦率地说明他们最紧迫的需求。这是在团队的能力和来自业务的优先事项的上下文中来讨论的。非常外交地讲，直线管理被置于一种情况，他们不得不直接和产品负责人协商优先级，而*不是*和团队协商。团队只需要观察，并通过各种方式来协助这个对话（比如：澄清团队能力、限制、依赖等）。通过摆脱潜在的不安全谈判，团队能够更多地专注于工作，而较少关注政治。这种方法行之有效，因为团队不再那么暴露，而且不会被伤害。

#### 最小化编外工作，支持单一产品代办事项列表 Minimizing Side-work and Supporting Single Product Backlog 

由于存在大量的打断，提高计划外的/“隐藏的”/编外工作的成本透明度就变得至关重要。 在辅导大型企业组织变革过程中，通常需要采用经验主义方法。为此，我们建议团队*停止使用单独的待办事项列表来管理打断和额外工作*，而应将所有工作放在一个共享的产品待办事项列表中。 这样，产品负责人就可以参考一个单一的“事实来源”而不是多个彼此独立的“愿望容器”，来了解团队被要求交付的总体工作量，还有优先级冲突，通过这种方式可以解决。

把不可避免的工作中断纳入管理，有助于团队的容量管理，并更好地反映在计划中。几个Sprint之后，高级管理层看到了数据，这些数据说明了临时的、计划外的中断性工作是如何影响团队专注力的，这使他们偏离了计划好的以产品为中心的工作。用来阐述问题的主要方式是通过从累积流程图（CFD）收集的数据，这些数据揭示了Sprint里的工作在每种状态下平均花费的时间。 总体来说，每个Sprint待办事项的WIP很高，这主要是由于频繁的中断（启动-停止-启动-停止）所致，这些中断是由经理强行加入Sprint的计划外工作导致的。

这导致做出一些艰难而又必要的决定：强制要求那些试图将其优先事项放在产品负责人优先事项之上的个人和业务组，马上停止这样做。 开发和业务团队的负责人们对此进行了讨论并达成了共识，所有请求都要经过产品负责人。

### 传统管理沟通途径 

如上所述，VBB的管理等级导致了上下级之间的命令和控制行为。无论正确或错误，任何偏离上级经理管理方针或挑战现有规范和秩序的行动，通常被视为冒险且不鼓励。

揭露潜在问题和障碍的大多数尝试都是徒劳的。这表明公司自身存在一些问题，因为从历史上看，该公司积极抵制变革。

教练们面临两难的境地：“*如何帮助高级管理人员承认问题是存在的，而且需要被关注，然后让其他人都愿意站出来，讲出来并参与进来？*”

为了克服这一障碍，教练们提出了一种折衷方案。它至少为一些更有勇气的人提供了一个安全保障，否则，他们只有选择通过等级制度升级问题来将自己的观察和顾虑说出来，让高级管理层知晓，这将使其处于危险之中。

作为实验，教练们与高级管理人员进行了几次会议，向他们介绍了“ gemba /go-see *”的好处。告知经理们（基于LeSS指南“Go See”），go-see的目的不是微管理，不是下达指令，也不是直接尝试解决团队的问题。相反，“go-see”的目的是学习/理解团队的问题，并教他们如何在管理控制之外独立解决问题。

我们鼓励管理层深入团队工区，在其工位上与个人交谈，询问工作上的顾虑，征求反馈。教练们特别指导管理人员，不要将问题推回团队，也不要尝试直接解决团队的问题。取而代之的是，管理层被引导去“教导”团队如何独立解决问题。

管理层还决定采用各种分散式的升级问题的方法，以鼓励较低级的个人直接与较高级的经理进行沟通。还引入了“ IRS”（Impediment Removal Service），作为一个将问题从团队和Scrum Masters升级到高级管理层的安全方式。它以专用内部电子邮件地址别名的形式出现，任何人都可以以社区讨论的形式提交其个人挑战/问题。

### 经理兼任组件负责人 Manager Component Owners

经理组件所有者是最初抵制形成跨组件特征团队的根源。为什么？对于组件所有者而言，[所有权]意味着展现个人重要性的机会、权力和控制力，从而，有利于个人升迁和薪资增长。

因此，更高级的经理们需要找出一种方法，以确保在采用LeSS期间将先前的组件所有者的角色从组织中去除。怎么能迅速做到这一点？

仍拥有强大技术技能的组件所有者可以参加团队并成为实际贡献者，还可以选择做“组件导师”，其职责是教授其他开发人员。

剩下的组件所有者被转岗到其他部门。

为了避免上述的变化造成太多麻烦，高级经理们与之前的组件所有者进行了一轮讨论，向他们解释说：今后，他们的个人贡献和绩效评估会降低在*组件所有权、自己做事、和告诉他人做*方面的考量，提高在*教学/指导他人做*方面的考量。他们得到管理层的保证：通过培训队友，之前的组件所有者不会使自己的重要性降低，也不会使自己的工作面临风险。 LeSS指南：“工作安全而不是角色安全” --- 被用于此。

### Management and Engineering Practices

**LeSS Test** - “*Avoid... Test department* - *Avoid... Separate test automation team* - *Try... Zero tolerance on open defects* - *Try... Acceptance test-driven development* - *Avoid... Traditional requirement handoff*”

Unfortunately, manual testing practices were long-established within VBB and this meant manual testers were distributed across newly formed teams. To remediate this weakness, test automation and sharing of good engineering practices was strongly encouraged across the teams. This advice was supported with training and coaching by one of the coaches (Sean). The primary vehicle for this focus was via an Engineering Community (see the LeSS Guide: *Communities*) and targeted training was also provided when particular needs came up. Teams were encouraged to transition from the traditional process of “testing a release candidate” using manual testing to manual or automated testing of features as part of the Definition of Done.

**Figure 4** shows the Definition of Ready/Done/Undone derived by all teams in one of the kickoff workshops. Unfortunately, notice the *initial* continued inclusion of manual testing in the DoD, even though some automated testing was introduced in the LeSS adoption.

<figure>
<img src="img/case-studies/very-big-bank/definition-of-done.png" alt="Definition of Done">
  <figcaption>Figure 4: Definition of Done</figcaption>
</figure>

Why? Unfortunately manual testing remained in two cases, both at the request of the teams:

1. The first was Integration Testing performed by the team in all environments
2. The second was User Acceptance Testing (UAT) performed by an external, separate group with their own cadence.

Both the teams and technology/business managers felt it was important to continue this practice until trust was built in an automated toolset. As mentioned in the above Definition of Done picture, manual integration testing continued across a minimum of two testing environments for any deployment including DEV, UAT and Production. For example, this included a deployment to DEV environments at the end of each Sprint. Deployment to UAT would then occur as Undone work that carried over to the subsequent Sprint. This resulted in significant ongoing wastes. Interruptions to the teams existed because of slow feedback and a plethora of release related sign-off meetings that made it very difficult to facilitate positive change across the board fast. For example, teams would typically wait weeks for UAT sign-off after a feature was accepted by the Product Owner. Any feedback from the UAT team that required code changes would manifest as urgent interruptions to the development team. After passing UAT, releases into Production would require coordination and more manual testing across each application and was only allowed to occur in restricted time-windows. Of course, this led to the continuation of massive wastes.

**LeSS Design and Architecture** - “*Avoid... System engineers and architects outside of regular feature teams* - *Try... Technical leaders teach at workshops* - *Try... Hire and strive to retain master-programmer ‘architects’* - *Avoid... Architecture astronauts (PowerPoint architects)*”

Another dysfunction in VBB was the existence of separate architecture groups (with managers that wanted to maintain their status quo positions) at multiple levels, both within Development and firmwide.

There were frequent interference attempts from the *firmwide* architecture groups that had the potential to be very disruptive. One minor benefit of the unfortunate continued existence of the local Development architecture group was to at least absorb this interference so that it didn’t cascade into the new teams.

Still the Development architecture group did not dissolve and so there were continuing wastes from the presence of this single-function group that made documents and dictates, not code.

In addition to architecture groups, technical managers also wanted to dictate architectural decisions, since their traditional positions were based on these kinds of actions. A Development manager introduced (without consultation with the teams) a weekly “Design meeting”. This had the effect of severely hampering in-flight and future work, and was a source of conflict for the developers across all teams. Because it was imposed by a middle manager, this was difficult to abolish. It took a number of Sprints until the problem was recognized by senior management (Scrum Masters escalated this problem and qualified it as an organizational impediment) and this low-level centralized decision-making attempt was abolished.

### HR政策

During the faux “Scrum” adoption, each team member was still officially a single specialist. There was almost no interest in learning new functional domains or technologies, as everyone's job title was ‘business analyst’, ‘tester’, ‘front-end developer’, ‘manager’, ‘architect’, etc. Lack of motivation by people to learn additional functional and technical skills was driven by the process of individual goal-setting and performance reviews, by line managers. Everyone’s end-of-year performance and discretionary incentives (bonuses, promotions) were based on an individual’s ability to prove that they delivered as per their original job descriptions (and did *better than* their peers/colleagues). For example, business analysts were measured based on how efficiently they were able to ‘write stories’, testers were measured on how many bugs they were able to discover, and so forth. This also led to local optimization by each single function and subsequently, to *sub-optimization* of the overall organizational system.

Because of that, everyone was risk-averse and not willing to experiment with anything new or innovative , as it would make them being perceived as ‘less efficient’. This was a class manifestation of [Law # 5 of Larman’s Laws of Organizational behaviour](https://www.craiglarman.com/wiki/index.php?title=Larman%27s_Laws_of_Organizational_Behavior) (“Culture follows Structure”), in which one can’t realistically expect people to behave in a way that is very contrary to the organizational system, especially when it involves salary and career promotion.

The partial success that the coaches were able to achieve was to persuade management to promote behaviors they were wishing to see: knowledge sharing, stepping out of a usual comfort zone and learning, shared ownership, *swarming*, etc.

A few years after the coaches disengaged, their prior effort to improve job roles finally paid off: A more general “developer” role with broad skills was introduced, and the job title of *Scrum Master* was added VBB-wide. This is a classic example that a coaching impact may have a delayed effect.

### 文化受组织设计影响

One of the most challenging aspects of organizational culture that the coaches had to face was the amount of emphasis that was put on *individual performance*. There was a deep systemic problem that had to be addressed, organization-wide.

Historically, VBB, had a culture that encouraged super-heroics and internal competition. People were primarily driven by extrinsic motivation and a desire to outperform their colleagues, competing for bonuses, promotions, and other perks. Individual performance appraisals and end-of-year reviews defined individuals’ behaviours and often led to system gaming, especially at year-end. *This culture of heroics and internal competition was strongly influenced by the* **organizational design**.

Such culture was not conducive to ways of working expected of teams in LeSS.

As an example, the below causal loop diagram (**Figure 5**) uncovers underlying system dynamics that involved individual performance evaluation process, and how it adversely impacted basic Scrum dynamics within the Development group (reminder: a faux “Scrum” had been already introduced before the coaches joined).

<figure>
<img src="img/case-studies/very-big-bank/individual-performance-evaluation-systems-model.jpg" alt="Individual Performance Review Systems Model">
  <figcaption>Figure 5: Individual Performance Reviews Systems Model</figcaption>
</figure>

To alleviate this problem within the LeSS product group, the coaches decided to leverage the following LeSS experiment: "*Avoid... Incentives linked to performance*", and "*Try... De-emphasize incentives*.” The goal was *not* to change norms and standards globally for the whole enterprise. Rather, the goal was to educate influential management to act locally by taking actions that would lead to changing individuals’ attitudes and behaviour, to make individuals more respectful of collective ownership and willing to cultivate “us- together” mentality. More about this effort below.

**LeSS Experiments**: *Try... De-emphasize incentives* - *Avoid... Putting incentives on productivity measures* - *Try... Team incentives instead of individual incentives* - *Try... Team-based targets without rewards* - *Avoid... Performance appraisals*

The Development management involved in the process of appraisals and rewards was educated on the harmful impact of these. How? A few workshops were conducted for managers and HR representatives to discuss:

* Research and studies of how individual performance appraisals and their linkage to monetary incentives can cause harm to employees and organizations (summarized, as [case 1](http://www.keystepstosuccess.com/2016/02/quotes-from-get-rid-of-the-performance-review-how-companies-can-stop-intimidating-start-managing-and-focus-on-what-really-matters-by-culbert-samuel-a-laurence-rout/) and [case 2](http://www.keystepstosuccess.com/2016/02/quotes-from-punished-by-rewards-the-trouble-with-gold-stars-incentive-plans-as-praise-and-other-bribes-by-alfie-cohn/))
* Systemic cause and effect relationships between individual performance appraisals/bonuses and health of Scrum dynamics. Below (**Figure 7**) is an example of a causal loop diagram that was produced during one of the discussions with managers to visualize the problem and educate people towards better behaviours.

The scope of these changes were of course local to Development. The LeSS adoption within Development was an experiment of organizational restructuring inside a *bank*, that — as in all banks that we have coached within — has deeply rooted traditional, hierarchical, top-down command & control culture aimed at shifting large cash bonuses to bank managers. So were not under a fantasy that these changes could be extended beyond our boundaries, and just sought to ring fence them locally.

One example of a locally controlled norm was emphasis on team-level ownership, responsibility and performance, rather than individual-level. Although the bank-wide process of individual performance appraisal still existed, Development management informally trivialized its importance. Valuing (and praising) team performance over individual performance became more of the norm. Eliminating the dysfunction-generating policy of appraisals and bonuses was not possible, but with the support of management what was possible was to reduce the harm and shift the emphasis.. This illustrated the LeSS experiment “*Try... Reduce harm of policies that cannot yet be removed*”

So within the organizational constraints the management tried to create an environment conducive to improved behaviour by developers. The following was made clear and continually stressed during Development events and regular communication:

* Importance of becoming T-shaped workers
* Benefits of learning new development tools and techniques
* Behaving towards other teammates in supportive, team-like fashion, as well as valuing team performance over individual performance.

Above all, a strong emphasis was made on customer happiness with the overall LeSS delivery being the most influential factor that identified financial rewarding of teams, and subsequently, individuals.

Although at the end of the year each Development employee was still given a year-end review and “report card”, it had much less bearing on how an employee was rewarded financially. Individual adherence and genuine support of agile transformation efforts and LeSS adoption were valued more than individual delivery and heroics. Letter-grading was still assigned informally by managers (it was entered in a centralized system of record, as it was required by HR) but everyone understood and spoke freely about the fact that it had practically no value to anyone. This illustrated the LeSS experiment *Try... Fill in the forms*, meaning that when it isn’t possible to eliminate wasteful HR processes, then just play the game by inputting the essentially meaningless information with the least effort, and focus instead on the important real work of improving how to delight the customer.

## 结论

LeSS采用有以下正面影响：
The LeSS adoption had some positive impacts:

* Users were pleased with frequent delivery of useful features. They could forecast better.. Also, the level of transparency and predictability brought by the LeSS adoption has grown much higher. Relationships between technology and business were at their best during the LeSS adoption .
* On both sides, Development and Business people learned how to identify organizational impediments and relate superficial discoveries to deeper, systemic root causes, that affected a broader system. We believe this learning will stay with people for a long time.
* The communities helped individual and group learning.
* Modern engineering practices grew deeper roots into Development and beyond, positively affecting the broader technology group.
* A handful of seasoned Scrum Masters was nurtured and some of them became so passionate about becoming change agents that they have decided to make this into a career journey.

The following challenges remained unresolved at the time both coaches departed:

* Component/application *ownership* did not completely transform into *mentorship*. There was still hidden resistance by former application owners to give up control and become mentors.
* People that were displaced because their original roles became no longer required in LeSS (e.g. business analysts, project managers, and manual testers) were not effectively accommodated by other parts of VBB. Effective cross-training to acquire additional skills (and hence work as an effective flexible team member) was not offered either. Therefore, displaced people continued to put up hidden resistance to the LeSS adoption.
* Self-management remained a challenge. For example, individuals were still required to “work with their managers” on individual career plans, even in situations when managers had little influence on decisions.
* Performance reviews and subjective bonuses continued to affect individuals' morale, even though their importance was trivialized: complete decoupling of performance reviews from subjective monetary incentives did not happen


