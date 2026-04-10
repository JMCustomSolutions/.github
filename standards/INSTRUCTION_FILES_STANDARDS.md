# **Instruction File Standard**  
*A deterministic, single‑responsibility contract system for automated vertical slice development.*

---

## **Overview**

Instruction files define the structure, behavior, and expectations for each layer of a vertical slice in a software system. They are designed to be:

- **Deterministic**  
- **Explicit**  
- **Machine‑readable**  
- **Non‑creative**  
- **Single‑responsibility**

Instruction files ensure consistent generation of database structures, API layers, and UI components across a codebase.

---

## **Why This System Exists**

Modern applications often suffer from:

- inconsistent patterns  
- developer‑specific interpretations  
- UI drift  
- API contract mismatches  
- onboarding friction  
- duplicated logic across layers  

Instruction files solve these problems by acting as **source‑of‑truth contracts** for each layer.  
They enable:

- predictable automation  
- consistent architecture  
- reduced cognitive load  
- faster onboarding  
- repeatable vertical slice development  

This standard defines how to write those contracts.

---

## **Core Principles**

### **1. Single Responsibility**

Each instruction file defines **one layer only**:

| File Type | Scope |
|-----------|-------|
| **DB Instruction File** | Schema, relationships, constraints |
| **API Instruction File** | Endpoints, envelopes, validation, errors |
| **UI Instruction File** | Components, flows, styling, tests |

### **2. Deterministic, Not Creative**

Instruction files must be explicit and complete.  
No inference. No guessing. No invention.

### **3. Machine‑Readable First**

These files are written for automation systems.  
Clarity and structure take priority over brevity.

### **4. Unlimited Length**

There is no line‑count limit.  
Scope determines boundaries, not size.

### **5. No Hidden Knowledge**

If it is not written in the file, it does not exist.

---

## **Instruction File Types**

---

### **A. DB Instruction File**

Defines the data layer.

**Required Sections:**

- Entities  
- Fields (name, type, constraints)  
- Relationships  
- Validation rules  
- Documentation  
- No‑invention rules  

---

### **B. API Instruction File**

Defines the backend contract.

**Required Sections:**

- Endpoints  
- Request envelopes  
- Response envelopes  
- Validation rules  
- Error states  
- Authorization rules  
- Unit test expectations  
- No‑invention rules  

---

### **C. UI Instruction File**

Defines the user‑facing layer, including styling.

**Required Sections:**

- Components to generate  
- Screens / routes  
- State management rules  
- Form definitions  
- Validation rules  
- API consumption details  
- **UI Styling Contract**  
- UI test expectations  
- No‑invention rules  

---

## **UI Styling Contract**

Styling is part of the contract and prevents UI drift.

**Includes:**

- Spacing, padding, and layout patterns  
- Typography tokens  
- Color tokens  
- Responsive rules  
- Design system references  
- Prohibited styling behaviors  
- Allowed variations  
- Global styling rules  

---

## **Formatting Rules**

To ensure consistency across instruction files:

### **1. Use Structured Sections**

Follow the required section order for each file type.

### **2. Use Declarative Language**

Examples:

- “Field `name` is required.”  
- “Use the standard list layout.”  

Avoid vague phrasing.

### **3. Use Consistent Naming Conventions**

Match the naming patterns used across the system.

### **4. Use Comments for Clarity**

Explain *why* when needed, not just *what*.

### **5. Keep Files Machine‑Friendly**

Prefer structured lists, tables, and key/value formats.

---

## **Common Mistakes to Avoid**

- Mixing DB, API, and UI concerns in one file  
- Leaving out validation rules  
- Forgetting error states  
- Using vague language (“etc.”, “as needed”)  
- Relying on implicit naming or conventions  
- Adding one‑off UI patterns  
- Omitting styling rules in the UI file  
- Assuming the automation layer will “figure it out”  

---

## **Versioning & Change Management**

Instruction file standards evolve over time.  
When updating this document:

- Maintain backward compatibility where possible  
- Document breaking changes clearly  
- Update templates and examples accordingly  
- Communicate changes to contributors  

---

## **Summary**

Instruction files are deterministic contracts that define one layer of a vertical slice.  
They must be explicit, complete, and unambiguous.  
UI styling is part of the contract.  
Length does not matter — scope does.  
If it’s not written, it doesn’t exist.
