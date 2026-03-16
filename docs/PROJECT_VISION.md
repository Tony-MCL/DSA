# Delivery Scope Assistant

## Project Owner
Morning Coffee Labs

## Purpose

Delivery Scope Assistant is an internal engineering tool designed to help generate a **first draft of delivery scope documents** based on customer specifications.

The tool assists engineers in quickly identifying relevant delivery elements from a structured library of standard scope blocks.

The system is intended to **support engineering work**, not replace engineering judgement.

---

## Background

Preparing delivery scope documents for technical projects often requires manually navigating large standard documents and adapting them to each customer specification.

This process can be time-consuming and increases the risk of:

- missing standard scope elements
- overlooking customer requirements
- missing potential deviations

The Delivery Scope Assistant aims to streamline this process by combining:

- structured standard scope blocks
- text analysis of customer specifications
- guided scope generation

---

## Primary Goals

The tool should:

- help engineers generate delivery scope drafts faster
- reduce the risk of missing important scope elements
- highlight possible deviations or unclear requirements
- provide a structured starting point for deviation lists

---

## Non-Goals

The tool will **not**:

- replace engineering judgement
- automatically produce final offer documents
- act as a full AI engineering system
- make engineering decisions without human review

Engineers must always review and approve generated scope.

---

## Core Concept

The system uses a **block-based delivery scope library**.

Each block represents a reusable element of a delivery scope.

Example blocks:

- Control system – general
- PLC system
- SCADA system
- Generator protection
- High voltage apparatus
- Battery system
- Commissioning

The system matches customer requirements against this block library to suggest relevant scope elements.

---

## Expected Benefits

If successful, the system should:

- reduce time spent preparing delivery scope
- improve consistency across proposals
- help engineers identify missing scope elements
- improve early identification of deviations

---

## Development Philosophy

The project follows a **progressive development approach**.

Instead of building a complex AI system immediately, the tool will evolve through stages:

1. Delivery scope generator
2. OBS and deviation detection
3. Advanced engineering assistance

Each stage must deliver practical value before moving to the next.

---

## Target Users

Primary users:

- technical sales engineers
- proposal engineers
- project engineers

Working with:

- hydropower projects
- control systems
- electrical apparatus
- plant automation systems

---

## Long-Term Vision

In the long term, the tool may evolve into a broader engineering assistant capable of:

- identifying deviations
- learning from previous projects
- suggesting missing scope elements
- supporting technical proposal preparation

However, the immediate focus is on **practical usefulness in daily engineering work**.
