---
layout: default
title: API Specification
nav_order: 3
---

# OpenAPI Payload Specification

This document provides the structural specification for the `submitConfiguration` tool called during Phase 6 of the assistant intake workflow.

---

## 📄 JSON Data Schema (`Data_Handoff_Payload`)

```json
{
  "client_info": {
    "full_name": "String (Required)",
    "email": "String (Required, Valid Email Format)"
  },
  "room_specifications": {
    "scenario_type": "Configurator | Spatial Planning",
    "width_cm": "Number",
    "depth_cm": "Number",
    "height_cm": "Number",
    "attic_slope": "Boolean"
  },
  "sauna_preferences": {
    "wood_type": "57mm Solid Wood Standard | Custom",
    "heater_type": "Electric | Bio-Combi",
    "glass_elements": "Boolean"
  },
  "verification": {
    "site_inspection_required": true,
    "disclaimer": "Maße sind bauseits zu prüfen"
  }
}
