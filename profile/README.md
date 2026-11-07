<picture>
  <source media="(prefers-color-scheme: dark)" srcset="img/hero/graphdone-dark.svg">
  <img src="img/hero/graphdone-light.svg" width="100%" alt="GraphDone: one graph of work for people and AI agents. The open-source core (web app, GraphQL API, MCP server), the hosted app at graphdone.com, AI agents and people connect round shared outcomes.">
</picture>

GraphDone is one graph of work that people and AI agents share. Work items, the people and agents who own them, and the dependencies between them all live in one graph, and the work converges on outcomes instead of flowing down a hierarchy. Agents are peers in that graph: they read and change it through an MCP server and an agent API, just as people do through the web app.

## How it fits together

- **GraphDone-Core** is open source (MIT): a React web app, a GraphQL API and an MCP server for AI agents. You can self-host it.
- **graphdone.com** is the hosted app, built on Core. It runs on Cloudflare: Pages for the web app, Workers for the API, and D1 (SQLite) for the graph. A private hosted layer adds hardened sign-in, enrollment, sharing and usage limits.
- **People and AI agents** work in the same graph, through the web app, the MCP server and the agent API.
- Deployment and test automation and the landing site are maintained privately.

```mermaid
flowchart LR
    P[People] --> W[Web app]
    A[AI agents] --> M[MCP server]
    A --> AA[Agent API]
    subgraph C [GraphDone-Core - open source, MIT]
        W --> G[GraphQL API]
        M --> G
        AA --> G
    end
    C -.-> S[Self-hosted by you]
    C -.-> H[graphdone.com on Cloudflare]
```

## Meet the Founders

<div align="center">

### Matthew Valancy
**Co-Founder, Engineer**

<p align="center">
  <img src="img/matthew-photo.png" alt="Matthew Valancy" width="150" height="150">
</p>

*From Silicon Valley, California, Matthew has worked with engineering teams across every startup phase—from garage startups to IPO. He's observed that the most talented engineers are often self-directed individuals who thrive with autonomy, yet most management approaches are designed for workers who need constant oversight. GraphDone emerged from his belief that passionate, independent contributors deserve tools that amplify their strengths rather than constrain them.*

---

### Lakshman Patel
**Co-Founder, Engineer** 

<p align="center">
  <img src="img/lakshman-photo.png" alt="Lakshman Patel" width="150" height="150">
</p>

*From a farming family in India that taught him hard work and seizing opportunities can transform lives, Lakshman brings that relentless drive to building technology. He champions rapidly adopting cutting-edge tools and methodologies to accelerate learning, continuously iterate on solutions, and deliver exceptional end-to-end experiences that exceed expectations.*

</div>

## Get started

- **[graphdone.com](https://graphdone.com)**: the hosted app.
- **[GraphDone-Core](https://github.com/GraphDone/GraphDone-Core)**: the open-source web app, GraphQL API and MCP server, with a [quick start](https://github.com/GraphDone/GraphDone-Core#quick-start) for running it yourself.
- **[Documentation](https://github.com/GraphDone/GraphDone-Core/tree/main/docs)**: guides and technical reference.

**Tech stack:** TypeScript, React, Node.js, GraphQL and MCP. graphdone.com runs on Cloudflare Pages, Workers and D1 (SQLite). Self-hosted Core runs with Docker; its graph store is Neo4j today, and [GraphDone-Core#244](https://github.com/GraphDone/GraphDone-Core/issues/244) plans SQLite as the default.

**License:** MIT, for GraphDone-Core.

---

*Started by Matthew Valancy & Lakshman Patel*
