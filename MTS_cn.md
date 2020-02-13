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
  <img src="/img/case-studies/mts-kassa/mts-kassa-product.jpg" alt="MTS Kassa Product">
</figure>

从此，LiteBox成为庞大的MTS公司（拥有70,000名员工）的一部分，但它在管理自己的业务方面几乎保持完全的自主权。 到LeSS实施时，LiteBox已拥有200多名员工，并作为一个独立的业务部门运作。

### 商业机会和紧迫感

MTS管理层向我寻求帮助。 2017年底，我们进行了首次协商。 原因是LiteBox管理层预计从2018年7月1日开始将掀起一股巨大的客户增长潮（或者说是海啸），用户群将增加大约100倍。 2017年12月，LiteBox的客户数量是6000多，而到2018年秋季预计将超过10万。LiteBox管理层希望产品开发具有适应性，并容易做到规模化扩展。 在与高层管理者们进行了数次面对面会谈之后，我们同意先从一些电话访谈开始，然后进行更深入和结构化的公司审计。

### 原有的组织结构

组织架构跟想象的一样，基于传统的管理理念设计的。 公司由各个职能部门或者说筒仓组成（财务，采购，销售，IT，市场营销，人力资源）。 每个职能部门都有自己的一些经理们，这些经理们也都有自己的一些KPI。

<figure>
  <img src="/img/case-studies/mts-kassa/original-organization.png" alt="原有的组织结构">
</figure>

### IT-department Structure

Despite the final goal transforming the whole company, we started interviewing people from IT at first. They were developing a core product and major value proposition. And this is what I found out.

**Development in Component Teams.**

30+ developers were working on the product organized in so called “project” teams. Each “project” was organized around architecture component, technology or function. Thus, they had 7 “projects”: old backend, new backend, android, windows, testing, analytics, and an API team.

<figure>
  <img src="/img/case-studies/mts-kassa/old-feature-flow.png" alt="Old Feature Flow">
</figure>

Technological stack consisted of several programming languages and relevant frameworks: Javascript, Android, Python, SQL, Java.

**Coordinating roles and hierarchy**

As none of the “projects” was able to create usable increment and produce something valuable for the customer, there was a need in several coordination roles and hierarchy in functions:

* Head of analytics department.
* Head of testing department.
* Chief architect.
* Backend tech leader.
* Android development tech leader.
* Windows development tech leader.
* Release engineer.

