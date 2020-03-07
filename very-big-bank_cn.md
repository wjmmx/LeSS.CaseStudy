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

这与[三项LeSS采用原则](https://less.works/less/adoption/three-principles.html)之一一致，该原则指出，为了成功地组织级采用LeSS，必须要“*深而窄优于宽而浅*”。进一步，LeSS指南之一还建议组织在采用LeSS时必须“ .. *将采用LeSS的工作重点放在某一个产品团队上，为他们提供所需的所有支持，并确保他们工作得很好* .... ”

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

在教练的引导下，代表了所有三个组件的高级管理人员和利益相关者一起进行了“工作坊准备活动”。使用了几种可视化技术（业务价值流，用户体验地图，用户故事地图）来吸引参与者进入对话和一系列用例模拟，这些用例模拟揭示了，没有哪个组件能代表完整的端到端客户或用户特性。

Perhaps the most important education activity during this step in preparing to create feature teams was the following:

**Managers had to learn to see that component-team development was the root cause of integration and excessive cross-team coordination problems.**

It was important that they understood some organizational implications of moving from component teams to feature teams. Specifically, with feature-team development, the control by existing VBB “component owners” would need to be eliminated. As will be explored later, this issue will become one source of dysfunction in the adoption.

The original CAR component team was in an external (and very remote) vendor company. It added an additional degree of complexity: time zones, vendor middlemen, handovers, and above all, commercial contracts influencing dysfunctional to internal behavioral “contracts”. As a part of moving towards feature teams, it was decided that vendor developers would be mixed with internal developers, in ways that would de-emphasize belonging to different companies and emphasize belonging to the same feature teams. A series of meetings with VBB and vendor managers were held about the importance of having legal contracts written in ways that supports agile ways of working Some LeSS experiments were presented and discussed in the context of what was known about the existing organizational dynamics:

* *Try...Lawyers study problems arising from silo mentality and lack of systems thinking*
* *Try...Lawyers study agile, iterative, & systems-thinking concepts*

The coaches also suggested that corporate attorneys should be invited to future training and coaching sessions. )

The coaches also organized **a <u>full-group training workshop</u>.** The coaches covered basic tenets of Scrum and LeSS. Particular focus was put on the difference between Scrum and LeSS, with respect to roles, events and artifacts. In training, developers were mixed with business people and managers at tables, for better collaboration and learning (there was no ‘developers-only’ table, or ‘managers-only’ table). During the workshop the coaches covered all LeSS rules and principles. They also discussed LeSS guides and provided some examples of documented LeSS experiments. The audience was also introduced to LeSS Huge but it was made clear that it would not be necessary in this adoption (since there was less than “8” feature teams).

#### 自设计团队会议 Self-Designing Teams Meeting

