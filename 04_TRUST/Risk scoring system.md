
This module combines multiple risk signals into a final safety classification.

---

## Inputs

The system receives inputs from:

- [[Ingredient risk engine]]  
- [[Cross-contamination model]]  
- certification data  
- data confidence signals  

---

## Core logic

The scoring process follows these steps:

1. Assign base risk from ingredient analysis  
2. Adjust risk based on contamination signals  
3. Modify confidence using certification data  
4. Apply data confidence weighting  
5. Generate final classification  

---

## Classification rules (simplified)

- confirmed gluten ingredients → HIGH RISK  
- ambiguous ingredients or contamination → CAUTION  
- no risk signals + strong data → SAFE  
- insufficient data → UNKNOWN  

---

## Design principles

- conservative in uncertain scenarios  
- prioritises user safety  
- explainable outputs  
- consistent across contexts  

---

## Future development

- probabilistic risk modelling  
- personalised sensitivity adjustments  
- integration with exposure tracking  