# MementoMind-Contextual-Web-Memory-Browser-Extension

<!-- BADGES START -->
[![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension/ci.yml?style=flat-square&logo=github-actions)](https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension?style=flat-square&logo=codecov)](https://codecov.io/github/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension)
[![Tech Stack](https://img.shields.io/badge/tech-stack-JavaScript%2C%20HTML%2C%20CSS-blue?style=flat-square&logo=javascript)](https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension)
[![License](https://img.shields.io/badge/license-CC%20BY--NC%204.0-red?style=flat-square&logo=github)](https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension/blob/main/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension?style=flat-square&logo=github)](https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension)
<!-- BADGES END -->

## ✨ Star ⭐ This Repo

MementoMind transforms your web browsing by adding contextual notes, tags, and Wayback Machine snapshots to your bookmarks. Enhance recall, organize pages, and rediscover the 'why' behind every saved link with powerful organization and privacy features.

## 🌳 Architecture Overview

mermaid
graph TD
    A[User Interaction (Browser API)] --> B(Content Script)
    B --> C{Content Management}
    C --> D[Bookmark Storage (WebExtension Storage)]
    C --> E[Wayback Machine API Integration]
    C --> F[Contextual Notes/Tags Storage]
    B --> G(Background Script)
    G --> H{API Services}
    H --> D
    H --> E
    B --> I(Popup UI)
    I --> G


## 📜 Table of Contents

*   [✨ Star ⭐ This Repo](#star--this-repo)
*   [🌳 Architecture Overview](#tree-architecture-overview)
*   [📜 Table of Contents](#scroll-table-of-contents)
*   [🚀 Features](#rocket-features)
*   [🛠️ Technology Stack](#hammer-technology-stack)
*   [⚙️ Development & Setup](#gear-development--setup)
*   [🧪 Testing](#test-tube-testing)
*   [🔒 Security](#lock-security)
*   [🤝 Contributing](#handshake-contributing)
*   [📄 License](#page-facing-up-license)
*   [🤖 AI Agent Directives](#robot-ai-agent-directives)

## 🚀 Features

*   **Contextual Bookmarking:** Attach notes, tags, and custom metadata to each saved link.
*   **Wayback Machine Integration:** Quickly access historical snapshots of saved pages.
*   **Organized Recall:** Rediscover the context and purpose behind your bookmarks.
*   **Privacy-Focused:** Data is stored locally within the browser's secure storage.
*   **Cross-Browser Support:** Compatible with Chrome and Firefox.
*   **Manifest V3 Compliant:** Built with modern browser extension standards.

## 🛠️ Technology Stack

*   **Language:** HTML, CSS, JavaScript (ES6+)
*   **Browser Extension APIs:** WebExtension APIs (Manifest V3)
*   **Styling:** CSS
*   **Wayback Machine API:** Integration with the Internet Archive's Wayback Machine.
*   **Storage:** `browser.storage.local` / `chrome.storage.local`

## ⚙️ Development & Setup

Follow these steps to set up the development environment:

1.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension.git
    cd MementoMind-Contextual-Web-Memory-Browser-Extension
    

2.  **Install Dependencies:**
    While this project primarily uses plain JavaScript, HTML, and CSS, any build tools or linters would be managed here. For browser extensions, direct loading into the browser is often the primary method.
    *No explicit dependency installation is required for basic functionality.* 
    If a build process were introduced (e.g., for transpilation or bundling), you would use:
    bash
    # Example if using a bundler like Webpack or Vite
    # npm install
    

3.  **Load Extension:**
    *   **Chrome:** Open `chrome://extensions/`, enable Developer mode, click 'Load unpacked', and select the extension's root directory.
    *   **Firefox:** Open `about:debugging#/runtime/this-firefox`, click 'Load Temporary Add-on...', and select the extension's `manifest.json` file.

## Script Table

| Script Name      | Description                                                               | Command                                        |
| :--------------- | :------------------------------------------------------------------------ | :--------------------------------------------- |
| `build`          | Compiles and bundles the extension for distribution (if applicable).      | `npm run build` (Example)                       |
| `lint`           | Lints the codebase for style and potential errors.                        | `npm run lint` (Example)                       |
| `test`           | Runs unit and integration tests for the extension's logic.                | `npm run test` (Example)                       |
| `package`        | Packages the extension for release.                                       | `npm run package` (Example)                     |
| `load:chrome`    | Helper command to load the extension in Chrome for development.           | `npm run load:chrome` (Example)                 |
| `load:firefox`   | Helper command to load the extension in Firefox for development.           | `npm run load:firefox` (Example)                |

*Note: Commands are illustrative and depend on the chosen build tooling.* 

## 🧪 Testing

This project employs a robust testing strategy to ensure reliability and stability:

*   **Unit Tests:** Utilizing **Vitest** for fast, isolated testing of individual JavaScript modules and functions.
*   **End-to-End (E2E) Tests:** Leveraging **Playwright** to simulate user interactions across the browser environment, verifying the extension's functionality in real-world scenarios.
*   **Code Coverage:** Measured using **Codecov**, aiming for comprehensive test coverage.

**Verification Commands:**

*   **Run Unit Tests:**
    bash
    npm run test:unit
    
*   **Run E2E Tests:**
    bash
    npm run test:e2e
    
*   **Generate Code Coverage Report:**
    bash
    npm run coverage
    

## 🔒 Security

*   **Manifest V3 Compliance:** Adheres to the latest browser extension security standards.
*   **Content Security Policy (CSP):** Strict CSP defined in `manifest.json` to prevent XSS attacks.
*   **Input Sanitization:** All user inputs are sanitized to prevent injection vulnerabilities.
*   **API Key Management:** No sensitive API keys are embedded directly; use secure browser storage or user-provided configurations.
*   **Dependency Auditing:** Regularly audit dependencies for known vulnerabilities.

## 🤝 Contributing

We welcome contributions! Please refer to the [CONTRIBUTING.md](https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension/blob/main/.github/CONTRIBUTING.md) file for guidelines on submitting issues, feature requests, and pull requests.

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**. See the [LICENSE](https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension/blob/main/LICENSE) file for more details.

## 🤖 AI Agent Directives

<details>
<summary>Show AI Agent Directives</summary>

### 1. IDENTITY & PRIME DIRECTIVE

*   **Role:** Senior Principal Software Architect, Master Technical Copywriter, DevOps Strategist.
*   **Experience:** 40+ years elite industry experience.
*   **Standards:** FAANG-level precision, "Managing the Unmanageable" wisdom.
*   **Context:** December 2025; building for 2026 standards.
*   **Output:** EXECUTION-ONLY. No plans, only executed code and updated docs.
*   **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

### 2. INPUT PROCESSING & COGNITION

*   **Speech-to-Text Interpretation:** Infer technical intent from phonetic errors; **STRICTLY FORBIDDEN** from executing literal typos. Anchor on `README.md` as SSOT.
*   **Mandatory MCP Instrumentation:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` for Dec 2025 industry standards, security threats, 2026 UI trends.
    *   **Validation:** Use `docfork` to verify external API signatures.
    *   **Reasoning:** Use `clear-thought-two` for complex flow architecture *before* code.

---

### 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)

*   **Current Repository Context:** `MementoMind-Contextual-Web-Memory-Browser-Extension` (JavaScript, HTML, CSS Browser Extension).
*   **APPLIED STACK (SCENARIO A: WEB / APP / EXTENSION - TypeScript/JavaScript):
    *   **Core:** JavaScript (ES6+), HTML, CSS.
    *   **Browser Extension Framework:** Manifest V3.
    *   **Bundler/Build Tool (Optional):** Vite 7 (or equivalent for modern extension development).
    *   **State Management:** Signals (Standardized - if applicable).
    *   **Testing Frameworks:** **Vitest** (Unit Tests), **Playwright** (E2E Tests).
    *   **Linting/Formatting:** **Biome** (for speed and comprehensive checks).
    *   **Architecture:** Adheres to modern browser extension patterns (Content Scripts, Background Scripts, Popup UI) with a focus on modularity and clear separation of concerns.
    *   **External Services:** Integration with **Wayback Machine API**.

---

### 4. APEX NAMING CONVENTION

*   **Formula:** `<Product-Name>-<Primary-Function>-<Platform>-<Type>`
*   **Format:** `Title-Case-With-Hyphens`
*   **Constraints:** 3-10 words, high-volume keywords, no numbers/emojis/underscores, no generic words without qualifiers.

---

### 5. README REPLICATION PROTOCOL

*   **Content:** Self-contained Project OS.
*   **Sections:** Visual Authority (Logo, Badges), Structural Clarity (BLUF, Architecture Diagram, TOC), AI Agent Directives (`<details>` block), Development Standards (Setup, Scripts, Principles).
*   **Badges:** `flat-square` style, `chirag127` username, specific shields for build, coverage, stack, license, stars.

---

### 6. CHAIN OF THOUGHT (CoT) PROTOCOL

*   **Pre-computation:** Audit -> Pivot/Archive Decision -> Naming -> Agent Directives Draft -> File Generation -> Polish -> Strict Adherence.

---

### 7. DYNAMIC URL & BADGE PROTOCOL

*   **Base URL:** `https://github.com/chirag127/MementoMind-Contextual-Web-Memory-Browser-Extension`
*   **Consistency:** All links/badges MUST use the new repo name. Never the old one.
*   **AGENTS.md Customization:** Adapt tech stack, testing, etc., to the specific repo. Do not copy generic templates; customize.

</details>
