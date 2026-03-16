# Block Library Specification

This document defines the structure and rules for the delivery scope block library.

The block library is the **core component** of the Delivery Scope Assistant.

---

# Concept

Each delivery scope element is represented as a **block**.

Blocks can be combined to build a complete delivery scope document.

Examples:

- Control system – general
- PLC system
- SCADA system
- Generator protection
- High voltage apparatus
- Commissioning

---

# Block Structure

Each block must contain the following fields.


ID
Category
Title
Keywords
Standard text
Standard flag


---

# Example Block


{
"id": "CTRL_003",
"category": "control_system",
"title": "PLC System",
"keywords": ["PLC", "controller", "automation"],
"standard": true,
"text": "PLC based control system including CPU, IO modules and communication modules."
}


---

# ID Naming Convention

Block IDs follow this pattern:

CATEGORY_NUMBER

Examples:

CTRL_001  
CTRL_002  
HV_001  
LV_002  

---

# Category List

The following categories are used.


control_system
high_voltage
low_voltage
instrumentation
mechanical
services
options


These categories allow grouping blocks when generating delivery scope documents.

---

# Keywords

Keywords are used for matching blocks with customer specifications.

Example:


keywords:
generator
protection
relay
differential


Keywords should include:

- technical terms
- common abbreviations
- alternative wording

---

# Standard Flag

The `standard` field defines whether a block is normally included.

Values:


true = standard scope
false = optional scope


Example:

Standard:

- control system
- PLC system
- SCADA system

Optional:

- data gateway
- remote monitoring

---

# Block Library Organization

Recommended folder structure:


blocks/

CTRL_001.json
CTRL_002.json
CTRL_003.json
HV_001.json
LV_001.json
INST_001.json
MECH_001.json
SERV_001.json
OPT_001.json


Each block is stored in its own file.

---

# Library Growth

The block library will expand over time.

Expected size:


Initial prototype: 20–30 blocks
Operational system: 80–150 blocks
Large library: 200+ blocks


New blocks can be added as new scope elements appear in projects.

---

# Engineering Responsibility

The block library represents engineering knowledge.

Therefore:

- blocks must be reviewed by engineers
- wording must be technically correct
- scope descriptions must remain consistent

The quality of the block library directly determines the usefulness of the system.

---

# Guiding Principle

The block library should reflect **real engineering scope**, not theoretical structures.

Blocks must represent practical elements used in real projects.
