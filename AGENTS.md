# Agent Instructions & Conversation Documentation Protocol

This repository maintains persistent documentation and archives for all agent interactions, study sessions, and code developments. Agents working in this repository must strictly adhere to the following protocols.

---

## 1. Directory Structure

All documentation and interaction archives must be organized under the `doc/` directory:

```text
doc/
├── notes/
│   └── <topic_summary_folder>/
│       ├── ... (detailed study notes)
│       └── ...
└── prompts/
    └── <topic_summary_folder>/
        ├── ... (full conversation archives with thinking)
        └── ...
```

- **`doc/notes/`**: Houses educational study notes, comprehensive breakdowns, code explanations, and reference materials derived from conversations.
- **`doc/prompts/`**: Houses verbatim/complete conversation logs, prompts, agent responses, and full thinking/reasoning traces.

---

## 2. Folder Naming & Management Rules

### A. Dedicated Conversation Folders
- For every distinct conversation or topic, maintain matching folder names under both `doc/notes/` and `doc/prompts/`:
  - `doc/notes/<topic_summary_folder>/`
  - `doc/prompts/<topic_summary_folder>/`

### B. Dynamic Renaming Based on Content Summary
- Name the folder descriptively to reflect a concise summary of the core concepts, topics, or files discussed (e.g., `01_linear_regression_gradient_descent`, `02_neural_network_backpropagation`).
- As the conversation evolves and expands to new sub-topics or broader concepts, update/rename the folder name so it continues to accurately reflect the overall summary of the content contained within.

### C. Chat Continuations
- If a new conversation is explicitly continued from a previous conversation or chat archive, **do not** create a new detached folder.
- Continue appending notes and transcripts into the **existing folder** corresponding to that prior chat archive.
- If the continuation meaningfully broadens the topic scope, adjust the existing folder's name accordingly to maintain an accurate summary.

---

## 3. Study Notes Standards (`doc/notes/`)

When writing or updating study notes:

1. **Simple, Accessible Language**:
   - Explain concepts using clear, intuitive language, analogies, and step-by-step reasoning.
   - Avoid unnecessary jargon; where technical terms are introduced, provide plain-English definitions first.

2. **Maximum Detail & Rigor**:
   - Be thorough. Do not gloss over edge cases, implementation nuances, mathematical derivations, or architecture choices.
   - Include code snippets, input/output examples, complexity analyses ($O(n)$, memory bounds), and diagrams where appropriate.

3. **Standard References & Citations**:
   - Include standard citations and authoritative references for all theory, algorithms, and libraries used.
   - Examples:
     - Textbook references (e.g., *Pattern Recognition and Machine Learning* by Christopher Bishop; *Deep Learning* by Goodfellow, Bengio, and Courville; *Hands-On Machine Learning* by Aurélien Géron).
     - Landmark research papers (author, title, arXiv/journal link).
     - Official documentation (Python, PyTorch, NumPy, Scikit-learn, etc.).

4. **Structured Note Layout**:
   - **Overview / Objective**: High-level motivation and what this topic addresses.
   - **Key Concepts & Theoretical Foundations**: Detailed explanations and formulas.
   - **Implementation Details**: Code explanations, walkthroughs, and practical considerations.
   - **Key Takeaways & Pitfalls**: Common bugs, gotchas, and performance tips.
   - **References & Further Reading**: Formal bibliography and documentation links.

---

## 4. Conversation Archives & Prompts (`doc/prompts/`)

When archiving conversation transcripts:

1. **Full Archive with Thinking**:
   - Record user prompts, tool interactions/calls, planner outputs, and agent thinking/reasoning traces in full without truncation.
   - Preserve chronological progression of how solutions were formulated, analyzed, and refined.

2. **File Format & Organization**:
   - Save archives in structured markdown format (e.g., `transcript_part1.md`, `session_<date>.md`).
   - Clearly delineate:
     - **User Prompt**
     - **Agent Internal Reasoning / Thinking** (enclosed in collapsible `<details><summary>Thinking Process</summary>...</details>` blocks or dedicated sections)
     - **Tool Invocations & Outputs**
     - **Final Response & Deliverables**
