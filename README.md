# 🖥️ Monitoring Architecture with Docker  
Complete system & application monitoring stack using Docker, Prometheus, Grafana, cAdvisor and Node Exporter.  
Designed following DevOps best practices for observability, containerization and metrics collection.

---

## 🚀 Project Overview

This project provides a ready-to-use monitoring architecture that supervises:

- **System metrics** (CPU, RAM, Disk, Network)
- **Docker container metrics**
- **Application performance**
- **Custom metrics via Prometheus**

It uses a full open-source stack and can be deployed on any machine running Docker.

---

## 🏗️ Architecture

### **ASCII Architecture Diagram**

              ┌───────────────────┐
              │     Host OS       │
              │ (System Metrics)  │
              └─────────┬─────────┘
                        │
                ┌───────▼────────┐
                │ Node Exporter   │
                │ (System Stats)  │
                └───────┬────────┘
                        │
        ┌───────────────▼────────────────┐
        │          Prometheus             │
        │  - Scrapes exporters            │
        │  - Stores time-series metrics   │
        └───────────┬────────────────────┘
                    │
            ┌───────▼────────┐
            │    Grafana     │
            │  Dashboards     │
            └────────────────┘

        ┌────────────────────────────────┐
        │            Docker              │
        │   ┌────────────────────────┐   │
        │   │       cAdvisor        │   │
        │   │  (Container Metrics)  │   │
        │   └────────────────────────┘   │
        └────────────────────────────────┘


---

## 🧰 Tech Stack

| Tool | Usage |
|------|--------|
| **Docker / Docker Compose** | Containerization & orchestration |
| **Prometheus** | Metrics scraping & storage |
| **Grafana** | Dashboard visualization |
| **cAdvisor** | Container-level monitoring |
| **Node Exporter** | Host machine metrics |

---

## 📦 Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Takwazayene/devops-monitoring.git
cd devops-monitoring
```
---

### 1️⃣ Start the monitoring stack
```bash
docker-compose up -d
```
---

## Access the services


| Service       | URL                                                            |
| ------------- | -------------------------------------------------------------- |
| Grafana       | [http://localhost:3000](http://localhost:3000)                 |
| Prometheus    | [http://localhost:9090](http://localhost:9090)                 |
| cAdvisor      | [http://localhost:8080](http://localhost:8080)                 |
| Node Exporter | [http://localhost:9100/metrics](http://localhost:9100/metrics) |






