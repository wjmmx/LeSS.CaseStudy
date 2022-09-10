## 鹿特丹港口信息管理系统开发：从LeSS的角度看

*这是一篇将鹿特丹港案例与LeSS原则以及组织设计进行比较的文章。它讲的是四个跨职能特性团队交付并运营一个至关重要的，7x24小时运转的港口管理产品的故事，该产品由船舶交通服务运营人员和其他几种类型用户使用。*

## 上下文与客户

鹿特丹港口管理局营业额约为 6 亿欧元，拥有 1,100 名员工，负责商业、航海和基础设施相关等各不相同的职责。 [特性团队](/less/structure/feature-teams)的首要客户是港务部门（Harbour Master）。该部门确保了航运交通（每年大约 33,000 艘远洋船舶和 110,000 艘内河船舶）能平稳、流畅并安全地运作。

用户多种多样。一些为港务部门工作，一些为其他部门工作，还有一些为鹿特丹港的众多合作伙伴工作。

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/port-of-rotterdam.png" alt="port-of-rotterdam.png">
  <figcaption>图 1：在常用物理设备上显示的实际 HaMIS 用户界面</figcaption>
</figure>

主要业务流程的核心是一个名为 HaMIS（Harbour Management Information System，港口管理信息系统）的产品。 HaMIS 的想法诞生于很多年前，当时的需要是替换掉既有的。 既有系统已经在鹿特丹港很好地运行了 20 年，但旧的技术和架构已经成为对业务流程做出任何重大改进的主要障碍。 鹿特丹港正在发展和变化，既有的老系统已无法满足要求。

