---
layout: default
title: System Architecture
nav_order: 2
---


# System Architecture & Overview

This document outlines the operational logic and architectural safeguards governing the **Reinbold Saunabau Custom AI Assistant Suite**.

---

## 🏗 System Architecture

The AI Suite is built on a two-tier operational framework designed to automate client intake while maintaining strict engineering safety standards.

### 1. The Configurator Engine
* **Target Rooms:** Standard rectangular or square spaces.
* **Logic:** Automatically calculates structural air gaps (subtracting 10cm total width/depth) and matches user constraints against standard 57mm solid wood catalog models.

### 2. Spatial Planning Engine
* **Target Rooms:** Complex architecture involving attic roof slopes (*Kniestock*), niches, or wellness suites.
* **Logic:** Applies individual engineering evaluation rules and flags custom dimensioning for human engineering review.

---

## 🛡 Non-Negotiable Architect Safeguards (VETO Rules)

1. **The 5cm Air Gap Rule:** Minimum 5cm ventilation gap required on all sides. Flush wall mounting is strictly forbidden.
2. **Door Clear Radius:** Requires a minimum 100cm outward door swing clearance.
3. **Attic Clearance:** Sauna heater must be located at peak height (min. 200cm). Any zone under 100cm ceiling height is classified as a forbidden zone.
4. **Glass Clearance:** Minimum 15cm distance required between heater unit and structural glass panels.
