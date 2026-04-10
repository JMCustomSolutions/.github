# **Contributing Guide**
*How to write, review, and submit instruction files under the JMCS deterministic architecture.*

---

## **Overview**

This guide explains how to contribute instruction files to JMCS projects. All contributions must follow the deterministic standards defined in this repository.

Before contributing, read:

- [INSTRUCTION_FILES_STANDARDS.md](INSTRUCTION_FILES_STANDARDS.md) — the core contract system
- [INSTRUCTION_FILE_TRAINING.md](INSTRUCTION_FILE_TRAINING.md) — how to write each file type
- [UI_STYLING_CONTRACT.md](UI_STYLING_CONTRACT.md) — styling rules for UI files

---

## **Philosophy**

This guide ensures all contributors follow the deterministic, single‑responsibility architecture used across JMCS projects.

---

## **Who This Guide Is For**

- Developers writing new instruction files
- Reviewers validating instruction files before automation runs
- Contributors updating existing standards

---

## **Core Contribution Rules**

### **1. One File Per Layer**

Each contribution must target exactly one layer:

| Layer | File Type |
|-------|-----------|
| Data | DB Instruction File |
| Backend | API Instruction File |
| Frontend | UI Instruction File |

Do not mix concerns across layers.

### **2. No Invention**

Do not introduce patterns, fields, or behaviors not explicitly required by the feature being built.

### **3. Explicit Over Implicit**

Every field, rule, relationship, and styling decision must be written out. Do not rely on assumptions, conventions, or prior knowledge.

### **4. Styling Is Part of the Contract**

UI instruction files must include a complete UI Styling Contract section. Styling cannot be left to the automation layer.

### **5. Write for Automation First**

Write for automation systems first — clarity and structure take priority over brevity.

---

## **Writing an Instruction File**

Follow the required section order for each file type. See [INSTRUCTION_FILE_TRAINING.md](INSTRUCTION_FILE_TRAINING.md) for full details.

### **DB Instruction File Checklist**

- [ ] Entities defined
- [ ] All fields listed with name, type, and constraints
- [ ] Relationships documented
- [ ] Validation rules explicit
- [ ] No‑invention rules included

### **API Instruction File Checklist**

- [ ] All endpoints listed
- [ ] Request and response envelopes defined
- [ ] Validation rules explicit
- [ ] Error states documented
- [ ] Authorization rules included
- [ ] Unit test expectations listed
- [ ] No‑invention rules included

### **UI Instruction File Checklist**

- [ ] All components listed
- [ ] Screens and routes defined
- [ ] State management rules explicit
- [ ] Form definitions included
- [ ] Validation rules explicit
- [ ] API consumption details documented
- [ ] UI Styling Contract section complete
- [ ] UI test expectations listed
- [ ] No‑invention rules included

---

## **Review Process**

Before submitting an instruction file for automation:

1. **Self‑review** against the checklist for the file type
2. **Verify** no ambiguous language is present ("etc.", "as needed", "similar to X")
3. **Confirm** all layers remain isolated — no cross‑layer references
4. **Validate** that styling is explicit and sourced from the design system
5. **Peer review** — a second contributor must confirm completeness before the file is used for generation

---

## **Submitting Changes**

When updating an existing instruction file or standard:

- Document what changed and why
- Note any breaking changes explicitly
- Update related files if the change affects multiple layers
- Communicate changes to all contributors before automation runs

See the **Versioning & Change Management** section in [INSTRUCTION_FILES_STANDARDS.md](INSTRUCTION_FILES_STANDARDS.md) for full guidance.

---

## **Common Mistakes to Avoid**

- Mixing DB, API, or UI concerns in one file
- Leaving validation rules implicit or incomplete
- Forgetting error states in API files
- Omitting styling rules in UI files
- Using vague language or relying on convention
- Writing for a human reader instead of an automation system

---

## **Summary**

Every instruction file is a deterministic contract.  
Write explicitly. Review carefully. Invent nothing.  
If it's not written, it doesn't exist.