They were a completely traditional org that had adopted scrum terminology; in short, a completely fake agile/scrum no-change. After interviews, I spent two days in the LiteBox office practicing [Go See](/less/management/go-see.html). Besides having mechanical or [*copy-paste* Scrum](https://agilix.nl/blog/481-the-problems-of-scaling-scrum) approach, I immediately noticed two more things:

* Each project aimed for maximum utilization, obviously that was the ultimate goal for everyone.
* IT development suffered heavily from a huge number of bugs/incidents coming from production.

### My Observations and Conclusions

LiteBox had the hierarchic and functional organizational design with all associated and well-known problems.

**Dependencies.** Due to organizational structure, none of the component teams was able to deliver any feature to the customer. All component teams had dependencies that caused unnecessary planning and coordination roles.

**Handoffs and waterfall-like style.** There were numerous handoffs between the components (“projects”) that caused big queues and delayed customer feedback. The average cycle time for a feature from start to finish was 6-7 weeks.

**Single function specialists.** Organizational structure encouraged a single function roles like business analyst, tester or developer, which made the organization fragile and vulnerable to the market changes. The current organizational structure has been optimized for busyness (“utilization”) of people, rather than for flexibility and fast value delivery.

**Narrow focus.** Teams didn’t see the whole product, just its parts. Developers were focused on their individual busyness, not on the system effectiveness and fast value delivery. Quoting from one of the interviews, "There is no feeling all teams are working together for a common goal." Developers didn’t fully understand the value and purpose of the features they developed, since they only did component parts.

**Lack of transparency.** Business people suffered from reduced transparency. They didn’t really know what the real progress of the development group was. Many things were worked on (large WIP) at once. The work was scattered all over the teams. Everyone was working hard and locally doing their best, but the development group was not effective at all.

**Poor requirements management.** There was no single source of requirements. Teams complained about conflicting priorities because so many stakeholders were able to push work on them: business analysts, CTO, call-center, marketing department, etc. There was no established process of ordering requirements. The current requirement management system, in the opinion of employees, was "garbage".

### Studying the Whole Company

After a series of telephone interviews and couple of days spent in LiteBox office, I presented my observations to the top managers and then rushed to the headquarters for an in-depth assessment of the whole company. We held a two days workshop with company senior management and employees focusing on company structure, values, flow of value etc. Our goal was to create an action plan and set the next steps. Some of the tools we used during the workshop were:

* **Scott-morton diagram.** This demonstrated the connection between key company building elements: strategy, processes, people and structure.
* **Weighted SWOT-analysis.** It was created in mixed groups. All the factors were weighed on-scale of importance from 1 to 5.
* **Value-stream Mapping.** This technique gave us insights into the amount of waste in the product development flow (from customer request to the value delivering). Usually it started from the first call to the customer support and finished with the new release.

**Assessment results.** The detailed company assessment proved my first conclusions regarding component teams and their dysfunctions. The value-stream mapping also showed that average cycle time for feature from start to finish was 6-7 weeks. I liked the fact that managers had some ‘Aha!’ moments during the workshop:

* They agreed there was too much hierarchy for such a middle-sized company.
* Understanding that individual KPI and bonuses locally optimized some departments in the company (sales and marketing) and opposed one function against another.
* Everybody in the room agreed that the company did not have a solid vision and no strategic plan.

**Suggestions.** No wonder that after the audit my suggestions were:

* Several Scrum trainings in IT product group to educate everyone.
* Scrum training for the CxO people.
* Strategy planning workshop to create the company vision and strategy for the upcoming 1-2 years.
* Simplify the organizational structure gradually and move away from functional organization to team-based one.
* Kick off the pilot feature-team and if it succeeds go on with LeSS.

<figure>
  <img src="/img/case-studies/mts-kassa/company-assessment.png" alt="Company Assessment">
</figure>

## Journey Start - LeSS Adoption Preparation

### Why LeSS Adoptions Require Structure Changes

An effective LeSS adoption (also an effective adoption of single-team Scrum) usually means organizational *structure* changes (*Guide: Three Adoption Principles*). The reason is that most of the organizational structures are optimised for individual outputs and have lots of local optimisations in their design. LeSS descales organizational complexity that comes from the old structures, and introduces new simpler structures. LeSS optimising goals are the following, and these usually require structure change to support them:

* Deliver highest customer value first.
* Cheap & easy adaptiveness (“turn on a dime for a dime”).
* Learning.

### Learning Basic Scrum

We invited senior management, some of the developers and all functional department managers (marketing, sales, compliance etc.) to attend a 2-day Professional Scrum Foundations (PSF) training. That helped them understand the values and principles that single-team Scrum is based on. There are guides in LeSS to help implement this framework in the organization (*Guide: Getting Started*). And the first step in that guide is: *educate everyone*. Now I realize that I did not properly educate everyone from the start and thus did not follow the guide. That caused problems with volunteering and support of the adoption quite soon.

### Aligning Management With Change Story

After training we brought together senior management again, to create a change story. It was a message for everyone in the company explaining why the company strives for changes. Luckily, we obtained support from the company owners at the very beginning. But that was not enough. We were looking for the help and support from the whole senior management group. Why? Large-scale adoption of Scrum and agile principles is not isolated to the development group. It bumps into product management, budgeting, launch, and marketing, sales and HR policies. As the company was organized by functional silos, any senior functional manager could potentially undermine the big change.

So then there was a change story workshop. As an outcome, we had two artifacts. The first was a matrix with filled Risks/Opportunities/Problems/Urgency. Managers aligned their views and why they needed Scrum.

<figure>
  <img src="/img/case-studies/mts-kassa/risks-opportunities-problems-urgency.png" alt="Risks Opportunities Problems Urgency">
</figure>

The second artifact was a change story. It is a helpful tool from [lean change management](http://leanchange.org/) movement. It looks like a short and compelling message for the rest of company with key points highlighted:

* Why we need the changes right now.
* What we are going to do.

> “Before we were agile and small. We liked it because we were autonomous, all information was transparent. Then one day we grew and became bigger and received investment from MTS. This influenced our thinking and increased the amount of work to do. That’s why we need changes in structures and processes in order to become more effective, eliminate errors and improve the product quality. We need support in mentoring and coaching to achieve agility.”

We made sure every employee received a digital version of the change story after the workshop.

<figure>
  <img src="/img/case-studies/mts-kassa/change-story.png" alt="Change Story">
</figure>

### Learning Scrum With Pilot

According to the LeSS rules, smaller LeSS implementations must be done “all-at-once”. It means that on Friday everyone works in a company with a traditional organizational structure and then on Monday a product group organizational design is flipped to the new one. Despite all the advantages of this approach, I was not able to "sell" the flip. Nevertheless, they agreed to launch a pilot feature team and later if it succeeds go on with the full LeSS adoption.

### Pilot Team Results

* In the first Sprint, the pilot feature team was able to release a new feature that unexpectedly was added to the Product Backlog after the customer interview during the kick-off. An unmet need was quickly revealed and the feature was released in a week.
* The end users participated in the Sprint Reviews and regularly gave their feedback–both qualitative and quantitative. We discovered that customer satisfaction had never been measured in the company before.
* In a few Sprints, the team dynamics changed a lot. They were starting to learn and were gradually turning into multi-functional developers. For example, an experienced windows developer during the Retrospective said that he was going to start writing Android code in a few months.
* The team members thinking and behavior changed. They started working in pairs and often swarmed. They grasped the idea that if everyone works on their own thing individually, they were unlikely to help each other and, in the long term, learn from each other.
* The team was able to implement multiple features in three different channels at once.
* The Product Owner received a more transparent development process. And he said he liked the team working like a black box that selects PBIs and gives completed features at the end with no need for extra coordination, control, etc.
* The Team directly interacted with the market. They didn't need any additional roles for coordination and they were independent.
* The average cycle time for the feature development was reduced 2-3 times in contrast to the component teams development.

I noticed that some of the component team members started visiting the Sprint Reviews. They were interested in what the pilot team was doing.

We uncovered a few negative or difficult consequences of the pilot:

* The Product Owner was under high pressure. He had to work simultaneously with the pilot feature team and other component teams. He managed 2 Product Backlogs - one сustomer-centric for the pilot, another filled with technical-task PBIs for the component teams.
* Feature team was operating in an environment that was different from the component teams. The Product Owner protected the pilot from the interruptions within a Sprint, for example production bugs and requests from technical support. Thus, some people said the feature team could not be considered a convincing experiment for them.
*There was a tension between the feature team and business analyst group. Developers started to communicate directly with the customers. The business analysts viewed the feature team concept as the threat for their job positions.
* Feature team could not independently release functionality to the market. There was still a role of the release engineer in a product group who did final system testing and made a “go for release” decision for a big batch of functionality. So, the cycle time for feature development indeed decreased a lot but the high level lead time was about the same. Features were done but had to stay in a long queue to be released.

### Company Strategy Workshop

The LeSS adoption was a part of the bigger initiative for the transformation of the whole company. One of the recommendations after a company assessment was to conduct a strategic session. The 3-days MTS Kassa strategy session was divided into two parts. The first two days were spent creating a vision of an organization and the new business strategy. During the third day the roadmap for the upcoming months was created.

**Vision story.** The punch line of the second day was creating a company vision. There were two activities: First, use a timeline to reveal the company's history with the most significant events and an industrial map creation (trends, players, industries, future market needs) and second, form the participants into small groups in which they created their version of a company vision story. We asked groups to imagine the company’s success in 2 years, “Imagine 2 years has passed and the MTC Kassa story is posted on the cover of a business magazine. What pictures/photos/quotes would be there? What would this article be about? What’s the title? What would be the main progress for the company?”

After the cover-story visioning exercise, we started crafting a short vision statement. We wanted to reach a consensus among all the participants (nearly 30 people). We spent several hours on it but it was well worth it because participants said they were really inspired by the vision created, which was:

*Every russian entrepreneur has chosen our ecosystem of B2B services as an assistant for their business.*

<figure>
  <img src="/img/case-studies/mts-kassa/vision-statement.png" alt="Vision Statement">
</figure>

**Outcomes.** One of the most important results of the strategic session was the concept of the **adaptive organization** that emerged among the senior managers. They agreed that the current organizational design was optimized for keeping people busy. That’s not consistent with adaptiveness, so therefore a key new organizational design decision was to adopt LeSS.

We banded people together around the quite bright and inspiring vision and then created a company roadmap. And that also turned out to be a great input for creating a Product Backlog.

<figure>
  <img src="/img/case-studies/mts-kassa/strategy-workshop.png" alt="Strategy Workshop">
</figure>

### Next Steps In LeSS Adoption

In the summer of 2017 I visited Craig Larman’s LeSS class in Milano. One of his memorable recommendations was "think like a politician, not like an engineer". Although the Product Owner pushed me to implement LeSS ASAP, Craig’s advice helped me to hold off with adoption. After the initial success of the pilot feature team, I observed that the level of trust from management was raised. And so we got full management support by that time. Great! But on the other hand, I realized that many developers from the component teams were still sceptical about LeSS. We wanted to educate them in order to get volunteers rather than *prisoners of the change* (*Guide: Three Adoption Principles*).

### Transformational Backlog

The Product Owner, a few volunteers from the product group, the Scrum Master from the pilot, and I formed the initial transformational group. Here are some of the items:

* Conduct Certified LeSS Basics (CLB) training.
* Conduct several lean coffee workshops to answer FAQ about LeSS.
* Create initial Product Backlog.
* Create *HitMap*.
* Facilitate team self-design workshop
* Create perfection goal.
* Teams select Scrum Masters.
* Create Definition of Done (DoD).
* Start communities and find component mentors.
* Conduct Initial PBR.

Looking back, we had spent almost two months preparing for a change to the LeSS structure.

### Learning LeSS Framework

As everyone had already attended Scrum Basics training, I thought that a one-day [Certified LeSS Basics (CLB) training](https://less.works/courses/less-basics.html) followed by a few lean coffee events would be enough to get the people buy-in. I was wrong. Now I'm sure that it is better to spend *several* days studying LeSS before you introduce the new organizational structure. People really need to understand the principles behind LeSS. You need at least several days to show how lean thinking, queueing theory and system thinking underpin LeSS rules (*Guide:Three Adoption Principles*).

Old habits and tendency towards local individual optimization appeared immediately in the first Sprint. I would definitely spend some time with developers doing system modeling and creating a few causal-loop diagrams (CLD). There is a big difference between people renting and owning the process. Also some of the topics could be covered more thoroughly during 3-day training.

Coordination seemed to be the hottest topic. People didn’t believe that it was possible to manage coordination using simple guides (*Guide: Just Talk, Guide: Communicate in code, Guide: Communities, Guide: Open Space*) because of a strong culture of narrow specialists and coordination roles that have been there for a long time. At the beginning of the training, developers filled three flipcharts with coordination questions. I asked them to create a simple table with two columns–"What to coordinate" and "Coordination Techniques". After we covered all LeSS coordination practices, I asked the participants to fill in the right column with appropriate coordination practices.

The workshop gave people an overview of LeSS, and most of the participants questions were closed. Nevertheless I felt it was only a shallow introduction. I wish I insisted on more deep dive into LeSS principles with system diagramming that could potentially result in more buy-in and better understanding of system thinking, queueing theory and lean thinking.

<figure>
  <img src="/img/case-studies/mts-kassa/certified-less-basics.png" alt="Certified LeSS Basics">
</figure>

### Try...Lean Coffee Events

Anger, uncertainty and frustration are at their peak in the early stages of the change. All change management models highlight the value of communication, and lean coffee format is a good way to maximize it. It helps provide an honest dialog and reduce the unknowns. I sent a mail and invited everyone to the lean coffee session. I thought “what if nobody comes in? That would be a total failure”. Fortunately a lot of people came in and we had wonderful discussions. Unfortunately Introduction to LeSS and training was very short. People still had lots of questions and lean coffee format helped them to get answer to those. I am using lean coffee for a long time and my experience tells me the number of people showing to it usually indicate the level of interest to the certain topic in the group.

### Selecting a Product Owner

CTO was a natural choice for the Product Owner. He was one of the co-founders of the company, knew the market, business and the customers better than anyone else. The choice was so natural that I didn’t expect any side effects, but they became visible in a few months.

### Product Backlog Creation

All the requirements were located in a redmine tool. As the current organizational design was based on component teams, Product Backlog mostly consisted of a large number of technical tasks for component teams and it was not useful. So we armed ourselves with the company vision, middle-term business goals and created the Product Backlog from scratch.

We used a visual management approach with the Product Backlog. Now it became visible and tangible, and was made of the flip-chart paper and post-its.

<figure>
  <img src="/img/case-studies/mts-kassa/product-backlog.png" alt="Product Backlog">
</figure>

### Try...Using HitMap To Analyze the Product Backlog

One of the LeSS Principles is [Customer Centric](https://less.works/less/principles/customer-centric.html). It means creating an organizational design that helps to deliver highest customer value first. We were not sure if all the feature teams should be able to simultaneously deliver value on all three UI platforms. Probably it made sense to form the teams according to the customer segments. We wanted the HitMap to give us an answer. It is a very simple and solid tool. It helps to see what architectural components are used for each PBI. HitMap outline looks this way:

<figure>
  <img src="/img/case-studies/mts-kassa/hit-map-principle.png" alt="Hit Map Principle">
</figure>

The *perfection goal* is creating feature teams that can select any PBI from the Product Backlog and deliver it to the market independently at least once per Sprint. Let's say we need same product features both on Android and iOS platforms. We probably need to create Features Teams with iOS and Android capability in each of them.

We spent a few hours creating HitMap. I asked the Product Owner to order the Product Backlog several months ahead to get a broad view. Finally, we had a few paper sheets filled with stickers. When we had finished our job, it was clear for the Product Owner that he needed fullstack feature-teams similar to a pilot Team one to obtain maximum agility. Major product features he planned to develop were needed through all three I/O channels (web, Android, Windows).

<figure>
  <img src="/img/case-studies/mts-kassa/hit-map.png" alt="Hit Map">
</figure>

### Team Self-designing Workshop

After HitMap creation Product Owner was sure that he needed fullstack feature teams. I helped him to set up a meeting and he presented everyone the final HitMap. The Product Owner arguments were very strong and there was no visible resistance for the idea of creating feature teams. Everyone could see the cross-functional cross-component feature teams could potentially give the company maximum agility and deliver the highest value features from the Product Backlog. Then we asked people to set up constraints for the Team formation and they came up with:

* Cross-functional (all development, testing, devops etc.).
* Cross-component (all platforms: Windows, Android, web).
* UI/UX.
* Size from 6 to 9 people (recommendation).
* Co-location in one room.
* I'm ok to work with these people.

I will not describe this process in details, it is better to read about it in [Ahmad Fahmy’s article](http://www.ahmadfahmy.com/blog/2013/12/5/the-rise-of-the-team).

I want to stress some interesting points that we faced. First, the members of the pilot team were allowed to join other teams but no one left the team. Second, after two rounds (15 min) we had two stable teams that satisfied all constraints. Still, there was lack of UI/UX skill in the third team. I had to facilitate quite a long discussion and the decision was:

* Someone in the team would study UI/UX.
* Use the coordination technique *Traveler* (*Guide: Traveler*).

Team self-design workshop was followed by a few team-building activities:

* Teams came up with the names (‘Alfa’, ‘Vegas’, ‘StarCraft’, ‘Circus’).
* Played the game “Market of skills”.
* Completed the matrix of competencies for all teams. Developers assessed their skill level and pointed out those they wanted to get better in.

Next morning, when I came to the office, developers had already moved to the new rooms.

<figure>
  <img src="/img/case-studies/mts-kassa/self-designing-team-workshop.png" alt="Self-designing Team Workshop">
</figure>

### Perfection Vision

One of the LeSS fundamental principles is [Continuous Improvement Towards Perfection](https://less.works/less/principles/continuous-improvement-towards-perfection.html). With LeSS framework you can improve delivering value to the customer endlessly. For instance, there are no additional roles for coordination. If the framework included them in its design, what would be the motivation for people to improve beyond it if it’s embedded into the system design? The goal of LeSS is to make single-team Scrum possible in multi-team environment without introducing new roles and rules (Principle: [Large-Scale Scrum is Scrum](https://less.works/less/principles/large_scale_scrum_is_scrum.html)).

The perfection vision for the product group or organization is a state that will never be achieved. Any improvement experiment can be considered in the context of a created perfection vision.

My colleague Cesario Ramos gave me an example of perfection vision of one organization. I had printed it and handed copies out to everybody as an example of what it could be. We asked the teams to come up with their own perfection vision. In 20 minutes, we wrote down all the ideas on a flip-chart and voted.

Ever after we referred to the perfection vision when making decision during Retrospectives. For instance, once there was an idea to create a dedicated coordinating role. It was in conflict with perfection vision and teams representatives rejected it.

<figure>
  <img src="/img/case-studies/mts-kassa/perfection-vision.png" alt="Perfection Vision">
</figure>

### Definition of Done (DoD)

We had a pilot feature team DoD as a benchmark but we still spent some time crafting the final DoD. As it often happens, developers had different understanding concerning testing terminologies (integration, e2e, functional, stress, performing). Also, their terminology was too complicated and overloaded. As a result, I suggested simplifying the categorization (*Experiment: Try... Simple testing classifications*). And it worked like a charm. The pilot feature team decided to employ a stronger version of the DoD which is in line with LeSS rules. Their list included an additional code review and more strict test coverage rules.

<figure>
  <img src="/img/case-studies/mts-kassa/definition-of-done.png" alt="Definition of Done">
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

