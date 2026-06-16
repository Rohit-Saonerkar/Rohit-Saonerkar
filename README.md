import { useState } from "react";

const readme = `<h1 align="center">Hi, I'm Rohit Saonerkar 👋</h1>

<p align="center">
  <b>Full-Stack Software Developer · Java · Python · React.js · SQL · Power BI</b><br/>
  📍 Nagpur, India &nbsp;|&nbsp;
  ✉️ <a href="mailto:rsaonerk@gmail.com">rsaonerk@gmail.com</a> &nbsp;|&nbsp;
  🔗 <a href="https://linkedin.com/in/rohit-saonerkar">LinkedIn</a> &nbsp;|&nbsp;
  🐙 <a href="https://github.com/RohitSaonerkar">GitHub</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/React.js-20232A?style=flat&logo=react&logoColor=61DAFB"/>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white"/>
</p>

---

## 👤 About Me

Full-Stack Software Developer with hands-on experience building Java and Python applications, RESTful APIs, and React.js interfaces. I enjoy working across the full SDLC — from translating business requirements into technical specs to shipping well-tested, maintainable code.

Currently at **Blinc Innovations Ltd**, where I build and maintain production software modules in an Agile/Scrum environment. Passionate about clean architecture, data-driven dashboards, and continuous learning.

---

## 🛠️ Technical Skills

| Category | Technologies |
|---|---|
| **Languages** | Java, Python, C, C++ |
| **Web & APIs** | React.js, HTML5, CSS3, REST APIs, JSON, JDBC |
| **Frameworks** | Spring Boot, Hibernate, Maven |
| **Databases** | MySQL, SQL (Joins, Stored Procedures, Indexing, Query Optimization) |
| **Data & BI** | Power BI (DAX, Slicers, KPIs, Drill-through), Excel (Pivot Tables, VLOOKUP) |
| **Tools & DevOps** | Git, GitHub, Docker, CI/CD, Postman, IntelliJ IDEA, VS Code, MySQL Workbench |
| **Concepts** | OOP, MVC, Agile/Scrum, SDLC, Unit Testing, Data Structures, REST Architecture |

---

## 🚀 Featured Projects

### 🏦 Bank Management System
> Java · MySQL · OOP · JDBC

Full-featured desktop banking application supporting account creation, deposits, withdrawals, fund transfers, and loan management. Built with a normalized MySQL schema for efficient data storage and retrieval.

---

### 🛒 Online Shopping Portal
> React.js · HTML5 · CSS3 · REST API

Responsive e-commerce SPA with product filtering, cart state management, and a mobile-first layout. Performance optimized through component-level code splitting.

---

### 🚗 BMW Sales Analytics Dashboard
> Power BI · DAX · Data Visualization

Executive dashboard tracking KPIs including revenue, profit margin, and regional performance. Replaced a manual monthly reporting process with a real-time self-service analytics solution.

---

### 📊 Retail Sales Analysis Dashboard
> Excel · Pivot Tables · Data Analysis

Multi-tab Excel dashboard analyzing sales data across multiple months. Identified top-performing product categories and revenue trends to support business purchasing decisions.

---

## 💼 Work Experience

**Software Engineer** — Blinc Innovations Ltd, Nagpur *(Jun 2023 – Present)*
- Developed and maintained software modules across the full SDLC, reducing post-release bug reports through systematic unit testing and code reviews
- Collaborated with cross-functional teams to translate business requirements into technical specifications and actionable deliverables
- Built internal tooling improvements that significantly reduced repetitive manual tasks for the operations team

**Python Developer** — IBase Electrosoft LLP, Nagpur *(Jan 2023 – May 2023)*
- Built and maintained Python-based internal tools automating data-processing workflows and reducing manual data entry time
- Wrote unit tests and technical documentation, improving developer onboarding time and code maintainability

---

## 🎓 Education

**B.E. — Computer Technology** · Nagpur University, Maharashtra *(2020 – 2024)*  
CGPA: 7.85 / 10

---

## 📜 Certifications

- 🏅 IBM: Java Fundamentals
- 🏅 IBM: SQL and Relational Databases
- 🏅 IBM: Web Development Using HTML
- 🏅 Master in Full-Stack Development using Java *(hands-on training program)*
- 🏅 Data Science and Analytics using AI *(hands-on training program)*

---

<p align="center">
  <i>Open to Software Developer and Backend Developer roles. Let's connect!</i>
</p>`;

export default function App() {
  const [copied, setCopied] = useState(false);

  const handleCopy = () => {
    navigator.clipboard.writeText(readme).then(() => {
      setCopied(true);
      setTimeout(() => setCopied(false), 2500);
    });
  };

  return (
    <div style={{ padding: "1rem 0" }}>
      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: "10px" }}>
        <span style={{ fontSize: "14px", fontWeight: 500, color: "var(--color-text-primary)" }}>
          GitHub Profile README.md
        </span>
        <button
          onClick={handleCopy}
          style={{
            display: "inline-flex", alignItems: "center", gap: "6px",
            padding: "7px 16px", borderRadius: "var(--border-radius-md)",
            fontSize: "13px", cursor: "pointer", fontWeight: 500,
            background: copied ? "var(--color-background-success)" : "var(--color-background-primary)",
            color: copied ? "var(--color-text-success)" : "var(--color-text-primary)",
            border: copied ? "0.5px solid var(--color-border-success)" : "0.5px solid var(--color-border-secondary)",
            transition: "all 0.2s"
          }}
        >
          {copied ? "✓ Copied!" : "⎘ Copy all"}
        </button>
      </div>
      <textarea
        readOnly
        value={readme}
        onClick={e => e.target.select()}
        style={{
          width: "100%", height: "420px", resize: "vertical",
          fontFamily: "var(--font-mono)", fontSize: "12px",
          lineHeight: "1.6", padding: "14px",
          background: "var(--color-background-secondary)",
          color: "var(--color-text-primary)",
          border: "0.5px solid var(--color-border-tertiary)",
          borderRadius: "var(--border-radius-md)",
          outline: "none"
        }}
      />
      <p style={{ fontSize: "12px", color: "var(--color-text-secondary)", marginTop: "8px" }}>
        Click inside the text area to select all, or use the "Copy all" button above.
      </p>
    </div>
  );
}
