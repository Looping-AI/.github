## Looping AI

Looping AI builds agent-native systems centered around the enterprise level trust-layer of Slack, with Cloudflare-hosted components for routing, orchestration, and agent execution.

We create practical AI teammates that live in Slack. We combine a central coordination layer (gateway) with specialized remote agents so requests are handled by the right capability at the right time, making automation feel conversational, fast, and reliable for real teams.

### Core Repository (Most Important)

#### [`Looping-AI/looping-gateway`](https://github.com/Looping-AI/looping-gateway)
**Gateway Template: Cloudflare hosted, Slack-anchored multi-agent gateway with A2A routing.**

This is the central entrypoint of the Looping AI ecosystem. At a high level, `looping-gateway` is responsible for:

- Acting as the **Slack-facing gateway** for incoming events and interactions.
- Providing a **multi-agent coordination layer**, where requests can be directed to the most appropriate agent.
- Handling **A2A (agent-to-agent) routing**, enabling agents to delegate or chain tasks across specialized services.
- Running in a **Cloudflare-hosted architecture**, optimized for low-latency edge execution and scalable event handling.
- Serving as the **integration hub** that connects Slack workflows to reactive/proactive agent behavior.

In short: if someone wants to understand how the Looping AI platform is wired together in production, this is the first repo to read or deploy.

### Other Important Repositories

- [`Looping-AI/proactive-agent`](https://github.com/Looping-AI/proactive-agent)  
  Agent service focused on **proactive behaviors** and usually invoked on every channel message (strong reasoning/coordination, initiating actions, scheduled/triggered outreach).

- [`Looping-AI/reactive-agent`](https://github.com/Looping-AI/reactive-agent)  
  Agent service focused on **reactive behaviors** and only invoked by name mention (responding to user inputs/events in real time, carrying powerful workflows with subtasks and recipes).

- [`Looping-AI/looping-ai-slack-app`](https://github.com/Looping-AI/looping-ai-slack-app)  
  The Slack app manifest that sets required capabilities covering the setup of Looping AI Slack App

---

### Suggested Reading Order

1. [`looping-gateway`](https://github.com/Looping-AI/looping-gateway) (core architecture and routing)
2. [`looping-ai-slack-app`](https://github.com/Looping-AI/looping-ai-slack-app) (Slack manifest)
3. [`reactive-agent`](https://github.com/Looping-AI/reactive-agent) (event-driven response behavior)
4. [`proactive-agent`](https://github.com/Looping-AI/proactive-agent) (proactive automation behavior)
