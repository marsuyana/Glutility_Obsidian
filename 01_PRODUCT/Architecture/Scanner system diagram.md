
This page provides a high-level visual and structural overview of the Gluten Exposure Scanner within the Glutility platform.

The scanner evaluates food safety for individuals with coeliac disease by analysing ingredient composition, contamination risk, and preparation environments.

---

## Scanner decision pipeline

User action  
↓  
Barcode scan / food entry  
↓  
[[Product database]]  
↓  
[[Ingredient risk engine]]  
↓  
[[Cross-contamination model]]  
↓  
[[Scanner risk scoring system]]  
↓  
Safety classification

- SAFE
    
- PROCEED WITH CAUTION
    
- HIGH RISK
    
- UNKNOWN
    

↓  
[[Exposure tracking]]

---

## Detailed system architecture

### Input layer

The scanner ingests:

- product data (barcode, ingredients, labels)
    
- restaurant data (menus, preparation practices, environment)
    
- ingredient-level knowledge
    
- contamination signals
    
- user-specific profiles
    

---

### Processing pipeline (internal logic)

The system processes inputs through:

1. data normalisation
    
2. ingredient risk analysis
    
3. cross-contamination modelling
    
4. biomedical interpretation
    
5. risk scoring
    

---

### Biomedical integration layer

The scanner connects to the ontology system:

- [[Gluten]]
    
- [[Gliadin]]
    
- [[Zonulin]]
    
- [[Tight junctions]]
    
- [[Intestinal permeability]]
    
- [[Cytokines]]
    
- [[Gut microbiome]]
    

This enables mapping:

→ exposure → mechanism → clinical impact

---

### Risk evaluation dimensions

The system evaluates:

- ingredient certainty
    
- contamination probability
    
- processing risk
    
- data reliability
    
- user sensitivity
    

---

### Output structure

The scanner produces:

- safety classification
    
- explanation of risk
    
- flagged ingredients
    
- confidence level
    

---

## Data sources powering the system

The scanner integrates multiple information layers through [[Scanner data sources]]:

- packaged food product databases
    
- ingredient classification datasets
    
- gluten-free certification registries
    
- restaurant safety databases
    
- regulatory allergen disclosures
    
- user-generated safety reports
    

---

## Ontology connections

The scanner logic is informed by the biological mechanisms described in:

[[Gluten exposure model]]

Which links to:

- [[Gluten]]
    
- [[Coeliac disease]]
    
- [[Zonulin]]
    
- [[Tight junctions]]
    
- [[Intestinal permeability]]
    
- [[Cytokines]]
    
- [[Gut microbiome]]
    

---

## Platform components

The scanner system interacts with several platform modules:

- [[Product database]]
    
- [[Ingredient risk engine]]
    
- [[Cross-contamination model]]
    
- [[Restaurant safety database]]
    
- [[Scanner risk scoring system]]
    
- [[Exposure tracking]]
    
- [[Scanner monetisation model]]
    

---
## Purpose of this page

This page serves as the architectural overview of the scanner system, showing how data sources, biological knowledge, and algorithmic risk models interact to produce a safety decision for users living with coeliac disease.