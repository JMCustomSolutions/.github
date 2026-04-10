# **Instruction File Training Guide**
*A practical guide for developers working with deterministic instruction‑file‑driven systems.*

---

## **Overview**

This guide teaches developers how to write, structure, and validate instruction files used for automated code generation across database, API, and UI layers.

Instruction files are:

- **Declarative**
- **Explicit**
- **Deterministic**
- **Machine‑readable**
- **Non‑creative**

They define the source‑of‑truth contract for each layer of a vertical slice.

---

## **Core Principles**

### **1. Single Responsibility**

Each instruction file defines one layer only:

- DB
- API
- UI

Do not mix concerns.

### **2. No Invention**

Automation systems must not guess, infer, or create patterns not defined in the file.

### **3. Explicit Over Implicit**

All fields, rules, relationships, and styling must be written explicitly.

### **4. Machine‑Readable First**

Structure and clarity matter more than brevity.

### **5. Unlimited Length**

Files may be long if the scope requires it.  
Scope determines boundaries, not line count.

---

## **Instruction File Types & Required Sections**

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
- UI Styling Contract
- UI test expectations
- No‑invention rules

---

## **UI Styling Contract (Summary)**

Styling is part of the deterministic contract.

**Includes:**

- Spacing, padding, layout patterns
- Typography tokens
- Color tokens
- Responsive rules
- Design system references
- Prohibited styling behaviors
- Allowed variations
- Global styling rules

*(See UI_STYLING_CONTRACT.md for full details.)*

---

## **Writing Instruction Files**

### **1. Use Structured Sections**

Follow the required order for each file type.

### **2. Use Declarative Language**

Examples:

- "Field `title` is required."
- "Use the standard list layout."

Avoid vague phrasing.

### **3. Include All Required Details**

Do not assume the automation layer knows anything not written.

### **4. Avoid Ambiguity**

Do not use:

- "etc."
- "as needed"
- "similar to X"
- "use your judgment"

### **5. Keep Layers Separate**

DB → API → UI must remain isolated.

---

## **Consuming Instruction Files**

**Automation systems will:**

- Read the instruction file
- Ask clarifying questions if needed
- Generate code deterministically
- Generate tests
- Produce a complete vertical slice

**Developers must:**

- Review generated code
- Run tests
- Validate behavior
- Confirm no drift or invention occurred

---

## **Common Mistakes to Avoid**

- Mixing DB, API, and UI concerns
- Missing validation rules
- Forgetting error states
- Vague styling instructions
- Relying on implicit naming
- Adding one‑off UI patterns
- Omitting test expectations
- Assuming the system will "figure it out"

---

## **Summary**

Instruction files are deterministic contracts.  
They must be explicit, complete, and unambiguous.  
UI styling is part of the contract.  
If it's not written, it doesn't exist.
