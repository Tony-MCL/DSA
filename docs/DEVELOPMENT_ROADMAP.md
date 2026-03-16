# Development Roadmap

This document describes the planned development phases for the Delivery Scope Assistant.

The project will be developed incrementally in three levels.

Each level must produce a **usable tool** before moving to the next.

---

# LEVEL 1 – Delivery Scope Generator

## Goal

Create a system capable of generating a **first draft delivery scope** based on:

- customer specification text
- a structured block library

The output should significantly reduce manual work when preparing scope documents.

---

## Core Workflow

1. Engineer provides customer specification
2. System analyzes the text
3. Relevant scope blocks are suggested
4. Engineer reviews and adjusts block selection
5. System generates delivery scope draft

---

## Phase 1 – Block Library Definition

### Goal

Convert the existing standard delivery scope document into structured reusable blocks.

### Tasks

- Identify main delivery categories
- Break the standard document into individual scope blocks
- Assign IDs to each block
- Define keywords for matching
- Store blocks in structured format

---

## Phase 2 – Customer Specification Input

### Goal

Allow engineers to provide customer requirements.

Input methods:

- copy/paste text
- PDF
- Word documents
- plain text input

The system extracts raw text for analysis.

---

## Phase 3 – Requirement Analysis

### Goal

Match customer specification content against block keywords.

Example process:

Customer specification  
↓  
Keyword matching  
↓  
Relevant scope blocks identified

---

## Phase 4 – Engineer Review Interface

The engineer must review suggested blocks.

Actions:

- approve block
- remove block
- manually add blocks

Engineering judgement remains essential.

---

## Phase 5 – Delivery Scope Generation

The system generates a structured delivery scope draft.

Example structure:

1 General  
2 Control System  
3 High Voltage Equipment  
4 Low Voltage Equipment  
5 Instrumentation  
6 Services  

Export formats:

- Word
- PDF

---

# LEVEL 2 – OBS Points and Deviation Detection

## Goal

Extend the system to identify potential issues in customer specifications.

Examples:

- missing technical data
- requirements outside standard scope
- unclear or ambiguous descriptions

---

## Phase 6 – Parameter Extraction

Extract technical parameters such as:

- generator voltage
- frequency
- power rating
- short circuit rating
- battery voltage

---

## Phase 7 – Rule-Based Checks

Introduce simple engineering rules.

Examples:

IF generator mentioned  
THEN suggest generator protection

IF busbar requested  
AND standard solution is cables  
THEN flag possible deviation

---

## Phase 8 – Deviation Draft List

Generate a preliminary deviation list.

Example:

| Area | Customer Requirement | Standard | Status |
|-----|-----|-----|-----|
| Generator connection | Busbars | Cables | Possible deviation |

The engineer must verify all deviations.

---

# LEVEL 3 – Advanced Engineering Assistance

## Goal

Provide smarter suggestions based on project history and engineering patterns.

---

## Phase 9 – Project Memory

Allow referencing previous projects.

Example:

Similar project detected → suggest similar scope.

---

## Phase 10 – Missing Scope Suggestions

Identify potentially missing scope elements.

Example:

Customer requests SCADA.

Typical additions:

- remote monitoring
- data gateway
- historian system

---

## Phase 11 – Continuous Improvement

Allow engineers to provide feedback on system suggestions.

Examples:

- relevant suggestion
- irrelevant suggestion
- missing suggestion

This feedback improves system performance over time.

---

# Development Strategy

Follow these principles:

- build useful features early
- keep the system simple initially
- avoid overengineering
- test using real specifications
