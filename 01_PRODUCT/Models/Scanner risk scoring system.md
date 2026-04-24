This page serves as a working design layer for the Glutility Gluten Exposure Scanner.

It consolidates system logic, workflows, and early-stage modelling before and alongside integration into the core architecture pages.

It acts as a bridge between concept development and formal system architecture.



Main architecture pages:

- [[Scanner architecture]]
    
- [[Product database]]
    
- [[Ingredient risk engine]]
    
- [[Cross-contamination model]]
    
- [[Restaurant safety database]]
    
- [[Exposure tracking]]
    

---

# Language standards

All documentation should follow **British English spelling**.

Examples:

- [[Coeliac disease]]
    
- fibre
    
- flavour
    
- organisation
    
- programme
    
- analyse
    

However, the American spelling **celiac** should remain searchable using page aliases.

Example:

[[Coeliac disease]]

Aliases:

- Celiac disease
    
- Celiac
    

---

# Platform objective

The platform helps individuals with [[Coeliac disease]] avoid exposure to [[Gluten]] by analysing:

- packaged food products
    
- restaurant environments
    
- contamination risks
    
- personal exposure events
    

The scanner integrates several systems:

- [[Ingredient risk engine]]
    
- [[Cross-contamination model]]
    
- [[Restaurant safety database]]
    
- [[Product database]]
    
- [[Exposure tracking]]
    

Together these systems form the **Gluten Exposure Scanner platform** used by Glutility.

---

# Scanner workflow (concept)

Example workflow when scanning a product:

1. User scans a product barcode
    
2. The scanner retrieves a record from the [[Product database]]
    
3. Ingredients are analysed using the [[Ingredient risk engine]]
    
4. Contamination signals are evaluated via the [[Cross-contamination model]]
    
5. Certification and allergen data are reviewed
    
6. A safety classification is returned
    

Possible scanner results:

- SAFE
    
- CAUTION
    
- HIGH RISK
    
- UNKNOWN
    

---

# Restaurant workflow (concept)

When evaluating a restaurant:

1. Restaurant profile retrieved from [[Restaurant safety database]]
    
2. Kitchen practices evaluated
    
3. Contamination risk assessed
    
4. Community reports considered
    
5. Safety classification returned
    

Possible results:

- SAFE
    
- CAUTION
    
- HIGH RISK
    
- UNKNOWN
    

---

# Future development ideas

Potential future features for the scanner platform:

- travel safety maps for gluten-free dining
    
- real-time restaurant safety alerts
    
- personal gluten exposure analytics
    
- symptom correlation with exposure events
    
- integration with wearable health tracking
    
- AI-assisted ingredient interpretation
    

These concepts will later be moved into the relevant architecture pages.

---

# Research opportunities

Exposure tracking may also generate useful research insights for understanding [[Coeliac disease]].

Possible research questions:

- common contamination environments
    
- symptom patterns following exposure
    
- regional differences in gluten contamination
    
- restaurant safety practices
    

This data could eventually support collaborations with clinicians and researchers studying [[Coeliac disease]].

---

# Notes and working ideas

This section can be used to capture ideas, drafts, and system concepts before moving them into the formal architecture documentation.

Examples:

- scanner algorithm improvements
    
- data partnerships
    
- regulatory considerations
    
- user interface concepts
    
- monetisation models

---
## Biological exposure model

The scanner's risk scoring logic is informed by the [[Gluten exposure model]], which describes how exposure to [[Gluten]] affects individuals with [[Coeliac disease]].

This model explains how gluten-containing ingredients and contamination pathways may trigger immune responses involving:

- [[Gliadin]]
- [[Intestinal permeability]]
- [[Zonulin]]
- [[T-cell activation]]
- [[IgA immune response]]

Understanding these mechanisms helps guide how the scanner evaluates ingredient risks and contamination scenarios when assigning safety classifications.

---
# Risk classification levels

The scanner returns one of four safety classifications.

## SAFE

The product or environment shows no credible evidence of gluten exposure.

Typical conditions:

- no [[Gluten]] containing ingredients
- no contamination warnings
- certified gluten-free product
- dedicated gluten-free preparation environment

---

## CAUTION

The product or environment may present indirect contamination risks.

Examples include:

- [[Oats]] with uncertain certification
- shared manufacturing facilities
- incomplete ingredient information
- ambiguous ingredients

These situations require caution for individuals with [[Coeliac disease]].

---

## HIGH RISK

The product or environment contains clear gluten exposure hazards.

Examples include:

- [[Wheat]]
- [[Barley]]
- [[Rye]]
- malt ingredients
- shared fryers
- flour dust environments

These items are unsafe for individuals with [[Coeliac disease]].

---

## UNKNOWN

The scanner cannot determine safety due to missing or unreliable data.

Possible causes:

- missing ingredient list
- unverified product database entry
- conflicting information sources
- unknown contamination conditions

Users should treat UNKNOWN classifications cautiously.

---

# Ingredient risk contribution

Ingredient-level analysis is performed by the [[Ingredient risk engine]].

Examples of ingredient triggers include:

High risk ingredients:

- [[Wheat]]
- [[Barley]]
- [[Rye]]
- [[Spelt]]
- [[Durum]]
- [[Semolina]]
- [[Kamut]]
- [[Triticale]]

Conditional ingredients:

- [[Oats]]
- modified starch
- flavouring
- malt derivatives

The ingredient engine assigns a base risk level.

---

# Contamination risk contribution

Environmental contamination is evaluated by the [[Cross-contamination model]].

Examples include:

- shared manufacturing facilities
- shared production lines
- restaurant kitchens
- shared fryers
- flour dust environments
- transport contamination
- shared utensils

Each contamination signal contributes to the overall exposure risk.

---

# Certification adjustment

Products that are certified gluten-free may receive an increased safety confidence.

However certification does not override clear ingredient risks.

For example:

A product containing [[Wheat]] cannot be classified as SAFE even if mislabelled.

---

# Data confidence weighting

Each product entry in the [[Product database]] has a confidence level depending on its data source.

Examples include:

- manufacturer label
- manufacturer website
- regulatory database
- user-submitted information

Higher confidence sources carry greater weight in the final risk score.

---

# Final scoring concept

The scanner combines several signals:

Ingredient risk  
+ contamination risk  
+ certification status  
+ data confidence  

This produces the final classification:

SAFE  
CAUTION  
HIGH RISK  
UNKNOWN

## Scientific Basis
This scoring logic is informed by [[Gluten exposure model]].