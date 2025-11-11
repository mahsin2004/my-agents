 Terminal open with as admistration run then switch the path belw command
**cd "D:\My Projects\Agent Development"**

Run project in terminal 
**adk run agentName or direactoryName**

Run project with web interface 
**adk web --port 8000**

open and select agent


## Summary - Choosing the Right Pattern

### Decision Tree: Which Workflow Pattern?

<!--
```mermaid
graph TD
    A{"What kind of workflow do you need?"} -- > B["Fixed Pipeline<br>(A → B → C)"];
    A -- > C["Concurrent Tasks<br>(Run A, B, C all at once)"];
    A -- > D["Iterative Refinement<br>(A ⇆ B)"];
    A -- > E["Dynamic Decisions<br>(Let the LLM decide what to do)"];

    B -- > B_S["Use <b>SequentialAgent</b>"];
    C -- > C_S["Use <b>ParallelAgent</b>"];
    D -- > D_S["Use <b>LoopAgent</b>"];
    E -- > E_S["Use <b>LLM Orchestrator</b><br>(Agent with other agents as tools)"];

    style B_S fill:#f9f,stroke:#333,stroke-width:2px
    style C_S fill:#ccf,stroke:#333,stroke-width:2px
    style D_S fill:#cff,stroke:#333,stroke-width:2px
    style E_S fill:#cfc,stroke:#333,stroke-width:2px
```
-->

<img width="1000" src="https://storage.googleapis.com/github-repo/kaggle-5days-ai/day1/agent-decision-tree.png" alt="Agent Decision Tree" />


### Quick Reference Table

| Pattern | When to Use | Example | Key Feature |
|---------|-------------|---------|-------------|
| **LLM-based (sub_agents)** | Dynamic orchestration needed | Research + Summarize | LLM decides what to call |
| **Sequential** | Order matters, linear pipeline | Outline → Write → Edit | Deterministic order |
| **Parallel** | Independent tasks, speed matters | Multi-topic research | Concurrent execution |
| **Loop** | Iterative improvement needed | Writer + Critic refinement | Repeated cycles |


---

## ✅ Congratulations! You're Now an Agent Orchestrator

In this notebook, you made the leap from a single agent to a **multi-agent system**.

You saw **why** a team of specialists is easier to build and debug than one "do-it-all" agent. Most importantly, you learned how to be the **director** of that team.

You used `SequentialAgent`, `ParallelAgent`, and `LoopAgent` to create deterministic workflows, and you even used an LLM as a 'manager' to make dynamic decisions. You also mastered the "plumbing" by using `output_key` to pass state between agents and make them collaborative.

**ℹ️ Note: No submission required!**

This notebook is for your hands-on practice and learning only. You **do not** need to submit it anywhere to complete the course.

### 📚 Learn More

Refer to the following documentation to learn more:

- [Agents in ADK](https://google.github.io/adk-docs/agents/)
- [Sequential Agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/sequential-agents/)
- [Parallel Agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/parallel-agents/)
- [Loop Agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/)
- [Custom Agents in ADK](https://google.github.io/adk-docs/agents/custom-agents/)

### 🎯 Next Steps

Ready for the next challenge? Stay tuned for Day 2 notebooks where we'll learn how to create **Custom Functions, use MCP Tools** and manage **Long-Running operations!**

