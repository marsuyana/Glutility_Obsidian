
---
## Start here (implementation focus)

This document defines the first version of the Gluten Exposure Scanner.

If you are implementing this system, focus on:

1. Product scanning flow
    
2. Ingredient risk evaluation
    
3. Basic contamination logic
    
4. Final safety classification
    

The goal is to build a working v1 quickly, then iterate.

Do not over-engineer the system at this stage.

---

## 1. Objective

The goal is to build a Gluten Exposure Scanner that helps individuals with coeliac disease avoid harmful gluten exposure in real-world conditions.

The system evaluates food safety by analysing:

- ingredients  
- contamination risk  
- preparation environments  
- data reliability  

It produces a clear safety decision for the user.

---
## 2. Design philosophy

The scanner is designed to be significantly more advanced than existing solutions.

It is not a simple ingredient checker, but a decision engine grounded in biological mechanisms, contamination modelling, and contextual risk evaluation.

The long-term vision includes:

- biologically informed risk interpretation  

- integration of multiple data layers  

- personalised exposure understanding  

- expansion beyond coeliac disease  

However, implementation will follow a staged approach:

- simple, reliable core system is built first
    
- additional sophistication is layered progressively
    

---

This ensures both speed of execution and long-term differentiation.

---
This philosophy directly informs what is included in the first version of the system.
## 3. What we are building (scope)

The first version of the system focuses on two primary use cases:

---

### A. Packaged food scanning

Core capabilities:

- barcode input  
- product lookup via [[Product database]]  
- ingredient analysis via [[Ingredient risk engine]]  
- detection of gluten-containing ingredients  
- identification of ambiguous or conditional ingredients  
- certification verification (gluten-free labels, registries)  
- evaluation of contamination signals (where available)  
- data confidence assessment  

Output:

- clear safety classification (SAFE / CAUTION / HIGH RISK / UNKNOWN)  
- supporting explanation (ingredient + contamination reasoning)  

---

### B. Restaurant safety evaluation

Core capabilities:

- restaurant profile retrieval via [[Restaurant safety database]]  
- evaluation of kitchen practices  
- detection of cross-contamination risks  
- analysis of preparation environments  
- integration of community safety reports (where available)  

Output:

- safety classification for the venue  
- contextual explanation of risk factors  

---

### Scope boundaries (v1)

The first version prioritises:

- reliable ingredient risk detection  
- clear safety classification  
- explainable results for users  

The following are not core to v1:

- full personalisation of risk thresholds  
- advanced predictive modelling  
- real-time environmental sensing  

These will be introduced in later phases.

---
## 4. Core modules

The scanner system is composed of several core modules, each responsible for a specific part of the decision process.

---

### 1. [[Product database]]

Stores structured information about packaged food products.

Responsibilities:

- barcode-to-product matching  
- ingredient list storage  
- allergen declarations  
- certification data (gluten-free labels, registries)  
- source tracking and data confidence  

---

### 2. [[Ingredient risk engine]]

Analyses ingredient lists to detect gluten-related risks.

Responsibilities:

- identification of gluten-containing ingredients  
- classification of ingredient risk levels  
- handling of ambiguous or conditional ingredients (e.g. oats, starches, flavourings)  
- mapping ingredients to gluten exposure risk  

---

### 3. [[Cross-contamination model]]

Evaluates environmental and production-related contamination risks.

Responsibilities:

- detection of shared manufacturing environments  
- evaluation of cross-contact signals  
- modelling of contamination probability in production and preparation  
- interpretation of restaurant kitchen risk factors  

---

### 4. [[Restaurant safety database]]

Stores and evaluates restaurant-specific safety information.

Responsibilities:

- restaurant profiles and metadata  
- kitchen practice indicators  
- contamination risk factors  
- user-generated safety reports  
- historical safety signals  

---

### 5. [[Risk scoring system]]

Combines multiple signals into a final safety decision.

Responsibilities:

- aggregation of ingredient risk  
- integration of contamination signals  
- incorporation of certification data  
- weighting based on data confidence  
- generation of final classification (SAFE / CAUTION / HIGH RISK / UNKNOWN)  

---

### 6. [[Exposure tracking]] (future layer)

Tracks user-specific exposure events over time.

Responsibilities:

- logging of scanned products and meals  
- tracking potential exposure events  
- linking exposure to symptoms (optional future layer)  
- enabling personalised risk insights  

This module is not required for the initial version but is part of the long-term system architecture.

---

## 5. End-to-end flow

This section describes how the scanner operates from user input to final safety decision.

---

### A. Packaged food scan flow

1. User scans product barcode  

2. System queries [[Product database]]  

3. Product data retrieved:
   - ingredient list  
   - allergen declarations  
   - certification data  
   - data source and confidence  

4. Ingredients analysed via [[Ingredient risk engine]]:
   - detection of gluten-containing ingredients  
   - identification of ambiguous ingredients  

5. Contamination signals evaluated via [[Cross-contamination model]]:
   - shared production environments  
   - cross-contact indicators  

