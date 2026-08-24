## Wes Jackson

I work on the control layer for enterprise AI agents, and on the layers underneath that make the controls work.

Thirty years building systems where a mistake is expensive: federal health, defense, public health, finance. Currently technical lead for an AI specialist architecture team. I write specifications, build reference implementations, and ship the platform pieces that governed agents actually need.

[**wesjackson.ai**](https://www.wesjackson.ai) · [**LinkedIn**](https://www.linkedin.com/in/profjackson) · [**Medium**](https://medium.com/@profjackson)

---

### The map

Enterprise AI is segmenting into five layers. Most people work in one or more of these. These are mine, with the code.

| Layer | The question it answers | What I've built |
| :---- | :---- | :---- |
| **Control** | now that they can act, how do we stop them breaking something | [ptc-gal-standards](https://github.com/wjatx/ptc-gal-standards) · [ptc-gal-reference](https://github.com/wjatx/ptc-gal-reference) · [stigcode](https://github.com/rdwj/stigcode) · [veripak](https://github.com/rdwj/veripak) |
| **Context** | make the AI understand my organization | [memory-hub](https://github.com/redhat-ai-americas/memory-hub) · [retrieval-hub](https://github.com/rdwj/retrieval-hub) |
| **Action** | don't give me a copilot, do the work | [fips-agents](https://github.com/fips-agents) · [mcp-test-mcp](https://github.com/rdwj/mcp-test-mcp) |
| **Capacity** | economical AI compute I can actually operate | upstream [llm-d](https://github.com/llm-d/llm-d) and [vllm](https://github.com/vllm-project/vllm) · [workshop-setup](https://github.com/rdwj/workshop-setup) |
| **Economics** | is this worth what I'm paying for it | [platform-billing-operator](https://github.com/rdwj/platform-billing-operator) |

---

### Start here

[**ptc-gal-standards**](https://github.com/wjatx/ptc-gal-standards) Two specifications for agentic systems, published under the Community Specification License 1.0. *Provenance & Trust Context* (43 conformance clauses): a signed trust-context object that travels with data across every agent and tool boundary. *Grant & Autonomy Lifecycle* (35 clauses): authority as stored, signed state per principal and action class, raised only through a maker-checker ceremony and lowered automatically by deterministic triggers. Both are filed for Linux Foundation agent-standards discussion; I sit on the committee.

[**ptc-gal-reference**](https://github.com/wjatx/ptc-gal-reference)  The implementation that shows how PTC and GAL can work. A deterministic tool broker that an agent cannot talk past. Controls that live inside the agent harness are advice to the component under attack; anything a model can be talked out of is not a control.

[**memory-hub**](https://github.com/redhat-ai-americas/memory-hub) Persistent, governed agent memory with scoped access, version history and audit. Built on the premise that memory is a context-assembly *policy* problem rather than a retrieval problem, and that the design should work backwards from the forensic question: what did this agent know when it acted, who wrote it, and was anyone allowed to see it?

[**platform-billing-operator**](https://github.com/rdwj/platform-billing-operator) Metering and FinOps for platform services on OpenShift. Token metering is not AI FinOps; the real problem is giving autonomous systems economic authority and being able to say afterward what it cost.

---

### Where things live

This work is spread across three accounts, for boring historical reasons.

- [**@rdwj**](https://github.com/rdwj) — here. Platform components, MCP servers, developer tooling, most of the day-to-day.  
- [**@wjatx**](https://github.com/wjatx) — the standards work: the specifications, their reference implementation, and the [Trust Bricks](https://wjatx.github.io/trust-bricks/) diagrams.  
- [**@fips-agents**](https://github.com/fips-agents) — building agents that run where compliance is not optional: templates, a CLI, a gateway, and a code sandbox with AST guardrails, Landlock and seccomp isolation.

