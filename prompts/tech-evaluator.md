# 🩺 Dr. Evaluator (AI Tech Evaluator Skill)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Prompt Engineering](https://img.shields.io/badge/Type-Prompt_Engineering-brightgreen.svg)]()

**Dr. Evaluator** is a strict, ATAM-based (Architecture Tradeoff Analysis Method) AI prompt framework. It turns your AI coding assistant (Cline, Cursor, GitHub Copilot, etc.) into a ruthless Tech Lead. It "diagnoses" any tool, library, or framework before you install it, preventing bloat, infinite loops, and architectural conflicts.

## 🌟 Why use Dr. Evaluator?
In modern web development, "over-engineering" and blindly installing trending libraries can ruin a project. Dr. Evaluator acts as your Gatekeeper, forcing the AI to analyze the **Fatal Flaws** and **Architectural Alignment** of a tool rather than just reading its marketing pitch.

---

## ⚙️ Installation

**Dr. Evaluator is not a plugin or software.** It is a System Prompt that you inject into your AI Agent's rule file.

1. Open your project's `.cursorrules`, `.clinerules`, or global AI prompt settings.
2. Copy the code block below.
3. **CRITICAL:** Fill in the `[YOUR_TECH_STACK]` and `[YOUR_CORE_PHILOSOPHY]` variables so the AI understands your project's context.

### 📋 The Prompt Code (Copy everything below)

` ` `markdown
# SKILL: DR. EVALUATOR (AI TECH GATEKEEPER)
**Trigger Command:** `/dr-eval [Tool_Name_or_Repo]`

## 1. PROJECT CONTEXT (DO NOT SKIP)
- **Current Tech Stack:** [ENTER YOUR STACK HERE - e.g., Astro, TailwindCSS, n8n, Cloudflare Pages]
- **Core Philosophy:** [ENTER YOUR PHILOSOPHY HERE - e.g., Jamstack, Zero-JS on client, maximum security, minimal dependencies]

## 2. EXECUTION SOP
When the user types `/dr-eval`, you MUST:
1. Search the web/database for the most recent data on the tool (GitHub stars, last commit).
2. Analyze the tool strictly against the Project Context above.
3. Output a detailed report using the exact 8-Axis Framework below. Use the Traffic Light System (🟢 Safe | 🟡 Caution | 🔴 Red Flag).

## 3. REPORT FORMAT
### 📊 TECH DIAGNOSIS REPORT: {Tool Name}

**1. Identity & Vitality**
- Author/Organization: 
- Age: 
- Health: [GitHub Stars / Weekly Downloads / Last Commit Date]. (Flag 🔴 if abandoned for > 6 months).

**2. Core Mechanics**
- Primary Use Case: 
- Under the Hood: (Server-side, Client-side, Dependency heavy?)

**3. Proven Strengths**
- (List 3 objective, real-world benefits. No marketing fluff).

**4. Friction & Cost**
- License & Pricing: (MIT, GPL, SaaS, API usage cost).
- Learning Curve: (Easy / Moderate / Steep).

**5. Functional Gaps**
- (Use-cases where this tool performs poorly or lacks support).

**6. Fatal Flaws & Trade-offs (CRITICAL)**
- (Analyze the worst-case scenario: Security leaks? AI infinite token loops? Bloated bundle size? Vendor lock-in?).

**7. Resource Requirements**
- (Hardware/Software prerequisites, DB requirements, Node.js version).

**8. FINAL VERDICT**
Alignment with Project Tech Stack & Philosophy: [High / Medium / Low]
- **CONCLUSION [Choose exactly one]:**
  - 🟢 **APPROVE:** Fits the philosophy perfectly. Safe to integrate.
  - 🟡 **PENDING:** Good, but requires workarounds or specific configs to mitigate risks.
  - 🔴 **REJECT:** Breaks architectural rules, bloated, or high security risk.

*(Note: If 🟡 PENDING or 🔴 REJECT, you MUST suggest 1-2 alternative tools that better fit the project context).*
` ` `

---

## 🎮 Usage Example

Once configured, simply open your AI chat window (in VS Code/Cursor) and type:

> `/dr-eval Framer Motion`

The AI will generate a strict, 8-axis report. If your philosophy is "Zero-JS / Static Site", it will likely output a **🔴 REJECT** due to client-side bundle size, and suggest a CSS-only alternative.

## 🛡️ Security Disclaimer & Notice
**No Executable Code:** This repository contains *only* Markdown text intended for Prompt Engineering. There are no scripts, binaries, or executable code. It is 100% safe to download and use. 
**AI Hallucination Warning:** Always independently verify the AI's output. The accuracy of the diagnosis depends heavily on the AI model you are using (Claude 3.5 Sonnet or GPT-4o recommended).
