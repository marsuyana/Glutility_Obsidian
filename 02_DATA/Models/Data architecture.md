## Purpose

Define the core data structure required to support the Glutility scanner MVP.

This page describes the main entities, relationships, and data flows needed for barcode scanning, ingredient risk evaluation, contamination assessment, confidence scoring, and future exposure tracking.

This architecture should support the current MVP while remaining extensible for future product development.

---
## MVP principle

The data model should be simple enough to support the current scanner build, but structured enough to avoid rework when adding trust signals, restaurant intelligence, and user history later.

For MVP, priority is given to:

- packaged food scanning
- ingredient risk evaluation
- contamination risk evaluation
- trust / confidence signals
- user-facing scanner outputs

---

## Core entities

### Product
A packaged item scanned or searched by the user.

Core fields:
- product_id
- barcode
- product_name
- brand_name
- category
- country
- ingredients_text
- allergen_statement
- gluten_free_claim
- certification_status
- certification_type
- source_id
- confidence_level
- final_risk_output
- explanation_summary
- last_updated

---

### Ingredient
A declared ingredient or ingredient component linked to a product.

Core fields:
- ingredient_id
- ingredient_name
- canonical_name
- ingredient_type
- gluten_risk_level
- ambiguity_flag
- notes
- related_ontology_pages

---

### Certification
A recognised trust signal associated with a product.

Core fields:
- certification_id
- certification_name
- certifying_body
- region
- recognised_status
- ppm_standard_if_known
- verification_notes

---

### Contamination signal
A contamination-related factor that affects risk scoring.

Core fields:
- contamination_id
- contamination_type
- environment_type
- severity_level
- evidence_source
- notes

Examples:
- shared production line
- shared fryer
- shared toaster
- flour dust environment
- shared utensils
- dedicated gluten-free facility

---

### Source
The origin of the information used by the scanner.

Core fields:
- source_id
- source_type
- source_name
- verification_level
- date_accessed
- recency_status
- conflict_flag

Examples:
- manufacturer
- certification body
- official database
- user report
- manual review

---

### Scanner result
The final result produced for the user.

Core fields:
- result_id
- product_id
- ingredient_risk_score
- contamination_risk_score
- certification_modifier
- confidence_score
- final_output
- recommended_action
- explanation_summary
- timestamp

---

## Future entities

### Venue
A restaurant, café, bakery, or foodservice location.

Future fields:
- venue_id
- venue_name
- address
- cuisine_type
- gluten_free_claim_type
- dedicated_fryer
- staff_training_status
- protocol_status
- user_reports
- confidence_level

### Exposure event
A user-recorded gluten exposure or suspected exposure.

Future fields:
- exposure_event_id
- user_id
- source_type
- linked_product_or_venue
- date
- symptoms
- notes
- severity
- confidence

### User profile
A future personalisation layer.

Future fields:
- user_id
- condition_type
- oats_preference
- sensitivity_notes
- saved_products
- saved_venues
- exposure_history_enabled

---

## Core relationships

- A product contains multiple ingredients
- A product may have zero or more certifications
- A product may have zero or more contamination signals
- A product is linked to one or more sources
- A scanner result is generated from one product plus its linked risk signals
- Future venue results will follow a parallel structure

---

## MVP data flow

### Packaged product scan

1. User scans barcode
2. Product record is retrieved
3. Ingredients are parsed
4. Ingredient risk is evaluated
5. Certification signals are checked
6. Contamination signals are applied
7. Source confidence is evaluated
8. Final scanner result is generated
9. Output is shown to user

---

## Output layer

The MVP should support the following final outputs:

- SAFE
- LOW RISK
- CAUTION
- HIGH RISK
- AVOID
- UNKNOWN

Each result should also include:

- confidence level
- explanation
- suggested action

---

## Design rules

- One product can produce different confidence levels depending on source quality
- Certification should reduce uncertainty, not erase all risk automatically
- Contamination signals can override otherwise safe ingredient lists
- Unknown is a valid output when evidence is weak
- The data model must support future restaurant and exposure tracking layers

---

## Build note

The MVP codebase already exists and opens on mobile.

This architecture should therefore be treated as a clarification and stabilisation layer for the current build, not as a disconnected redesign.

The goal is to align Obsidian logic with implementation in VS Code and support cleaner future handoffs.