6. Certification and labelling reviewed  

7. Signals passed to [[Risk scoring system]]  

8. Final safety classification generated:
   - SAFE  
   - CAUTION  
   - HIGH RISK  
   - UNKNOWN  

9. Result returned to user with explanation  

---

### B. Restaurant evaluation flow

1. User searches or selects restaurant  

2. System queries [[Restaurant safety database]]  

3. Restaurant data retrieved:
   - kitchen practices  
   - contamination indicators  
   - historical safety signals  
   - community reports  

4. Contamination risks evaluated via [[Cross-contamination model]]  

5. Signals passed to [[Risk scoring system]]  

6. Final safety classification generated  

7. Result returned with contextual explanation  

---

### Output characteristics

The system must always return:

- a clear safety classification  
- a short explanation of key risk factors  
- indication of data confidence (where relevant)  

The output should be understandable to non-technical users while remaining grounded in system logic.

---

## 6. Safety classification

The scanner returns one of four standardised safety classifications.

These classifications translate complex system signals into clear, actionable guidance for users.

---

### SAFE

Definition:

The product or environment shows no credible evidence of gluten exposure.

Typical conditions:

- no gluten-containing ingredients detected  
- no contamination indicators  
- certified gluten-free product or controlled environment  
- high confidence in data sources  

User guidance:

Safe for individuals with [[Coeliac disease]] under normal conditions.

---

### CAUTION

Definition:

The product or environment presents potential indirect or uncertain risks.

Typical conditions:

- ambiguous or conditional ingredients (e.g. [[Oats]], starches, flavourings)  
- shared production environments  
- incomplete or partially reliable data  
- limited certification information  

User guidance:

Proceed with caution depending on individual sensitivity and risk tolerance.

---

### HIGH RISK

Definition:

The product or environment contains clear gluten exposure hazards.

Typical conditions:

- presence of [[Wheat]], [[Barley]], [[Rye]], or derived ingredients  
- explicit gluten-containing components  
- high-risk contamination environments (e.g. shared fryers, flour exposure)  

User guidance:

Not safe for individuals with [[Coeliac disease]].

---

### UNKNOWN

Definition:

The system cannot determine safety due to insufficient or unreliable data.

Typical conditions:

- missing ingredient information  
- unverified product entry  
- conflicting data sources  
- absence of contamination data  

User guidance:

Avoid or verify through external sources before consumption.

---

### Classification principles

The classification system is designed to be:

- conservative in risk detection  
- transparent in reasoning  
- consistent across products and environments  

The system prioritises user safety over false reassurance.

---

## 7. Decision logic (high-level)

This section describes how the scanner combines multiple signals to produce a final safety classification.

The decision logic integrates:

- ingredient risk  
- contamination risk  
- certification data  
- data confidence  

---

### Step 1: Ingredient risk evaluation

The [[Ingredient risk engine]] assigns a base risk level based on detected ingredients.

Possible states:

- HIGH → gluten-containing ingredients detected (e.g. [[Wheat]], [[Barley]], [[Rye]])  
- MEDIUM → ambiguous or conditional ingredients (e.g. [[Oats]], modified starch, flavourings)  
- LOW → no gluten-related ingredients detected  

This step establishes the initial risk baseline.

---

### Step 2: Contamination risk evaluation

The [[Cross-contamination model]] evaluates environmental and production risks.

Possible signals:

- shared manufacturing environments  
- shared preparation surfaces  
- cross-contact indicators  
- restaurant kitchen practices  

Contamination risk can increase the overall risk level but cannot reduce confirmed ingredient risk.

---

### Step 3: Certification adjustment

Certification data is used to refine confidence in safety.

Examples:

- certified gluten-free → increases confidence in LOW risk  
- absence of certification → no adjustment  
- conflicting certification → reduces confidence  

Certification cannot override confirmed presence of gluten-containing ingredients.

---

### Step 4: Data confidence weighting

Each input signal is weighted based on its reliability.

Examples:

- manufacturer label → high confidence  
- official regulatory database → high confidence  
- user-generated data → variable confidence  
- incomplete data → low confidence  

Lower confidence increases the likelihood of a CAUTION or UNKNOWN classification.

---

### Step 5: Risk aggregation

All signals are combined to determine the final classification.

Core principles:

- confirmed gluten ingredients → HIGH RISK  
- ambiguous ingredients + contamination → CAUTION  
- low risk + strong certification + high confidence → SAFE  
- insufficient or conflicting data → UNKNOWN  

---

### Step 6: Final classification output

The [[Risk scoring system]] assigns one of the four classifications:

- SAFE  
- CAUTION  
- HIGH RISK  
- UNKNOWN  

Each result must include:

- classification  
- key contributing factors  
- confidence indication (where applicable)  

---

### Design principles of the decision logic

The system is designed to be:

- conservative in uncertain scenarios  
- explainable at every step  
- consistent across products and environments  
- extensible for future personalisation  

The goal is not only to classify risk, but to make the reasoning transparent to the user.

