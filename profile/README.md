<div align="center">
<img src="img/graphdone-logo.svg" alt="GraphDone Logo" width="120" height="120">

# GraphDone
**Your Team's Todone List**

## 🚀 Public Repository & Documentation

[![Main Application](https://img.shields.io/badge/📦_Main%20Application-GraphDone--Core-blue?style=for-the-badge)](https://github.com/GraphDone/GraphDone-Core) [![Documentation](https://img.shields.io/badge/📖_Documentation-Setup%20%26%20Guides-green?style=for-the-badge)](https://github.com/GraphDone/GraphDone-Core/tree/main/docs)

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

## Enterprise Multi-Tenant Architecture

GraphDone's future architecture vision: distributed services with per-organization isolation across your infrastructure:

```mermaid
graph TB
    subgraph "Frontend Load Balancer"
        LB[🌐 Main Load Balancer<br/>Route by Organization<br/>nginx/haproxy]
    end
    
    subgraph "Organization A - Server Cluster 1-3"
        subgraph "Org A Services"
            WEB_A[🖥️ Web Server A<br/>orgA.graphdone.local<br/>Port 3127]
            API_A[🔧 GraphQL API A<br/>Port 4127]
            DB_A[(🗄️ Neo4j A<br/>Port 7687)]
            REDIS_A[⚡ Redis A<br/>Port 6379]
        end
    end
    
    subgraph "Organization B - Server Cluster 4-6"
        subgraph "Org B Services"
            WEB_B[🖥️ Web Server B<br/>orgB.graphdone.local<br/>Port 3127]
            API_B[🔧 GraphQL API B<br/>Port 4127]
            DB_B[(🗄️ Neo4j B<br/>Port 7687)]
            REDIS_B[⚡ Redis B<br/>Port 6379]
        end
    end
    
    subgraph "Organization C - Server Cluster 7-9"
        subgraph "Org C Services"
            WEB_C[🖥️ Web Server C<br/>orgC.graphdone.local<br/>Port 3127]
            API_C[🔧 GraphQL API C<br/>Port 4127]
            DB_C[(🗄️ Neo4j C<br/>Port 7687)]
            REDIS_C[⚡ Redis C<br/>Port 6379]
        end
    end
    
    subgraph "Shared Services - Server 10"
        MCP_SHARED[🤖 Shared MCP Server<br/>All Organizations<br/>Port 3128]
        MONITOR[📊 Central Monitoring<br/>Prometheus/Grafana]
        DNS[🔍 Internal DNS<br/>Service Discovery]
        BACKUP[💾 Backup Services<br/>Cross-org backups]
    end
    
    subgraph "Client Access"
        ORG_A_USERS[👥 Organization A Users]
        ORG_B_USERS[👥 Organization B Users]  
        ORG_C_USERS[👥 Organization C Users]
        AI_AGENTS[🤖 AI Agents]
    end
    
    ORG_A_USERS --> LB
    ORG_B_USERS --> LB
    ORG_C_USERS --> LB
    AI_AGENTS --> LB
    
    LB -->|orgA.graphdone.local| WEB_A
    LB -->|orgB.graphdone.local| WEB_B
    LB -->|orgC.graphdone.local| WEB_C
    
    WEB_A --> API_A
    WEB_B --> API_B
    WEB_C --> API_C
    
    API_A --> DB_A
    API_B --> DB_B
    API_C --> DB_C
    
    API_A --> REDIS_A
    API_B --> REDIS_B
    API_C --> REDIS_C
    
    AI_AGENTS --> MCP_SHARED
    MCP_SHARED --> DB_A
    MCP_SHARED --> DB_B
    MCP_SHARED --> DB_C
    
    MONITOR --> API_A
    MONITOR --> API_B
    MONITOR --> API_C
    MONITOR --> DB_A
    MONITOR --> DB_B
    MONITOR --> DB_C
    
    BACKUP --> DB_A
    BACKUP --> DB_B
    BACKUP --> DB_C
    
    DNS --> API_A
    DNS --> API_B
    DNS --> API_C
    
    style LB fill:#ff6b6b,stroke:#fff,stroke-width:2px,color:#fff
    style WEB_A fill:#4ecdc4,stroke:#fff,stroke-width:2px,color:#fff
    style WEB_B fill:#4ecdc4,stroke:#fff,stroke-width:2px,color:#fff
    style WEB_C fill:#4ecdc4,stroke:#fff,stroke-width:2px,color:#fff
    style API_A fill:#45b7d1,stroke:#fff,stroke-width:2px,color:#fff
    style API_B fill:#45b7d1,stroke:#fff,stroke-width:2px,color:#fff
    style API_C fill:#45b7d1,stroke:#fff,stroke-width:2px,color:#fff
    style DB_A fill:#f9ca24,stroke:#fff,stroke-width:2px,color:#fff
    style DB_B fill:#f9ca24,stroke:#fff,stroke-width:2px,color:#fff
    style DB_C fill:#f9ca24,stroke:#fff,stroke-width:2px,color:#fff
    style REDIS_A fill:#eb4d4b,stroke:#fff,stroke-width:2px,color:#fff
    style REDIS_B fill:#eb4d4b,stroke:#fff,stroke-width:2px,color:#fff
    style REDIS_C fill:#eb4d4b,stroke:#fff,stroke-width:2px,color:#fff
    style MCP_SHARED fill:#6c5ce7,stroke:#fff,stroke-width:2px,color:#fff
```

**Enterprise Multi-Tenant Benefits:**
- **🏢 Organizational Isolation** - Complete data separation between teams/companies
- **🔒 Enhanced Security** - Each org has dedicated infrastructure and database
- **📊 Resource Control** - Allocate specific server resources per organization
- **🌐 Flexible Routing** - Route by subdomain (orgA.graphdone.local)
- **🔧 Custom Configuration** - Per-org settings, themes, and integrations
- **💾 Centralized Management** - Shared monitoring, backups, and DNS services
- **🤖 AI Agent Access** - Shared MCP server can access all orgs (with permissions)

**Current Status:** *This is a future architecture vision - GraphDone-Core currently runs as single-server application*

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
