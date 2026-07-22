# 🪵 Reinbold Saunabau AI Assistant Suite — Documentation Portal

Welcome to the official technical documentation repository for the **Reinbold Saunabau AI Assistant Suite**. This portal contains technical specifications, architectural guidelines, safety compliance frameworks, and webhook integration guides powering our AI-driven client intake system.

---

## 📌 Table of Contents
- [About the System](#-about-the-system)
- [Core Operational Scenarios](#-core-operational-scenarios)
- [Architect Safeguards (VETO Rules)](#-architect-safeguards-veto-rules)
- [System Architecture & Automation Pipeline](#-system-architecture--automation-pipeline)
- [Repository Structure](#-repository-structure)
- [Deployment & GitHub Pages Configuration](#-deployment--github-pages-configuration)
- [Data Handoff Payload Schema](#-data-handoff-payload-schema)
- [Privacy & Compliance](#-privacy--compliance)
- [Maintainer](#-maintainer)

---

## 💡 About the System

The **Reinbold Saunabau AI Assistant Suite** is an enterprise-grade AI intake and configuration tool designed to handle customer inquiries 24/7. Built on top of custom-trained OpenAI models, the suite assists prospective clients in configuring custom saunas, validating room dimensions against engineering constraints, and scheduling expert consultations.

The entire system operates statelessly during client interactions, converting raw conversation history into structured JSON payloads for automated CRM logging and scheduling.

---

## 🎯 Core Operational Scenarios

The suite operates under two primary intake logic tracks:

### 1. The Configurator Engine
* **Target Environment:** Standard rectangular or square room layouts.
* **Operational Logic:** 
  * Automatically calculates mandatory structural air gaps (subtracting 10 cm total width/depth from available room dimensions).
  * Matches customer preferences against standard **57mm solid wood catalog models**.
  * Recommends optimal heater types (Electric vs. Bio-Combi) and seating configurations.

### 2. Spatial Planning Engine
* **Target Environment:** Complex architectural spaces (e.g., attic roof slopes /*Kniestock*/, room niches, non-standard angles, or large wellness suites).
* **Operational Logic:**
  * Evaluates variable ceiling heights and structural obstructions.
  * Applies custom engineering validation rules.
  * Automatically flags custom dimensions for mandatory manual human review prior to final quoting.

---

## 🛡 Architect Safeguards (VETO Rules)

The AI Assistant is governed by strict engineering safety constraints. If a client requirement violates any of the following rules, the assistant triggers an automated engineering flag and halts configuration:

1. **The 5cm Air Gap Rule:** A minimum 5 cm ventilation gap is strictly required on all wall-facing sides. Flush mounting against exterior walls is forbidden.
2. **Door Clearance Radius:** Requires a minimum **100 cm outward swing clearance** in front of the sauna door.
3. **Attic Roof Slope (*Kniestock*) Clearance:** 
   * Sauna heaters must be situated under ceiling heights of at least **200 cm**.
   * Any space with a ceiling height under **100 cm** is classified as a forbidden installation zone.
4. **Heater-to-Glass Safety Margin:** Minimum **15 cm clearance** required between any heater unit and structural glass panels.

---

## 🔄 System Architecture & Automation Pipeline

The intake suite connects conversational frontend interfaces directly into back-office business operations via **Make.com**:

```text
┌─────────────────────────┐
│ Client Interaction      │
│ (Custom GPT / API)      │
└────────────┬────────────┘
             │
             ▼ (Phase 6: Action Execution)
┌─────────────────────────┐
│ Make.com Webhook        │
└────────────┬────────────┘
             │
             ├──────────────────────────────────────┐
             ▼                                      ▼
┌─────────────────────────┐            ┌─────────────────────────┐
│ Google Sheets (CRM DB)  │            │ Cal.com Scheduling URL  │
│ Logs Config Payload     │            │ Dynamic Pre-fill Link   │
└─────────────────────────┘            └────────────┬────────────┘
                                                    │
                                                    ▼
                                       ┌─────────────────────────┐
                                       │ Consultation Booked     │
                                       │ Updates Row Status      │
                                       └─────────────────────────┘
```

---

## 📁 Repository Structure

```
reinbold-saunabau-docs/
├── _config.yml              # Jekyll configuration (Just the Docs theme & Dark Mode)
├── index.md                 # Homepage & Getting Started Guide (nav_order: 1)
├── Privacy_Policy.md        # Public Privacy Policy for GPT Actions (nav_order: 5)
├── README.md                # Main repository manual (This file)
└── docs/
    ├── overview.md          # Detailed Architecture & VETO Safeguards (nav_order: 2)
    ├── api-spec.md          # OpenAPI 3.0 / JSON Handoff Specification (nav_order: 3)
    └── make-integration.md  # Make.com & Cal.com Webhook Integration Guide (nav_order: 4)
```

---

## 🚀 Deployment & GitHub Pages Configuration

```
title: AI Assistant Suite 
description: Technical Guides, Client Onboarding & Compliance for AI Configurator & Spatial Planning.
remote_theme: just-the-docs/just-the-docs

# Enable native left-sidebar search
search_enabled: true

# Lock global display to Dark Mode
color_scheme: dark
```

---

## 📄 Data Handoff Payload Schema

```
{
  "client_info": {
    "full_name": "Jane Doe",
    "email": "jane.doe@example.com"
  },
  "room_specifications": {
    "scenario_type": "Configurator",
    "width_cm": 220,
    "depth_cm": 200,
    "height_cm": 210,
    "attic_slope": false
  },
  "sauna_preferences": {
    "wood_type": "57mm Solid Wood Standard",
    "heater_type": "Bio-Combi",
    "glass_elements": true
  },
  "verification": {
    "site_inspection_required": true,
    "disclaimer": "Maße sind bauseits zu prüfen"
  }
}
```

---

## 🔒 Privacy & Compliance

To comply with OpenAI Action requirements and European data privacy guidelines (GDPR), the endpoint privacy policy is exposed at:

https://dwayne-dcosta.github.io/reinbold-saunabau-docs/privacy/

No personally identifiable information (PII) processed by the AI Assistant is retained within the model's chat history after session execution. All client details are forwarded immediately to secure backend storage.

---

## 🛠 Maintainer

AI Solutions Architecture & Integration: Dwayne D'costa

Client: Reinbold Saunabau

Repository: dwayne-dcosta/reinbold-saunabau-docs
