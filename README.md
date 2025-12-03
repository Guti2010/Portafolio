# Portafolio
Personal portfolio showcasing academic and personal projects in software development, data engineering, AI, and cybersecurity. Built with Python, Docker, and modern web technologies.


## 🚀 Proyectos | Projects

# Transparency in Political Financing (CR) — ML/AI Focus

[Repository](https://github.com/miguelc-14/Proyecto-PIDA) • **Python** • **scikit-learn** • **Streamlit** • **Altair/Plotly** • **ReportLab**

This project is a reproducible ML dashboard for analyzing political-donation data in Costa Rica. It combines a supervised forecasting model (Model A) with an anomaly-surfacing view (Model B), wrapped in an accessible Streamlit UI.

- ## ML highlights

  - **Model A — Expected Amount Forecasting (per party × month)**
    - **Task:** supervised regression to estimate the expected donation amount ŷ.
    - **Signals / features:** election participation flags (presidential/municipal), election-cycle position (`m_ciclo_rem`, `m_ciclo_pos`), recent history (t−1, t−3, t−6) with a user-controlled **history multiplier**, donor structure (unique donors, # donations, **HHI**), composition shares (legal entities / in-kind).
    - **Training protocol:** time-based hold-out (`split_test_start` in the meta JSON), **median imputation from train only**, and a feature list/version pinned in `modelo1_rf_Amae_meta.json`.
    - **Model:** `scikit-learn` **RandomForestRegressor** (artifact: `models/modelo1_rf_Amae.joblib`).
    - **Diagnostics in UI:** predicted ŷ, observed y (optional), residual and a **severity** score `rz = residual / (|ŷ| + 1)` categorized as NORMAL, MODERATE+, HIGH+, HIGH−.
    - **Scenario engine:** users can override lags or adjust “activity”/“contribution structure” to stress-test ŷ without touching the model weights.

  - **Model B — Unusual Behavior Surfacing**
    - **Input:** precomputed `anomalias.csv` with `anomaly_score` and `anomaly_flag` produced by an external offline pipeline.
    - **UI:** sortable ranking, timeline with outlier markers, and a proportion view to contextualize the weight of flagged months. (The app treats scores/flags as model outputs and focuses on explainable presentation.)
  
- ## Data & reproducibility
  
  - **Schema inference:** robust column guessing for `año_mes`, `partido`, `tipo_contribucion`, `tipo_persona`, `donante`, `monto_real`.
  - **XLSX → CSV converter:** automatic, with header detection and caching.
  - **Artifacts under version control:** `.joblib` model + `.json` meta (features, target, split), ensuring repeatable predictions.
  - **Exports:** filtered CSVs, metrics CSV, and a **print-ready A4 PDF** (same charts, built via Altair→PNG + ReportLab).

- ## Stack
    Streamlit (UI) · scikit-learn (ML) · pandas · Altair/Plotly (viz) · vl-convert (vector→PNG) · ReportLab (PDF).


# AI Game Hub (collaborative)  
[Repository](https://github.com/Guti2010/AI-Game-Hub) · **Minimax + Alpha-Beta** · **A\*** · **Genetic Algorithm (GA)** · Heuristics · ML/RL foundations

AI Game Hub is a compact playground for game AI and search. It includes:
- **Dots & Boxes** with Minimax + alpha-beta pruning (risk-aware and chain-control heuristics).
- **Peg Solitaire** with **A\*** and an admissible heuristic, outputting the full solution path.
- **MountainCar-v0** with **GA**: a 2×3 chromosome mapping \[position, velocity\] → action; fitness by total return, with selection, elitism, crossover, and mutation.

Features: modular \(n×n\) boards, step-by-step search visualization, heuristic comparisons, and player profiles (Human vs AI, AI vs AI). Clean, extensible code with reproducible examples and docs to add new games or strategies.


---

### 📚 Paradigms & Languages

**Paradigms (Lisp/Scheme, Prolog, Bash)**  
[Repository](https://github.com/Guti2010/Paradigmas)

- **Functional (Scheme):** Roman numerals toolkit — convert Roman ↔ decimal and perform arithmetic (add, subtract, multiply, divide)
- **Logic/Declarative (Prolog):**
  - **Fractals with Turtle graphics:** snowflakes, carpets, bowties, honeycombs, stars; includes RGB and random variants with exported images.
  - **Logic puzzle solver:** boards with burrows, rabbits, foxes, and mushrooms; automatic solving with printable progress.
  - **Family relations (Latin facts/rules):** births, marriages/divorces, ancestors/descendants; infers kinship (e.g., grandparents, cousins).
- **Imperative/Scripting (Bash):** **WordShelle** — a Wordle-style CLI game for fruits/vegetables, with a word list and Docker support.

---

### 🗄️ Data & Streaming (Pair)

- **Proyecto II — DB**  
  [Repository](https://github.com/Guti2010/Proyecto-II--DB) — Dockerized data sandbox with **PostgreSQL** + **pgAdmin** (optional **Neo4j**). Includes an EDA notebook (`Analisis.ipynb`), a transactions CSV, a ready-to-run **Docker Compose** stack, and `init-postgres.sql` to seed aggregated tables (e.g., `Total_Spent_Per_Customer`, `Product_Purchase_Count`). Spin it up in minutes, run SQL queries, and optionally project the same domain into a property graph for exploratory **Cypher** analysis.


- **Kafka**  
  [Repository](https://github.com/Guti2010/Kafka) — **Kafka + Neo4j** integration in Python that simulates an e-commerce social network. A **producer** emits purchases, follows, reviews, and ratings; a **consumer** writes nodes/relations to Neo4j (`USERS`, `PRODUCTS`, `TRANSACTIONS` with `PURCHASED`, `FOLLOWS`, `REVIEWED`, `RATED`). Comes with **Docker Compose** for Kafka/ZooKeeper/Neo4j, **Poetry** setup, and ready-made **Cypher** examples (`consultasCypher.txt`, `.ipynb`) to analyze the graph. Run `poetry run python main.py` to create topics, generate events, and populate the graph. :contentReference[oaicite:1]{index=1}

> *Together, they connect relational/analytical workflows (Spark + SQL) with real-time, event-driven modeling (Kafka → Neo4j).*


---

### ⚙️ C++ Data Structures (Pair)

- **Caso 1 — Estructuras**  
  [Repository](https://github.com/Guti2010/Caso-1-Estructuras) — Doubly linked list that manages news fetched from **NewsAPI**, using `nlohmann/json` for easy JSON handling. Supports insert, search (by keywords), delete, re-positioning of nodes, “show all” and **top-5** displays. Includes Docker-based build/run notes (with `libcurl`) and a simple CLI to demo the operations.

- **Caso 3 — SMART BOOK READER**  
  [Repository](https://github.com/Guti2010/Caso-3---Estructuras) — Full C++ app to search phrases/keywords across classic books. Uses **B-Trees** (and hash tables) for fast indexing/lookups, extracts keywords via GPT (NLP preprocessing), serves a **REST-style HTTP API** with `cpp-httplib`, and generates related images via **DALL·E**. Comes with a lightweight **HTML/CSS/JS** frontend, Dockerfile, Makefile, and examples to compile and run the server on port 8080.


---

## Other topics

- 🧩 **Ensamblando un sándwich**  
  [Repository](https://github.com/MoonFoxCake/Ensamblando-un-sandwich) — Educational, collaborative **transpiler** in **Python** that translates a small domain-specific language (DSL) about “sandwich assembly” into executable steps. Shows how to design grammar/rules, parse tokens, and emit target code for a simple runtime.

- 🖌️ **DIS_prototipo** *(collaborative)*  
  [Repository](https://github.com/fmasis25/DIS_prototipo) — Lightweight **web prototype** to manage **VIE-TEC project proposals** (create, review, and track submissions). Currently used as a proof-of-concept; the repo has no dedicated README yet.


---

### 🧰 Tech Stack

<p>
  <!-- Lenguajes -->
  <img src="https://img.shields.io/badge/C++-00599C?logo=c%2B%2B&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Java-007396?logo=java&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge" />
  <img alt="NumPy" src="https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white&style=for-the-badge" />
  <img alt="pandas" src="https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white&style=for-the-badge" />
  <img alt="scikit-learn" src="https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white&style=for-the-badge" />
  <!-- Web -->
  <img src="https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white&style=for-the-badge" />
  <!-- Frontend -->
  <img src="https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB&style=for-the-badge" />
  <!-- Backend / Runtime -->
  <img src="https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white&style=for-the-badge" />
  <!-- DevOps / Infra -->
  <img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Nginx-009639?logo=nginx&logoColor=white&style=for-the-badge" />
  <!-- Bases de datos -->
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

