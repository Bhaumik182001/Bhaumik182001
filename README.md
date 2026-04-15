# ⚡ Bhaumik | Software Development Engineer

Building enterprise-grade distributed systems and resilient microservices architectures.

## 💫 About Me
- 🎓 **B.Tech in Computer Science and Engineering** @ Lovely Professional University
- ☁️ Architecting fault-tolerant healthcare and banking ecosystems deployed on **GCP (GKE)** and **AWS**.
- 🧠 Deeply focused on **Java 21**, **Spring Boot**, **Kubernetes**, and distributed data consistency (Saga Pattern).
- 🔗 **Portfolio:** [Check out my live projects](https://portfolio-deploy-six-khaki.vercel.app/)
- 📫 **Reach me:** bhaumik182001@gmail.com

---

## 💻 Enterprise Tech Stack
[![My Skills](https://skillicons.dev/icons?i=java,spring,docker,kubernetes,gcp,aws,terraform,postgres,mongodb,redis,rabbitmq,ts,react,nextjs,nginx,git)](https://skillicons.dev)

---

## 🏗️ Featured Architecture

### 🏥 [MediSync: Enterprise Healthcare Microservices](https://github.com/Bhaumik182001/medisync-frontend.git)
A cloud-native microservices ecosystem decoupling complex healthcare domains across 4 independent Java 21 applications. 

```mermaid
graph TD
    %% Define Styles
    classDef cloud fill:#f2f6ff,stroke:#4285f4,stroke-width:2px,color:#333;
    classDef frontend fill:#000,stroke:#fff,stroke-width:2px,color:#fff;
    classDef service fill:#34a853,stroke:#fff,stroke-width:2px,color:#fff;
    classDef database fill:#fbbc05,stroke:#fff,stroke-width:2px,color:#000;
    classDef broker fill:#ea4335,stroke:#fff,stroke-width:2px,color:#fff;

    %% Client Layer
    User([🩺 Patient / Provider])

    %% Frontend Layer
    subgraph Vercel ["Vercel Edge Network"]
        UI["💻 React SPA (medisync-ui)<br/>Zustand, TanStack, Chaos UI"]:::frontend
    end

    %% Cloud Infrastructure Layer
    subgraph GCP ["Google Cloud Platform (GKE Cluster)"]
        Ingress["🌐 Global HTTP(S) Load Balancer<br/>(medisync-api.duckdns.org)"]:::cloud
        Gateway["🔀 API Gateway<br/>(Java 21 / Spring Cloud)"]:::service
        Discovery["🔍 Eureka Registry<br/>(Service Discovery)"]:::service
        Identity["🔐 Identity Service<br/>(JWT Auth)"]:::service
        Core["⚙️ Core Service<br/>(Schedule / Providers)"]:::service
    end

    %% Data & Messaging Layer
    subgraph Data ["External Managed Services"]
        Mongo[("MongoDB Atlas<br/>(User Credentials)")]:::database
        Neon[("Neon Postgres<br/>(Relational Schema)")]:::database
        Redis[("Redis<br/>(Caching Layer)")]:::database
        Rabbit[["RabbitMQ<br/>(Saga Orchestration)"]]:::broker
    end

    %% Traffic Flow
    User -->|HTTPS| UI
    UI -->|Axios w/ JWT| Ingress
    Ingress -->|Route| Gateway
    
    Gateway -->|Forward| Identity
    Gateway -->|Forward| Core

    %% Service Discovery Flow
    Gateway -.->|Register| Discovery
    Identity -.->|Register| Discovery
    Core -.->|Register| Discovery

    %% Database & Messaging Flow
    Identity ==>|Read/Write| Mongo
    Core ==>|JPA / Hibernate| Neon
    Core -.->|Cache| Redis
    
    Identity <==>|Async Events| Rabbit
    Core <==>|Async Events| Rabbit
```

* **Core Stack:** Java 21, Spring Boot 4.x, GCP (GKE), Terraform, PostgreSQL, MongoDB, RabbitMQ.
* **Engineering Impact:** Implemented the Saga Orchestration Pattern for distributed data consistency and built a dedicated Chaos Engineering dashboard for resilience testing.

### 🏦 [FinGuard: Enterprise Banking Platform](https://github.com/Bhaumik182001/finguard-sentinel-backend.git)
A highly secure, monolithic banking backend facilitating ACID-compliant financial transactions.
* **Core Stack:** Java 21, Spring Boot 3.x, AWS EC2, PostgreSQL, Nginx, GitHub Actions.
* **Engineering Impact:** Engineered strict pessimistic database locking mechanisms, JWT-based stateless authentication, and automated CI/CD pipelines utilizing ephemeral H2 databases.

---

## 🧠 Algorithms & Problem Solving

### 🧩 [Data Structures & Algorithms Repository](https://github.com/Bhaumik182001/Data-Structure-Algorithms.git)
A centralized, automated repository tracking my continuous algorithmic problem-solving progression across LeetCode and GeeksforGeeks.
* **Focus Areas:** Arrays, Dynamic Programming, Graphs, and Distributed System logic.
* **Consistency:** Secured the LeetCode 50-Days Badge (2025) and continuously expanding this repository as a personal technical wiki.

---

## 🏋️ Beyond the IDE
Engineering isn't just about code; it's about discipline and balance. When I am not architecting backend services, I am usually:
* **Exploring Digital Worlds:** Diving into notoriously unforgiving Dark Souls-style RPGs, open-world titles, and geeking out over hardware performance across PC and console.
* **Building Resilience:** Applying the same strict consistency required in tech to my structured heavy-lifting and bodybuilding routines.

---
## 🌐 Let's Connect
<table>
  <tr>
    <td align="center"><a href="https://www.linkedin.com/in/bhaumik182001/"><img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" width="40" height="40" alt="LinkedIn"/></a></td>
    <td align="center"><a href="https://portfolio-deploy-six-khaki.vercel.app/"><img src="https://cdn-icons-png.flaticon.com/512/1005/1005141.png" width="40" height="40" alt="Portfolio"/></a></td>
  </tr>
</table>

<br>

![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight)
