# JMCS Instruction File Standards

JMCS uses a deterministic, instruction‑file‑driven architecture to ensure consistent, repeatable vertical slice development across all layers of an application. The documents below define the standards, training, and styling rules used across the organization.

---

## 1. Instruction File Standard

**Purpose:**  
Defines how JMCS uses deterministic, single‑responsibility instruction files to generate consistent vertical slices across database, API, and UI layers.

**Key Concepts:**

- Each instruction file defines one layer only
- Files must be explicit, complete, and machine‑readable
- No inference or invention is allowed
- UI styling is part of the contract
- Length does not matter — scope does

**Covers:**

- DB Instruction Files
- API Instruction Files
- UI Instruction Files (including styling)
- Core principles, required sections, and formatting rules

Full document: [INSTRUCTION_FILES_STANDARDS.md](INSTRUCTION_FILES_STANDARDS.md)

---

## 2. Instruction File Training Guide

**Purpose:**  
Provides developers with practical guidance on how to write, structure, and validate instruction files used in automated code generation.

**Key Concepts:**

- Follow required section order
- Use declarative, unambiguous language
- Include all validation, error states, and styling rules
- Keep DB, API, and UI concerns separate
- Avoid vague or implicit instructions

**Covers:**

- How to write each type of instruction file
- How automation consumes them
- Common mistakes to avoid
- Best practices for clarity and consistency

Full document: [INSTRUCTION_FILE_TRAINING.md](INSTRUCTION_FILE_TRAINING.md)

---

## 3. UI Styling Contract

**Purpose:**  
Defines the deterministic styling rules automation systems must follow when generating UI components.

**Key Concepts:**

- Styling is contractual, not decorative
- No invented colors, spacing, or layout patterns
- All styling must reference the design system
- Responsive and accessibility rules must be explicit
- Only documented variations are allowed

**Covers:**

- Component‑level styling rules
- Design system references
- Prohibited and allowed behaviors
- Global styling rules (grid, spacing, typography, palette, motion)

Full document: [UI_STYLING_CONTRACT.md](UI_STYLING_CONTRACT.md)

---

## 4. Contributing Guide

**Purpose:**  
Explains how to write, review, and submit instruction files in compliance with JMCS deterministic standards.

**Key Concepts:**

- One instruction file per layer — no mixing concerns
- All fields, rules, and styling must be explicit
- Peer review required before automation runs
- Breaking changes must be documented and communicated

**Covers:**

- Per‑file‑type contribution checklists (DB, API, UI)
- Five‑step review process
- Submission and change management guidance
- Common mistakes to avoid

Full document: [CONTRIBUTING.md](CONTRIBUTING.md)
