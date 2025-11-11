
### 3.1 Example: Blog Post Creation with Sequential Agents

Let's build a system with three specialized agents:

1. **Outline Agent** - Creates a blog outline for a given topic
2. **Writer Agent** - Writes a blog post
3. **Editor Agent** - Edits a blog post draft for clarity and structure

<img width="1000" src="https://storage.googleapis.com/github-repo/kaggle-5days-ai/day1/sequential-agent.png" alt="Sequential Agent" />

---

### Section 3
## 🚥 Sequential Workflows - The Assembly Line

**The Problem: Unpredictable Order**

The previous multi-agent system worked, but it relied on a **detailed instruction prompt** to force the LLM to run steps in order. This can be unreliable. A complex LLM might decide to skip a step, run them in the wrong order, or get "stuck," making the process unpredictable.

**The Solution: A Fixed Pipeline**

When you need tasks to happen in a **guaranteed, specific order**, you can use a `SequentialAgent`. This agent acts like an assembly line, running each sub-agent in the exact order you list them. The output of one agent automatically becomes the input for the next, creating a predictable and reliable workflow.

**Use Sequential when:** Order matters, you need a linear pipeline, or each step builds on the previous one.

To learn more, check out the documentation related to [sequential agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/sequential-agents/).

**Architecture: Blog Post Creation Pipeline**

<!--
```mermaid
graph LR
    A["User Input: Blog about AI"] -- > B["Outline Agent"]
    B -- >|blog_outline| C["Writer Agent"]
    C -- >|blog_draft| D["Editor Agent"]
    D -- >|final_blog| E["Output"]

    style B fill:#ffcccc
    style C fill:#ccffcc
    style D fill:#ccccff
```
-->