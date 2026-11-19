# ASE-Portfolio-Santilices

**Course:** CPELX230-330  
**Activity:** Weeks 02–04

## Course Introduction

This course explores how software engineering practices support the design and development of AI agents. Topics include the differences between conventional and agentic systems, Agile teamwork, Git version control, and responsible AI deployment.

## Personal Learning Goals

- Design an AI agent with a clear goal, limited tool permissions, and a way for people to intervene.
- Practice using Git branches, commits, and pull requests to review changes and track progress.
- Apply iterative testing to a PondSense advisory feature and evaluate how it handles stale sensor data, false alarms, and missed warnings.

## Part A — Concept Analysis and Reflection

### 1. What is Agentic Software Engineering?

Agentic Software Engineering applies software engineering practices to systems that use AI agents. It also covers using agents to assist with development tasks such as writing tests or reviewing code. When building an agentic system, developers define its goal, decide which tools it can use, limit its permissions, and test how it behaves when information is missing or a tool fails.

### 2. How does an AI agent differ from a traditional application?

A traditional application follows workflows defined in code. For example, a pond dashboard can send a fixed alert when dissolved oxygen falls below a configured threshold. An AI agent can pursue a broader goal, such as helping a farmer assess a potential oxygen drop. It can check recent readings, notice that a reading is stale, and ask for a manual check before recommending action. The agent chooses its next step based on the information available and the tools it is allowed to use.

### 3. Why are Agile methods appropriate?

An agent can respond differently as inputs and conditions change, so short development cycles give the team frequent opportunities to inspect results and improve the system. In a Scrum Sprint, the team could test one small feature, review false alarms with farmers at the Sprint Review, and update the backlog based on feedback. Git commits and pull requests help teammates trace changes, review them, and restore a working version if needed.

### 4. What risks should developers consider?

Agents can make incorrect recommendations, expose private data, or take unintended actions with their tools. In a pond, stale sensor data could make an agent miss a drop in oxygen, while repeated false alerts could cause a farmer to ignore a real warning. Developers should test failure cases, restrict tool permissions, and keep records of important decisions and actions.

### 5. Why is human oversight important?

A person can verify uncertain results, approve actions with serious consequences, and override the system when conditions change. The interface should show what the agent observed and why it made a recommendation. Assigning responsibility for reviewing alerts and handling failures also makes it clear who should intervene.

**Reflection.** A pond monitoring agent can help a farmer interpret readings, but I would test its recommendations before letting farmers rely on them. Showing the age of each reading and giving farmers a way to verify a warning would make the feature easier to use responsibly.

## Part C — Reflection Paper

For our PondSense capstone, I would use an AI agent to help farmers decide when to check their pond for possible oxygen problems. If dissolved oxygen starts falling overnight, the agent could summarize the recent trend, show when the last reading was taken, and recommend a manual check if the data is incomplete. A farmer could then see why an alert appeared and decide what to do.

I would start by testing the agent in advisory mode using recorded readings. I would include cases such as a disconnected sensor, delayed data, and a sudden oxygen drop to see whether its recommendations are appropriate. For equipment control, I would keep the tested local aeration rules in place and give the operator a way to override them. A clear “data unavailable” message would help a farmer recognize when the system needs a manual check.

Privacy matters because a farmer’s contact details and pond records may be sensitive. I would limit the data the agent receives, restrict account access to the assigned pond, and tell farmers what is collected and why. I would also log alerts and review missed warnings and false alarms with operators. To me, responsible AI means giving farmers information they can verify and keeping them in control of decisions that affect their livelihood.

## References

- Sommerville, I. Software Engineering, 10th ed., Chapters 1–2.
- [Russell, S., & Norvig, P. Artificial Intelligence: A Modern Approach, Chapter 2.](https://aima.cs.berkeley.edu/)
- [Schwaber, K., & Sutherland, J. (2020). The Scrum Guide.](https://scrumguides.org/scrum-guide.html)
- [Chacon, S., & Straub, B. Pro Git, 2nd ed., Chapters 1–2.](https://git-scm.com/book/en/v2)
- [NIST. (2023). Artificial Intelligence Risk Management Framework (AI RMF 1.0).](https://doi.org/10.6028/NIST.AI.100-1)
