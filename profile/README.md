<div align="center">
<img src="img/graphdone-logo.svg" alt="GraphDone Logo" width="120" height="120">

# GraphDone
**Your Team's Todone List**

## 🚀 Public Repository & Documentation

[![GraphDone-Core](https://img.shields.io/badge/📦_GraphDone--Core-Main%20Application-blue?style=for-the-badge)](https://github.com/GraphDone/GraphDone-Core) [![Core Docs](https://img.shields.io/badge/📖_Documentation-Comprehensive%20Guides-green?style=for-the-badge)](https://github.com/GraphDone/GraphDone-Core/tree/main/docs/guides)

</div>

> Connecting people of all thinking styles through a shared workspace where humans and intelligent machines collaborate naturally from day one. Open source project management that celebrates cognitive diversity and treats automation as a team member, not an afterthought.

## GraphDone Ecosystem

```mermaid
graph TB
    subgraph "GraphDone Ecosystem"
        subgraph "Public Repository"
            CORE[📦 GraphDone-Core<br/>🌐 Web Application<br/>🔧 GraphQL API<br/>🗄️ Neo4j Database<br/>🤖 AI Agent SDK]
        end
        
        subgraph "Mobile Applications"
            IOS[📱 GraphDone-iOS<br/>Native SwiftUI App<br/>Touch-optimized Interface]
            ANDROID[📱 GraphDone-Android<br/>Native Kotlin App<br/>Mobile-first Design]
        end
        
        subgraph "Shared Foundation"
            API[GraphQL API<br/>Port 4127]
            DB[(Neo4j Database<br/>Graph Storage)]
            REALTIME[WebSocket<br/>Real-time Sync]
        end
    end
    
    CORE --> API
    API --> DB
    API --> REALTIME
    
    IOS --> API
    ANDROID --> API
    
    REALTIME --> IOS
    REALTIME --> ANDROID
    REALTIME --> CORE
    
    style CORE fill:#3b82f6,stroke:#fff,stroke-width:2px,color:#fff
    style IOS fill:#8b5cf6,stroke:#fff,stroke-width:2px,color:#fff
    style ANDROID fill:#10b981,stroke:#fff,stroke-width:2px,color:#fff
    style API fill:#f59e0b,stroke:#fff,stroke-width:2px,color:#fff
    style DB fill:#ef4444,stroke:#fff,stroke-width:2px,color:#fff
    style REALTIME fill:#06b6d4,stroke:#fff,stroke-width:2px,color:#fff
```

## Philosophy

GraphDone celebrates cognitive diversity by providing tools where different minds—human and AI—can collaborate naturally. Traditional project management forces everyone into the same workflow. We believe the best results come from teams where diverse thinking styles become strengths, not obstacles.

## Key Features

🧠 **Multiple Views** - Graph, list, calendar, or kanban - work how your mind works best  
🔗 **Natural Dependencies** - Connect tasks through real relationships, not artificial hierarchies  
⚡ **Focus-Friendly** - Deep-dive modes with gentle transitions for different attention styles  
🤖 **Human-AI Collaboration** - AI agents as team members, not afterthoughts

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

## Get Started

**[⭐ GraphDone-Core](https://github.com/GraphDone/GraphDone-Core)** - Open source web application and GraphQL API  
**[📖 Documentation](https://github.com/GraphDone/GraphDone-Core/tree/main/docs)** - Complete technical documentation and guides

**Tech Stack:** React, TypeScript, Node.js, GraphQL, Neo4j, Docker  
**License:** MIT - Open source and community-driven

---

**GraphDone** - For teams who think differently.

*Started by Matthew Valancy & Lakshman Patel*