---
## 8. Role of biomedical knowledge

The scanner is not a purely data-driven system. It is informed by a structured biomedical understanding of gluten exposure and its effects on individuals with [[Coeliac disease]].

This biomedical layer provides the foundation for how risk is interpreted within the system.

---

### Biological grounding

The scanner’s logic is informed by mechanisms described in the [[Gluten exposure model]].

Key concepts include:

- [[Gluten]] and its protein components (e.g. [[Gliadin]])  
- intestinal barrier function and [[Intestinal permeability]]  
- regulation via [[Zonulin]] and [[Tight junctions]]  
- immune activation pathways (e.g. [[T-cell activation]], [[Cytokines]])  
- systemic and gastrointestinal responses  

These mechanisms explain why even small amounts of gluten exposure can trigger adverse effects.

---

### Implications for risk modelling

The biomedical model informs several system design choices:

- strict classification of gluten-containing ingredients as HIGH RISK  
- conservative handling of ambiguous ingredients  
- prioritisation of contamination risk detection  
- avoidance of false “safe” classifications in uncertain scenarios  

The system is therefore designed to minimise false negatives rather than maximise permissiveness.

---

### Connection to system components

Biomedical knowledge directly informs:

- [[Ingredient risk engine]] → ingredient classification logic  
- [[Cross-contamination model]] → interpretation of exposure pathways  
- [[Risk scoring system]] → conservative aggregation of risk signals  

---

### Role in future development

As the platform evolves, biomedical knowledge may support:

- personalised sensitivity modelling  
- correlation between exposure and symptoms  
- deeper analysis of cumulative exposure  
- extension to other immune-mediated conditions  

This ensures the system remains grounded in scientific understanding while evolving over time.

---
## 9. Implementation priorities (v1)

The initial version of the scanner should prioritise speed of execution, clarity of logic, and reliability of core functionality.

The goal is to build a working system that can be tested and iterated quickly, without overengineering.

---

### Phase 1 — Core scanner (must build first)

Focus on delivering a complete end-to-end product scanning flow.

Components:

- basic [[Product database]] (static dataset or simple API)  
- [[Ingredient risk engine]] (rule-based logic)  
- simple [[Cross-contamination model]] (deterministic rules)  
- basic [[Risk scoring system]] (clear classification logic)  

Capabilities:

- barcode → product lookup  
- ingredient parsing and classification  
- basic contamination handling  
- final safety classification output  

This phase should result in a functional scanner that produces consistent results.

---

### Phase 2 — Context improvements

Enhance the quality and reliability of risk evaluation.

Components:

- expanded product data coverage  
- improved handling of ambiguous ingredients  
- more structured contamination modelling  
- introduction of [[Restaurant safety database]]  

Capabilities:

- better classification accuracy  
- improved handling of edge cases  
- initial restaurant evaluation functionality  

---

### Phase 3 — Extensions (later)

Introduce advanced features and deeper system intelligence.

Components:

- [[Exposure tracking]]  
- more advanced [[Risk scoring system]] logic  
- improved data confidence modelling  

Capabilities:

- tracking of user exposure events  
- more nuanced classification decisions  
- improved explanation of risk  

---

### Implementation principles

- prioritise correctness over complexity  
- favour transparent, rule-based logic in early stages  
- ensure all classifications are explainable  
- avoid premature optimisation  

---

### Out of scope for v1

The following are intentionally excluded from the first version:

- multi-condition support beyond [[Coeliac disease]]  
- advanced AI or machine learning models  
- full personalisation of risk thresholds  
- real-time environmental sensing  

These may be introduced once the core system is stable and validated.

---

## 10. What we are NOT building yet

To maintain focus, the following are out of scope for v1:

- multi-condition support beyond [[Coeliac disease]]  
- full ontology integration into the user interface  
- advanced AI or machine learning models  
- real-time adaptive or learning systems  

These areas are part of the long-term vision but are not required for the initial implementation.

The system architecture is designed to support these capabilities in future iterations.

---

## 11. Strategic direction

The scanner is built on a modular architecture, allowing the system to evolve without redesigning core components.

This enables:

- expansion into additional dietary or medical conditions  
- integration of new data sources and regulatory datasets  
- development of API and SaaS-based offerings  
- collaboration with research and clinical partners  

[[Coeliac disease]] is the initial focus, not the long-term limitation.

The long-term goal is to establish a broader health-oriented risk intelligence platform built on the same core principles.

---

## 12. Summary

The Glutility scanner is designed as a decision engine that evaluates gluten exposure risk using a combination of:

- ingredient analysis  
- contamination modelling  
- certification data  
- data confidence  

It translates complex biological and environmental signals into clear, actionable guidance for users.

The first version focuses on delivering a reliable and explainable core system, while the architecture supports progressive expansion in sophistication and scope.

This approach ensures:

- immediate usability  
- technical clarity for implementation  
- long-term scalability  

The system is designed to evolve into a comprehensive platform for dietary and health-related risk evaluation, starting with [[Coeliac disease]].

---