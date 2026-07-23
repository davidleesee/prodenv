# 🖥️ ProdEnv
> **A narrative-driven, client-side SQL training environment simulating a live data analyst workstation.**

<a href="https://davidleesee.github.io/prodenv/index.html" target="_blank">
  <img src="https://img.shields.io/badge/Live_Demo-ProdEnv-34d399?style=for-the-badge&logo=github" alt="Live Demo" />
</a>
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Tech: WebAssembly](https://img.shields.io/badge/Tech-WebAssembly_--_sql.js-6366f1?style=for-the-badge)](https://sql.js.org/)

---

## 🎯 What This Is

**ProdEnv** redefines technical learning by dropping students into an authentic desktop workspace rather than a standard, text-heavy LMS. 

Learners log in as a newly onboarded Data Analyst at **QOast**—a fictional e-commerce logistics enterprise—and execute SQL queries against a live, client-side relational database.

### Key Highlights

* **Zero Textbook Friction:** Grounded in authentic business scenarios (e.g., fulfillment delays, inventory mismatches, customer tier calculations).
* **In-Universe Operating System:** Features a functional mail client, desktop background personalization, custom audio streaming player (*DataBass*), and hidden worldbuilding lore.
* **Intelligent Diagnostic Agent (Ana):** Evaluates SQL execution console errors (e.g., `no such column`) in real time to offer progressive hints rather than dumping flat answer keys.

---

## 🎓 Instructional Design & Methodology

ProdEnv was built to demonstrate advanced Curriculum Design, Learning Architecture, and Scaffolding Principles (aligned with Purdue University’s MSEd in Learning Design and Technology).

It explicitly bridges the gap between passive reading and active performance through four core mechanisms:

| Instructional Principle | System Implementation |
| :--- | :--- |
| **Mastery-Gated Progression** | Students cannot advance through lesson bands without demonstrating functional query execution against live data targets. |
| **Dynamic Execution Grading** | Queries are validated by running the student's submission and the answer key against the *same* WebAssembly database instance simultaneously to prevent stale evaluation drift. |
| **Cognitive Scaffolding (Ana)** | A regex-driven diagnostic engine analyzes thrown SQLite errors to provide contextual hints—mirroring a real-world senior mentor code review. |
| **Environmental Storytelling** | Worldbuilding, employee chatter, and narrative easter eggs maintain high learner engagement during dry technical topics. |

---

## ⚡ Tech Stack

Designed intentionally with zero heavy framework overhead or compile dependencies—ensuring instantaneous load times and 100% client-side execution.

* **Database Engine:** SQLite compiled to WebAssembly via `sql.js` (runs entirely inside the browser memory space).
* **Frontend Architecture:** Vanilla JavaScript (ES6+), Semantic HTML5, CSS3 Grid/Flexbox.
* **State Management:** Browser `localStorage` for dynamic chat retention, user preferences, and lesson progression.
* **Deployment:** Static hosting via GitHub Pages.

> 💡 **Why No Framework?**  
> The absence of React or Vue is a deliberate architectural decision. A browser-based training tool should load instantly with zero dependency drift or build pipeline overhead.

---

## 🚦 Track Development Status

- [x] **Beginner Track (100% Complete)**
  - [x] Workspace Onboarding & System Setup
  - [x] Data Retrieval, Filtering (`WHERE`, `LIKE`, `BETWEEN`)
  - [x] Aggregations (`GROUP BY`, `HAVING`)
  - [x] Multi-Table Relational Joins (`INNER`, `LEFT`)
  - [x] String Concatenation (`||`) & Dynamic Date Manipulation (`julianday`)
- [ ] **Intermediate Track** *(Planned)*
  - [ ] CTEs (Common Table Expressions) & Window Functions
  - [ ] Schema Modifications (`INSERT`, `UPDATE`, `DELETE`)
- [ ] **Advanced Track** *(Planned)*
  - [ ] Index Optimization, Query Performance Profiling, & View Creation

---

## 💻 Running Locally

Because ProdEnv operates as a zero-build static application, you can spin up the full desktop environment locally in seconds.

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_GITHUB_USERNAME/prodenv.git

# 2. Navigate to the project directory
cd prodenv

# 3. Serve using any static server (e.g., Python)
python3 -m http.server 8000

Once running, navigate to http://localhost:8000/login.html in your browser.
```

📄 License
Distributed under the MIT License. See LICENSE for more information.
