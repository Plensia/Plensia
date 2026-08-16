<!-- Banner + snake are served from this repo. Badges are shields.io.
     Nothing here depends on a hobby-tier third-party renderer staying up. -->

<img width="100%" src="./banner.svg" alt="Plensia Lukosi — Data Analyst, Dar es Salaam">

<p align="center">
  <a href="https://www.linkedin.com/in/plensia-lukosi/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
  <a href="mailto:plensiapl@gmail.com">
    <img src="https://img.shields.io/badge/Email-Say%20hi-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  <a href="./Plensia_Lukosi_CV_Data_Analyst.pdf">
    <img src="https://img.shields.io/badge/CV-Download%20PDF-14B8A6?style=for-the-badge&logo=adobeacrobatreader&logoColor=white" alt="Download CV">
  </a>
  <a href="https://github.com/Plensia?tab=repositories">
    <img src="https://img.shields.io/badge/All%20repos-Browse-24292E?style=for-the-badge&logo=github&logoColor=white" alt="Repositories">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black" alt="Power BI">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Excel-217346?style=flat-square&logo=microsoftexcel&logoColor=white" alt="Excel">
  <img src="https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white" alt="dbt">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit">
</p>

---

I turn vague asks into checkable questions, then answer them in SQL, Power BI and Excel — and publish the working out, bugs included.

**Open to data analyst roles and freelance dashboard work** — remote or Dar es Salaam.

---

## 📂 Projects

Click any row to open the write-up.

| | Project | Headline | Stack |
|:--:|:--|:--|:--|
| 🕵️ | **[PaySim Fraud Detection](https://github.com/Plensia/PaySim-Fraud-Analysis)** | **97.7% of fraud caught, zero false positives** across 6.36M transactions | `Python` `PostgreSQL` `Power BI` |
| 🏭 | **[Maven Fuzzy Factory](https://github.com/Plensia/maven-fuzzy-factory-etl)** | **1.2M+ rows**, incremental ETL → 5 dbt marts → dashboard, containerized | `Python` `PostgreSQL` `dbt` `Docker` |
| 📈 | **[LinkedIn Content Performance](https://github.com/Plensia/linkedin-content-performance-analysis)** | Loudest posts ≠ best posts — recap content converted at **39.5%** | `Excel` |
| ☕ | **[Coffee Taste Test](https://github.com/Plensia/great-american-coffee-taste-analysis)** | Stated preference survived the blind test, across **4,023** respondents | `Power BI` `Power Query` |

<details>
<summary><b>🕵️ PaySim — the numbers behind that headline</b></summary>

<br>

| | |
|:--|:--|
| **Scope** | 6,362,620 mobile-money transactions |
| **Status quo** | The bank's existing rule caught 16 of 8,213 fraud cases — 0.2% recall. Effectively dormant. |
| **The obvious fix** | Flag transfers over 200,000 → 66.6% recall, but 1,192,198 false positives. Roughly **218 false alarms per fraud caught**. |
| **What shipped** | One behavioural signal — the sender's balance drained to zero. **97.7% recall, 0 false positives.** Not a compromise between the other two; better than both. |
| **Proven, not assumed** | Merchants exempt because 2.15M merchant-bound transactions contained zero fraud — checked, not guessed. |

</details>

<details>
<summary><b>🏭 Maven Fuzzy Factory — what's actually in the box</b></summary>

<br>

| | |
|:--|:--|
| **Ingest** | Incremental ETL into PostgreSQL on a `created_at` watermark, with primary-key validation. A rerun extends the warehouse instead of duplicating it. |
| **Model** | 5 dbt marts — channel performance, product profitability, refund trends, cohort retention, order value |
| **Serve** | Streamlit executive dashboard |
| **Ship** | Docker Compose, reproducible from a single command |

</details>

<details>
<summary><b>📈 LinkedIn — reach and engagement are different questions</b></summary>

<br>

| | |
|:--|:--|
| **Scope** | 59 organic posts, Jan–Nov 2024 |
| **Finding** | Top-reach topics pulled 8,703 impressions. Recap posts pulled 1,209 — and **39.5% engagement**, double the next best. |
| **Bonus** | "Shorter is better" turned out false: medium-length posts hit 11.4% CTR vs 3.6% for the shortest. |
| **Caught in the audit** | A casing typo splitting one category into two, and a "Total" row buried inside the raw data table injecting phantom categories into every chart. |

</details>

<details>
<summary><b>🙈 Things I got wrong first</b></summary>

<br>

- **Transfer velocity looked like an obvious fraud signal.** It isn't — 99.86% of accounts transact exactly once, so there's no velocity to measure.
- **Wrote a DAX column that referenced its own source field.** Circular dependency. Rebuilt it in Power Query.
- **Assumed a plain text match would sort correctly.** An earlier cleanup step left trailing spaces and mixed casing, so every comparison silently failed.

The gap between "looks correct" and "is correct" is where most of the actual work lives.

</details>

---

## 🐍 Watch the commits get eaten

<img width="100%" src="https://raw.githubusercontent.com/Plensia/Plensia/output/snake.svg" alt="Contribution snake animation">

---

## 🎓 Credentials

<p align="left">
  <img src="https://img.shields.io/badge/Google-Advanced%20Data%20Analytics-4285F4?style=flat-square&logo=google&logoColor=white" alt="Google Advanced Data Analytics">
  <img src="https://img.shields.io/badge/DataCamp-Associate%20Data%20Analyst-03EF62?style=flat-square&logo=datacamp&logoColor=black" alt="DataCamp Associate Data Analyst">
  <img src="https://img.shields.io/badge/Maven%20Analytics-Power%20BI%20Desktop-F2C811?style=flat-square" alt="Maven Analytics Power BI">
  <img src="https://img.shields.io/badge/PL--300-in%20progress-64748B?style=flat-square&logo=microsoft&logoColor=white" alt="PL-300 in progress">
</p>

---

<p align="center">
  <i>Bring me a question you haven't finished defining yet.</i><br>
  Tell me the decision waiting on the data, and I'll tell you what it can actually support.
</p>
