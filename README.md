# Portfolio

Final-year Computer Engineering student at Tecnológico de Costa Rica (TEC) with a strong focus on software development and hands-on experience building backend systems, web applications, data-driven solutions, and containerized environments.

This portfolio highlights selected academic and personal projects in software engineering, backend development, distributed systems, data analysis, machine learning foundations, and modern deployment workflows.

---

## 🚀 Featured Projects

### LEGO Store Recommendation Chatbot
[Repository](https://github.com/Guti2010/lego-store) • **Python** • **FastAPI** • **React/Vite** • **SQLite** • **scikit-learn** • **Sentence Transformers** • **Docker**

Full-stack AI recommendation assistant for a LEGO store, designed to help users discover relevant sets through natural-language queries, curated visual recommendations, and catalog management tools.

**Highlights**
- Built a hybrid recommendation engine combining TF-IDF retrieval, dense semantic embeddings, structured filters, reranking, and result diversification
- Developed a FastAPI backend with a chatbot recommendation endpoint, SQLite catalog persistence, reindexing support, and admin CRUD APIs
- Created a React/Vite conversational interface with visual product cards, local chat history, branded styling, and product-level Messenger contact CTA
- Added an admin workflow to create, edit, activate, deactivate, and reindex products so catalog updates are reflected in the chatbot
- Containerized the full application with Docker Compose for reproducible local deployment and demo use
- 
---

### Transparency in Political Financing (Costa Rica)
[Repository](https://github.com/miguelc-14/Proyecto-PIDA) • **Python** • **scikit-learn** • **Streamlit** • **Altair/Plotly** • **ReportLab**

Machine learning dashboard for Costa Rican political donation data, designed to support transparency analysis through forecasting and anomaly detection.

**Highlights**
- Built a supervised forecasting workflow to estimate expected donation amounts by party and month
- Developed an anomaly detection view to surface unusual patterns in donation behavior
- Created an interactive Streamlit dashboard for exploration, ranking, and timeline analysis
- Added reproducibility support through versioned artifacts, structured exports, and automated report generation
  
---

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

### Administrative Management Platform
[Repository](https://github.com/LuisFernandoUC/Plataforma-de-Gesti-n-Administrativa) • **React** • **PostgreSQL** • **Docker**

Role-based web platform designed for the School of Industrial Production at TEC to centralize academic and administrative workflows in a single system.

**Highlights**
- Implemented role-based access for teachers, administrative staff, and coordination/director roles
- Developed modules for profiles, special activities, inventory, documents, schedules, academic load, and administration
- Organized the application around modular workflows and role-specific navigation
- Built for practical academic and administrative use cases in an educational environment
  
---

### Reverse Proxy with Redis Cache and Kubernetes
[Repository](https://github.com/Guti2010/Reverse-Proxy) • **C** • **Redis** • **Docker** • **Kubernetes** • **Helm**

Low-level HTTP reverse proxy built in C with host-based routing, API-key protection, and a shared Redis cache designed to support multiple replacement strategies.

**Highlights**
- Built socket-level HTTP handling and request routing based on the `Host` header
- Implemented Redis-backed caching with TTL control and replacement policies such as LRU, LFU, FIFO, MRU, and Random
- Used Docker for containerization and Kubernetes + Helm for deployment and configuration
- Added health checks and automated test coverage for validation of key behaviors

---

### Relational Data Analysis Sandbox
[Repository](https://github.com/Guti2010/Proyecto-II--DB) • **PostgreSQL** • **pgAdmin** • **Neo4j** • **Docker Compose**

Dockerized data sandbox for relational analysis and exploratory data workflows, combining PostgreSQL, pgAdmin, and optional Neo4j support.

**Highlights**
- Built a ready-to-run environment for SQL exploration and data analysis
- Included an EDA notebook, transactional data, and seeded aggregate tables
- Supported both relational querying and optional graph-based exploration with Cypher
- Used Docker Compose to simplify setup and reproducibility

---

### Kafka + Neo4j Demo
[Repository](https://github.com/Guti2010/Kafka) • **Python** • **Kafka** • **Neo4j** • **Docker Compose**

Event-driven demo that simulates an e-commerce social network using Kafka producers and Neo4j consumers to model user activity and relationships.

**Highlights**
- Simulated real-time events such as purchases, follows, reviews, and ratings
- Modeled graph relationships in Neo4j from streaming event data
- Included Docker Compose setup for Kafka, ZooKeeper, and Neo4j
- Added Cypher examples and notebooks for graph analysis and exploration

---

### News Feed Manager
[Repository](https://github.com/Guti2010/Caso-1-Estructuras) • **C++** • **libcurl** • **nlohmann/json** • **Docker**

C++ application that uses a doubly linked list to manage and explore news articles fetched from NewsAPI.

**Highlights**
- Implemented article storage and navigation with a doubly linked list
- Added keyword search, deletion, node repositioning, and top-5 views
- Integrated external data retrieval using libcurl and JSON parsing
- Included Docker-based build and execution support

---

### Smart Book Reader
[Repository](https://github.com/Guti2010/Caso-3---Estructuras) • **C++** • **B-Trees** • **Hash Tables** • **REST API** • **HTML/CSS/JS**

Search-oriented C++ application for exploring classic books through phrase and keyword lookup, supported by structured indexing and a lightweight web interface.

**Highlights**
- Implemented indexing with B-Trees and hash tables for efficient text search
- Added keyword extraction and REST-based query support
- Built a lightweight frontend for interactive exploration
- Included Dockerfile and Makefile for reproducible setup

---

### AI Game Hub (collaborative)
[Repository](https://github.com/Guti2010/AI-Game-Hub) · **Minimax + Alpha-Beta** · **A\*** · **Genetic Algorithm (GA)** · Heuristics · ML/RL foundations

Compact playground for game AI and search:
- **Dots & Boxes** — Minimax + alpha-beta with risk-aware & chain-control heuristics.  
- **Peg Solitaire** — **A\*** with an admissible heuristic and full solution trace.  
- **MountainCar-v0** — **GA** with a 2×3 chromosome mapping \[position, velocity\] → action; selection, elitism, crossover, mutation.  

Features: modular \(n×n\) boards, step-by-step search visualization, heuristic comparisons, and player profiles (Human vs AI, AI vs AI). Clean, extensible code with reproducible examples.

---

## Additional Projects

### AI Game Hub
[Repository](https://github.com/Guti2010/AI-Game-Hub) • **Minimax** • **Alpha-Beta Pruning** • **A\*** • **Genetic Algorithms**

Collection of game AI and search experiments focused on decision-making, heuristics, and optimization techniques.

**Highlights**
- Implemented Minimax with alpha-beta pruning for Dots & Boxes
- Applied A* search with heuristic design for Peg Solitaire
- Used a genetic algorithm to explore action strategies in MountainCar-v0
- Included modular boards, heuristic comparisons, and step-by-step visualization

---

### Paradigms & Languages
[Repository](https://github.com/Guti2010/Paradigmas) • **Scheme** • **Prolog** • **Bash**

Repository of projects exploring functional, logic, and scripting paradigms through small practical applications.

**Highlights**
- Built Roman numeral conversion and arithmetic tools in Scheme
- Developed Prolog projects for fractals, puzzle solving, and family-relation inference
- Created a Bash-based Wordle-style CLI game with Docker support

---

### Ensamblando un sándwich
[Repository](https://github.com/MoonFoxCake/Ensamblando-un-sandwich) • **Python** • **DSL** • **Transpiler**

Educational transpiler project that parses a small domain-specific language for sandwich assembly into executable steps.

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
- ✉️ alejandrogutierrezchaves@gmail.com