Before facilitating a self-designing teams meeting, both coaches studied [one of the older case studies](https://less.works/blog/2018/12/27/how-to-form-teams-a-story-of-self-designing-teams.html), that described a similar event at another large bankfinancial company). This was helpful as the coaches got to read about some practical techniques that could be used with the teams.

Graphic illustration of key elements of the new product group was visualized on giant whiteboards: the components, other supporting applications outside the group, individual skills and domain expertise required, and geographic locations. A few additional graphic illustrations were written on flip-charts of historical learnings of shortcomings of working in siloed ways, to remind people ‘the WHYs’ behind the exercise.

During the meeting some managers were on standby to address organizational issues, should those arise. Specifically, going into this meeting, there were some concerns about:

* attempts by prior designated team leads to influence decisions of others
* building teams around existing reporting lines and/or single components (e.g. UI or DB team)
* persons not wanting to be on the same team with someone else because personal dislikes, etc.

Managers were explicitly asked to stay out of the self-designing teams meeting unless concerns became true risks. Luckily the only manager involvement that was necessary was providing some information about a small handful of newly hired but not yet on-boarded developers that would be added to the team within weeks. Another managerial input was reinforcing that the newly formed teams would be long-lived.

Of course, the key activity of the meeting was that people self-organized into new teams. This was done with all people coming together and discussing best ways to cluster into teams to deliver end-to-end features. The LeSS “use volunteering” adoption principle was used. At the beginning, everyone was reminded of the goals of the product and the workshop, as well as what it would mean to form well-structured teams, by ensuring that each team is co-located, cross-functional, knowledgeable of several components, self-managed, sized between 3 to 9 people, and long-lived.

Finally, three collocated feature teams were formed to work on the same product, sharing one Product Backlog.

### 初始PBR工作坊

Before starting Sprint 1, the product group decided to follow one of LeSS guides and hold an *initial* Product Backlog Refinement (PBR) workshop, during which the scope and vision of the product were clarified, key people required for work selected, highest priority features identified, and an initial Definition of Done clarified.

Here is an example of the vision statement for CAPCOMCAR:

> “VBB employees and external clients will prefer to use our document capture platform as the most efficient solution that enables timely setup and management of products and accounts and conforms with global, legal, regulatory and control requirements. The process will include information capture, communication and storage”

During the workshop both business and development stakeholders agreed on the high-level product themes and strategic, long-term goals. Facilitated by the coaches, this was done by using a combination of user journey identification and story mapping techniques and helped visualize *big work* that had strategic meaning. All future work was captured in one shared Product Backlog.

### 找到一个产品负责人和领域专家

Identifying someone for the role of Product Owner was challenging. It was practically impossible to find a person that would have a sufficient strategic vision and enough organizational empowerment to set priorities for multiple teams. Finally, such a person was found in the business group.

But then another challenge was faced: she did not have any knowledge of basic Scrum (let alone LeSS), and thus, of the role of Product Owner. This was addressed by helping her through Scrum training followed by personal continuous coaching support by one of the coaches.

Lastly, the product group was directly introduced to *real hands-on internal users* that were asked to be available to provide clarifications and details to the teams. Special care was exercised in selecting these people and making sure that they were not middlemen, delegates, or proxies. Three individuals were identified that had a lot of hands-on knowledge with each one of the above mentioned components (and related steps in the Document Management process): CAP, COM, CAR.

### 形成社区

In line with the LeSS guide and experiments, several communities were created. (*LeSS experiment: Try... Cultivate Communities of Practice. Try... Use CoPs for functional learning.*)

This started with a **Scrum Master Community**. Emphasis was made on improving facilitation skills of Scrum Masters and their ability to distinguish between team-level (internal) impediments and organizational (external) impediments. Based on the community involvement it was easy to differentiate between individuals that could become great candidates for the role of Scrum Master and those that would not. Through the community, Scrum Masters were able to further develop.

There was a lack of maturity in automated testing. To remediate this a **Test Automation community** was created. This allowed experience to be shared and establish better testing practices. This gave birth to gradual absorption of test automation activities into the teams.

### 使组织结构和沟通扁平化

(*LeSS Experiment: Try... Keep the organization as flat as possible*)

A key message that was frequently delivered to management was that *organizational design is the first order (key) factor* that influences organizational culture and individual behaviours, and the behavior of the overall organizational system. Various coaching tools and techniques were used to help people see this: causal-loop diagrams, surveys, discussions. As a result some steps were taken to improve dynamics within Development:

* Strong messages were delivered by senior management that becoming a ‘line manager’ (by title) and acquiring reportees did not equate to a guarantee of promotion or salary increase
* The number of people reporting to the same manager was increased to the upper recommended level of about 20-25.
* Individuals were encouraged *not* to perceive their immediate line manager as an impermeable layer, above and beyond which they were forbidden to go. On the contrary, a series of meetings with line-manager+1 were instituted.
* To strengthen the message that line managers were *not* the only channel for communication, more senior management (at the recommendation of the coaches) instituted the Impediments Removal Service (“IRS”) so that any team member could escalate their problem.

Below (**Figure 3**), is a graphic illustration that was used to educate the organization on the concept of organizational flattening that was required for scaling organizational adaptiveness:

<figure>
<img src="img/case-studies/very-big-bank/organizational-flattening.png" alt="Organizational Flattening">
  <figcaption>Figure 3: Organizational Flattening</figcaption>
</figure>

## 早期迭代

### 运行LeSS的Sprint

The following was implemented by the teams:

* Sprint Planning - Multi-team with whole teams in attendance.
* PBR - *Overall* Product Backlog Refinement (PBR) sessions were followed by *multi-team* PBRs, during which the teams discussed low-level implementation details. The coaches made it explicit that having single-team PBRs would be undesirable, because it would lead to creating separate “implicit” Product Backlogs per team and local optimizations.
* Sprint Review - Attended by all teams with Product Owner, users, and stakeholders.
* Retrospectives - There were team-specific Retrospectives attended by Scrum Masters and teams only. There was an Overall Retrospective attended by Product Owner, team members, and Development managers. The latter was invited to learn and take responsibility for removing organization-level impediments.

### 早期成果和业务感知

The first step of the LeSS adoption to a broader product and feature teams impressed the users enough to ask for *more*. In short, they said, “*we really like what you have been producing and we want more of it. What would it take to have more features delivered to us, more frequently*”?

Why were the users pleased with the *initial* results of the LeSS adoption?

* First, they were able to see more complete features at the end of each Sprint, not just disjointed components that require further integration.
* Second, thanks to teams’ improved design and stability, consistency of delivery was increased. It further led to improved ability to forecast delivery of features to users.
* Third, and as a result to the first two points, overall relationship between business and technology improved. Trust and respect started building up.

### 特性团队从三个扩展为五个

Because of the benefits and also the desire for more features, two more teams were created with developers from the same technology space, and put through some initial preparatory steps.

These steps included: a refresher training on basic Scrum, introduction to LeSS, familiarizing new teams with the Product Backlog, priorities and strategic goals, and then bringing them into the LeSS product group for an upcoming Sprint.

One of the experienced Scrum Masters from the first three teams was asked to serve the new teams, and the other Scrum Master served the original three teams. Now the product group of five teams had two Scrum Masters. This was in line with a LeSS rule: “*A Scrum Master is a dedicated full-time role. One Scrum Master can serve 1-3 teams*”.

A few senior developers from the first three teams were asked to temporarily take on the role of <u>developers-travelers</u> (*LeSS experiment: Try... Travelers*), and join the new teams, to lead by example and provide some guidance. The travelers temporarily became a *pivot* for each of the newly created teams by teaching new members not just the dynamics of LeSS but also certain nuances of different components that the new teams did not know.

To speed the process of assimilation with more experienced teams, all teams agreed that both *new* teams would be coming to multi-team LeSS events (Sprint Planning 1, multi-team PBR) in *full*, whereas the three seasoned teams would be sending just representatives. Also, for a few initial Sprints, the two new teams went into multi-team Sprint Planning 2 with at least one of the original three teams. This approach was used for a few Sprints until everyone gained confidence that the newly joined teams became comfortable enough with the process of the LeSS events.

#### 在运行五个团队Sprint时的调整 Changes in Running a Sprint with Five Teams

Sprint Planning - Part 1 (“what”) and 2 (“how”) became more clearly distinguished in purpose and attendance. Part 1 had just *representatives* from the three mature teams, plus *all members* from the newly added teams. Having all new team members made sense: while planning sessions did not get too crowded, newbies benefited from attending and learning together.

In Sprint Planning Part 2, the goal of each team was to define its own Sprint Backlog. Given the nature of work and the preference to discuss technical solutions of backlog items together - something that would increase domain knowledge and mutual understanding of the work, as well as allow leaving decisions about which team picks up which Product Backlog item until the last possible moment, the 5 teams would typically do planning *together* (*LeSS Guide: Multi-Team Sprint Planning Two*). Rarely, the teams split up into two teams + three teams sub-groups for planning .

## 限制改进的组织元素

### 财务和预算政策

(**LeSS Experiment**: *Try... Beyond budgeting*)

At VBB, there is a strong belief that “*everyone must follow the plan and say on-budget*”, as opposed to “*everyone needs to be able to respond to changes, and take advantage of newly raising opportunities*”. As such, budgeting is still done traditionally by once-a-year allocating a fixed amount to new projects (with fixed timeline and scope), basing decisions on a prior year’s expenditures and coarse-grained estimates from hands-off Development managers.

With this approach, the following challenges are constantly in faced:

* Of course very broadly, delivering the wrong thing and not responding to changes and learning, because of a *project* model rather than a *product* model.
* Decisions about what to do made by Development managers, rather than a business-side Product Owner.
* Inacuracy of estimated budgets are translated unexpectedly de-scoping critical features, and by doing so, upsetting users.
* Rushing to deliver fast, without proper testing, and by doing so, compromising product quality.
* Terminating good but more expensive developers and hiring cheap low-quality developers.
* Related to the all above, process-heavy budget-extension requests that are frequently accompanied by finger-pointing between Development and Business, leading to relationship deterioration.
* Fea by developers to experiment and innovate, because experimentation and innovations are not budgeted for.
* In some cases if an allocated budget is not fully spent by year-end, ‘burning’ it on something unimportant. Otherwise risking not getting the same amount the following year.

The coaches organized a workshop to educate managers in

* adaptive budget planning
* work on a *product* with continuous adaptive delivery rather than on *projects*
* differences between output and outcome

One of LeSS experiments “*Try... Beyond Budgeting*” was introduced and explained by leveraging industry examples described in “Implementing Beyond Budgeting” by Bjarte Bogsnes (selected <u>excerpts</u> from the author’s book were reviewed).

Although the coaches *were* able to develop appreciation by management for these ideas, unfortunately, conventional top-down fiscal year planning remained the official approach to do budgeting during the LeSS adoption.

However, the *limited victory* that the coaches had was convincing the management to consult more frequently and directly with teams with respect to forecasting, and with the Product Owner with respect to emerging needs and (re)prioritization. These conversations started happening every month (after every second Sprint).

### 产品负责人 Availability

One issue was continuous unavailability of one of the key stakeholders, whose input to Product Owner and the teams was critical. This person was continuously travelling and not too keen to attend Sprint Reviews. Instead, she would send delegates to ‘*represent her views*’. This was not sufficient, since information was often skewed and twisted in translation. Senior management took necessary steps to ensure that the required person became available in future Sprint Reviews.

### 现有的汇报结构

While the LeSS structure prevailed, and the self-formed teams were also self-managing, without any apparent interference from first-line management, the formal traditional reporting relationships were *not* officially eliminated. This was primarily due to the twice-annual performance-review process forced by HR. This led to a variety of wastes and some conflicts.

### 产品负责人身边的经理们

Even after CAPCOMCAR product was properly defined, teams properly structured and Product Owner elected, there was still one issue remaining: *communication*.

There were still attempts by technical managers of Development, that were outside of LeSS product group, to request technical improvements and “side work” from teams, without cleaning it first with the Product Owner - and justifying their actions by perceived urgency. For some time, it continued, despite strong recommendations by the coaches not to do so and follow LeSS the advice in the “Getting Started” guide instead: “*only the Product Owner provides work for the teams*” and “*keep project managers away from the teams*”.

Given the potentially unpleasant implications to developers (e.g. accusing them in not respecting subordination boundaries, leading to low performance appraisals), of refusing to obey hierarchical lines, an experiment was attempted by the teams to* inform* the Product Owner of such managerial “emergency changes”. This was done implicitly, rather than explicitly, to avoid inflaming situations, and as follows:

On a few occasions, line management was invited in PBR sessions as guests where they were asked to state their most pressing needs explicitly and candidly, in front of Product Owner and some key stakeholders. This was discussed in the context of the teams’ capacity and priorities coming from the business. Very diplomatically, line management was put in a situation, when they had to negotiate *not* with the teams but with Product Owner directly - what priorities should be. The teams merely observed and contributed to a dialogue in various ways (e.g. clarifying capabilities, limitations, dependencies, etc). By removing themselves from potentially unsafe negotiations, the teams were able to focus more on work and less on politics. This approach has worked, as the teams were no longer as exposed and were out of harm’s way.

#### 最小化副作用，而且支持单一产品订货单 Minimizing Side-work and Supporting Single Product Backlog 

Due to a significant amount of interruptions it became critical to increase transparency on the associated dollar-cost of unplanned/”hidden”/side-work. As it is often the case within large enterprise organisations, facilitating big changes required an empirical approach. For this, the teams were advised to *stop using a separate backlog to manage interruptions and side-work*, and instead keep all of their work in one shared Product Backlog. This allowed the Product Owner to refer to one single “source of truth”, instead of multiple independent “containers of wishes” - to see the overall amount of work the teams were asked to deliver, with conflicting priorities, and by doing so, set real priorities.

Taking into account inevitable work interruptions, helped manage the teams’ capacity and better reflect it during planning. After several Sprints, senior management was presented with the data that illustrated how ad-hoc, unplanned/interruptive work diluted the teams’ attention and shifted their focus away from planned and forecasted product-centric work. The main way to illustrate the problem was data collected from cumulative flow diagrams (CFD) that exposed how long Sprint work, on average, spent in each status. Overall, WIP for each Sprint backlog item was very high and it was mainly due to frequent interruptions (start-stop-start-stop), caused by new, unplanned work, being forced into a Sprint by managers.

This led to making some hard, but necessary, decisions: to mandate from requesting individuals and business groups that tried to put their priorities on top of and around Product Owner’s priorities, to stop doing so. It was discussed and agreed upon by the heads of Development and Business organizational structures that requests would go through the Product Owner.

### 传统管理沟通途径 

As mentioned above, the hierarchy of VBB was such that it led to command and control behaviours between reporting layers. Any action that, rightly or wrongly, deviated from the path dictated by management lines, or challenged existing norms and order, was often seen as risky and was discouraged.

Most attempts to put to light underlying problems and impediments went in vain. This was indicative of an endemic problem, as historically, the company actively resisted changes.

The coaches faced the dilemma: “*how to help senior management admit that problems exist and require attention, and then make everyone else comfortable to step up, speak up and engage?*”

To overcome this barrier, a compromise solution was proposed. It provided at least a safety-net for some more courageous individuals, who would otherwise have had only the option of escalating through the hierarchy and putting themselves at risk, to get their observations and concerns brought to light and to senior management.

As an experiment, the coaches have conducted a few sessions with senior management, educating them on the benefits of *gemba/go-see*. Specifically, managers were informed (based on the LeSS Guide “Go See”) that the purpose of go-see was not to micromanage, give orders or attempt to solve problems for teams. Rather, the purpose of *go-see* was to learn/understand teams’ problems and teach them how to solve problems independently of managerial control.

The management was encouraged to start coming down to teams’ area, and talk to individuals in their work area/seats, and ask questions about concerns, solicit feedback. Management was guided specifically *not* to *push back* problems back onto teams and *not* to try to *solve* problems for teams. Instead, the management was guided to *teach* teams how to solve problems independently.

The management also decided to resort to various discrete escalation techniques that would encourage individuals from lower organizational levels communicate directly to higher organizational levels. The “IRS” (Impediment Removal Service) was introduced, as a means of safer escalation of problems from teams and Scrum Masters to senior management. It came in the form of a dedicated internal email address alias that anyone could submit their personal challenge/problem in the form of a community discussion.

### 管理Manager Component Owners

The manager component owners were a source of initial resistance against forming cross-component feature teams. Why? For component owners, *ownership* meant personal visibility, power and control and, therefore, a better chance to be promoted and better compensated.

So the more senior managers needed to figure out a way to ensure that prior component owners were removed from the organization during LeSS adoption. How could this be done swiftly?

Component owners that still possessed strong technical skills were offered an opportunity to join teams and become hands-on contributors. They were also offered the role of *component mentors* whose responsibility would be to teach other developers.

The other component owners were moved to other parts of the organization.

In order for the above changes not to cause too much unest, senior managers conducted a round of discussions with all prior component owners and explained to them that going forward, their individual contribution and performance would be measured based less on *owning, doing and telling* others what to do and more on teaching/mentoring. People were given assurance that by educating their teammates, prior component owners would be neither reducing their own importance, nor putting their own jobs at risk. LeSS Guide: “Job Safety but not Role Safety” - was leveraged for this.

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


