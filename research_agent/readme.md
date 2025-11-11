### 2.1 Example: Research & Summarization System

Let's build a system with two specialized agents:

1. **Research Agent** - Searches for information using Google Search
2. **Summarizer Agent** - Creates concise summaries from research findings



---
### Section 2

## 🤔 Why Multi-Agent Systems? + Your First Multi-Agent

**The Problem: The "Do-It-All" Agent**

Single agents can do a lot. But what happens when the task gets complex? A single "monolithic" agent that tries to do research, writing, editing, and fact-checking all at once becomes a problem. Its instruction prompt gets long and confusing. It's hard to debug (which part failed?), difficult to maintain, and often produces unreliable results.

**The Solution: A Team of Specialists**

Instead of one "do-it-all" agent, we can build a **multi-agent system**. This is a team of simple, specialized agents that collaborate, just like a real-world team. Each agent has one clear job (e.g., one agent *only* does research, another *only* writes). This makes them easier to build, easier to test, and much more powerful and reliable when working together.

To learn more, check out the documentation related to [LLM agents in ADK](https://google.github.io/adk-docs/agents/llm-agents/).

**Architecture: Single Agent vs Multi-Agent Team**

<!--
```mermaid
graph TD
    subgraph Single["❌ Monolithic Agent"]
        A["One Agent Does Everything"]
    end

    subgraph Multi["✅ Multi-Agent Team"]
        B["Root Coordinator"] -- > C["Research Specialist"]
        B -- > E["Summary Specialist"]

        C -- >|findings| F["Shared State"]
        E -- >|summary| F
    end

    style A fill:#ffcccc
    style B fill:#ccffcc
    style F fill:#ffffcc
```
-->