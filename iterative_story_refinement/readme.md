
### 5.1 Example: Iterative Story Refinement

Let's build a system with two agents:

1. **Writer Agent** - Writes a draft of a short story
2. **Critic Agent** - Reviews and critiques the short story to suggest improvements



<img width="250" src="https://storage.googleapis.com/github-repo/kaggle-5days-ai/day1/loop-agent.png" alt="Loop Agent" />

---
### Section 5
## ➰ Loop Workflows - The Refinement Cycle

**The Problem: One-Shot Quality**

All the workflows we've seen so far run from start to finish. The `SequentialAgent` and `ParallelAgent` produce their final output and then stop. This 'one-shot' approach isn't good for tasks that require refinement and quality control. What if the first draft of our story is bad? We have no way to review it and ask for a rewrite.

**The Solution: Iterative Refinement**

When a task needs to be improved through cycles of feedback and revision, you can use a `LoopAgent`. A `LoopAgent` runs a set of sub-agents repeatedly *until a specific condition is met or a maximum number of iterations is reached.* This creates a refinement cycle, allowing the agent system to improve its own work over and over.

**Use Loop when:** Iterative improvement is needed, quality refinement matters, or you need repeated cycles.

To learn more, check out the documentation related to [loop agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/).

**Architecture: Story Writing & Critique Loop**

<!--
```mermaid
graph TD
    A["Initial Prompt"] -- > B["Writer Agent"]
    B -- >|story| C["Critic Agent"]
    C -- >|critique| D{"Iteration < Max<br>AND<br>Not Approved?"}
    D -- >|Yes| B
    D -- >|No| E["Final Story"]

    style B fill:#ccffcc
    style C fill:#ffcccc
    style D fill:#ffffcc
```
-->