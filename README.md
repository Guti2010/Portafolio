# Portfolio

Final-year Computer Engineering student at Tecnológico de Costa Rica (TEC) with a strong focus on software development and hands-on experience building backend systems, web applications, data-driven solutions, and containerized environments.

This portfolio highlights selected academic and personal projects in software engineering, backend development, distributed systems, data analysis, machine learning foundations, and modern deployment workflows.

---

## 🚀 Featured Projects

### Transparency in Political Financing (Costa Rica)
[Repository](https://github.com/miguelc-14/Proyecto-PIDA) • **Python** • **scikit-learn** • **Streamlit** • **Altair/Plotly** • **ReportLab**

Machine learning dashboard for Costa Rican political donation data, designed to support transparency analysis through forecasting and anomaly detection.

**Highlights**
- Built a supervised forecasting workflow to estimate expected donation amounts by party and month
- Developed an anomaly detection view to surface unusual patterns in donation behavior
- Created an interactive Streamlit dashboard for exploration, ranking, and timeline analysis
- Added reproducibility support through versioned artifacts, structured exports, and automated report generation

### HTTP/1.0 Concurrent Web Server
[Repository](https://github.com/Guti2010/Proyecto-SO) • **Go** • **Concurrency** • **Docker**

Concurrent HTTP/1.0 server built to study how scheduling, queue depth, and workload type affect latency and throughput under different conditions.

**Highlights**
- Implemented a fixed worker pool with a bounded queue and backpressure
- Designed JSON-based endpoints for repeatable performance experiments
- Explored CPU-bound and I/O-bound workloads with latency metrics such as p50, p95, and p99
- Included Docker Compose setup and user documentation for reproducible testing

---

### Mini-Spark — Distributed Processing Engine
[Repository](https://github.com/Guti2010/Mini-Spark) • **Rust** • **Tokio** • **Docker**

MapReduce-inspired distributed processing engine built from scratch with master, workers, and client components for orchestrating and executing data-processing jobs.

**Highlights**
- Implemented distributed job orchestration with master-worker coordination
- Supported operations such as `map`, `filter`, `flat_map`, `reduce_by_key`, `join`, and `shuffle`
- Added asynchronous worker execution with configurable concurrency
- Included fault-tolerance features such as heartbeats and work reassignment

---

### 🗂️ Administrative Management Platform (TEC — EIPI)
[Repository](https://github.com/LuisFernandoUC/Plataforma-de-Gesti-n-Administrativa)

Web platform for the School of Industrial Production (TEC) that centralizes academic/administrative processes with **role-based access**:
- **Roles:** Teacher, Administrative Assistant, Coordination/Director (Coordinator, Assistant Director, Director).  
- **Modules:** Profile & CV (editable sections), Special Activities (hours/week), **Inventory** of peripherals (change/repair/retire with status tracking), **Documents** (memorandums, official letters, search/filter), **Forms**, **Schedules** and **Academic Load**, plus **Administration** (users/roles, periods, courses). :contentReference[oaicite:0]{index=0}
- **Navigation:** clean side menu per role with dedicated routes (e.g., `/panel-docente`, `/inventario/perifericos/solicitudes`, `/admin/roles`). :contentReference[oaicite:1]{index=1}  
- **Demo (test env):** `docente@itcr.ac.cr`, `asistente@itcr.ac.cr`, `coordinador@itcr.ac.cr`, `directivo@itcr.ac.cr`, `director@itcr.ac.cr` — password `demo123`. :contentReference[oaicite:2]{index=2}

---

### 🔁 Reverse Proxy — C + Redis Cache + Kubernetes
[Repository](https://github.com/Guti2010/Reverse-Proxy)

HTTP reverse proxy written in **C** that routes by **Host** header, enforces **API-Key** auth, and adds a shared **Redis** cache with multiple replacement policies (**LRU/LFU/FIFO/MRU/Random**). It’s containerized with **Docker**, deployed on **Kubernetes** via **Helm**, and includes an automated test battery and install guide. :contentReference[oaicite:0]{index=0}

- **Core features:** socket-level HTTP server, dynamic routing (Host → upstream), API-Key checks (env-configurable), cache key Host+path, TTL & replacement policy selection, and standard endpoints (e.g., `/_health`). :contentReference[oaicite:1]{index=1}  
- **Cache system:** proxy-first lookup → hit returns immediately; on miss → forward to backend, store in Redis, return to client; coherent across replicas. :contentReference[oaicite:2]{index=2}  
- **Docker:** multi-stage build, minimal runtime image; configuration only via environment variables. :contentReference[oaicite:3]{index=3}  
- **Kubernetes + Helm:** Deployments/Services for proxy, web, API, and Redis (via chart); proxy exposed as **NodePort**; backends/Redis as **ClusterIP**; readiness/liveness with `/_health`; values managed in `values.yaml`, **ConfigMaps** and **Secrets**. :contentReference[oaicite:4]{index=4}  
- **Tests:** PowerShell suite validates health, login redirect, session cookies, API protection (valid/invalid API-Key) under a default release/namespace. :contentReference[oaicite:5]{index=5}  
- **Install (excerpt):**  
  `docker build -t c-reverse-proxy:dev -f ./proxy/Dockerfile ./proxy` →  
  `helm upgrade --install proyecto ./proyecto -n rp --create-namespace -f ./proyecto/values.yaml`  
  (For **kind/minikube**: `kind load docker-image c-reverse-proxy:dev` / `minikube image load c-reverse-proxy:dev`.) :contentReference[oaicite:6]{index=6}

---

## 🗄️ Data & Streaming (Pair)

- **Proyecto II — DB**  
  [Repository](https://github.com/Guti2010/Proyecto-II--DB) — Dockerized data sandbox with **PostgreSQL** + **pgAdmin** (optional **Neo4j**). Includes an EDA notebook (`Analisis.ipynb`), a transactions CSV, a ready-to-run **Docker Compose** stack, and `init-postgres.sql` to seed aggregated tables (e.g., `Total_Spent_Per_Customer`, `Product_Purchase_Count`). Spin it up, run SQL, and optionally project the same domain into a property graph for exploratory **Cypher** analysis.

- **Kafka**  
  [Repository](https://github.com/Guti2010/Kafka) — **Kafka + Neo4j** demo in Python simulating an e-commerce social network. A **producer** emits purchases, follows, reviews, and ratings; a **consumer** writes nodes/relations to Neo4j (`USERS`, `PRODUCTS`, `TRANSACTIONS` with `PURCHASED`, `FOLLOWS`, `REVIEWED`, `RATED`). Includes Docker Compose (Kafka/ZooKeeper/Neo4j), Poetry setup, and ready-made Cypher examples/notebooks to analyze the graph. Run: `poetry run python main.py`.

> *Together, they connect relational/analytical workflows (SQL) with real-time, event-driven modeling (Kafka → Neo4j).*

---

## ⚙️ C++ Data Structures (Pair)

- **Caso 1 — Estructuras**  
  [Repository](https://github.com/Guti2010/Caso-1-Estructuras) — Doubly linked list managing news fetched from **NewsAPI**. Uses `nlohmann/json` (JSON) and `libcurl` (HTTP). Supports insert, keyword search, delete, re-positioning of nodes, **top-5** and show-all. Docker-based build/run notes and a simple CLI demo.

- **Caso 3 — SMART BOOK READER**  
  [Repository](https://github.com/Guti2010/Caso-3---Estructuras) — C++ app to search phrases/keywords across classic books. Uses **B-Trees** (and hash tables) for indexing, GPT-based keyword extraction, a **REST** API with `cpp-httplib`, and image generation via **DALL·E**. Includes a lightweight **HTML/CSS/JS** frontend, Dockerfile, Makefile; server runs on port 8080.

---

### AI Game Hub (collaborative)
[Repository](https://github.com/Guti2010/AI-Game-Hub) · **Minimax + Alpha-Beta** · **A\*** · **Genetic Algorithm (GA)** · Heuristics · ML/RL foundations

Compact playground for game AI and search:
- **Dots & Boxes** — Minimax + alpha-beta with risk-aware & chain-control heuristics.  
- **Peg Solitaire** — **A\*** with an admissible heuristic and full solution trace.  
- **MountainCar-v0** — **GA** with a 2×3 chromosome mapping \[position, velocity\] → action; selection, elitism, crossover, mutation.  

Features: modular \(n×n\) boards, step-by-step search visualization, heuristic comparisons, and player profiles (Human vs AI, AI vs AI). Clean, extensible code with reproducible examples.

---

## 📚 Paradigms & Languages

**Paradigms (Lisp/Scheme, Prolog, Bash)**  
[Repository](https://github.com/Guti2010/Paradigmas)

- **Functional (Scheme):** Roman numerals toolkit — convert Roman ↔ decimal and perform arithmetic (add, subtract, multiply, divide).  
- **Logic/Declarative (Prolog):**  
  - Fractals with Turtle graphics: snowflakes, carpets, bowties, honeycombs, stars; RGB/random variants with exported images.  
  - Logic puzzle solver: boards with burrows, rabbits, foxes, mushrooms; automatic solving with printable progress.  
  - Family relations (Latin facts/rules): births, marriages/divorces, ancestors/descendants; kinship inference (e.g., grandparents, cousins).  
- **Imperative/Scripting (Bash):** **WordShelle** — Wordle-style CLI for fruits/vegetables; Docker support.

---

## Other topics

- 🧩 **Ensamblando un sándwich**  
  [Repository](https://github.com/MoonFoxCake/Ensamblando-un-sandwich) — Educational **transpiler** in **Python**: a small DSL for “sandwich assembly” parsed into executable steps (grammar/rules, token parsing, code emission).

- 🖌️ **DIS_prototipo** *(collaborative)*  
  [Repository](https://github.com/fmasis25/DIS_prototipo) — Lightweight **web prototype** to manage **VIE-TEC project proposals** (create, review, track). Proof-of-concept; no dedicated README yet.

---

### 🧰 Tech Stack
<p>
  <!-- Languages -->
  <img src="https://img.shields.io/badge/C++-00599C?logo=c%2B%2B&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Java-007396?logo=java&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white&style=for-the-badge" />

  <!-- Data/ML -->
  <img alt="NumPy" src="https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white&style=for-the-badge" />
  <img alt="pandas" src="https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white&style=for-the-badge" />
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white&style=for-the-badge" />

  <!-- Web -->
  <img src="https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white&style=for-the-badge" />

  <!-- Frontend -->
  <img src="https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB&style=for-the-badge" />

  <!-- Backend/Runtime -->
  <img src="https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white&style=for-the-badge" />

  <!-- DevOps/Infra -->
  <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white&style=for-the-badge" />

  <!-- Databases -->
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?logo=microsoftsqlserver&logoColor=white&style=for-the-badge" />

  <!-- Tools -->
  <img src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?logo=postman&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Poetry-60A5FA?logo=poetry&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white&style=for-the-badge" />
</p>


---

## 🌐 Contact
- [LinkedIn](https://www.linkedin.com/in/alejandro-gutierrez-chaves-856451333)
- ✉️ alejandrogutierrez@gmail.com
