---
title: MTS
page-category: case-study
order: 860
id: mts-kassa
owner: illia-pavlichenko
---

# 学习在MTS Kassa是如何学习的

## 学习的旅程

当我查看成文的案例时，我发现它就是一段走向学习型组织的旅程，一段人们不断地探索如何进行变革，以及为什么要变革的旅程。 因此，请将本案例当做一个故事来阅读、欣赏，看一群勇敢的人是如何展开永无止境的学习旅程的。

## 踏上旅程前

### МТS收购LiteBox

在2017年，俄罗斯最大的电信公司MTS对LiteBox公司的股票进行了控制权收购，后者的经营业务为基于云的零售自动化：包括仓库处理系统，采购管理，分析报告等。

<figure>
  <img src="/img/case-studies/mts-kassa/mts-kassa-product.jpg" alt="MTS Kassa产品">
</figure>

从此，LiteBox成为庞大的MTS公司（拥有70,000名员工）的一部分，但它在管理自己的业务方面几乎保持完全的自主权。 到LeSS实施时，LiteBox已拥有200多名员工，并作为一个独立的业务部门运作。

### 商业机会和紧迫感

MTS管理层向我寻求帮助。 2017年底，我们进行了首次协商。 原因是LiteBox管理层预计从2018年7月1日开始将掀起一股巨大的客户增长潮（或者说是海啸），用户群将增加大约100倍。 2017年12月，LiteBox的客户数量是6000多，而到2018年秋季预计将超过10万。LiteBox管理层希望产品开发具有适应性，并容易做到规模化扩展。 在与高层管理者们进行了数次面对面会谈之后，我们同意先从一些电话访谈开始，然后进行更深入和结构化的公司审计。

### 原有的组织结构

组织架构跟想象的一样，基于传统的管理理念设计的。 公司由各个职能部门或者说筒仓组成（财务，采购，销售，IT，市场营销，人力资源）。 每个职能部门都有自己的一些经理们，这些经理们也都有自己的一些KPI。

<figure>
  <img src="/img/case-studies/mts-kassa/original-organization.png" alt="原有的组织结构">
</figure>

### IT部门结构

尽管最终目标是对整个公司进行变革，但我们还是先从对IT部门的人员访谈开始。他们正在开发核心产品和主要价值主张。下面是我的一些发现。

**开发以组件团队进行。**

30多个开发人员通过“项目”团队组织起来进行产品开发。 每个“项目”都是围绕着架构组件，技术或职能组织的。 因此，他们有7个“项目”：旧后端，新后端，android，windows，测试，分析和API团队。

<figure>
  <img src="/img/case-studies/mts-kassa/old-feature-flow.png" alt="旧的特性开发流">
</figure>

技术栈由几种编程语言和相关框架组成：Javascript, Android, Python, SQL, Java.

**协调角色及层级**

由于这些“项目”都无法创造可用的产品增量从而为客户创造有价值，因此需要几个协调角色和职能层级结构：

* 分析部门主管。
* 测试部门负责人。
* 首席架构师。
* 后端技术负责人。
* Android开发技术负责人。
* Windows开发技术负责人。
* 发布工程师。

