# Portafolio
Personal portfolio showcasing academic and personal projects in software development, data engineering, AI, and cybersecurity. Built with Python, Docker, and modern web technologies.

---

## 🚀 Projects

### Transparency in Political Financing (CR) — ML/AI Focus
[Repository](https://github.com/miguelc-14/Proyecto-PIDA) • **Python** • **scikit-learn** • **Streamlit** • **Altair/Plotly** • **ReportLab**

Reproducible ML dashboard for Costa Rican political-donation data. Combines a supervised forecasting model (Model A) with an anomaly-surfacing view (Model B), wrapped in a Streamlit UI.

- **Model A — Expected Amount Forecasting (party × month)**  
  Task: supervised regression for ŷ. Features include election flags (presidential/municipal), cycle position (`m_ciclo_rem`, `m_ciclo_pos`), recent history (t−1, t−3, t−6) with a **history multiplier**, donor structure (unique donors, # donations, **HHI**), and composition shares.  
  Protocol: time-based hold-out (`split_test_start`), **train-only median imputation**, feature list/version pinned in `modelo1_rf_Amae_meta.json`.  
  Model: `RandomForestRegressor` (`models/modelo1_rf_Amae.joblib`).  
  UI diagnostics: ŷ, observed y (opt), residuals and **severity** score `rz = residual/(|ŷ|+1)` categorized as NORMAL / MODERATE+ / HIGH+ / HIGH−.  
  Scenario engine: override lags or adjust “activity/contribution structure” to stress-test ŷ (no retraining).

- **Model B — Unusual Behavior Surfacing**  
  Input: `anomalias.csv` with `anomaly_score`/`anomaly_flag` from an offline pipeline.  
  UI: sortable ranking, timeline with outlier markers, and a proportional context view.

- **Data & reproducibility**  
  Schema inference for common columns; XLSX→CSV converter with caching; artifacts under VC (`.joblib` + meta `.json`); exports (filtered CSVs, metrics CSV, and **A4 PDF** built via Altair→PNG + ReportLab).

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
