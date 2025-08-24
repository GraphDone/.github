# GraphDone
**Your Team's Todone List**

> Connecting people of all thinking styles through a shared workspace where humans and intelligent machines collaborate naturally from day one. Open source project management that celebrates cognitive diversity and treats automation as a team member, not an afterthought.

## Overview

```mermaid
graph TB
    A[Shared Data Foundation] --> B[Human Contributors]
    A --> C[Intelligent Machines]
    A --> D[Project Goals]
    
    B --> E[Visual Thinkers<br/>Graph Views]
    B --> F[Linear Thinkers<br/>List Views]
    B --> G[Detail Focused<br/>Deep Dive Modes]
    B --> H[Big Picture<br/>Overview Modes]
    
    C --> I[Pattern Recognition]
    C --> J[Data Processing]
    C --> K[Task Automation]
    
    E --> L[Collaborative Output]
    F --> L
    G --> L
    H --> L
    I --> L
    J --> L
    K --> L
    
    L --> D
    
    style A fill:#4f46e5,stroke:#fff,stroke-width:2px,color:#fff
    style L fill:#10b981,stroke:#fff,stroke-width:2px,color:#fff
    style D fill:#f59e0b,stroke:#fff,stroke-width:2px,color:#fff
```

## Our Philosophy

High-performing teams are full of brilliant minds that work differently—both human and machine. Some think in patterns and connections, others need to hyperfocus on details. Some thrive on rapid task-switching, others prefer deep, uninterrupted work. Some process information visually, others through movement or sound. Traditional tools force everyone into the same box, and treat automation as an awkward add-on. 

GraphDone provides a shared foundation where every type of mind—biological or digital—can contribute in their most natural way toward goals that benefit everyone.

## Key Features

### 🧠 **Multiple Thinking Modes**
Visual graphs, linear lists, detail views, big picture overviews - access your data the way your mind works best.

### 🔗 **Non-Linear Workflows** 
Jump between tasks naturally. Perfect for minds that think in connections rather than sequential steps.

### 👥 **Strengths-Based Teams**
Different minds see different solutions. Our tools help diverse thinkers collaborate without masking their natural styles.

### ⚡ **Hyperfocus Friendly**
Deep-dive modes for intense focus sessions, plus gentle transitions to help you surface when ready.

### 🛡️ **Sensory Considerations**
Customizable interfaces, reduced cognitive load, and calm design that doesn't overwhelm sensitive processing styles.

### 🌐 **Pattern Recognition**
Visualize complex relationships and dependencies in ways that make sense to pattern-oriented minds.

## How It Works

1. **Shared Data, Personal Views** - Everyone works with the same information, but sees and interacts with it in their preferred style - graphs, lists, calendars, or kanban boards.

2. **Natural Connections** - Link tasks through real dependencies and relationships, not artificial hierarchies that don't match how minds actually work.

3. **Adaptive Interfaces** - Customize sensory inputs, interaction patterns, and information density to match your processing preferences.

4. **Celebrate Differences** - Different thinking styles become team strengths rather than obstacles to overcome.

## Meet the Founders

<div align="center">

### Matthew Valancy
**Co-Founder**

<img src="img/matthew-photo.jpg" alt="Matthew Valancy" width="120" height="120" style="border-radius: 50%; border: 3px solid #10b981;">

*From Silicon Valley, California, Matthew has worked with engineering teams across every startup phase—from garage startups to IPO. He's observed that the most talented engineers are often self-directed individuals who thrive with autonomy, yet most management approaches are designed for workers who need constant oversight. GraphDone emerged from his belief that passionate, independent contributors deserve tools that amplify their strengths rather than constrain them.*

---

### Lakshman Patel
**Co-Founder** 

<img src="img/lakshman-photo.jpg" alt="Lakshman Patel" width="120" height="120" style="border-radius: 50%; border: 3px solid #3b82f6;">

*From a farming family in India that taught him hard work and seizing opportunities can transform lives, Lakshman brings that relentless drive to building technology. He champions rapidly adopting cutting-edge tools and methodologies to accelerate learning, continuously iterate on solutions, and deliver exceptional end-to-end experiences that exceed expectations.*

</div>

## Open Source Philosophy

GraphDone's core services and applications are open source, reflecting our commitment to transparent, community-driven development for human collaboration tools. We believe the best tools for human-machine collaboration should be accessible to everyone.

## Getting Started

GraphDone is currently in development. To stay updated:

- ⭐ **Star this repository** to get notified of releases
- 📧 **Join our community** for early access updates

## Tech Stack

- **Frontend**: React, TypeScript, D3.js for graph visualization
- **Backend**: Node.js, GraphQL, Neo4j
- **Infrastructure**: Docker, Kubernetes
- **Testing**: Playwright, Vitest

## Project Structure

### Open Source Core
**GraphDone-Core** - Main application and services
- `packages/core/` - Graph engine and algorithms  
- `packages/web/` - React web application
- `packages/server/` - GraphQL API server
- `packages/agent-sdk/` - SDK for AI agent integration

### Additional Projects
- **GraphDone-iOS** (private) - Native iOS application
- **GraphDone-Android** (private) - Native Android application

## Contributing

We welcome contributions from developers who share our vision of cognitive-inclusive technology. More contribution guidelines coming soon.

## License

Open source license details coming soon.

---

**GraphDone** - For teams who think differently.

*Built by Matthew Valancy & Lakshman Patel*