他们是一个使用了一些Scrum术语的传统组织。 简而言之，就是骨子里根本没变的伪敏捷组织。 访谈后，我在LiteBox办公室里花了两天时间进行[Go See](/less/management/go-see.html)。除了生搬硬套或[*copy-paste* Scrum](https://agilix.nl/blog/481-the-problems-of-scaling-scrum) 方法外，我立即注意到另外两件事：

* 每个项目都旨在最大程度地提高资源使用率，而且显然这是每个人的终极目标。
* IT开发饱受来自生产环境的大量缺陷或者事故的折磨。

### 我的观察和结论

LiteBox是具有层级结构的职能型组织，并拥有与此结构相关的所有众所周知的问题。

**依赖关系。** 由于组织结构的原因，所有组件团队都无法独立向客户交付任何功能。 所有组件团队都具有依赖性，从而导致不必要的计划和协调角色。

**交接和瀑布式。** 组件（“项目”）之间存在大量交接。这导致了严重的排队现象，客户反馈也因此延迟。一个功能从开始到完成的平均周期时间为6-7周。

**单职能专家。** 组织结构鼓励像业务分析师，测试人员或开发人员这样的单一职能角色，这使组织变得脆弱并且容易受到市场变化的影响。 当前的组织结构是针对人员的忙碌程度（“资源使用率”）进行优化的，而不是针对灵活性和快速的价值交付进行优化。

**狭窄的视野。** 团队看到的不是整个产品，而只是产品的一部分。开发人员专注于他们个人的忙碌，而不是系统效率和快速的价值交付。在一个访谈中，有成员这么说：“没有感觉到所有团队都为共同的目标而共同努力。”开发人员并没有完全理解他们开发的功能的价值和目的，因为他们只是工作在组件部分。i

**缺乏透明度。** 业务人员饱受低透明度的困扰。 他们不知道开发工作的真正进展到底是什么。很多事情是在并行处理的（很大的在制品数量）。工作散落在各个团队中。每个人都工作得很辛苦，在各自的局部里尽着自己最大的努力，但是作为开发小组整体却没有成效。

**差劲的需求管理。** 不存在单一的需求来源。 团队抱怨着优先级冲突，因为如此多的利益相关者能够给他们派活儿：业务分析师，CTO，呼叫中心，市场部门，等等等等。没有确定的流程为需求排序。当前的需求管理系统在员工的眼中就是“垃圾”。

### 研究整个公司

经过一系列电话访谈并在LiteBox办公室工作了几天之后，我对高层管理者们介绍了自己的观察结果，然后赶往总部对整个公司进行了深入评估。我们与公司高级管理层和员工举行了为期两天的工作坊，重点讨论公司的组织结构，价值观，价值流等。我们的目标是制定下一步计划和行动方案。 我们在工作坊上使用的一些工具是：

* **Scott-Morton图。** 这展示了关键的公司要素之间的联系：战略，流程，人员和结构。
* **加权SWOT分析。** 它是在混合组中创建的。所有相关因素都使用从1到5的标准对其重要性做了权衡。
* **价值流图。** 这项技术使我们可以获得对产品开发流（从收到客户请求到相应的价值交付）中浪费的洞察。通常，它是从客户支持收到的客户首次致电开始，结束于相应的新版本发布。

**评估结果。** 细致的公司评估证明了我对组件团队及其功能障碍的最初论断。 价值流图还显示了一个特性从开始到结束的平均周期时间为6-7周。 我喜欢工作坊时管理人员的那些“啊哈！”时刻：

* 他们都同意，对于这样一个中型公司而言，层次结构太多了。
* 了解到个人的KPI和奖金在公司只是在公司的某些部门（销售和市场）做了局部优化，并将导致两个职能部门相对立。
* 会议室中的每个人都同意公司没有明确的愿景和战略计划。

**建议。** 不足为奇，在评估之后我给出的建议是：
* 在IT产品组中举办Scrum培训。
* 针对CxO人员的Scrum培训。
* 战略规划工作坊，以明确公司愿景并制定接下来1到2年的公司战略。
* 简化组织结构，从职能型组织逐步转变为基于团队的组织。
* 启动特性团队作为试点，如果成功，导入LeSS。

<figure>
  <img src="/img/case-studies/mts-kassa/company-assessment.png" alt="公司评估">
</figure>

## 旅程开始 - LeSS导入准备

### 为什么导入LeSS需要更改组织结构

有效的LeSS导入（有效的单团队Scrum导入也是同样）通常意味着*组织结构*发生变化（ *指南：三个LeSS导入原则* ）。 原因是大多数组织结构的设计是针对个体产出进行优化的，当中包含了许多的局部优化。 LeSS降低了原有结构带来的组织复杂性，并引入了新的更简单的结构。 LeSS的优化目标如下，而这些目标通常需要更改组织结构以支持它们：

* 交付最高的客户价值优先。
* 便宜且容易的适应性（“轻盈优雅地转身”）。
* 学习。

### 学习Scrum基础

我们邀请了高层管理者，一些开发人员以及所有职能部门的经理（市场，销售，合规等）参加为期2天的专业Scrum基础（PSF，Professional Scrum Foundations）培训。 这个培训帮助他们了解了作为单团队Scrum基石的价值观和原则。LeSS中提供了一些指南，以帮助在组织中实施该框架（ *入门指南* ）。 该指南的第一步是：*教育所有人*。 现在，我意识到我从一开始就没有严格地遵循该指南，做到教育所有人。 这很快就导致了导入时志愿和支持方面的问题。

### 管理层共同讲述的变革故事

培训之后，我们再次将高层管理者们召集起来，共同创造一个变革故事。 这个故事是讲述给公司中每个人的，解释公司为什么要努力变革。幸运的是，我们从一开始就获得了公司负责人的支持。 但这还不够。 我们一直在寻求整个高层管理团队的帮助和支持。 为什么？ Scrum和敏捷原则的大规模导入并不局限于开发团队。 它涉及产品管理，预算，发布，营销，销售和人力资源策略。 由于公司是由职能筒仓组成的，因此任何一个筒仓的高层管理都有可能对这一重大变革产生负面影响。

因此，这里我们设计了一个变革故事工作坊。 工作坊有两个产出。 第一个是一个矩阵，风险/机会/问题/紧急事件的信息分别归类在四个象限中。在填充矩阵的过程中，管理者们统一了他们的观点以及他们需要Scrum的原因。

<figure>
  <img src="/img/case-studies/mts-kassa/risks-opportunities-problems-urgency.png" alt="风险 机会 问题 紧急事件">
</figure>

第二个产出是一个变革故事。它是[精益变革管理](http://leanchange.org/)中的一个有用的工具。 对于其他公司而言，似乎这只是一条简短而引人注目的信息，强调了以下要点：

* 为什么现在需要变革。
* 我们即将要做的事情。

“之前我们小且敏捷。那时我们是自治的，所有信息都是透明的。我们喜欢那时的我们。然后有一天，我们成长起来，规模变得更大，并且获得了MTS的投资。 这影响了我们的思考方式并且工作量也相应的增加。 这就是我们需要对结构和流程进行变革的原因。它会帮助我们变得更加有效，清除错误并提高产品质量。在实现敏捷变革的过程中，我们需要指导和教练方面的支持。”

工作坊结束后，我们确保每个员工都能收到这个变革故事的数字版本。

<figure>
  <img src="/img/case-studies/mts-kassa/change-story.png" alt="变革故事">
</figure>

### 通过试点团队学习Scrum

根据LeSS规则，较小的LeSS实施必须“一次全部”完成。 这就意味着周五每个人都还在具有传统组织结构的公司中工作，然后在周一，产品开发的组织设计就翻转为一个崭新的组织结构。 尽管这个方法具有众多优点，但我还是无法“兜售”出该方案。尽管如此，他们还是同意成立一个特性团队作为试点，如果成功的话，随后将进行完全的LeSS导入。

### 试点团队结果

* 在第一个Sprint中，试点特性团队能够发布一个启动过程中做客户访谈时发现并被添加到产品待办列表中的新功能。该功能是一个未满足的需求，被很快发现后在一周内发布。
* 用户参加Sprint评审会议，因而能够定期地提供反馈，有定性的也有定量的反馈。我们发现公司以前从未度量过客户满意度。
* 在一些Sprint中，团队动力发生了很大变化。 他们开始学习，以逐渐成为多栈开发人员。 例如，在一次回顾会议中，一位经验丰富的Windows开发人员表示，他将在接下来的几个月内开始编写Android代码。
* 团队成员的思想和行为发生了变化。 他们开始结对工作，并且经常集中力量一起解决问题。 他们掌握了这样一个想法：如果每个人都单独处理自己的事情，那么他们就不太可能互相帮助，从而从长远来看不太可能互相学习。
*该团队能够同时工作在三个管道中，从而进行多个特性的开发。
* 开发过程对产品负责人更加透明。 产品负责人说，他喜欢团队选择PBI后不需要额外的协调和控制等就能交付完整特性的，这种像黑盒子一样的工作方式。
* 团队直接与市场互动。 他们不需要任何其他角色来进行协调。他们是独立的。
* 与组件团队相比，特性开发的平均周期时间减少了2-3倍。

我注意到一些组件团队成员开始参加Sprint评审会议。 他们对试点团队的工作很感兴趣。

我们也发现了这次试点产生的一些负面结果或者困难：

* 产品负责人承受着巨大的压力。 他必须与试点特性团队和其他组件团队同时工作。 他管理了2个产品待办列表：一个为了以客户为中心的试点项目，另一个是为组件团队提供技术性工作任务。
* 特性团队在与组件团队不同的环境中运作。产品负责人有意保护试点团队在Sprint中不被干扰，比如生产环境缺陷和技术支持要求。因此，有些人说特性团队试点不能被认为是有说服力的实验。
* 特性团队和业务分析师小组之间存在紧张关系。开发人员开始直接与客户沟通。业务分析师将特性团队开发模式视为对其工作岗位的威胁。
* 特性团队无法独立向市场发布功能。产品组中的发布工程师仍然扮演着他们的角色，他们对一个包含很多特性的批量实施最后的系统测试，并做出“可以发布”的决定。 因此，功能开发的周期时间虽然确实减少了很多，但再高一层的周期时间却差不多。特性即便已经完成，却仍须排长队才能发布。

### 公司战略工作坊

LeSS导入是整个公司转型举措的一部分。 对公司全面评估后的建议之一是进行战略会议。为期3天的MTS Kassa战略会议分为两个部分。 前两天用于建立组织愿景和新的业务战略。 第三天则用于创建接下来几个月的路线图。

**视觉故事。** 第二天的重点是建立公司愿景。 包含两个活动：首先，使用时间表来显示公司历史中的重要事件并创建产业地图（趋势，参与者，行业，未来市场需求）；其次，将参与者划分为小组，由他们来创建各自版本的公司愿景故事。 我们请各个小组想象公司在2年内能够达到的成功，“想象2年过去了，MTC Kassa的故事被刊登在商业杂志的封面上。那里会有什么样的画面/照片/引述？这篇文章是关于什么的？标题是什么？公司的主要进展是什么？”

进行封面故事的愿景练习后，我们开始编写简短的愿景声明。 我们希望在所有参与者（将近30人）中达成共识。 我们花了几个小时在上面，但这时值得的。因为参与者说，他们切实受到了共创的愿景的激励，这个愿景是：

*每个俄罗斯企业家都选择我们的B2B生态系统服务作为其业务的助手。*

<figure>
  <img src="/img/case-studies/mts-kassa/vision-statement.png" alt="愿景声明">
</figure>

**结果。** 战略会议的最重要成果之一是高层管理者中涌现了适应性组织的概念。 他们一致认为，当前的组织设计是将让人们忙碌作为优化目标的。 这与适应性的目标不一致，因此，组织设计的一项新的关键决定就是导入LeSS。

我们将人们召集在一起，围绕着明亮且鼓舞人心的愿景，制定了公司路线图。 事实证明，这对于创建产品待办列表也是一个很好的输入。

<figure>
  <img src="/img/case-studies/mts-kassa/strategy-workshop.png" alt="战略工作坊">
</figure>

###  LeSS导入的后续步骤

2017年夏天，我旁听了Craig Larman在米兰的LeSS课程。 他的一个建议“像政治家一样思考，而不是像工程师一样” 让人记忆深刻。尽管产品负责人要求我尽快实施LeSS，但Craig的建议帮助我推迟了导入。在特性团队试点取得初步成功之后，我观察到管理层的信任度有所提高。 因此，到那时我们已经获得了全面的管理支持。 很棒！ 但是另一方面，我意识到组件团队的许多开发人员仍然对LeSS持怀疑态度。 我们想对他们进行教育，以便让他们成为变革的志愿者而不是囚徒 （ *指南：三项导入原则* ）。

### 转型待办列表

产品负责人，来自产品小组的一些志愿者，试点团队的Scrum Master，还有我组成了最初的转型小组。 以下是一些转型待办事项：

* 进行LeSS基础认证（CLB）培训。
* 举办多个精益咖啡工作坊，回答LeSS相关的常见问题。
* 创建初始的产品待办列表。
* 创建HitMap 。
* 引导团队自设计工作坊
* 创建完美目标。
* 团队选择Scrum Master。
* 创建完成的定义（DoD）。
* 建立社区并寻找组件导师。
* 进行第一次产品待办列表梳理。

回顾过去，我们花了将近两个月的时间来准备LeSS结构的导入。

### 学习LeSS框架

因为每个人都已经参加了Scrum基础培训，所以我认为为期一天的[LeSS Basics认证培训](https://less.works/courses/less-basics.html)（CLB），然后再进行通过几次精益咖啡聚会，就足以使人们接受LeSS。但是，我错了。现在，我认为在引入新的组织结构之前最好花几天时间学习LeSS。 人们确实很需要了解LeSS背后的那些原则。您至少需要几天的时间，才能证明精益思想，排队理论和系统思考是LeSS规则的基础（ 指南：三种导入原则 ）。

旧习惯和针对个体的局部优化在第一个Sprint很快就出现。 我绝对会花一些时间与开发人员一起进行系统建模，绘制因果关系图（CLD）。 人们在使用他人制定的流程和自己拥有的流程之间存在着巨大的差异。 在为期3天的培训中，也可以更全面地介绍一些相关主题。

协调似乎是最热门的话题。因为领域狭窄的专家文化和协调角色在公司里存在很长时间了，人们不相信遵循这些简单的指南（ *指南：Just Talk，指南：用代码交流，指南：社区，指南：开放空间* ）能够来管理协调。在培训开始时，跟协调相关的问题，开发人员写满了三张大白纸。于是，我请他们创建一张简单的表格，该表格只有两列：“要协调的内容”和“协调技术”。 在介绍了所有LeSS协调实践活动之后，我请参会人员在正确的栏中填入合适的协调实践活动。

工作坊向参与者概要介绍了LeSS，大多数人的问题都能得到解答。 但是，我认为这个介绍还是太简短。 我希望当时我能坚持通过系统图例帮助他们更深入地了解LeSS原则，这可能会带来更多的认同以及对系统思考，排队理论和精益思想的更好理解。

<figure>
  <img src="/img/case-studies/mts-kassa/certified-less-basics.png" alt="LeSS Basics认证培训">
</figure>

### 尝试…精益咖啡

在变革的早期阶段，愤怒，不确定性和挫败感达到顶峰。 所有变革管理模型都强调了沟通的价值，而精益咖啡是最大化沟通价值的一种好方法。 它有助于提供诚实的对话并减少未知数的机会。 我发送了一封邮件，并邀请所有人参加精益咖啡聚会。 当时我想“如果没人来怎么办？ 那可就失败到家了。” 幸运的是，有很多人进来，我们进行了有益的讨论。 不幸运的是，对LeSS的概要介绍和培训非常简短。 人们仍然有很多问题，在精益咖啡聚会上他们找到了答案。 我长期使用精益咖啡这种形式，我的经验告诉我，有多少人在喝咖啡，通常就表明他们对这个话题的兴趣程度。

### 选择产品负责人

CTO很自然的被选为了产品负责人。 他是公司的联合创始人之一，比其他人更了解市场，业务和客户。 选择是如此自然，以至于我没想到会有任何副作用，但是几个月后它们就变得可见了。

### 产品待办列表的创建
所有需求都位于一个Redmine工具中。 由于当前的组织设计是基于组件团队的，因此当时的产品待办列表主要包含了针对组件团队的大量技术任务，从用户的视角来看并没有什么价值。 因此，我们围绕着公司愿景和中期业务目标，从头开始创建产品待办列表。
我们在创建过程中使用了可视化的方法。 现在产品待办列表变得可见且有形，由大白纸和便签纸构成。

<figure>
  <img src="/img/case-studies/mts-kassa/product-backlog.png" alt="产品待办列表">
</figure>

### 尝试…使用HitMap分析产品待办列表

LeSS原则之一是以[客户为中心](https://less.works/less/principles/customer-centric.html) 。 这意味着要创建有助于优先交付最高客户价值的组织设计。 我们不确定是否所有的特性团队都应该能够同时工作在三个不同的UI平台上来交付价值。 也许根据客户细分来组建团队是有意义的。 我们希望HitMap能帮我们找到答案。 这是一个非常简单而可靠的工具。 它能帮我们看到每个PBI使用了哪些架构组件。 HitMap看起来大致是这样的：

<figure>
  <img src="/img/case-studies/mts-kassa/hit-map-principle.png" alt="Hit Map 原则">
</figure>

*完美目标*是创建特性团队，以从产品待办列表中选择任何PBI，并在每个Sprint至少一次独立地发布到市场。 假设我们在Android和iOS平台上都需要相同的产品功能。 我们就可能需要创建具有iOS和Android开发能力的特性团队。

我们花了几个小时来创建HitMap。几个月前我就要求产品负责人对产品待办列表进行排序整理，以获得一个长远的视图。 最终，我们在几张大白纸上贴满了便签纸。 当HitMap创建完成后，对于产品负责人来说，为了拥有最大的敏捷性，他显然需要与试点团队类似的全栈特性团队。他计划开发的主要产品功能都需要通过所有三个I/O渠道（web，Android，Windows）进行。

<figure>
  <img src="/img/case-studies/mts-kassa/hit-map.png" alt="Hit Map">
</figure>

### 团队自设计工作坊

HitMap被创建了之后，产品负责人确定他需要全栈特性团队。 我帮助他召开了一个会议，他向所有人介绍了最终的HitMap。产品负责人非常强烈地表达他的观点，创建特性团队的想法没有遇到很明显的阻力。每个人都可以看到跨职能跨组件的特性团队可以为公司提供最大的灵活性，并从产品待办列表中交付最高价值。 接着我们要求大家为组建团队设置约束条件，下列各项就是他们想到的：

* 跨职能（所有开发，测试，devops等）。
* 跨组件（所有平台：Windows，Android，Web）。
* UI/UX技能。
* 人数从6到9人（推荐）。
* 坐在同一房间工作。
* 我愿意和这些人一起工作。

我不在此详细描述这一过程，您可以通过阅读[Ahmad Fahmy的文章](http://www.ahmadfahmy.com/blog/2013/12/5/the-rise-of-the-team)获得更多。

我想列举一些我们看到的有趣现象。 首先，试点小组的成员是被允许加入其他小组的，但没有人离开。 其次，经过两轮（15分钟），我们有了两个稳定的可以满足所有限制条件的团队。 但是，第三个团队仍然缺乏UI/UX技能。 我不得不引导相关的讨论，讨论时间很长，,而最终决定是：

* 团队中的某些人将学习UI/UX。
* 使用*Traveler*这一协调技术（ *指南：Traveler* ）。

团队自设计工作坊之后，我们组织了一些团队建设活动：

* 团队拥有了自己的名字（“阿尔法”，“维加斯”，“星际争霸”，“马戏团”）。
* 玩了“技能市场”游戏。
* 绘制了所有团队的能力矩阵。开发人员评估了他们自己的技能水平，并识别出了他们想要提高的技能。

第二天早上，当我来到办公室时，发现开发人员都已经搬到了各自的新房间。

<figure>
  <img src="/img/case-studies/mts-kassa/self-designing-team-workshop.png" alt="团队自设计工作坊">
</figure>

### 完美愿景

LeSS的基本原则之一是持续改进以实现[完美愿景](https://less.works/less/principles/continuous-improvement-towards-perfection.html)。使用LeSS框架，您可以持续不断地对交付价值给客户加以改进。举个例子，没有额外的角色做协调工作。如果框架将它们包含在设计中，那么如果将其嵌入在系统设计中，人们将有何动力对其进行改进呢？ LeSS的目标是使单团队Scrum在多团队环境中也可以工作，而无需引入新的角色和规则（原理： [大规模Scrum是Scrum](https://less.works/less/principles/large_scale_scrum_is_scrum.html)）。

产品或组织的完美愿景是一个永远无法实现的状态。 在完美愿景的驱动下，人们可以考虑任何实验来进行改进。

我的同事Cesario Ramos给了我一个组织的完美愿景作为例子。 我把它打印了出来分发给所有人，以作参考。我们要求团队提出自己的完美愿景。20分钟后，我们在大白纸上写下了所有想法并进行投票。

在回顾会议期间，我们在做出决策时就提到了完美愿景。例如，曾经有一个想法来创建一个专门的协调角色。这与完美愿景相冲突，团队的代表们否决了它。

<figure>
  <img src="/img/case-studies/mts-kassa/perfection-vision.png" alt="完美愿景">
</figure>

### 完成的定义（DoD）

虽然有试点特性团队DoD为基准，但是我们仍然花了一些时间来设计最终的DoD。 通常，开发人员对测试术语（集成，端到端，功能，压力，性能）有不同的理解。 而且，他们自己的术语过于复杂和繁琐。所以我建议简化分类（ *实验：尝试…简化测试分类* ）。非常奏效。 试点特性小组决定引入与LeSS规则相符的也更严格的DoD。他们的完成定义清单上包括额外的代码审查和更严格的测试覆盖率。

<figure>
  <img src="/img/case-studies/mts-kassa/definition-of-done.png" alt="完成的定义">
</figure>

### Selecting Scrum Masters

In LeSS Scrum Master is a full-time dedicated role that works with 1-3 teams. We were eager to hire an experienced Scrum Master from the market before the day we changed the organizational structure. Unfortunately, it never happened. So I eventually decided to become a second Scrum Master until somebody could replace me. We had 2 full-time Scrum Masters (Sergey Gospodchikov and me) working with 4 teams.

Teams chose the Scrum Masters they wanted to work with by voting and selecting. We facilitated the process of setting up the expectation lists for the Scrum Masters. There were some interesting topics in this list:

* Scrum Master could get a black spot from the team.
* Don’t be offended when you’re fired by the team.

### Learning With Communities

Before the first Sprint, we offered teams to start off the communities. We did it in the format of an Open Space meeting. Everyone wanting to start a community would just come up to the center of the room and announce it loudly, then write down its name on a sticky and put it on the flip-chart. This is how 14 communities were created in less than half an hour.

The first communities were launched in a few days, the rest during the first two Sprints. We made sure they had a Scrum Master support to help them define:

* Purpose of the community.
* Working agreements.

I started and supported Scrum Master Community ([Guide: Communities](https://less.works/less/structure/communities.html)). We met every week for an hour or so to share new practices and Scrum Master techniques. E.g. there were lots of meetings around facilitation and team coaching.

Developers met regularly and participated in the communities with pleasure. I remember a special meeting dedicated to automation testing held with mob-programming technique. One of the designers joined it because she wanted to start studying automation. People wanted to learn!

<figure>
  <img src="/img/case-studies/mts-kassa/communities.png" alt="Starting Communities">
</figure>

### Initial PBR

**Product vision and business model.** It is useful to align developers’ understanding of a product not only on the vision level, but also getting deeper into the *business model*. LeSS product group is a part of a larger organizational context with marketing, sales, compliance, legal. and so on. That is why we started Initial PBR with teams filling business canvases and then merging them into one. We discussed all the business model sectors one by one and the Product Owner corrected us.

<figure>
  <img src="/img/case-studies/mts-kassa/business-model.png" alt="Business Model">
</figure>

### Try...Item Splitting Workshop.

It is a typical problem: teams not being able to slice PBIs into smaller ones. It becomes even more important when you have feature teams because we want to reduce the variability with smaller batches and thus reduce the overall cycle time. We suggested teams to conduct a splitting workshop with all teams participating.

I distributed the sheets of paper with patterns and examples of splitting items (*Experiment: Try... Split Product Backlog items*). Then I started the timer for 10 minutes and asked the participants to read the document. The most effective way to learn is to teach other people, so after 10 minutes I asked them to form pairs and gave them 10 more minutes to share learning material. The Product Owner then selected a big PBI from the Product Backlog. People formed small mixed groups and they started splitting it.

After 20 minutes we merged and asked each group to share their results. We highlighted the most successful splitting options. I used to bring splitting patterns sheets to all the PBRs during the first Sprints so that it could be easily referred to.

### Try...Estimation and Correlation Net.

When multiple teams work on the same Product Backlog, there is a need to align units of estimates. The pilot feature team already had an experience with relative-size estimates and had many done items. We created an *estimation net* where we placed done items for benchmarking. Then I facilitated a workshop in which pilot feature team members explained to other developers *reference PBIs* and helped them to align the story points.

<figure>
  <img src="/img/case-studies/mts-kassa/estimation-net.png" alt="Estimation Net">
</figure>

**Facilitating first multi-team PBR.** Before the LeSS implementation teams were getting specifications from a dedicated analysis group. Now they were responsible for clarifying the details of each item themselves. We invited the domain experts to the room. Teams formed mixed groups and organized at four stations by different wall areas. Each station had an expert helping them in clarifying the PBI. In 25 minutes, everyone moved clockwise to another station (except the anchoring experts). The previous group already left notes, diagrams and explanations on the flip chart and it really helped. Thus, the teams needed a little bit more than an hour to clarify three PBIs. After the break, we repeated the process again.

<figure>
  <img src="/img/case-studies/mts-kassa/first-multi-team-refinement.png" alt="First Multi-team Product Backlog Refinement">
</figure>

## Adopting LeSS Structure

Remember the product group had a component structure? Now, after the team self-design workshop the structure changed and developers formed 4 new feature teams. Each team was a cross-component cross-functional autonomous unit that could take potentially any PBI from the Product Backlog. The Teams’ names were: “Alfa”, “Vegas”, “StoreCraft”, Hotfixies”.

<figure>
  <img src="/img/case-studies/mts-kassa/team-structure.png" alt="Team Structure">
</figure>


In the old structure, there was a business analyst team with four people in it. Those guys knew the product and its domain really well. Product support decided whether any customer request should go to the development group or should be managed by customizing product settings. Most of their time, they were writing the specs and pushing them on the component teams.

**Fundamental failure of a LeSS adoption.** I recommended putting business analysts inside the teams and they got an invitation, but actively resisted the new process and LeSS adoption. We left them outside the teams and the Product Owner asked them to represent him during the multi-team PBRs. That was an unskillful idea and fundamental failure of a LeSS adoption. The idea is that real customers and users (not BAs) talk directly with real coders, with no one in between, and the ex-BAs volunteer to join teams and become regular team members. This situation is the opposite of key rules & guides in for LeSS adoption. So this was not a normal/healthy adoption because this basic element was not fixed, due to a lack of understanding what volunteering in LeSS means, and the importance of removing BAs as middlemen.

**My failure in understanding volunteering principle.** One of the three principles of adopting LeSS is use *volunteering* (*Guide: Three Adoption Principles*). The product group and I misunderstood volunteering. it includes the meaning that no one joins the product group unless they have fully understood the LeSS rules, and volunteer to follow them. We had "anti-adoption" people in the adoption, which is the opposite of what is meant to happen.

From that moment we had people who were not volunteering to join a LeSS adoption, who were still inside the adoption and fighting it. That caused lots of pain and frustration because “anti-adoption” people tried to undo the changes. They were eager to revert everything backwards to the previous status quo and component teams structure.

**Middlemen create waste.** The BAs stopped creating specs and handing them over and started collaborating with teams on the Product Backlog Items. Unfortunately, their focus moved to acting as middlemen in between the developers and customers/users:

* Talking with stakeholders (partners, internal marketing, sales, compliance).
* Talking with customer support.
* Talking with customers.

Those were exactly the things that the real developers are meant to do in a LeSS adoption. But middlemen positions continued to create the wastes and problems intended to be eliminated in a LeSS adoption.

**Release manager.** Another coordination role that was still left in place for a while was the release manager. The automation testing package was small at the time of the structural change and the group suffered from lots of manual end-to-end testing. That was a job of the release manager who was the most competent for that. This kind of testing became a part of the Definition of Done (DoD) at once and teams started doing this on themselves meanwhile expanding the automation pack in order to get rid of the manual testing.

In the previous component structure, the release manager was the one who made the final decision if the increment was shippable or not. She got the invitation to stay in any team, but declined the offer. This was again the point of how I misunderstood the volunteering principle of LeSS adoption.

The positive point was that the release manager didn’t resist the LeSS process, actively participated in the LeSS events (multi-team refinements, Overall Retrospective) and led one of the communities (system testing). In two months, the teams grew their skills and each teams could ship the increment to the market themselves.  By that time, the release manager joined one of the teams as the second full-time Scrum Master and replaced me. That was my recommendation because I noticed she had the right mindset, was eager to learn and wanted to help people using the facilitation style instead of command and control.

**Management.** All the management roles in development were disbanded officially all at once. Coordinators and managers now became developers in the teams. Therefore, the titles ‘team leaders’ and ‘tech leaders’ did not exist anymore. There were still a support and training departments that were headed by their own managers but they were not included in the LeSS group. I think, in the future they could be absorbed by the LeSS product group and DoD would be extended by adding new activities: creating video and website tutorials for the clients.

## Learning to Sprint With LeSS

### First Sprint

As the Russian proverb says, "you must spoil before you spin". This was true for the first Sprint. Despite all preparation and training, the teams met the evil of local optimization face to face. There was no customer-centric Product Backlog in the company before. Now the order in the Product Backlog was determined primarily by importance for the customer.

When Android developers and designers looked at the Product Backlog they could see there was not enough work for them for the first Sprint. And they had to spend a lot of time in the Sprint studying and helping others. This is a common pattern in Scrum adoptions: for the first time, the “knowledge debt” that was always there but hidden in the silos suddenly becomes painfully visible. This is especially true in large-scale adoptions, where the silos (and knowledge debts) are large. This new “organizational transfer of learning” (to use the language of the original 1986 HBR Scrum paper), was so unfamiliar for people in the group, that some were uncomfortable with teaching and learning, rather than “doing something productive.”

We discovered some problems that we did not take into account during the start-up. E.g. how to deal with incoming urgent tasks and bugs from technical support. Also, we did not take into account how to do regression testing in advance. Unfortunately, there was a huge technical debt and the automation tests coverage was low.

I also noticed that people were quite tired from lots of training and a long (3 days) kick-off. Nevertheless, the first Sprint Review was successful. The teams had PBIs to show during the Sprint Review. And the internal stakeholders who came to the event gave them positive feedback.

During the first Sprint a lot of questions arose and accumulated. There were so many similar questions from the teams that at the end of Sprint Review I suggested to hold a longer-than-usual Overall Retrospective with everyone from the product group participating. It took us three hours and a lot of patience. The outcomes were:

* Script for those developers who had not enough work during the Sprint for their primary skill: help someone in the team (through pairing), continue learning new skills, help other teams.
* How to do regression testing and actually release the increment. We clarified the previously created Definition of Done (DoD) and expanded it.
* How to process urgent tasks and bugs during the Sprint: they were communicated through the separated slack channel and any team with a free capacity could take it.

The first Sprint was not easy but the Product Owner and most of developers were committed to moving forward and succeeding.

### Adopting Visual Management

**Visual management for the Product Backlog.** We visualized the Product Backlog (*Experiment: Try... Visual management for the Product or Release Backlog*) from the start. The Product Owner and the two people opposing the Scrum adoption that therefore should not have been part of the group (the 2 business analysts) maintained Product Backlog that also was there on the wall up to date. Each PBI was represented by the sticky on the board. Items moved from left to the right along the wall, getting to the “ready” state and finally becoming a part of the Sprint Backlog.

**Visual management for the Sprint Backlog.** I suggested teams to visualize their Sprint Backlogs and limit work in progress (WIP). We conducted a short workshop on limiting the queue size and played [FeatureBan](https://www.agendashift.com/featureban). I think that this short game perfectly demonstrates why you need to limit your WIP and how better manage the queues. Each team set explicit WIP-limits for the Sprint Backlog.

**Visual management helps in collaboration.** In LeSS there are no dependencies between teams. Why? Any feature team can work across the code base for their items. And teams manage their coordination between themselves, applying ideas such as continuous integration, communities, multi-team workshops, and sharing and swapping work. So there are only opportunities for collaboration and shared work.

During Sprint Planning Two we found it helpful to mark PBIs that needed collaboration between several teams in an upcoming Sprint. Usually it was just an additional small sticky with coordination technique written on it (e.g. "scout", "component mentor", “just talk” etc.).

**Visual management for working agreements.** All major working agreements (DoD, "ready" etc.) and Retrospective decisions were kept in the same room along with Product Backlog. We put LeSS events schedule in a visual schedule and hung it in the corridor. There was also a communities events schedule next to it.

<figure>
  <img src="/img/case-studies/mts-kassa/visual-management.png" alt="Visual Management">
</figure>

### Try...Visual Meetings.

I'm a fan of David Sibbet and concept of **visual meetings**. I like to visualize everything during the meetings. I call visual meetings "alive" because they stimulate a high level of participation, create a big picture of what is going on, and support a group memory. Here is what distinguishes "alive" meeting from the "dead" ones:

* Participants are standing and have an active discussion.
* Working in small groups (up to 5 participants).
* No electronic devices, just stickies, markers, scissors, flip charts and paper.
* Visualising everything that is being discussed (everyone is heard).
* Cycles of diverge and merge which help teams to benefit from working in small groups and autonomous discussions as well as synchronizing with others during the plenary (merge).

<figure>
  <img src="/img/case-studies/mts-kassa/visual-meetings.png" alt="Visual Meetings">
</figure>

### Coordination

It is interesting that the team saw coordination as the most important issue before being introduced to LeSS. I noticed during lean coffee that most of questions were about coordination. We closed the issue quickly. Before the changing structure all-at-once, we had a [Certified LeSS Basics (CLB)](https://less.works/courses/less-basics.html) training where we discussed coordination. From what I have observed that the most common coordination practices used then were *Guide: Communicate in Code*, *Guide: Just Talk* and its more advanced version *Just Shout*. Teams also picked up the needed practices just-in-time during Sprint Planning Two. LeSS relies on emerging coordination based on self-organization. One of the important elements of self-organization was the location of all the teams in the side-rooms connected with one big corridor. We also had a joint room with all information radiators in it.

### Sprint Planning One

One hour before the first part of Sprint Planning, the Product Owner with the two business analysts made final changes to the Product Backlog. Then representatives from all teams (usually 2 people per team) participated in Sprint Planning One.

**Meeting agenda**. We usually followed the following agenda:

* Product Backlog update (return not done work to the Product Backlog and reestimate the remaining efforts).
* Product Owner briefly describes the top of the Product Backlog and clarifies the final minor details of the items if requested.
* Look at the Definition of Done (DoD) again.
* Team representatives physically select the PBIs from top of the “ready” column and put them in their team’s swimlanes on a board.
* Find the opportunities for collaboration between the teams and visualize them on the board.
* Decide if teams need *multi-team* Sprint Planning Two.
* Define a common Sprint Goal for the whole product group and/or individual Sprint Goals for the teams.

<figure>
  <img src="/img/case-studies/mts-kassa/sprint-planning-one.png" alt="Sprint Planning One">
</figure>

**Sprint Goals**. LeSS does not mention the Sprint Goal, as one of LeSS principles is [Large-Scale Scrum Is Scrum](https://less.works/less/principles/large_scale_scrum_is_scrum.html), so LeSS does not duplicate *elements* in the Scrum Guide (*to avoid repetition*).

**The Examples of Sprint Goals in LeSS**. The question appears - whether to define one Sprint Goal for the whole product group or each team should have their own Sprint Goal, or both? There is no right answer. All options are possible in my humble opinion. Here are a few examples:

1. The common goal of the first Sprint was "Kick-off LeSS". Besides that, Alfa team had their own goal “create an order for the cashier”.
2. The common coal of the second Sprint was "say goodbye to the legacy of component teams", each team had additional goals "completing the module of import of goods", “complete the order creation for the cashier", "cashier + MGTS ", "release + yandex OFD".
As you can see, different combinations are possible. I personally like when the whole product group defines a common Sprint Goal.

### Sprint Planning Two

The second part of the Sprint Planning in our case was trivial. As all coordination possibilities were revealed in the first part, the teams determined whether the planning of several teams together should take place. In this case, teams decided to conduct Sprint Planning Two in a big joint room (*Guide: Multi-Team Sprint Planning Two*). But usually teams just went to their rooms and with the help of the Scrum Masters created their Sprint Backlogs. It took around 30-40 minutes maximum. Now, my recommendation for the Sprint Backlog tools goes in line with the LeSS guide (*Guide: No Software Tools for Sprint Backlog*):

> Don’t use any software tool for Sprint Backlogs; just use physical visual management, probably cards on a wall (Large-Scale Scrum: More with LeSS)

<figure>
  <img src="/img/case-studies/mts-kassa/sprint-planning-two.png" alt="Sprint Planning Two">
</figure>

### Learning Refinement in LeSS

In Large-Scale Scrum PBR becomes a mandatory *event* (rather than *activity*). That happens because PBIs are really huge in large product groups and there’s a strong need for broad learning and coordination across the teams, and a practical need to schedule a minimum number of meetings with customers and users.. In LeSS, there are several options for conducting PBR (*Guide: Product Backlog Refinement Types*):

* Overall PBR with team representatives that implies high level analysis and visioning, estimation and splitting items (*Guide: Overall PBR*).
* Multi-team PBR. Several teams in one room refine several PBIs at the same time (preferred) (*Guide: Multi-Team PBR*).
* Single-team PBR. As in usual single-team Scrum.

There are no rules on the combination of PBRs you should have, however LeSS recommends conducting multi-team PBR. Let’s look at it closer.

### Overall PBR

In the first Sprint it took us several hours for the overall PBR through it should be a shorttish event. Everyone was exhausted. In the next Sprints the time was reduced twice with better facilitation. The open discussion format took so long time, disengaged people and felt boring. I strictly timeboxed all the activities and suggested to conduct an event standing to keep the energy up.

We stuck to the same facilitation pattern. The Product Owner selected the next PBI to discuss and pulled it from the wall. Then he answered clarifying questions for 5-10 minutes.

Then an express estimation followed. If PBI was more than 13 points we split it (Experiment: Try... Prefer cell-like splitting over treelike splitting).

<figure>
  <img src="/img/case-studies/mts-kassa/overall-product-backlog-refinement.png" alt="Overall Product Backlog Refinement">
</figure>

### Multi-team PBR

One could think - why do several teams need to work in one room and to refine several PBIs at the same time? Wouldn't it be more *locally* “efficient” for each team to conduct their own single-team PBR? Let’s figure that out.

**Adaptiveness**. If several teams know several PBIs then the Product Owner can decide as late as possible which PBIs to offer for the upcoming Sprint, not constrained by limited knowledge in particular teams. It gives additional flexibility in changing priorities for the Product Owner.

**Understanding product**. The more PBIs teams know the better they understand the business domain and the product itself. And more brains thinking about the items creates a more thorough clarification, considering aspects that only one team might miss (*Principle: whole product focus*).

**Coordination based on self-organization**. When teams know many PBIs they can help each other in the Sprint. Therefore, a coordination based on self-organization emerges. This is how it looks with a *system model*:

<figure>
  <img src="/img/case-studies/mts-kassa/multi-team-product-backlog-refinement-system-model.png" alt="Multi-team Product Backlog Refinement System Model">
</figure>

### Multi-team PBR complexity

There are many benefits you can get from multi-team PBR. Nevertheless, there are issues. Let’s look at them.

**Information overload**. The more teams are in the same room participating in multi-team PBR the more PBIs they know together. So information overload can be the side-effect of multi-teams PBR.

**Facilitation**. It is not easy to facilitate the event with dozens of people participating. When facilitated badly it causes wastes and developers no longer want to be part of multi-team PBR. Let’s explore that in a system model:

<figure>
  <img src="/img/case-studies/mts-kassa/multi-team-product-backlog-refinement-complexity-system-model.png" alt="Multi-team Product Backlog Refinement Complexity System Model">
</figure>

### Tips for Multi-team PBR Facilitation

I want to share a few tips that I used for making multi-team PBR more effective.

**Thorough preparation**. It may take up to several hours to prepare. It includes but is not limited to: meeting with the event stakeholders beforehand, developing facilitation plan, visualization on the flip-charts (purpose, agenda), and the preparation of the room before the event (removing tables, chairs, putting flip-charts etc).
* **Warming up**. In my opinion it is important to start any LeSS event with a small game or icebreaker to turn on participation. You can find a lot of these activities in the book [Moving Beyond Icebreakers](http://www.movingbeyondicebreakers.org/).
* **Small groups**. You can effectively facilitate a meeting with a large number of people using small groups and other decentralization techniques. There are many formats of working in small groups in the book [Facilitator's Guide To Participatory Decision Making](https://www.amazon.com/Facilitators-Participatory-Decision-Making-Jossey-bass-Management/dp/1118404955).

> Centralization destroys energy; decentralization creates it (Large-Scale Scrum: More with LeSS).

**Mixed groups**. In addition to a previous recommendation, it is preferable to work in small groups that include members from different teams.

> Start by forming temporary mixed groups with people from each team. For example, two teams re-form into two mixed groups (Large-Scale Scrum: More with LeSS).

 This is the way to enhance the collaboration between the different teams and decrease the information scatter. Every member of the individual team becomes is a part of common knowledge puzzle.

**Diverge-Merge and rotation**. In addition to previous two recommendations, these are two more usable techniques for large facilitations. First one is giving a PBI to each small group, let them work in parallel at several stations and refine until “ready” state, then merge everyone into an open discussion.

> Groups spend some time working separately in different areas of the room for refinement on different (or identical) items, and then spend time all together to share insights, ask questions, and seek other coordination opportunities (Large-Scale Scrum: More with LeSS).

Rotation means that small groups move clockwise from station to station in several rounds, while the business experts stay still on the station. Every station works on its own PBI. I like this practice very much and I have multiple experiences of its effectiveness. Imagine that after the first round that takes approximately 20-25 min, another group approaches the station. This group is not familiar with the feature yet but they have an information regarding acceptance criterias, graphics, etc., created by previous group that occupied that station. All they need is just grasp the new information.

**Visual management**. Often when people use electronic devices during the meetings, these meetings become dead. Somebody becomes a bottleneck with keyboard in his hands, the rest are also bored looking at their phones. On the other hand, scissors, paper, stickers, and flip-charts stimulate the collaboration.

**Work standing**. If possible I take off all the chairs from the room where I conduct a multi-team PBR beforehand. Meetings with people standing are more dynamic, people are engaged, have more energy and stay focused.

**Definition of "ready"**. Teams thrive when they share the same definition of “ready” for the PBIs they refine on the station because it reduces variability a lot. Here is the first version of the “ready” we agreed on the start:

* There is a size estimate (in points) for each PBI.
* There is business value estimate from the Product Owner.
* PBI is less than 13 points, otherwise it’s split.
* The understanding of the feature is at least 7 out of 10 where 10 is an exceptional understanding of the PBI, no other clarification needed.
* If graphical interface needed, there is an HI mockup.
* Acceptance criterias are in place.

**Strict timeboxing**. Do not let the meeting "fall apart". Use strict timeboxes for all activities and rounds of the world cafe (rotate) and alert the group with a signal. When the time is up don’t be afraid to explicitly stop the group and ask them how much time they need more.

**Feedback**. Conduct a small retrospective at the end of each PBR event. I asked everyone to evaluate the effectiveness of an event on the scale of 1 to 10 voting with a sticky with detailed feedback written on it.

We experimented with different formats of multi-team PBR. As a result, after some time, we achieved a stable format of it that we didn't change much afterwards:

* Teams, the Product Owner (optional) and experts participate in multi-team PBR.
* Mixed groups are organized.
* Mixed groups select Product Backlog Items they want to discuss and bring them to the station.
* Work at the stations, estimating, refining and writing acceptance criterias up to the “ready” state. If necessary groups add mockups, diagrams, examples and other graphical explanations.
* Experts stay at the stations while other participants move in across the room (world cafe) and explore the PBIs refined by other groups.

<figure>
  <img src="/img/case-studies/mts-kassa/multi-team-product-backlog-refinement.png" alt="Multi-team Product Backlog Refinement">
</figure>

I found that both parts of the Sprint Planning take no more than an hour and a half (two hours maximum) when a multi-team PBR is done properly. Multi-team PBR has become a key event in this adoption as it was a driver for coordination, better product understanding and adaptiveness.

### Sprint Reviews

The early Sprint Reviews were conducted without end users, and Product Owner invited internal customers only. Teams wanted to practice in running these events before inviting guests from the market. That is why the first visitors of the Sprint Reviews were employees from other departments: technical support, marketing, sales, HR, and compliance. I will describe the usual Sprint Review:

* The Product Owner opens the meeting and reads loud Sprint Goal(s) the product group worked on. The Product Owner says which items are done.
* Teams shared shortly the main obstacles during the Sprint and how they coped with them (or not).
* Guests were invited to visit one or more stations in a format of the bazaar or a more structured format of the *tradeshow*. In each station we had at least two developers, one of them demonstrated increment and then asked for an open feedback, another one silently wrote things down.
* After a demo we got back to the open discussion format. The Product Owner shared the market news, changed ordering (if any) and answered the questions.
* When guests left the room, the teams and the Product Owner merged feedback from multiple stations and could updated some of these artifacts: impact map, value-proposition canvas, story mapping and, of course, Product Backlog.

**The whole product focus**. I noted that the developers who were not actively engaged on the stations moved actively between stations and gave feedback to their peers. They became genuinely interested in work of others. Small groups were formed here and there with interesting discussions regarding the product.

<figure>
  <img src="/img/case-studies/mts-kassa/sprint-review.png" alt="Sprint Review">
</figure>

### Try...Innovation games.

End users visited the development site once per two Sprints. We often used two innovative games that perfectly complemented each other: “speed boat” and “prune the tree”. Speed boat is good in identifying the customer pains and jobs to be done. *Prune the product tree* is a well fit for finding better solutions (features) for the Product Backlog.

<figure>
  <img src="/img/case-studies/mts-kassa/prune-the-product-tree.png" alt="Prune the Product Tree">
</figure>

### Team Retrospectives

For me, the Retrospective in Scrum was always a special event. Moving from a component team structure to feature team structure is a large shift for people. That is why I expected that a zillion problems/questions would arise in the early Retrospectives. And I was right. The first Sprint was a great stress for all the teams and we combined the Overall Retrospective with team Retrospectives in one big event, because almost all the issues were the same and it was important to include the whole product group in problem solving. Everyone's participation and *SMART* actionable improvements had a great influence. Stress significantly decreased and in the following Sprints, each team conducted its own separate team Retrospective, in addition to an Overall Retrospective

**System and team-level impediments**. As system issues are discussed during the Overall Retrospective, I always asked teams to separate system impediments from the team ones. I often started with a *circles of influence activity*. I introduced the flip-chart with two embedded circles drawn on it, the inner circle was filled with topics the team was able to sort out by themselves, external one was filled with the cross-cutting concerns.

<figure>
  <img src="/img/case-studies/mts-kassa/team-retrospective.png" alt="Team Retrospective">
</figure>

### Overall Retrospectives

The end of the Sprint was at the end of the week (on Friday) and that is why it was decided to conduct Overall Retrospective on Tuesday afternoon, early in the next Sprint. Its permanent participants were the Product Owner, Scrum Masters, and team representatives.

**Perfection vision and eight topics for discussion**. At the kick-off, the teams created the perfection vision. This is a never truly reachable check-list of how an organization may look in ideal. Any decision made during the Overall Retrospective was inspected in order to see how it was aligned with with the perfection vision. Overall Retrospective is focused on eight topics which you can see [here](https://less.works/less/framework/overall-retrospective.html). We reminded them on each Retrospective and a lot of issues that had been forgotten and that were not in focus.

I'd like to list a few issues that were discussed during those Retrospectives:

* Completion of all DoD criterias by all teams.
* Strengthening Definition of Done (DoD).
* Production bugs distribution within a Sprint.
* Teams interaction with tech support group.
* Changing the release cycle.

<figure>
  <img src="/img/case-studies/mts-kassa/overall-retrospective.png" alt="Overall Retrospective">
</figure>

### Learning to Work With 7 Teams

It became a big surprise when I learnt that MTS and LiteBox in 2017 had agreed to increase the number of teams to 7. So just after the structure changed even more new teams were added to the product group quickly.

**RITG team from outsourcing partner**. The Product Owner felt very enthusiastic starting new teams and he created a partnership with one of the outsourcing companies in the city. In several weeks, a new team named RITG was added to the product group. During several Sprints, we tried to integrate the people in the process and we failed miserably. We suffered from communication problems during PBR(s) heavily. Besides, they didn’t show up in the Sprint Review and then I recommended to bring them physically to the office. It was not an easy thing to do but despite that the Product Owner succeeded. From that moment we had 5 co-located teams in the office.

**ROST team in the office**. Meanwhile the internal HR function helped us to create another feature team named ROST. Two member of the former pilot feature team joined it for several Sprint to make the transition more comfortable for them.

**Remote team from Ukraine**. MTS Kassa had several developers in Ukraine from the very start of the product. Those people even took part in the initial Scrum training. We agreed to not include them in the product group until they could form a co-located feature team in Kiev (they worked remotely and lived in different cities in Ukraine). And it finally happened.

**Unfortunately more middlemen**. I mentioned before that one of the key failure points of the adoption was involving people that didn’t support the change initiative and acted as the middlemen between teams and the customers. The number of teams grew and the dysfunctional business analysis group increased as well. There has been hired a new business analyst with focus on outward activities. This is how the structure looked at that moment:

<figure>
  <img src="/img/case-studies/mts-kassa/seven-teams.png" alt="Seven Teams">
</figure>

### Moving Focus From Local to System Improvements

During the first months, we were focused on establishing useful processes within a new LeSS structure, holding LeSS events skillfully (believe me, multi-team PBR and Sprint Review are not easy things to implement effectively) and indeed improved a lot. At the beginning most of the developers were new to LeSS and most of the problems we coped with were:

* Learning and growing multi-functional people.
* Helping each other during the Sprint.
* [Swarming](https://sites.google.com/a/scrumplop.org/published-patterns/product-organization-pattern-language/development-team/swarming--one-piece-continuous-flow) over PBIs.
* Sprint Backlog tooling.
* Limiting WIP in a Sprint Backlog.

Coordination between feature teams and communities worked like a charm from the very start. Anyway, after some time, it became clear that most of the issues we should focus on are on the system level. Roughly all the system issues were related to 3 big topics: technical debt, CI/CD, and flow of requirements from ideas/stakeholder request to delivery.

### Communities Over the Time

**Communities were still alive**. After 7 months, 5 communities were still alive (CI/CD, QA, Scrum Master, UI/UX, frontend), 2 (CI/CD and backend) merged into one (CI/CD) and others died. And that is normal. The processes of birth and death should be natural for the communities.

**Coordination**. Communities met regularly once per week or two. Each community had its own slack channel for communication. During the early months Scrum Masters were heavily involved in facilitating their meetings, but when time passed the people became more skillful and learned to facilitate by themselves. Anyway, the Scrum Master service was still available by demand and sometimes communities asked for it. For example, I remember an important point for a frontend community when they had to choose one of the several frameworks. That was really a tough and complex decision. They needed help and invited a Scrum Master who helped them to reach the consensus finally. Each community had its own wall space in a big room where they placed the announcements.

**Communities recommend PBIs for inclusion**. Quite often the result of the meetings were a set of technical PBIs and improvements that community recommended the teams and product owner for the inclusion in the Product Backlog.

<figure>
  <img src="/img/case-studies/mts-kassa/community-boards.png" alt="Community Boards">
</figure>

### Changing Requirements Flow Over the Time

**Multiple problems with requirements**. Looking at the system issues raised in Overall Retrospective, it became clear that many of them were related to the flow of requirements. And indeed, during the first months I was concentrated on the teams coaching and events facilitation. I didn’t have enough time to coach the Product Owner and/or the group of BAs unwilling to join the LeSS adoption, and so didn’t spend enough time with them. I got feedback from the main internal stakeholders (marketing, sales mostly) that they were not satisfied with the product group. It was a black box for them and they told me the Product Owner didn’t pay enough attention to their requests. Another thing was - I realized the flow of items from the Product Backlog to the Sprint wasn’t good enough. PBR(s) didn’t go as smoothly as I wanted them to be and sometimes the teams select too-vague (“unready”) features for the Sprint. I suggested to focus on the flow of requirements and this is what we’ve done.

**Product workshop**. I have conducted an intensive 2-day on hands workshop for the Product Owner, the group of BAs, Scrum Masters and team representatives during which we have:

* Aligned product vision using elevator pitch format.
* Thoroughly analyzed and discussed each of the 8 customer profiles using jobs/pains/gains template.
* Created a business goal for the next quarter and made it SMART (decrease the churn rate).
* Created an impact map and and prioritized the impacts.
* Filtered features in the Product Backlog with regards to the impact map.
* User story mapping for some of the big features in the Product Backlog.

The Product Owner now was armed with new tools and also he saw the strong connection between the vision, business goals, customer goals, and features. From that moment, we suggested the teams to have a different format of overall PBR and multi-team PBR(s).

<figure>
  <img src="/img/case-studies/mts-kassa/product-workshop.png" alt="Product Workshop">
</figure>

### Adjusted Refinement Process

Just after the product workshop, we invited the teams representatives (they were rotating each Sprint to avoid privileged or single positions) and collaboratively co-created a new process for overall- and multi-team PBR(s). This is what we came to.

<figure>
  <img src="/img/case-studies/mts-kassa/adjusted-product-backlog-refinement.png" alt="Adjusted Product Backlog Refinement">
</figure>

**Overall PBR**:

* Shortish discussion and a quick estimation
* If estimated more than 13 points the feature is analyzed with story mapping or splitting patterns.

**Single-team PBR**: only for the team based in Ukraine.

**Multi-team PBR**:

* Conducted 2 times per Sprint for the different set of 3 teams.
* Detailed discussions.
* Acceptance criterias created.
* Estimation refined if necessary.

A new process of working with the requirements was much better than the previous one. Firstly, the process became more disciplined. We explicitly defined the inputs and outputs of each step. Another important thing was that each feature now was clearly expressed in with relation to customer and business goals which is important for intrinsic motivation. Every team went to the decomposition workshop again and learned a story mapping technique. Indeed, in a few Sprints the new process turned out highly enjoyable for the teams (at least they told us so) and the flow improved. Now we had less surprises during the Sprints, the Product Owner had a more free time (he visited only overall PBR), and the cycle time decreased.

## Lessons Learned & Resulting Experiments

Some of the experiments (*Try...Avoid...*) you could read during the text as they were a great fit to the case story line. Below you can find some of the experiments that emerged after I retrospected the whole LeSS adoption. You may think of them as my lessons learned.

### Avoid...Bringing Sceptics On Board

In a typical hierarchical functional organizational design, people work as machine cogs and perform only one function. But people have the meta-skill of learning and can become more flexible in team-based organizational design (*Guide: Build Team-Based Organizations*). Just before changing the teams structure I noticed some people being explicitly unhappy about the fact that the company would become a team-based organization. They really wanted to be narrow single-specialists, were really unhappy about Scrum and were very explicit about that. They didn’t hide their motives and were really straight. To be honest, I wanted to get LeSS as soon as possible and now I understand that was a huge mistake. You cannot even imagine how much damage and harm just a couple of people can make if they really want to undermine the change. There is a [useful video](https://www.youtube.com/watch?v=Wdroj6F3VlQ) by Dr. Kotter talking about the resistance and his advice is:

> “Get them out of the way no matter who they are in terms of power of relationships to you because if you let them inside the tent they will do so much damage that the change will be undermined”.

### Try...Flipping Later With Volunteers Only

Instead, prepare the structure well and use 100% volunteers if possible. That will save your time and make the LeSS adoption more enjoyable for all parties.

### Avoid...Teams and Scrum Masters Report to the Product Owner

As I explained before, CTO as a Product Owner was a natural choice for us. Still in a few months we got a negative side effect. As the company management forecasted the customer base grew rapidly and the product group become under a large pressure to deliver more. New requests usually came from marketing, sales, and new clients asked for customized solutions etc. It fell out of my attention that the Product Owner hired and fired developers as he did it before the changing structure, nothing actually changed. Teams directly reported to him. For instance, developers wanting to get a salary raise needed to approach him and start negotiations. I want to include a quote from the *Guide: LeSS Organizational Structure*:

> “An important point in this organizational structure is that the Teams and the Product Owner are peers—they do not have a hierarchical relationship”.

One of the Scrum Masters told me that Product Owner started questioning the teams forecasts, put pressure on them and was chronically unsatisfied by their performance. Scrum Masters did their best and protected teams as they could but once during the Overall Retrospective they had a conflict with the Product Owner and were warned they could be fired. We managed to resolve the conflict but from that moment it was obvious Product Owner being a boss for the teams is an organisational impediment. And it is in our Impediment list. Still working on it.

### Avoid...Scaling When DoD Is Not Shippable

DoD and transparent shippable increment each Sprint is the heart of Scrum but it becomes even more important in the scaling environment. Why? Adding new teams and having a weak DoD means you scale the dysfunctions too. Undone work accumulates even quicker with more teams. Don’t add new teams if your technical debt is large, adding new teams is like putting out the fire with a gasoline. Instead focus on removing the undone and making the Increment completely transparent.

### Try...Make DoD As Detailed As Possible

After a first draft of Definition of Done (DoD) was created a few Sprints passed until we noticed that DoD wasn’t followed by all the teams equally. We started to investigate the issue and found out that the first version of it wasn’t detailed quite enough and could be interpreted in different ways. Not all terms and words had the same meaning for all the teams. The agreement wasn’t 100% clear. Therefore, we collaboratively clarified the DoD again and made it as detailed and specific as possible. Now I recommend you to use the following format for defining the DoD: put it on the flip-chart and create two columns. Activity column where you describe the activity itself and criteria column answering the question: how can we measure or clearly understand that activity is really completed? Be prepared to spend 2-3 hours on clarifying the DoD, but it’s worth it.

<figure>
  <img src="/img/case-studies/mts-kassa/definition-of-done-format.png" alt="Format for the Definition of Done">
</figure>

### Try... Explain DoD Defines Adaptiveness

I find that many product groups find the DoD quite a formal check-list and are not aware of the fact that DoD indeed defines how adaptive they are. I also found that teams and business start looking at the DoD more seriously when you show them that DoD defines their agility. Use system diagrams for that. I did it several months after the LeSS launch and now will do at the start of any further LeSS endeavor.

<figure>
<img src="/img/case-studies/mts-kassa/definition-of-done-system-model.png" alt="Definition of Done System Model">
</figure>

### Try...Mature and Courageous Scrum Masters

Scrum is a big change even for the single-team context. Having a *courageous* Scrum Master seems to be one of the key success LeSS adoption factors. By courageous Scrum Master I mean a solid and experienced person that is able to talk about unpopular things and able to uncover the ugly truth. One of my clients (a big bank) decided to hire inexperienced young university graduates and make them Scrum Masters. The experiment failed miserably. The young people were able to learn how to facilitate. They prepared great looking flip-chart and drew lovely burndown charts. But they never became change agents and were unable to remove any organizational impediment. They were not mature enough and were not prepared for working under pressure. In MTS Kassa it was a pleasure to work with 2 great and mature Scrum Masters that protected the teams, sometimes directly confronting a Product Owner and senior management. Thank them!

### Try...Learn From Other LeSS adoptions

In 2018 I helped three companies with their LeSS Adoptions and knew lots of people, both Product Owner and Scrum Masters. One of the companies that adopted LeSS in Russia in 2018 was DoDo Pizza. They were especially strong in engineering practices. The Product Owner asked if he could visit and see how LeSS was implemented in that company and I helped him to get there. He came back with lots of insights and I guess that was very helpful as many technical related PBI went up in the Product Backlog just after that. That never happened before.

### Try...Obtain an Experienced LeSS Mentor

During MTS Kassa adoption I was not completely alone. By that time I had help from a very experienced mentor Cesario Ramos who is a Certified LeSS Trainer (CLT). We communicated through chat and also co-trained three Certified LeSS Practitioner (CLP) classes during a year. During co-training I could hear many war stories from Cesario and also observed him while answering tricky questions from students. Each training I learned something new from him, every class was unique. Besides the co-training my mentor supported me in providing his personal materials for different workshops by request: perfection vision, product definition, people and rewards in LeSS. Having an experienced LeSS Coach as your mentor is one of the best things that have happened to me and can happen to you. It’s an accelerated personal growth!

## Outcomes

It was one of the most dynamic transformations I had ever participated. My coaching engagement started in Jan 2018 and still continues. More teams are planned to be added to the product group by the end of the year. Apparently it also will be necessary to add one more channel (iOS).

When I asked the Product Owner, who was also CTO of the company, what the most valuable things were, that he learned with LeSS, he mentioned a few points:

* The ability to scale painlessly by adding independent feature teams.
* Transparency in priorities (one through the Product Backlog) and clear overview of what is going on and progress.
* Fast value delivery. Back to the first audit that happened in Jan 2018 the average cycle time for the feature was 5 weeks. Now, the feature is usually done within a two-week Sprint.

Summing up, I want to highlight some other important points from my point of view:

* In January, I started working with a typical functional organization where people didn't want to learn. In half a year it was different organization where an HI designer wanted to start studying programming, 5 communities thrive, and people are constantly developing new skills.
* People noted in one-on-one conversations that they got a greater sense of work. In January, they all were narrow specialists that wanted to “utilize” themselves as much as possible. Developers from *project* teams didn't want to collaborate and help each other. With the LeSS implementation people finally realized their internal need to improve, learn and become better. Isn’t it amazing?

## Credits

I want to thank the senior managers of the company Sergei Muzykantov and Roman Ariffulin for believing in LeSS concept in January, 2018. This case is the first official LeSS case study in Russia. Sergey and Roman are pioneers indeed. Thank them for their courage and desire to move forward.

Also, I want to thank Sergey Gospodchikov. He was the first LeSS Scrum Master in Russia. His devotion to Scrum's values, perseverance and extraordinary persistence were a huge contribution to overall success.

经过一系列电话访谈并在LiteBox办公室工作了几天之后，我对高层管理者们介绍了自己的观察结果，然后赶往总部对整个公司进行了深入评估。我们与公司高级管理层和员工举行了为期两天的工作坊，重点讨论公司的组织结构，价值观，价值流等。我们的目标是制定下一步计划和行动方案。 我们在工作坊用的一些工具是：
