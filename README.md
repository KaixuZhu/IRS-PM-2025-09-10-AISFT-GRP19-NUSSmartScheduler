---

## SECTION 1 : PROJECT TITLE

## NUS Smart Scheduler

An AI-Powered Multi-Agent Smart Event Scheduling System

---

## SECTION 2 : EXECUTIVE SUMMARY / PAPER ABSTRACT

University students and staff often struggle to manage lectures, meetings, personal activities, and campus travel within limited time. Traditional scheduling tools require manual input, lack contextual understanding, and cannot adapt to individual preferences or optimize across multiple constraints. As a result, users spend significant effort planning their day, yet still end up with inefficient schedules.

To solve this problem, we developed **NUS Smart Scheduler**, an AI-powered system that converts natural language descriptions into optimized daily schedules. The system supports both structured task input and conversational interaction, allowing users to plan their day in a flexible and intuitive manner. Schedules are displayed using timeline visualizations and multiple candidate plans can be compared easily.

The core of the system is a **multi-agent collaborative architecture**. DialogueAgent understands user intent and extracts tasks, KnowledgeAgent retrieves campus information via **RAG**, MemoryAgent loads personalized preferences, RerankerAgent improves the relevance of retrieved results, and SchedulingAgent generates optimized plans using a **custom-built solver**. All agents communicate through a shared global state and follow a ReAct-style reasoning and acting workflow, making the process interpretable and flexible.

To generate high-quality schedules, tasks are modeled in discrete time slots with **hard constraints**. A **hybrid greedy + local search solver** is implemented, supporting multiple optimization modes such as travel-first, preference-first, and compact-day. The system also features **adaptive learning**, continuously improving through memory, feedback, and personalized objective tuning.

Evaluation results show that our solver produces more feasible and user-centric schedules than baseline methods, with significantly lower travel cost and higher preference satisfaction. Reranker experiments demonstrate improved retrieval and ranking accuracy. With an intuitive frontend offering Solver Mode and Agent Mode, **NUS Smart Scheduler** provides an intelligent, personalized, and scalable solution for real-world academic scheduling.

---

## SECTION 3 : CREDITS / PROJECT CONTRIBUTION

| Official Full Name | Student ID | Work Items (Who Did What)                                                                                                                                                                                       | Email              |
| :------------------- | :----------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------- |
| Zhu Kaixu          | A0328919M | Full-stack system development , multi-agent implementation, custom solver development, agent logic & API integration, system integration and testing, demo video, and writing Section 3 and Section 4 of report | e1553246@u.nus.edu |
| Chen Xinyu         | A0317887J | Business problem analysis, requirement research, use case design, and writing Section 1,2,5 of report                                                                                                           | e1519747@u.nus.edu |

---

## SECTION 4 : VIDEO OF SYSTEM MODELLING & USE CASE DEMO



---

## SECTION 5 : USER GUIDE

Refer to appendix **<Installation & User Guide>** in project report (Github Folder: `ProjectReport`)

---

## SECTION 6 : PROJECT REPORT / PAPER

Refer to full project report in Github Folder: `ProjectReport`.

---

## SECTION 7 : MISCELLANEOUS

Refer to `Miscellaneous` folder for additional resources.

Possible contents:

- Survey / Dataset
- UI Mockups / Prototype images
- PPT slides or presentation assets

---

**This project is part of the Artificial Intelligent Systems Programme at NUS-ISS.**