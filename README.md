<h1 align="center">Ganpati Kumar Sah</h1>

<p align="center">
  <b>AI/ML Engineer</b> &nbsp;·&nbsp; LLM Applications &nbsp;·&nbsp; RAG &nbsp;·&nbsp; Agent Systems
</p>

<p align="center">
  <i>Building retrieval and agent systems that are grounded, access-controlled, and cost-aware.</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Bengaluru-India-0d1117?style=flat-square&logo=googlemaps&logoColor=white" alt="Location" />
  <a href="mailto:ganpatikrsah1405@gmail.com"><img src="https://img.shields.io/badge/Email-ganpatikrsah1405%40gmail.com-0d1117?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
  <!-- Add LinkedIn here:
  <a href="https://www.linkedin.com/in/YOUR-HANDLE"><img src="https://img.shields.io/badge/LinkedIn-Connect-0d1117?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  -->
</p>

---

## About

I build LLM-powered systems end to end: ingestion, retrieval, generation, validation, and the service boundaries between them. I care most about what makes AI systems trustworthy: verifiable answers, isolated tenant data, bounded token spend, and predictable agents.

B.E. in Computer Science & Engineering (AI & ML), AMC Engineering College, Bengaluru. **Open to** AI/ML engineering roles focused on LLM applications, RAG, and agent systems.

---

## Featured Work

<p align="center">
  <a href="https://github.com/Spark-of-Sun/MLQA-RAG">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/pin/?username=Spark-of-Sun&repo=MLQA-RAG&theme=github_dark&hide_border=true">
      <img width="49%" alt="MLQA-RAG" src="https://github-readme-stats.vercel.app/api/pin/?username=Spark-of-Sun&repo=MLQA-RAG&theme=default&hide_border=true" />
    </picture>
  </a>
  <a href="https://github.com/Spark-of-Sun/CPAA">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/pin/?username=Spark-of-Sun&repo=CPAA&theme=github_dark&hide_border=true">
      <img width="49%" alt="CPAA" src="https://github-readme-stats.vercel.app/api/pin/?username=Spark-of-Sun&repo=CPAA&theme=default&hide_border=true" />
    </picture>
  </a>
</p>

### [MLQA-RAG](https://github.com/Spark-of-Sun/MLQA-RAG): citation-validated Q&A over legal and medical documents

Five FastAPI services (gateway, ingestion, retrieval, generation, citation validator) that run together under `docker compose`.

- **Verified citations:** every `[chunk_id]` must resolve to a retrieved chunk and pass an NLI entailment check, otherwise it is marked `[unverified]` or regenerated
- **Access control before ranking:** tenant, matter/patient, and confidentiality tier are filtered before scoring, and enforced at both the Gateway and Retrieval
- **Hybrid retrieval:** dense search (Qdrant) plus BM25 and a cross-encoder reranker, with clause- and SOAP-aware chunking
- **Token budget:** whole-chunk trimming, LLMLingua compression, and a per-tenant Redis response cache
- **Testable by design:** every model sits behind a fake/real backend, giving 75 unit tests and per-service CI with no GPU or API keys

> **Status:** active development. Services, contracts, and tests are in place; persistence, the evaluation harness, frontend, and production infra are next.

`Python` `FastAPI` `Qdrant` `Redis` `PostgreSQL` `Docker Compose` `GitHub Actions`

### [CPAA](https://github.com/Spark-of-Sun/CPAA): configurable personal AI agent on WhatsApp

An agent, "Kai", that carries out natural-language requests over WhatsApp across Gmail, Google Calendar, Slack, Zoom, and other Composio toolkits.

- **Agent runtime:** Strands Agents SDK on AWS Bedrock, with per-user tools loaded over MCP
- **Memory and identity:** mem0 long-term memory; Auth0 login with OTP-based WhatsApp number linking
- **Backend:** Redis caching and a Gmail event queue, PostgreSQL with Alembic migrations, and a Next.js dashboard

`Python` `FastAPI` `Strands Agents` `Composio` `mem0` `Redis` `PostgreSQL` `Next.js`

### [noirchat](https://github.com/Spark-of-Sun/noirchat): privacy-first ephemeral messaging

- **X25519** session keys, with private keys **AES-256-GCM** encrypted before they touch Redis
- **Argon2id** hashing in the browser with an HMAC challenge-response, so the server never sees the raw passphrase
- Randomized response jitter against timing leaks, plus hard deletion of read or expired messages

`Python` `FastAPI` `PostgreSQL` `Redis` `Vite`

---

## Tech Stack

<table>
  <tr>
    <td><b>Languages</b></td>
    <td>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
      <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
      <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black" />
    </td>
  </tr>
  <tr>
    <td><b>Backend & Data</b></td>
    <td>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" />
      <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
      <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" />
      <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square&logo=qdrant&logoColor=white" />
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" />
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td><b>AI / ML</b></td>
    <td>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
      <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" />
      <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" />
      <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black" />
      <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white" />
    </td>
  </tr>
  <tr>
    <td><b>Tooling</b></td>
    <td>
      <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" />
      <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
      <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" />
      <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" />
      <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white" />
    </td>
  </tr>
</table>

---

<p align="center">
  <sub>English · Hindi · Nepali &nbsp;|&nbsp; Bengaluru, India</sub>
</p>
