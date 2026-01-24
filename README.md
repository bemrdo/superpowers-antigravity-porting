# Superpowers Antigravity Porting

> **"Give your agents the engineering discipline they deserve."**

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Gemini CLI](https://img.shields.io/badge/Gemini%20CLI-Google-blue)](https://github.com/google-gemini/gemini-cli)
[![Antigravity](https://img.shields.io/badge/Antigravity-Google-purple)](https://antigravity.google/)

This project is a dedicated port of the revolutionary **Superpowers** framework, adapted specifically for **Google Antigravity** and the **Context7** ecosystem. It empowers AI agents to write high-quality, reliable, and testable code by enforcing rigorous software engineering workflows.

**Superpowers Skill for Antigravity**

## 🙏 Tribute & Inspiration
**This project stands on the shoulders of giants.**

The core philosophy, methodology, and original implementation of "Superpowers" were created by **Jesse Vincent (obra)**.

*   **Original Project**: [obra/superpowers](https://github.com/obra/superpowers)
*   **Original Creator**: [Jesse Vincent (@obra)](https://github.com/obra)

We are deeply grateful to **obra** for pioneering the concept of "Agentic coding with discipline" — specifically the **git superpower** idea that transforms AI from a chaotic code-generator into a structured, thoughtful engineer. His work demonstrated that with the right "skills" (instructions) and "workflows" (processes), AI can practice true Test-Driven Development (TDD), systematic debugging, and careful planning.

This port is a humble attempt to bring that same engineering rigor to the Antigravity community, ensuring that Obra's vision of reliable AI coding extends to new platforms.

---

## ⚡ What is "Superpowers"?

Superpowers is not just a library; it's a **mindset** for AI agents. It shifts the paradigm from:
> *User asks → AI guesses & codes → User fixes bugs*

To:
> *User asks → AI Brainstorms → AI Plans → User Approves → AI Executes (TDD) → AI Verifies → Working Code*

### Core Principles
1.  **Planning First**: No code is written without a detailed, approved blueprint.
2.  **TDD (Test-Driven Development)**: Write tests before implementation. Red -> Green -> Refactor.
3.  **Systematic Debugging**: Don't guess. Isolate variables, hypothesize, and verify fixes.
4.  **Verification**: Every step requires proof of success.

---

## 📚 Project Structure

This repository adapts the original skills into the Antigravity `.agent` format:

### 🛠 Skills (`.agent/skills`)
"Instructions that teach the agent *how* to do things."

*   **`using-superpowers`**: The master skill. Teaches the agent the overall philosophy.
*   **`brainstorming`**: How to ask clarifying questions and refine a loose idea into a spec.
*   **`writing-plans`**: How to break a spec into tiny, verifiable implementation steps (2-10 min each).
*   **`executing-plans`**: How to reliably execute a plan, file by file, with verification.
*   **`test-driven-development`**: The strict discipline of writing failing tests first.
*   **`systematic-debugging`**: A scientific method for finding bugs (trace, isolate, fix, verify).
*   **`verification-before-completion`**: Final quality gates before marking a task done.
*   **`subagent-driven-development`**: Delegating tasks to sub-agents (utilized by execution workflows).
*   **`dispatching-parallel-agents`**: Orchestrating multiple sub-agents.
*   **`finishing-a-development-branch`**: wrapping up work cleanly.
*   **`requesting-code-review`** & **`receiving-code-review`**: Collaborative review processes.
*   **`using-git-worktrees`**: Managing isolated workspaces for tasks.
*   **`writing-skills`**: Meta-skill for extending the system.

### 🔄 Workflows (`.agent/workflows`)
"Slash commands that trigger specific agent behaviors."

*   `/superpowers-brainstorm`: Start a session to explore ideas and requirements.
*   `/superpowers-write-plan`: Generate a rigorous implementation plan for approval.
*   `/superpowers-execute-plan`: Run the approved plan step-by-step.

---

## 🚀 Getting Started

To enable Superpowers in your Antigravity environment:

1.  **Copy the `.agent` directory** from this repository into the root of your project.
    ```bash
    cp -r superpowers-antigravity-porting/.agent /path/to/your/project/
    ```
2.  **Initialize Superpowers** in your chat (run this to load/update configurations):
    ```
    /superpowers-reload
    ```
3.  **Start using it!**
    *   *Have a vague idea?* -> `/superpowers-brainstorm`
    *   *Ready to build?* -> `/superpowers-write-plan`

### 🛡 Rules (`.agent/rules`)
"Guardrails that enforce the Superpowers philosophy."

*   **`superpowers`**: Always-on rules requiring planning, checking, and safety.
---

## 📝 Example Workflow

1.  **You**: `Use /superpowers-brainstorm to discuss a Python script for web scraping.`
2.  **Agent**: *Asks clarifying questions about the target site, data format, and frequency.* -> produces a summary.
3.  **You**: `/superpowers-write-plan based on the brainstorm summary.`
4.  **Agent**: *Produces a `plan.md` file with detailed steps.*
    > "I will create `scraper.py`, add `requirements.txt`, write `test_scraper.py`, and verify using a mock server."
5.  **You**: "APPROVED"
6.  **You**: `/superpowers-execute-plan`
7.  **Agent**:
    *   *Step 1*: Creates `requirements.txt`. Verifies installation. ✅
    *   *Step 2*: Writes `test_scraper.py` (it fails). 🔴
    *   *Step 3*: Writes `scraper.py` (test passes). 🟢
    *   *Step 4*: runs final verification. ✅

---

## 🤝 Contributing

We welcome contributions to improve the Antigravity port!
*   Found a bug in a skill? Open an Issue.
*   Improved a prompt? specific a PR.

*Note: Please ensure any improvements to the core philosophy honor the original intent of the Superpowers project.*

---

## 📜 License

MIT License. See [LICENSE](LICENSE) file for details.

Original content © [Superpowers](https://github.com/obra/superpowers).
Ported to Antigravity Skills.