产品的首要目标很简单：最小化过时的老系统带来的负面影响。 但另一方面，次要目标并不是太明确。 鹿特丹港正在增长，尤其是随着 [Maasvlakte 2](http://en.wikipedia.org/wiki/Maasvlakte_2) 的扩建。 该产品必须能在工作人员数量不变的情况下支持港口不断增长的交通情况。 这意味着需要加强信息交换、对相关利益方更好的协调，以及更好地支持港务部门的主要流程。

## 一起是如何开始的

在决定用 HaMIS 替换旧系统之后，就开始了制定计划、制定预算、涉及供应商和软件集成商的可怕的采购流程一系列复杂的过程。预期中这是一个外包开发项目。在这个过程中产生了很多文档，但除了概念性验证（POC）之外没有真正的代码产生。

最终，港口管理局做出了一个勇敢的决定，全面停止这个过程。开发计划太复杂了，不可能成功。需求复杂且高风险。太多的不确定，而且如果项目失败，这将会是荷兰的大新闻。如果有缺陷的系统投入到生产，后果可能会更糟糕。

但现有系统已接近其使用寿命，因此港口管理局别无选择，只能以一个主要目标重启该项目：用至少提供相同功能的新系统替换当前系统。但这一次，港口管理局选择了作为一个内部产品开发，而非外包给一个或多个系统集成商。

新产品的开发选择的方法是 RUP 和伪 Scrum 的组合（当然，它没有正式标记为“伪”）。虽然有 3 个完全由开发人员组成的“Scrum”团队开始举行站立会议并尝试其他实践，但是也存在在另一个独立的由 8 名不同类型的架构师和分析师组成的名为 AQUA（architecture and quality assurance）的架构和质保团队。

这么看来，最初的意向是**改善**。在现有组织的各种假定限制内，准备实施“开发级别的 Scrum”。而这项工作是由分析师和架构师组成的一群人设定的。

### 从 Scrum-But-But 到 Scrum-But

 RUP和Scrum-but-but的组合体并不真正地发挥作用。一家教练服务公司被引入来帮助他们学习如何转向Scrum。这家公司提供了Scrum培训和具体的工作辅导。但还是没有转为全面使用Scrum。比方说，团队决定培养并任命两个人为“Product Owner”，同时，任何事件中实际上都是一个项目及程序经理做决策。

 译者注：
 1. RUP：https://zh.wikipedia.org/wiki/统一软件开发过程
 2. Scrum-But-But：Scrum-But是指团队无法全面使用Scrum进行产品开发的原因。这些原因有特殊的句法结构来描述，“我们使用Scrum，But......”，Scrum-But也由此得名。作者这里的Scrum-But-But是指比Scrum-But还要更低一个层次的状态。

Scrum作为实践而非会影响既有团队和经理角色的*组织设计变革*不正确地导入。AQUA团队仍然存在，并且“Scrum”团队既非跨职能、自管理，也不能展现多面学习和多技能。没有一位真正的产品负责人，项目经理仍然存在，为“达成目标”负责。一些SAFe实践，比如“架构跑道”，仍然被讨论或引入了。

教练辅导公司引入了许多团队及技术层面的实践。比如，一次代码提交后（使用SVN，基于主干的集成），构建服务（Jenkins）就开始了包含使用Sonar进行质量检查的构建。测试包含单元测试，少量的Fitnesse测试以及通过录制播放工具进行界面测试。后来后者被完全弃用。此外，在这个阶段自动化测试还没有作为自动化构建的一部分。

改善在进行并逐步靠近Scrum，成果也不断地展现出来。迭代是3周，所有的Scrum会议也都被践行。最为重要的是，每个迭代后，一个**单一的潜在可交付产品增量**被发布到一个预生产环境，然后一些关键客户会试用新功能。

### 从 Scrum-But 到 Scrum

这个时候我作为架构师兼敏捷教练入场，同时那家教练服务公司离开了。

尽管他们叫我敏捷教练和架构师，但我那时的意图是作为Scrum Master来引入真正的Scrum推动组织设计。每个团队都有一个任命的Scrum Master，但实际上他们只是比其他成员多承担了一些引导工作的普通团队成员。

> LeSS规则：Scrum Master负责一个运转良好的LeSS导入。他们关注于团队、产品所有人、组织和开发实践。一个Scrum Master不只关注一个团队，而是整个组织系统。

我们做的第一件事是以“系统改善”为目标，逐步废除AQUA团队。废除工作通过逐步把决策权转移到特型团队来进行。此外，剩余的AQUA团队成员并没有坚持待在老的团队中。尽管如此，他们中有些人在AQUA团队被废除后仍然想保留他们在分析、架构及质量保证领域的权威性。

最后，没有什么活儿留给那个团队做了。换句话说，真正的可以端到端交付的Scrum特性团队成功地建立起来了。在特性团队与用户之间也没有任何人了。AQUA团队成员要么加入特性团队，要么就是做一些产品开发组织之外的任务。

与需求和架构关注点相关的知识，经验，新的洞察以及业务的持续改变都始于团队。

这一转变真正有挑战的地方是AQUA团队成员的特定头衔和角色。在经过很大的努力后，它们才被完全移除。这些头衔和角色，如不同的分析师和架构师，是双重的。他们真正的在组织中被公司和HR授予的岗位从来没有被正式地改变过。与此同时，在组织变革后，这些岗位和角色从HaMIS产品开发的角度看已经变得没有意义了。

有时，当直线部门试图通过人们的角色来影响产品开发时，这会产生一个小问题。一个例子是对“项目完成后移交到运营”的讨论。但实际上，项目已经不在存在，只有持续的产品开发和管理。另一个稍大一点的挑战是直线经理试图（并没有成功）将任务分配给他的下属，尽管他们已经完全分配给 HaMIS 产品开发。此外，还有一些KPI需要通过相关年度评估。一些团队成员因为没有达成他们的KPI而获得全部加薪。

这些问题的根本原因是持续存在的矩阵管理结构，从官方定义来说人们汇报给他们的直线职能经理及项目经理。组织变革移除了对项目经理的汇报，但是对直线职能经理的汇报仍然保留在后台。这个问题只是影响着少数的人，并且由于典型的荷兰企业文化以及优秀的总体成果，他们能够简单地忽略直线经理的影响。

在这个时间点上，我们仍然有一个活跃的项目经理正在学习着如何放手。他仍然可以表达他想要什么，而非所有的控制都在一个真正的产品负责人手中。

两个伪产品负责人中的一个开始表现得像一个真正的产品负责人，他也被看作是真正的产品负责人。两个产品负责人都是从港口管理（业务）部门来的。[真正的产品负责人](/less/framework/product-owner)也是那个做优先级排序以及产品代办列表更新的人。他拥有足够的权力来做产品相关的决策。第二个人官方也被叫做产品负责人，但是实际上并不被视为“产品负责人”。不幸的是，他持续地充当团队和用户之间的中间人（业务分析师），增加了交接，与人们谈话并且收集反馈。这个问题从来没有被完全解决过，只是及时减少其影响。我后来学到的教训是拥有一个待在团队和用户之间做分析师的伪产品负责人存在非常重要的缺点。这是我曾经在一开始时（错误地）以为这是一个可接受的妥协，并没有预见到它会带来的复杂度。

> LeSS规则：对整个可以交付的产品有一个产品所有人和一个产品待办列表。

在这个阶段真正的产品负责人负责对产品待办列表的排序，并且通过澄清条目及提供对任何问题的答案与团队合作。不幸的是他仍然持续地充当一个团队与其他利益相关者的中间人，而不是去直接连接团队和利益相关者。

> LeSS规则：产品所有人不应该独自工作于产品待办列表的梳理；他通过让多个团队直接和客户／用户以及干系人工作来获得支持。

在这次更具意义的组织设计变革之后的最初五个月里，在产品待办列表上高优先级条目已经不再是老功能的替代，而是全新的功能。这一结果带来的技术含义就是相当简单，团队可以快速交付。此外，用户也更期待着去使用这些HaMIS中的具有真正价值的，在老系统中没有的新功能。

在这一切之前，当陷在超载的RUP和SAFe船里时，注意力集中在交付各种文档和做出太多推测性的架构决策上。在移除RUP并开始Scrum后的第一个迭代中，焦点已经转向嵌入敏捷思维。每个人都在谈论这个叫做Scrum的东西以及它是如何工作的。有些人持怀疑态度（例如，关于持续的实验），但大多数人都在渴望尝试和学习。此外，开发生命周期的每个方面都已开始改善。持续集成、TDD、ATDD、结对编程和其他XP实践逐渐被嵌入。有人可能会说，尽管在学习上花费了精力，但团队已经在每个Sprint之后，根据**统一的完成的定义**将新功能交付到生产环境中。但我更愿意说，由于努力学习了，团队在每个Sprint都提供了新功能！

每个（对）开发人员代码的签出和签入周期时间开始从每天一次改进为大约每小时一次。简而言之，团队开始走向真正的持续集成（CI）。开发人员在本地构建期间不断扩展质量检查。最终，即使是稍微复杂的函数也会使构建失败。产品始终处于准备好发布的状态。每当有人在没有运行这些检查而匆忙做事时，为大家带来美味的蛋糕成为一种惯例。这不包括由于频繁集成而中断构建的时候。过了一段时间，构建系统变成了一个多阶段CI系统，3个构建阶段主要由自动发布到下一环境和一些并行处理所驱动。最终，开发人员形成了一种行为改变的文化，即持续地集成（这才是真正的“CI”），而不仅仅是使用了构建服务器就错误地认为这就是“CI”。

### LeSS

*因为LeSS（大规模Scrum）是与多个团队合作时对Scrum的直接、简单、一致的扩展，所以即便不熟悉2008年和2010年出版的LeSS书籍（由Larman和Vodde出版），各个小组重新创建大部分或全部LeSS可能很常见。这也是我们在2010年第一次开始这个旅程时的情况（Scrum在港口的引入）。因此，现在我对LeSS有了充分的了解，反思我们所做的工作，将我们的案例与标准LeSS进行比较和对比，这对我来说很有趣。*

因此，“[LeSS]（/less/framework/index）”开始形成，尽管我们从未提到过LeSS框架。工作方式和实践是根据以前的经验引入的，但更多的是作为**实验**。这些是开始时最重要的原则：

* 整个产品聚焦在每个迭代产出潜在可交付的增量
* 尽可能地离客户近
* 每个人都聚焦在整体产品上，移除任何不必要的角色和职责
* 让团队直面挑战，不要试图在团队外解决它们

[LeSS巨型框架](/less/less-huge/index)在这里绝对不需要。在重组之前，有3个组件团队，1个架构/QA（AQUA）团队和1个运营团队。重组后，我们有3个特性团队。很久以后，扩展到了4个特性团队，如后文解释的那样。

> LeSS规则：多数团队都是以客户为中心的特性团队。

在这次重组之后，大力推动自管理。这个推动的含义将在后文解释。项目经理逐渐停止了他们的干预，他们停止了做出任何决策或分配任何工作，而只是安排预算并与组织的其他不太了解敏捷开发是如何工作的成员进行沟通。理想情况下，这项工作应该由产品负责人完成，但他缺乏项目经理的影响力。虽然项目经理态度的转变很慢，但却是无痛的。主要原因是其中一位项目经理是Scrum的第一个也是主要的倡导者。现在，他不再是项目经理了。

> LeSS规则：在LeSS里，管理者是可选的，但是如果管理者还存在的话他们的角色可能会改变。他们的焦点从管理日常产品工作转向改进产品开发系统的价值交付能力。

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/hamis-timeline.png" alt="hamis-timeline.png">
  <figcaption>图标 2: HaMIS 时间表</figcaption>
</figure>

## The Product

The first version of product was already partially implemented before the Scrum introduction. The fundamental technical elements were use of Java, a standalone Java client written in Swing in combination with JIDE, an IBM WebSphere platform on the server side, and SOAP over HTTP as the protocol between client and server. There was even a SOA with an enterprise service bus. Design and layering of the backend was based on standard JEE patterns (service, business, data). A separate server-based solution with Erdas Apollo software delivered geospatial data to clients. Altogether, this was definitely not the simplest possible solution, it was over-designed. In fact, the front-end part was based on a proof of concept, which unfortunately was not thrown away. Nevertheless, with a few adjustments it was workable in the first Sprints.

Almost all of these original choices were changed significantly or removed in the following years, replaced with simpler solutions as the number of features and intrinsic complexity grew. The statement “We need to choose complex technology in order to anticipate complex requirements later on!” proved to have the opposite outcome. The chosen technologies were not needed, so other technologies replaced them along the way.

Similarly, the original overall design was put aside after the reorganisation into cross-functional feature teams. Focus has moved towards *actual code* and therefore an already-implemented design.

Architecture and design still had the teams’ full attention. The main driving forces in evolving the architecture were requested features, rather than speculation. This translated into following key design rules for the group:

* If it is not needed by business in this or the next Sprint, than it is not decided upon, designed, or built. It might be discussed, but only briefly.
* We must replace the old system as soon as possible.

The biggest challenge here was not the technology and knowledge of design techniques but getting clear information from domain experts and users. The complex subject matter meant that not many people could explain how things really worked outside in the real world.

Thinking in simple solutions was gradually embedded in the minds of everyone involved. This thinking manifested in continuously questioning and replacing already implemented choices and always choosing the simplest possible option while clarifying and estimating big and small items. An example was replacing the SOAP over HTTP interface between the client and server with Hessian binary protocol. This primarily meant removing a lot of code, which felt really good.

Nevertheless, before any of these technical discussions, teams demanded not only requirements behind items for the following Sprint but also a proper explanation of context, the business process behind items, and any requirement that might impact the choices at hand.

The teams were *solving a problem*, and therefore not merely delivering a solution. This was most visible during a whole day Product Vision Box workshop, where teams intensively engaged with Harbour Master and other business people to define a product vision.

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/product-vision-box.jpg" alt="product-vision-box.jpg">
  <figcaption>Figure 3: Product Vision Box workshop, part of Initial Product Backlog workshop</figcaption>
</figure>

The results of this workshop were a shared vision and high-level items for the Product Backlog for the coming 2 years. There were many more, different kinds of workshops after this one.

Instead of spending a lot of time on choosing a grand new technology to serve for the next 20 years, teams refocused on understanding which requirements would fulfil design or technology choices in the present. When requirements were currently lacking or much further in the future, teams would take these into consideration:

* Is the current choice going to prevent us from meeting those requirements in future,
* and will it be costly to replace this choice?

If no, it becomes a waste of time to further analyse the choice.

In other words, we spent huge amounts of time on understanding short-term and long-term business requirements but very little or no time on the design and architecture of things not used after following Sprint.

All significant decisions, decisions with larger impact, were taken during two kinds of **cross-team design workshops**:

* Triggered by a just-in-time need from any team, for the current or the next sprint
* Chosen from a wall with subjects, where everyone at any time could place any to be discussed subject.

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/technical-debt-wall.jpg" alt="technical-debt-wall.jpg">
  <figcaption>Figure 4: Wall with technical debt or architecture related subjects</figcaption>
</figure>

Such sessions were timeboxed at one hour and usually followed diverge / converge setup. After one hour, teams either made a decision or concluded to do more research.

All design decisions were made by teams. In the beginning, the most experienced team members made these decisions. This caused problems in team dynamics. Design discussions resulted in decisions and whiteboard sketches. Since these drawings largely defined the tasks belonging to a story, the other team members felt disconnected from what was happening.

> LeSS rule : Cross-team coordination is decided by the teams.

Eventually, design and architecture discussions became a team and cross-team effort. They usually started during the [Sprint planning One](/less/framework/sprint-planning-one), but the real work was done just before a team started to work on a specific item. When item required coordination with other teams, the dependency was resolved in a natural way by simply talking to each other directly. There was no cross-team coordination in any way outside the teams.

> LeSS Guidance: Coordination via Open Space, joining other teams’ Daily Scrum, Scrum of Scrums, multi-team workshops, or “simply” working in the same space, talking to each other, and using visual management.

On a more detailed level, a Sprint may had one discussion for each item if needed. The rule of thumb was that a discussion ended when all team members understood the design and could participate in its implementation. The more experienced developers were still the most active during these sessions. Other team members usually asked questions, which the experienced developers answered. All teams were invited to participate in any decisions with big impact.

Every single aspect of architecture emerged gradually or changed. Everything was introduced only when needed, except for the planned, gradual replacement of many obsolete technologies. In the beginning, only one server instance provided services to clients, and the database and the domain model contained only those classes needed for the stories built at that moment. We had a [walking skeleton](http://alistair.cockburn.us/Walking+skeleton) with only one leg. It could jump and that was good enough at that moment. Once we realised it would probably fall because of additional weight, we introduced another leg, and a cluster was born.

*In my experience, a complex architecture like this can definitely emerge as long as teams constantly spend a considerable amount of time on design and architecture through discussion and workshops.*

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/code-quality-audit.jpg" alt="code-quality-audit.jpg">
  <figcaption>Figure 5: Result of an external code quality audit</figcaption>
</figure>

A remarkable achievement was that teams were improving the overall quality, while intrinsic complexity of the product was growing. The quality was continuously monitored with Sonar and many related tools. At some point, an external company also performed an audit and graded this system as top 5% of all systems they have measured worldwide. The major driving force for high quality is a strong sense of craftsmanship in most team members.

Since teams, together with the Product Owner, were able to decide how to spend their time, they would often choose to experiment and build new innovations. We often held hackathons and ShipIt Days, during which we would try to deliver in one day something that was not yet on the Product Backlog, more or less free from any constraints.

## Process

### Focus on Users

We used many of the well-known practices for understanding business needs: user stories, epics, themes, and releases. Although they’d been useful, teams spent most effort on simply inviting users to visit or visiting users on the job, talking to them, and, most importantly, observing their work (“[Me and My Shadow](http://www.innovationgames.com/me-and-my-shadow/)” - an innovation game). HaMIS team members would take the initiative, without Product Owner involvement, to arrange visits. As a result of this effort, epics and user stories were often rewritten or replaced. Teams would usually involve the Product Owner afterwards. While the Product Owner was generally absent during these sessions, he or she still decided whether or not items should be placed on the Product Backlog, and where in the Product Backlog.

> LeSS rule: All prioritization goes through the Product Owner, but clarification is as much as possible directly between the Teams and customer/users and other stakeholders.

Users had become involved in the process, and were visiting teams on weekly basis. Sometimes, a whole team would take their laptops and work at place where users are for a few days. Certain features required a lot more feedback, and proximity makes collaboration more efficient.

During Sprint Reviews (one in which every team demonstrated their features), where product increment was shown and feedback received, a meeting room would be completely filled with users and business people. Unfortunately, it gradually became more difficult to keep them coming after every Sprint. Continuously delivering new features for years became business as usual. In the beginning, everyone was excited by such fast delivery.

> LeSS rule : There is one product Sprint Review; it is common for all teams.  Ensure that enough stakeholders join to contribute the information needed for effective inspection and adaptation.

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/sprint-review.jpg" alt="sprint-review.jpg">
  <figcaption>Figure 6: Sprint Review</figcaption>
</figure>

A big lesson learned was that comments from the Product Owner or someone similar could never replace talking to users. In complex challenges, collaboration with users became even more important. Occasionally, teams misunderstood the need, which resulted in rewritten functionality in the following Sprints. An interesting observation was that talking to users seemed occasionally difficult. Users really liked to talk when asked specific questions. They would expound on all kinds of detail at that moment, while we came for specific answers to specific questions. This was due to different perspectives between their world and our software world. Nevertheless, team members found that talking to real users was definitely the most effective and accurate way to discover requirements. Despite difficulties, it was always worth the effort and beneficial for all involved.

On other hand, requirements were often unclear or improperly justified, frequently due to a difference between how users were working with the old system and how harbour management wished to improve the existing process. The usual solution to this problem was to simply choose the most probable approach and show it to everyone. In other words, an **experiment**. Any changes as a result of this shortcut were still more cost-effective than further discussion or pushing the problem back to business. Probably the most important reason for why this worked is the **trust** higher management had in the Product Owner. Imagine the cost of four teams during one or more Sprints, and then duplicate costs in following Sprints as they must partially or completely replace functions.

A major mistake we made was that the Product Owner worked with so-called “subject-matter experts” or “domain experts” who were actually analysts that gathered information, met with people, and wrote requirements.

They created another **queue with functionally analysed requests**, with more WIP, handoff and information scatter wastes. This approach prevented teams from really understanding the problem and asking “why” questions. Not only did real understanding got lost in translation, but one of the first feedback loops became broken.

Eventually, we decided to apply one of the guides in *LeSS: Hands-on development feature teams help the Product Owner more, doing most of the clarification work on items and talking directly with the users. So then the overall Product Owner could focus more on prioritization, while the teams focused on clarification.*

Therefore, analysis and exploration of items shifted from analysts to the teams. The presumption that “nerds” were incapable of asking the right questions and should not talk to business proved to be completely wrong.

### Just-in-time delivery improved

We have removed this **queue** (functionally analysed requests) completely and gradually **reduced batch size**. In the first 20 Sprints, a lot work is spent before an item was ready. Each team’s tendency was to reject an item if something was unclear. In the early phase (before the teams did most clarification) this pushed the PO and “domain experts” (really, just analysts) to keep spending time on “preparation”. Therefore, the PO would usually prepare items many Sprints in advance. At some point, the realisation came that this “preparation” makes things only worse. Lead time was long, premature preparation was essentially making feedback loop much longer or too late to give, and prepared information was not really useful after all. There was more of the wastes of overprocessing, WIP, and handoff.

This was first changed into much more meaningful and intensified Product Backlog refinement, where sometimes barely identified ideas were given by the Product Owner and then teams would define and split into or write fine-grained items.

In other words, *teams took over the clarification of items*. The teams did this clarifying more just-in-time. The items were prepared only one Sprint ahead. Also, teams became more comfortable with accepting relatively “unprepared” items and doing all analysis (also talking to users to clarify things on a detail level) during the Sprint. At some point, tasks were not defined during Sprint Planning part 2, but written just-in-time, when team decided to pick up the next item during a Sprint. The reason was the waste created by asking questions like: “Does anybody know what this task was about?”. They were simply created too early. The effect was reduction of tasks batch size.

Another thing team members did is to continuously ask each other during the Daily Scrum how to help finish an item they started working on, before picking up a new one. This action reduced WIP further to 2-3 items per team. Accepting the fact that sometimes team members didn’t have much to do, and would try to help others to finish an item first. Pair-work fitted perfectly in this practice.

### More work, so more teams?

Our teams constantly improved, with great results. The rest of the organisation noticed. This had two effects:
* Other IT departments and teams started introducing Kanban or Scrum
* Business people with budgets made more and more requests, even from outside of Port of Rotterdam.

About 2 years ago, also the *Port of Amsterdam* wanted to replace their system with HaMIS. This did not mean they would receive a download with our software; our teams and the PO suddenly had a whole new group of stakeholders and users for the same product. The principles of incremental delivery and close contact with users and customers are still applied. The difference was that teams needed to spend some time in Amsterdam, too.

> LeSS rule: The definition of product should be as broad and end-user/customer centric as is practical. Over time, the definition of product might increase. Broader definitions are preferred.

The Product Backlog contains work for multiple years. All these stakeholders wanted to have their value preferably yesterday. This automatically triggered the question about scaling towards more teams. More people means more work can be delivered, right? Every time the question would arise, the teams’ answer was “No!”

We realised that the request for more teams was by itself an incorrect request. The correlation between more teams and more production was, at best, weak. At worst, it could have exactly the opposite effect. The requests were followed by a number of questions from the teams:
* What is the exact need? Is it clear enough?
* Should this be part of HaMIS as a product?

The most important conclusion was that teams would rather keep improving effectiveness through better ways of working together, improving the organizational system, and especially with users and stakeholders, instead of introducing new teams or team members. Eventually, both teams and management agreed on this way of thinking. We all had a strong feeling that a lot can be improved in the system, even after four years.  We came back to the observation that one of the most important areas of improvement was the Product Backlog. This was also the reason for the question above.

In the first three years, only three teams built HaMIS. Eventually, the teams themselves decided they could hire additional experienced craftsmen and craftswomen, create another team, and still be effective. A good thing about new team members is the experience they bring from other projects.

## Organisation

### Self-managed, cross-functional feature teams

It took a lot effort to give teams the authority to make decisions on their own. The challenge was not the teams, but the rest of organisation. Management and other involved people were accustomed to certain ways of working (“It is part of my responsibility as a manager to make these decisions”), which needed to be moved to teams. The main mantra, whenever someone from outside suggested to change something or make a decision, became: “Bring this subject to the teams!”.

This trust given by management to a whole team created sense of *responsibility*. It is the trust that teams were very much capable of making decisions with large impact. Management and PO also gradually stopped approaching individual team members for specific tasks or any kind of performance review or feedback.

> LeSS rule: Each team is (1) self-managing, (2) cross-functional, (3) co-located, and (4) long-lived.

Team members *identified* mainly with a whole product and therefore all teams together, and secondly to their own team. Teams were fairly stable, although they decided to shuffle 3 times in 4 years for more fun, better knowledge sharing and getting to work more closely with other people too.

This shuffling was a **self-designing teams** session and was done in about 1-2 hours:

1. Define all skills / disciplines a team should have with post-its.
2. Remove doubles or similar skills.
3. Have consensus about remaining skills
4. Make 4 copies of each remaining post-it and place one set on each table of the 4 tables.
5. Everyone uses 3 different colours post-its with own name on each: one colour is skill she masters, other was skill with average knowledge, and last one is skill she would like to learn.
6. Everyone walks around and places all of his/hers post-it on one table on specific skills.
7. After this first team composition, each team discussed if they are well-balanced compared to other teams and potentially discuss this with other teams directly, and make adjustments accordingly.

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/self-designing_teams.jpg" alt="self-designing_teams.jpg">
  <figcaption>Figure 7: Self-designing teams session</figcaption>
</figure>

### Internal and external focus

One of the biggest challenges was getting rid of statements such as: “We shouldn’t be responsible for these things, they (business, management, somebody else) should deal with it. If we deal with it, then we have less time to code”. For a long time there was a *lack of external focus* driven by combination of factors. The focus shifted very gradually with realisation that all those “external” things, such as understanding how users do their work in real life is crucial for delivering real value, and that working code itself is not necessarily same as value. Self-managing teams became significantly more efficient than anyone outside in dealing with these issues. There were no translations, *no broken feedback loops* because of e.g. technical limitations.

### Growing multilearning team members

The teams were **cross-functional** and capable of taking care of *all aspects for a full delivery*. This was achieved quite early. What also happened is gradual cross-pollination of skills within each of the teams. Pair-work and overall collaboration enabled team members to learn new skills. At some point, almost all team members were capable of doing any of the disciplines and therefore became **generalising specialists**. E.g. in the beginning, testers were mainly building automated tests, but gradually started to deliver production code too. Operations guys from former operations team, spent most of their time coding since there was not much to do in operations.

### Cross-component teams

When Scrum was introduced, teams were cross-functional, but still specialised in certain components. One team took care of messaging, other team dealt with “port map”, and yet another “ship inspections”. The PO would select a **qualified feature team** for a feature. In time, they started to become more **cross-component**, and therefore take care of any component required to deliver any feature. In time, any team was capable of doing anything. In other words, teams invested in deep learning in less familiar territory. Eventually, there was *no significant difference* between teams concerning knowledge areas.

A very interesting advantage is reduced architectural complexity. There was a less tendency to choose overly complex solutions. In contrary, more redesigns and refactorings are done in order to reduce cross-component complexity.

### Coordination between teams

During the early days of “Scrum-But-But” (very fake Scrum) , there was a Scrum of Scrums meeting where the so-called Scrum Master of each team would come together with project managers to discuss topics. Ouch!

After some time, representatives from each team would come, and not necessarily the “Scrum Master”. In time, not much relevant was discussed in these meetings.

Eventually, as all project management related activities disappeared or replaced by Scrum activities, real coordination happened directly between team members as needed, and in many different ways. There was no special dedicated meeting for this. When needed, anyone could organise **multi-team design workshops** for any significant decision. Everyone is invited, but they were not compelled to participate.

Besides design workshops, we organised regularly coding dojos for knowledge sharing purposes, TDD katas, discussing some tricky approaches, etc. Because of strong generalising specialist culture and already strong collaboration between everyone, and being just a few teams together at the same site, there was no need for  formal **communities of practice**. Rather, emergent multi-team coordination mechanisms were good enough.

### Reporting

Scrum practices are the only means of reporting at HaMIS. Teams didn’t really report to anyone in any way. Line management existed, but was even further away. More than half of team members are contractors, and others were employees. Any direct line manager of team members didn’t really know what they were doing or had any influence on their work.

The most remarkable about this situation is that team members really felt part of HaMIS, and not their official organisation.

### Cross-cutting activities

Decisions from workshops often led to some work (often, some supporting infrastructure work such as replacement of the application server or Java version upgrade) that is not related to a single feature. This work item was added to the bottom of the Product Backlog, and after the Product Owner’s consent during Sprint Planning, one of the teams would take the responsibility for delivery. This team becomes essentially a **temporary infrastructure team** for one or few Sprints, although we never named the team as such.

### UI Design knowledge

In the beginning Scrum-But-But days, UI design was done by a dedicated technical “architect” who designed and developed the front-end of the system up-front in a proof of concept. He was not a UI design specialist. After Scrum introduction, this responsibility is fully given to teams. Therefore, anyone was allowed to make suggestions for user interface design and together as a team make a decision.

Unfortunately, this was not enough because none of members had proper knowledge and experience to do this really good. Everyone, PO, users, and teams were not happy with the design or resulting user experience, but nobody knew how to properly deal with the problem.

The solution was to hire a specialist to be a **generalizing-specialist in her home team**, but who in addition also acted as a teacher and coach to other teams. In the early days, she spent more time *showing* other teams a good design; later, she could spend more in pair-work or reviewing other teams’ UI designs.

### Cross-team working agreements

All teams share one **Definition of Done**. This was inevitable since any team could deliver any of the features.

Any significant architectural decisions, which would immediately affect production code were first shared with other teams. Everyone was invited to discuss the solution, and attending team members were permitted to take decisions on behalf of everyone. Decisions making were almost always based on consensus, not compromise.

Anyone could suggest anything, and therefore could organise a session where significant decisions could be made. The person who made a suggestion had to have valid argumentation, which was challenged by others. Therefore, nobody except the Product Owner had special authority to force any decision, whether it was subtly based on too aggressive influencing or directly imposed.

## Events

### Sprint planning

At the start of the Sprint, all teams would first gather in front of a physical (cards on wall) Product Backlog where items for the upcoming 3 Sprints were always visible, together with the Product Owner. Each team would choose, negotiate with other teams and possibly clarify any cross-team coordination issues. In short, a common  **Sprint Planning part 1**. The whole meeting took between 10 and 15 minutes.

The chosen items were then further discussed and planned by each team in their own Sprint Planning part 2. The PO was not always present during part 2 meetings, but could always be contacted by phone if needed.

> LeSS rule: Sprint Planning consists of two parts: Sprint Planning Part One is common for all teams while Sprint Planning Part Two is usually done separately for each team.

### Product Backlog Refinement

In the first year, we held a Product Backlog refinement (PBR) workshop with all teams all together. Everyone knew quite well all items, but it didn’t feel efficient. There was also not much collaboration. Team members felt guilty to speak up in an already inefficient meeting.

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/product-backlog.jpg" alt="product-backlog.jpg">
  <figcaption>Figure 8: Product backlog, top priority items. Each lane are items chosen by a team. Columns are potential items for each Sprint</figcaption>
</figure>

This was changed into a “gut feeling estimation” workshop, where everyone participated. In LeSS  terms, **multi-team PBR** focusing on estimation. Teams would ask questions and discuss crucial points, where everyone continuously learned to stay out of details.

We had considered only *representatives* in the workshop, but the knowledge gained during this workshop proved to be very useful to everyone, and there were only a few teams.

After multi-team PBR focusing on estimation, each team did their own **team-level PBR** after choosing set of items most likely to be done by their own team.

A problem with this approach was that during Sprint planning, items could be switched between teams because of changing priorities or to remove constraints between teams. That’s good agility, but this would often require doing refinement all over again for this item by the new team.

In retrospect, the LeSS guide to hold an **overall PBR** meeting with representatives from each team, to due some lightweight clarification all together, would have reduced that problem. At least a few people from all teams would have had some exposure to all items, to increase flexibility across teams. But we didn’t try that.

> LeSS Rule: Product Backlog Refinement (PBR) is done per team for the items they are likely going to do in the future.

> LeSS Guidance: (1) Hold an overall PBR with representatives before each team PBR to explore which teams might work on which items, and to increase learning and alignment. (2) Hold a multi-team PBR to increase shared understanding and exploit coordination opportunities.

### Retrospective

Right after the Sprint Review, each team held own team retrospective, which took 1 hour usually.

> LeSS rule: Each Team has their own Sprint Retrospective.

After this retrospective, all teams got together for an **overall retrospective**. Each team presented own conclusions / actions they wished to communicate, and things they wished to discuss with other teams.

An example of a difficult to solve system-level issue was a big bang effect (not a minimal viable product) caused by prioritization in the product backlog. One or multiple teams had noticed that although the goal is to turn off the old product as soon as possible, they were working on items which didn’t seem to align with the stated goal. In other words, most important PBL items didn’t seem that important.

During the group retrospective, the issue is explained and action defined if other teams also agreed that issue should be resolved. The action is assigned to a specific person. This could be a team member, the PO, a Scrum Master, or a manager. In the above case, it was a PO who would tackle the problem together with teams during a next Overall PBR meeting. During this Overall PBR meeting, the teams would go into details of the problem, propose prioritization suggestions to PO, with reprioritization as a result.

In this process, the question was raised “Can we (teams) resolve this problem ourselves?” Only if not, the problem was given to someone else. Once an action is assigned, there was no specific process. It was suppose to be taken care of as soon as possible. Teams didn’t have a list of system-level issues or improvements, since they focussed on resolving them as fast as possible instead of keeping a list.

In a next group retrospective, everyone was reminded of actions from a previous retrospective and whether they were already done. It was usually only one system-level action and maximum three.

If action was given to a specific team, this team would usually place a post-it note on their Scrum backlog, next to other actions related to their team only.

> LeSS rule: An Overall Retrospective is held after the Team Retrospectives to discuss cross-team and system-wide issues, and create improvement experiments. This is attended by Product Owner, Scrum Masters, Team Representatives, and managers (if there are any).

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/overall-retrospective.jpg" alt="overall-retrospective.jpg">
  <figcaption>Figure 9: Overall retrospective on a sunny day outside</figcaption>
</figure>

### Sprint backlog & Daily Scrum

Every team used visual management for their Sprint Backlog and held their Daily Scrum in front of it. They were not held at the same time, to enable other teams to observe. There were often a few members from other teams.

<figure>
  <img src="img/case-studies/port-of-rotterdam-hamis/sprint-backlog.jpg" alt="sprint-backlog.jpg">
  <figcaption>Figure 10: Sprint Backlog of one team (this was not Daily Scrum :-))</figcaption>
</figure>

> LeSS rule: Each Team has their own Sprint Backlog.

## Practices

### ATDD

Teams started to use Fitnesse and several other tools already during Scrum introduction. It took some time before they learned to properly define tests, also without making a mess. At some point, they started to use Fitnesse to document specifications by using ATDD / Specification by Example practices. This happened at the beginning of the Sprint, together with PO, subject matter experts, or users.

### Definition of Done

> LeSS rule: The perfection goal is to improve the Definition of Done so that it results in a shippable product each Sprint (or even more frequently).

A **Potentially Shippable Product Increment** was brought into production after every Sprint (with few exceptions, which they felt as a big failure). Production deployment happened a few days after the Sprint was finished. This short process of about 1 hour didn’t involve HaMIS teams. Only **travelling infrastructure expert**, PO and external infrastructure provider were involved.

Everything else was part of the **Definition of Done** and done within the Sprint. It took us a lot of effort to achieve this. In time, this was more and more challenging because of growing complexity, and dependencies with other systems that were less agile than our group. This involved all testing (fully automated), customer documentation, deployment scripting, scripted production database changes, etc.

> LeSS rule: One shared Definition of Done for the whole product.

Also, all supporting work was done by the feature teams. E.g. configuration, upgrades of all tooling.

### Real DevOps: Elimination of the Separate Operations Group

When Scrum was introduced, three teams were building the new product, while a separate operations team of six people dealt with the existing system 24/7. When the first parts of the new system were released, this operations team took on responsibility for operations of the new one also. In the beginning, this was not much of a problem because the required availability of delivered features was not high. The development teams could usually take care of any problem the next day.

In time, HaMIS grew and larger changes were put in place. Although the operations team had limited or no Java experience, we all decided to introduce **DevOps**: to dissolve the separate operations team and spread operations people over HaMIS development teams and increase the responsibility of the feature teams to include operations. To start, the ex-operations people (now in feature teams) were still scheduled for 24/7 standby, just in case something happened in production. Gradually, the operations people would contribute more and more to HaMIS development. All of them were given an opportunity to learn from their teammates about Java and many applied practices and technologies.

On the other hand, as mentioned before, the new product definitely had issues entering production. Someone had to take care of those. The solution was to appoint one feature team as the **operations team** during one Sprint. Therefore, we didn’t have permanent operations team anymore, but a *rotating team*. A normal development team would temporarily become an operations team, in addition to doing normal feature development. They would take care of any issue and provide second-line support. In the beginning, this team would spend the whole Sprint on incidents, monitoring, issues, and so on. Since any developer would rather build something instead of solve self-created defects, all teams would spend time analysing and preventing these issues; this is popularly called “eating your own dog food”. Eventually, the number of issues dropped, even with growing system complexity. An “operations team” would start delivering more and more regular feature items. Ever more powerful **Continuous Integration** (behavior and system) helped a lot too.

By the way, the teams usually treated any work on infrastructure configuration as one or multiple tasks belonging to a Product Backlog feature-item. Even large infrastructure work was preferably split into smaller parts and done incrementally in the context of customer features.

Officially, the infrastructure was managed externally. In reality, the development teams were monitoring the whole infrastructure, introducing and scripting changes. The external company was more or less only executing tasks teams defined. We have spent a lot of effort in involving them in the process, thereby increasingly resembling a single team, and in the process removing this last **functional unit** dependency. Communication between the teams and the company was direct, through Skype, and one day per week a visit to our office.

Probably the most crucial cog in this was to have an infrastructure expert **as a traveller** between teams. He made sure that the delivery process was going smoothly and did most of the communication with the external service provider. Ideally, this work was not needed, but thanks to him we managed to deliver after almost every Sprint.

With this measure, this infrastructure and all other **shared resource queues** are removed. Teams were capable of fully delivering business or user requests into production. In the beginning there was one week between delivering the PSPI and the actual deployment on production. By having someone of the external company once a week at our location, the waiting time was decreased to about 2 days. Besides this, team did not have to wait for anyone to make a delivery.

IT management started also to realise that this was *not a project anymore*, but **continuous product development**. Especially in the last year, a massive influx of new requests resulted in new budgets being reserved. Mainly thanks to great results, the project-paradigm organisation rather silently transformed into a product-paradigm group.

### Project management

Speaking of “projects”, In the early Scrum-But-But days, HaMIS had two project managers and one program manager, due to traditional assumptions within the larger organization still based on a project- rather than product-paradigm One of the project managers was an official HaMIS project manager while the other was mainly concerned with external communication and coordination with partially dependent projects in other companies or departments.

Unfortunately, these roles were imposed to remained after the reorganisation to a better Scrum adoption. This created some systemic conflict with the Product Owner, because the PO should have been fully responsible for communicating with external stakeholders, and coordination with other major parties. But the project managers and program manager also tried to do that.

However, they did help with administrative tasks such as producing traditional reports for traditional managers, and most important, ensuring everyone got paid ;)

Any organisational aspect concerning teams were done by teams, not managers, including: teams (re)design, hiring (except financial part) and firing people, significant architectural decisions, changing working processes. By the way, hiring was done via one full day hands-on evaluation by one of the teams. This included pair-programming, participation in Scrum meetings, and design workshops.

Effectively, although still there, the project and program managers were not part of the organization in any meaningful way, but would occasionally help by doing teams’ requests.

