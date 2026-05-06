# QA Portfolio: E-commerce Testing Project (Joom-like Web App)

## 📌 Project Overview
This repository contains a testing project for an e-commerce platform. The goal was to perform functional, UI/UX, and business logic testing using professional QA methodologies and tools

## 🛠 Tools & Technologies
*   **Testing Tool:** Chrome DevTools (Elements, Console, Network, Device Mode)
*   **Documentation:** Markdown (MD)
*   **Environment:** Windows 11 (Desktop Chrome) & **iPhone SE Emulation**
*   **Version Control:** Git & GitHub

## 🧪 What's Inside?
I have organized the testing artifacts into a clear structure:

1.  **[Test Execution Report](docs/test-cases/execution-report.md)**: A master list of **32 test cases** covering the entire user journey—from Email Registration and Social OAuth to Checkout and Payment processing.
2.  **[Bug Reports Registry](docs/bug-reports/bug-registry.md)**: Detailed reports for 8 identified defects, including reproduction steps, severity, and visual proofs.
3.  **[Test Design Analysis](docs/test-design/analysis-summary.md)**: Application of **Equivalence Partitioning (EP)**, **Boundary Value Analysis (BVA)**, **Decision table**, and **State transition Testing** **** 

## 📈 Key Testing Highlights
*   **Full User Journey:** Tested registration via email (including email confirmation checks) and social media login, profile management, search and filters moduls, shoping cart, payment, and checkout moduls using State Transition Testing
*   **Complex Logic:** Verified a multi-condition coupon system using Decision Tables to ensure correct discount application.
*   **Mobile Emulation:** Identified UI/UX issues (Layout Shifts, Tap Area violations) specifically on small-screen devices (iPhone SE) using Chrome DevTools.
*   **Boundary Testing:** Discovered boundary bypass bugs in price filters through rigorous BVA analysis.

## 📁 Repository Structure
```text
├── docs/
│   ├── test-cases/      # Execution reports and test suites
│   ├── bug-reports/     # Detailed bug registry
│   └── test-design/     # EP, BVA, State Transition Testing, and Decision Table analysis
├── assets/
│   └── screenshots/     # Visual evidence for bug reports
└── README.md            # Project overview
```

---
*This project demonstrates my ability to handle end-to-end testing, document results professionally, and use technical tools to identify deep-level system defects.*
