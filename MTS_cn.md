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

因为每个人都已经参加了Scrum基础培训，所以我认为为期一天的[LeSS基础认证培训](https://less.works/courses/less-basics.html)（CLB），然后再进行通过几次精益咖啡聚会，就足以使人们接受LeSS。但是，我错了。现在，我认为在引入新的组织结构之前最好花几天时间学习LeSS。 人们确实很需要了解LeSS背后的那些原则。您至少需要几天的时间，才能证明精益思想，排队理论和系统思考是LeSS规则的基础（ 指南：三种导入原则 ）。

旧习惯和针对个体的局部优化在第一个Sprint很快就出现。 我绝对一些时间与开发人员一起进行系统建模，绘制因果关系图（CLD）。 人们在使用他人制定的流程和自己拥有的流程之间存在着巨大的差异。 在为期3天的培训中，也可以更全面地介绍一些相关主题。

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

### 选择Scrum Master

在LeSS中，Scrum Master是一个专门的角色，可以服务于1-3个团队。我们期待在改变组织结构的那一天能从市场上聘请到经验丰富的Scrum Master。 不幸的是，它根本没有发生。 因而，最终我决定成为第二位Scrum Master，直到有人可以代替我为止。 这样我们有2个全职ScrumMaster（Sergey Gospodchikov和我）与4个团队合作。

团队通过投票来选择想要合作的Scrum Master。 我们还引导了为Scrum Master建立期望列表的过程。 产生的列表中有一些项挺有趣：
* Scrum Master可能从团队处得到一个臭鸡蛋。
* 当您被团队开除时，请不要生气。

### 与社区一起学习

在第一个Sprint之前，我们为团队提供了开始建立社区的机会。这是以开放空间(Open Space)的形式进行的。每个想要建立社区的人都会走到房间的中央，大声宣布社区的成立，然后在便签上写下它的名字，再贴在一张大白纸上。这就是在不到半小时的时间内创建14个社区的方式。

第一个社区在几天后启动，其余的社区则在前两个Sprint中启动了。 我们确保每个社区都有Scrum Master的支持来帮助他们定义：

* 社区宗旨。
* 工作协议。

我启动并支持了Scrum Master社区（ [指南：社区](https://less.works/less/structure/communities.html) ）。我们每周聚在一起大约一个小时，分享新实践及Scrum Master技术。 例如，有很多次都在讨论关于引导和团队教练的话题。

开发人员定期聚在一起，愉快地参加社区活动。 我还记得有一次活动是用mob编程的形式进行自动化测试开发。一位设计师之所以参加这个活动，是因为她想学习自动化。人人想学习！

<figure>
  <img src="/img/case-studies/mts-kassa/communities.png" alt="启动社区">
</figure>

### 最初的PBR

**产品愿景和商业模式。** 这使开发人员对产品的理解不仅停留在愿景层面，还能更深入地理解其商业模式。 LeSS的产品组是更大的组织环境的一部分，这个环境里有市场、销售、合规性和法律， 等等。 这就是我们开始进行最初的PBR的原因。团队先填充商业画布，然后将它们合并为一个。 我们一一讨论了商业模式相关的所有领域。对我们在讨论中出现的错误，产品负责人进行了纠正。

<figure>
  <img src="/img/case-studies/mts-kassa/business-model.png" alt="商业模式">
</figure>

### 尝试…条目拆分工作坊。

这是一个典型问题：团队无法将PBI切成更小的PBI。 当您拥有特性团队时，足够小的PBI就变得尤为重要，因为我们希望减少小批量生产的可变性，从而减少总的周期时间。我们建议举办一个所有团队参与的条目拆分工作坊。

我向团队分发了印有拆分模式和示例的纸（ *实验：尝试…拆分产品待办列表条目* ）。 然后，我启动计时10分钟，要求大家阅读文档。 学习的最有效方法是教别人，所以10分钟后我让他们结成对，并给他们10分钟的时间来做学习分享。接着，产品负责人从产品待办列表中选择了一个大的PBI。人们组成了小的混合群体，然后开始拆分这个PBI。

20分钟后，我们重新聚集，每个小组都被要求分享他们的拆分结果。我们重点介绍了一些最成功的拆分选项。 我通常在第一个Sprint期间的每个PBR活动中都带着拆分模式表，这样就可以轻松地参考它。

### 尝试…估算和类比估算网。

当多个团队处理同一个产品待办列表时，需要统一估算单位。 试点特性团队已经具有相对估算的经验，并且有许多已完成的条目。于是我们创建了一个类比估算网 ，把已完成的条目放进去以作为基准。 然后，我主持了一个工作坊，期间试点特性团队成员向其他开发人员解释了可以**被参考的PBI**，我帮助他们对齐了故事点估算标准。

<figure>
  <img src="/img/case-studies/mts-kassa/estimation-net.png" alt="类比估算网">
</figure>

**引导第一个多团队PBR。** 在LeSS实施之前，团队是从专门的需求分析小组那里获得需求。 现在，他们自己负责澄清每个条目的细节。我们邀请了领域专家到会议室。团队组成混合小组，分布在按不同的墙壁区域划分的四个站点里。 每个站点都有一位专家帮助他们澄清PBI。 25分钟后，每个人都顺时针移动到另一个站点（驻扎站点的专家除外）。上一组已经在大白纸上留下了注释，图表和说明，这对新的一组人确实有帮助。因此，团队需要一个多小时来澄清三个PBI。稍作休息后，我们再次重复该过程。

<figure>
  <img src="/img/case-studies/mts-kassa/first-multi-team-refinement.png" alt="第一次多团队产品待办列表梳理">
</figure>

## 导入LeSS结构

还记得产品团队的组件团队结构吗？ 现在，在团队自设计工作坊之后，团队结构发生了变化，开发人员组成了4个新的特性团队。 每个团队都是一个跨组件跨职能的自治单元，可以工作在产品待办列表上的任何一个PBI上。 团队的名字是：“阿尔法”，“维加斯”，“ StoreCraft”，“ Hotfixies”。

<figure>
  <img src="/img/case-studies/mts-kassa/team-structure.png" alt="团队结构">
</figure>

在旧的结构中，有一个业务分析师团队，包含四个人。 那些人非常了解产品及其领域。 对于一个来自客户的请求，产品支持人员决定是应该发送给开发小组，还是应该通过调整产品配置项来实现。 他们大部分时间都在编写需求文档然后推向组件团队。

**LeSS导入的根本失败。** 我建议业务分析师加入团队。他们得到了邀请，但是他们积极抵制新流程和LeSS导入。最终我们将他们放到了团队之外，而产品负责人要求他们在多团队PBR时代表他。 这是一个不成熟的想法，也是导入LeSS的根本失败。 理想情况是真正的客户和用户（而不是BA）直接与真正的开发人员沟通，没有中间人，而且前BA自愿加入团队并成为常规团队成员。 现在的情况与LeSS导入的关键原则和指南相反。 因此，这不是一个正常/健康的导入方式。由于缺乏对LeSS使用志愿的方式，以及消除BA作为中间人之重要性的理解，该基本要素并未实现。

**我未能理解志愿原则。** 导入LeSS的三项原则之一是*使用志愿的方式*（ *指南：三项导入原则* ）。 我和产品小组误解了使用志愿的方式。 它实际包含的含义是，没有人可以加入产品团队，除非他们完全了解LeSS规则并自愿遵守。而我们在导入过程中有“反对导入”团队人员，这与原则刚好相反。

从那一刻起，我们有了一些不支持LeSS导入但是却在导入范围内的人，他们时时与导入抗争。 这带来了很多痛苦和沮丧，因为“反对导入”的人们总试图阻挠变革。他们渴望将所有都恢复到以前的状态和组件团队的结构。

**中间人造成浪费。** BA停止制造需求说明并将其移交给团队，并开始与团队在产品待办条目进行合作。 不幸的是，他们的重点转向了在开发人员与客户/用户之间充当中间人：

* 与利益相关者（合作伙伴，内部市场人员，销售人员，合规人员）进行交谈。
* 与客户支持交谈。
* 与客户交谈。

这些正是真正的开发人员在LeSS导入后要做的事情。 但是中间人的角色继续存在，不断造成浪费和问题。这都是应该在LeSS导入时予以摈弃的。

**发布经理。** 仍然保留了一段时间的另一个协调角色是发布经理。 在进行结构更改时，自动化测试包很小，因此产品团队不得不手动执行大量的端到端测试。 那本是这位发布经理的最擅长的工作。这些测试很快成为了完成的定义（DoD）的一部分。团队开始自己做，同时扩展了自动化测试包以减少手动测试。

在以前的组件团队结构中，发布经理是最终决定产品增量是否可以发布的人。 她得到了留在任何团队的邀请，但她拒绝了邀请。这再次说明了我如何误解了导入LeSS的志愿原则。

好的一点是，发布经理没有抵制LeSS相关的流程，而是积极参与了一些LeSS活动（多团队产品待办列表梳理，总体回顾会议），并领导了一个社区（系统测试）。在两个月内，团队提高了技能，每个团队都可以自己将产品增量交付到市场。在那个时候，发布经理加入了其中一个团队，取代我成为了第二位全职Scrum Master。 那是我的建议。因为我注意到她有正确的心态，渴望学习并且想通过使用引导而不是命令和控制的方式帮助别人。

**管理。** 开发中的所有管理角色都立即被正式解散。 协调人员和经理们现在成为团队中的开发人员。 因此，不再有“团队领导”和“技术领导”的称谓。 仍然有一个由他们自己的经理领导的支持和培训部门存在，但它们不在LeSS实施范围内。 我认为，将来它们可能会被LeSS产品团队吸收，而DoD也将增加新的扩展：为客户创建视频和网站教程。

## 学习使用LeSS框架跑迭代

### 第一个迭代

正如俄罗斯谚语所言，“不犯错，不成事”。 对于第一个Sprint来说确实如此。尽管进行了所有准备和培训，但团队仍然不得不直面局部优化的弊端。 以前，公司从来没有以客户为中心的产品待办列表。现在，产品待办列表中的排序主要由对客户的重要性决定。

当Android开发人员和设计师查看产品待办列表时，他们可能会发现他们在第一个Sprint的工作量不足。 他们不得不在Sprint中花费大量时间来学习和帮助他人。 这是Scrum导入中的一种常见情况：团队因骤然背负上这些始终存在但隐藏在筒仓中的“知识债务”而变得痛苦不堪。 在筒仓（和知识债务）很大的大规模导入中尤其如此。 这种全新的“学习的组织转移”（organizational transfer of learning，这是1986年HBR Scrum论文中的原文。译者注：这篇Scrum论文是"[The New New Product Development Game]( https://hbr.org/1986/01/the-new-new-product-development-game)）对于团队成员来说是非常陌生的，以至于有些人对教与学感到不舒服，因为他们认为还不如“做一些产出更多的事情”。

我们发现了一些在启动过程中没有考虑到的问题。 例如，如何处理来自技术支持的紧急任务和错误。 另外，我们没有考虑如何提前进行回归测试。 而且不幸的是，存在巨大的技术债务，并且自动化测试的覆盖率很低。

我还注意到，人们因大量的培训和漫长的（3天）启动而感到非常疲倦。 尽管如此，第一次Sprint评审会议还是成功的。团队在Sprint评审会议期间显示了PBI。 参加评审的内部干系人也给予了他们积极的反馈。

在第一个Sprint期间，出现并积累了很多问题。团队中有许多问题都很类似，因此在Sprint评审会议结束时，我建议与产品团队中的每个人一起参加比以往更长的总体回顾会议。 我们耐心地花了三个小时。 结果是：

* 针对那些在Sprint期间没有足够工作是匹配其主要技能的开发人员：帮助团队中的某个人（通过结对），继续学习新技能，帮助其他团队。
* 如何进行回归测试并实际发布产品增量。 我们澄清了先前创建的完成的定义（DoD），并对其进行了扩展。
* 在Sprint期间如何处理紧急任务和缺陷：它们都通过一个单独的slack频道进行沟通的，任何有闲置带宽的团队都可以工作在其上。

第一个Sprint并不容易，但是产品负责人和大多数开发人员都致力于向前推进乃至实现目标。

### 导入可视化管理

**产品待办列表的可视化管理。** 我们从一开始就可视化了产品待办列表（ *实验：尝试…可视化管理产品待办列表或发布待办列表* ）。 产品负责人和反对Scrum导入的两个人，因此也不应该成为该小组的成员（两位业务分析师），维护着墙上的产品待办列表，保持它一直在最新的状态。 每张便签纸都代表一个PBI。待办条目沿着墙从左到右移动，进入“Ready”状态，最终成为迭代待办列表的一部分。

**迭代待办列表的可视化管理。** 我建议团队可视化他们的迭代待办列表，并限制进行中的工作（WIP）。 我们举办了一个关于限制队列大小的简短工作坊，并播放了[FeatureBan](https://www.agendashift.com/featureban)。 我认为这段简短的视频完美地说明了为什么您需要限制WIP以及如何更好地管理队列。每个团队都为迭代待办列表设置了明确的WIP限制。

**可视化管理有助于协作。** 在LeSS中，团队之间没有依赖关系。 为什么？ 任何特性团队都可以为其待办条目跨代码库工作。团队应用诸如持续集成、社区、多团队工作坊以及共享和交换工作之类的方式，对彼此进行管理和协调。因此，团队要做的就是合作和共享工作。

在迭代计划会议第二部分时，我们发现在需要几个团队之间协作的PBI上做上标记对即将到来的迭代会很有帮助。 通常，我们就在条目上面贴一个写有对应协调技术（例如“侦察员”，“组件导师”，“只是说”等）的小便签。

**可视化管理工作协议。** 所有主要的工作协议（DoD，“Ready”等）和回顾会议的产出项与产品待办事项都保存在同一房间。 我们将LeSS的活动时间做成一个可可以看到的时间表，并将其挂在走廊的墙上。它旁边还有一个社区活动时间表。

<figure>
  <img src="/img/case-studies/mts-kassa/visual-management.png" alt="可视化管理">
</figure>

### 尝试…可视化会议。

我是David Sibbet和可视化会议的粉丝。 我喜欢在会议中可视化所有内容。 我将视觉会议称为“活的”会议，是因为它可以激发高水平的参与度，呈现正在发生的事情的全面情况，并支持群组记忆。 以下是“活的”会议与“死的”会议的区别：

* 与会者们站着进行积极的讨论。
* 以小组形式（最多5人）进行工作。
* 没有电子设备，只有黏胶，马克笔，剪刀，大白纸和打印纸。
* 可视化正在讨论的所有内容（每个人的声音都被听到）。
* 周期性的分散和合并有助于团队从小组讨论和自主讨论中受益，并在整个会议期间与他人保持同步（合并）。

<figure>
  <img src="/img/case-studies/mts-kassa/visual-meetings.png" alt="可视化会议">
</figure>

### 协调

有趣的是，在引入LeSS之前，团队将协调视为最重要的问题。 我在精益咖啡聚会时注意到大多数问题都与协调有关。我们很快就解决了这个问题。 在一次性更改团队结构之前，我们进行了LeSS基础认证（CLB）培训，期间我们讨论了协调。从我的观察中可以看出，最常使用的协调方法是 *指南：用代码交流*，*指南：只是说* 及其更高级的版本 *只是喊*。 团队还在迭代计划第二部分的时候及时选择了所需的实践。 LeSS依靠基于自组织的协调行为。自组织的重要要素之一是所有团队的房间都通过一个大走廊相连。 我们还有一个共享的房间，在里面可以看到所有的信息。

### 迭代计划会议第一部分

在迭代计划会议的第一部分开始前一个小时，产品负责人和两名业务分析师对产品待办事项进行了最终更改。 然后，所有的团队代表（通常每个团队2人）参加了迭代计划会议第一部分。

**会议议程**。我们通常遵循下面的议程：

* 产品待办事项更新（未完成的工作返回到产品待办事项，并重新估算剩余的工作）。
* 产品负责人简要介绍处于产品待办列表顶部的待办条目，并根据请求情况对这些条目的部分细节做最后的澄清。
* 再次查看“完成的定义”（DoD）。
* 团队代表从“就绪”区域顶部开始实际选择PBI，并将它们放入团队的泳道中。
* 找到团队之间需要进行合作的待办条目，在公告板上对它们进行标识。
* 决定团队是否需要多团队迭代计划会议第二部分。
* 为整个产品团队定义一个共同的迭代目标 并且/或者 为各个团队定义各自的迭代目标。

<figure>
  <img src="/img/case-studies/mts-kassa/sprint-planning-one.png" alt="迭代计划会议第一部分">
</figure>


**迭代目标** 。 LeSS中并没有提到迭代目标，因为LeSS的原则之一是 [大规模Scrum是Scrum](https://less.works/less/principles/large_scale_scrum_is_scrum.html) ，所以LeSS不会拷贝粘贴Scrum指南中的元素 （ 以避免重复 ）。

**LeSS中迭代目标的例子**。 问题出现了：是为整个产品团队定义一个迭代目标，还是每个团队都应该有自己的迭代目标，还是两个都定义？ 没有标准答案。我认为所有选项都是可能的。这里有一些例子：

1.	第一个迭代的共同目标是“启动LeSS”。 除此之外，阿尔法团队有自己的目标“为收银员创建订单”。
2.	第二个迭代的共同目标是“告别组件团队的传统”，每个团队还有其他目标：“完成货物进口模块”，“完成收银员的订单创建”，“收银员+ MGTS”， “发布+ yandex OFD”。

就像您看到的这样，可能有不同的组合。 个人来说，我比较喜欢整个产品团队定义一个共同的迭代目标。

### 迭代计划会议第二部分

在我们的案例中，迭代计划的第二部分是微不足道的。 因为在会议的第一部分中识别了所有的协调可能性之后，团队会决定是否应该一起讨论多个团队的计划。 如果需要的话，团队决定在一个大的共享空间中进行迭代计划会议第二部分（ *指南：多团队迭代计划第二部分* ）。 但大多数情况下，团队只是回到自己的房间，在Scrum Master的帮助下创建他们的迭代待办列表。 最多花30-40分钟。 对于迭代待办列表的工具，我的建议与LeSS指南一致（ *指南：不使用软件工具管理迭代待办列表* ）：

不要为迭代待办列表使用任何软件工具； 只用使用可视化管理，可能只是贴在墙上的卡片（大规模Scrum：少即是多）

<figure>
  <img src="/img/case-studies/mts-kassa/sprint-planning-two.png" alt="迭代计划会议第二部分">
</figure>

### 学习LeSS中的待办列表梳理

在大规模Scrum中，PBR是一个强制性事件 （而不是可有可无的活动）。 之所以这样，是因为产品待办条目在大型产品团队中确实非常大，非常需要在整个团队层面进行广泛的协调与学习，并且根据实际需要安排一定数量的与客户和用户的会议。在LeSS中，有几种PBR方法（ *指南：产品待办列表梳理* ）：

* 团队代表参加的整体PBR，这意味着高阶的分析和展望，估算和待办条目分解（ *指南：整体PBR* ）。
* 多团队PBR。 一个房间中的多个团队可以同时优化多个PBI（首选）（ *指南：多团队PBR* ）。
* 单团队PBR。跟单个Scrum团队的做法一样。

对于应该使用哪些产品待办列表梳理的方法组合LeSS没有设定任何规则，但是LeSS建议进行多团队产品待办列表梳理。让我们来仔细看一下。

### Overall PBR

### 整体PBR

在第一个迭代中，尽管时间应该可以再短一些，整体PBR仍然花费了我们好几个小时的时间。 每个人都精疲力尽。 在下一个迭代中，通过更好的引导，时间缩短了两倍。 开放讨论花费的时间很长，参会者往往心不在焉，倍感厌烦。 为了保持拥有充沛的精力，我对所有活动作了严格的限时并建议举办一个事件。

我们使用了相同的引导方法。 产品负责人从墙上拿下一个PBI进行讨论，然后他使用5-10分钟对提出的问题进行澄清。

然后进行明确的估算。 如果PBI超过13个点，我们就将其拆分（*实验：尝试…细胞一样的拆分而非树状拆分*）。

<figure>
  <img src="/img/case-studies/mts-kassa/overall-product-backlog-refinement.png" alt="整体PBR">
</figure>

### 多团队PBR

谁会想到，为什么需要几个团队在一个房间里工作并同时优化几个PBI？ 每个团队进行自己的单团队PBR会 “效率”更高吗？ 让我们弄弄清楚。

**适应性**。 如果几个团队对几个PBI都了解，则产品负责人可以推迟决定哪些PBI该包含在接下来的迭代范围里，不用受特定团队只有某些特定知识的约束。 它为产品负责人的修改优先级提供了更大的灵活性。

**了解产品**。 团队对PBI了解的越多，他们对业务领域和产品本身的了解就越多。而且只有一个团队关注可能会有遗漏的方面，有更多个大脑进行思考，这些条目的澄清就会更彻底（ *原理：关注整个产品* ）。

**基于自组织的协调** 。 团队了解的PBI越多，他们越能够在迭代中互相帮助。 因此，也越容易出现基于自组织的协调。 下面是相关的系统模型：

<figure>
  <img src="/img/case-studies/mts-kassa/multi-team-product-backlog-refinement-system-model.png" alt="多团队产品待办列表梳理系统模型">
</figure>

### 多团队PBR的复杂性

多团队PBR有许多好处。 尽管如此，还是有一些问题。 让我们看看它们。

**信息过载** 。 同一房间中参与多团队PBR的团队越多，他们需要了解的PBI就越多。 因此，信息过载可能是多团队PBR的副作用。

**引导** 。 要让数十人参加这个事件并不容易。如果引导不当，则会造成浪费，从而开发人员不再希望参加多团队PBR。 让我们在系统模型中探索一下：

<figure>
  <img src="/img/case-studies/mts-kassa/multi-team-product-backlog-refinement-complexity-system-model.png" alt="多团队产品待办列表梳理复杂度系统模型">
</figure>

### 多团队PBR引导技巧

我想分享一些使多团队PBR更有效的技巧。

**充分的准备** 。 准备最多可能会需要几个小时。 它包括但不限于：事先与事件干系人会面，制定引导计划，在活动挂图上进行可视化（目的，议程）以及在事件之前准备好空间（移走桌子，椅子，放置活动挂图架等等）。

* **热身** 。 我认为通过小型游戏或破冰活动开始任何LeSS事件以提高参与度很重要。 您可以在《 [Moving Beyond Icebreakers](http://www.movingbeyondicebreakers.org/)》一书中找到很多类似的活动。
* **小组** 。您可以使用小组和其他分散技术有效地引导有很多人参加的会议。 《 [Facilitator's Guide To Participatory Decision Making](https://www.amazon.com/Facilitators-Participatory-Decision-Making-Jossey-bass-Management/dp/1118404955)》一书中有许多以小组进行工作的形式。

> 中心化毁了活力；去中心化创建活力（大规模Scrum：少即是多）。

**混合组** 。 除了前面的建议外，小组最好是由来自不同团队的成员组成。

> 从由每个团队的人员组成临时的混合小组开始。 例如，两个团队重组为两个混合组（大规模Scrum：少即是多）。

这是增强不同团队之间的协作并减少信息分散的方法。 每个团队的每个成员都是常识谜题的一部分。

**分散-集中和轮转** 。 除了前面的两个建议外，这是可用于大型人群引导的另外两种技术。 首先是将PBI分配给每个小组，让他们在多个站点并行工作并完善到“就绪”状态，然后每个人都参加到一个集中的公开讨论中。

> 各个小组花一些时间在房间的不同区域分别工作，以完善不同（或相同）的项目，然后花时间在一起共享各自的见解，提出问题并寻求其他协调机会（大规模Scrum：少即是多）。

轮转表示小组从一个站点到另一个站点按顺时针方向移动多次，而业务专家仍然停留在对应的站点上。 每个工作站点都工作在自己的PBI上。我非常喜欢这种做法，并且对它的效果有过多种体验。想象一下，第一轮大约需要20到25分钟，然后另一个小组接近了这个站。 该小组尚不熟悉该站点对应的特性，但是他们拥有先前工作在该站点的小组创建的有关验收标准、界面等信息。 他们所需要的就是去掌握新信息。

**可视化管理** 。 通常，当人们在会议期间使用电子设备时，这些会议就死定了。 忙活于键盘的某些人成为了瓶颈，其他无聊的人则盯着他们的电话。另一方面，剪刀，纸，便签纸和大白纸会激发协作。

**站着工作** 。 如果可能的话，我会从进行多团队PBR的房间里挪走所有椅子。 人们站在一起开的会议更加活跃，人们参与度更高，精力更充沛并且专注。

**“就绪”的定义**。 当团队在工作站上梳理PBI时拥有相同的“就绪”定义时，就会蓬勃发展，因为可变性大大降低了。这是我们都同意的“就绪”的第一个版本：

* 每个PBI都有一个大小估计（以点数为单位）。
* 产品负责人提供了商业价值估算。
* PBI小于13点，否则就要被拆分。
* 对特性的理解至少为10分的7分，其中10代表对PBI的完全理解，无需其他说明。
* 如果需要图形界面，则需要有高仿真视觉稿。
* 验收标准已经定义。

**严格的计时** 。 不要让会议“垮掉”。对世界咖啡的所有活动和轮数使用严格的时间盒（轮转），并设定到时提醒信号。时间到了的时候，别害怕叫停小组，并且问他们需要多少时间。

**反馈** 。 在每个PBR事件结束时进行一次小型回顾。 我要求每个人以1到10的比例评估事件的有效性，并附上详细的反馈。

我们尝试过不同形式的多团队PBR。 经过一段时间，形式逐渐稳定，此后我们没有做太多更改：

* 团队，产品负责人（可选）和专家参加多团队PBR。
* 使用混合小组的组织形式。
* 混合小组选择要讨论的产品待办列表条目并将其带到工作站。
* 在工作站工作，估算、完善和编写直至“就绪”状态的验收标准。如有必要，可以添加视觉稿，图表，示例和其他图形说明。
* 专家留在车站，而其他参与者则轮转（世界咖啡），探索由其他小组改进的PBI。

<figure>
  <img src="/img/case-studies/mts-kassa/multi-team-product-backlog-refinement.png" alt="多团队产品待办列表梳理">
</figure>

我发现，多团队PBR能正确完成后，迭代计划的两个部分都不会超过一个半小时（最多两个小时）。 多团队PBR已成为此导入中的关键事件，因为它是协调，更好地了解产品和适应性的驱动力。

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
旧习惯和针对个体的局部优化在第一个Sprint很快就出现。 我绝对会花一些时间与开发人员一起进行系统建模，绘制因果关系图（CLD）。 人们在使用他人制定的流程和自己拥有的流程之间存在着巨大的差异。 在为期3天的培训中，也可以更全面地介绍一些相关主题。
