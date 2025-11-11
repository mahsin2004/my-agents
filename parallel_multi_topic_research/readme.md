
### 4.1 Example: Parallel Multi-Topic Research

Let's build a system with four agents:

1. **Tech Researcher** - Researches AI/ML news and trends
2. **Health Researcher** - Researches recent medical news and trends
3. **Finance Researcher** - Researches finance and fintech news and trends
4. **Aggregator Agent** - Combines all research findings into a single summary


<img width="600" src="https://storage.googleapis.com/github-repo/kaggle-5days-ai/day1/parallel-agent.png" alt="Parallel Agent" />

---
### Section 4
## 🛣️ Parallel Workflows - Independent Researchers

**The Problem: The Bottleneck**

The previous sequential agent is great, but it's an assembly line. Each step must wait for the previous one to finish. What if you have several tasks that are **not dependent** on each other? For example, researching three *different* topics. Running them in sequence would be slow and inefficient, creating a bottleneck where each task waits unnecessarily.

**The Solution: Concurrent Execution**

When you have independent tasks, you can run them all at the same time using a `ParallelAgent`. This agent executes all of its sub-agents concurrently, dramatically speeding up the workflow. Once all parallel tasks are complete, you can then pass their combined results to a final 'aggregator' step.

**Use Parallel when:** Tasks are independent, speed matters, and you can execute concurrently.

To learn more, check out the documentation related to [parallel agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/parallel-agents/).

**Architecture: Multi-Topic Research**

<!--
```mermaid
graph TD
    A["User Request: Research 3 topics"] -- > B["Parallel Execution"]
    B -- > C["Tech Researcher"]
    B -- > D["Health Researcher"]
    B -- > E["Finance Researcher"]

    C -- > F["Aggregator"]
    D -- > F
    E -- > F
    F -- > G["Combined Report"]

    style B fill:#ffffcc
    style F fill:#ffccff
```
-->