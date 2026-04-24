
The Gluten Exposure Model describes how exposure to [[Gluten]] occurs and how it can affect individuals with [[Coeliac disease]].


---

# Definition

Gluten exposure occurs when a person consumes food containing [[Gluten]] proteins or food that has been contaminated with gluten-containing grains.

These grains include:

- [[Wheat]]
    
- [[Barley]]
    
- [[Rye]]
    
- [[Spelt]]
    
- [[Durum]]
    
- [[Semolina]]
    
- [[Kamut]]
    
- [[Triticale]]
    

Exposure may occur through direct ingredients or through [[Cross-contamination]].

---

# Types of exposure

Gluten exposure can occur through several pathways.

## Direct ingredient exposure

This occurs when foods contain gluten-containing ingredients.

Examples include:

- wheat flour
    
- barley malt
    
- rye bread
    
- wheat-based pasta
    

These exposures represent the highest risk.

---

## Cross-contamination exposure

Exposure may also occur when gluten-free foods come into contact with gluten-containing foods.

Examples include:

- shared kitchen preparation surfaces
    
- shared fryers
    
- shared utensils
    
- flour dust environments
    
- shared manufacturing equipment
    

These contamination pathways are evaluated by the [[Cross-contamination model]].

---

# Exposure thresholds

Scientific and regulatory standards often define gluten-free foods as containing less than **20 parts per million (ppm)** of gluten.

However, individuals with [[Coeliac disease]] may still experience symptoms depending on:

- individual sensitivity
    
- total exposure dose
    
- repeated exposure over time
    

This makes contamination detection important even when gluten levels are low.

---

# Biological response

When gluten is consumed, proteins such as [[Gliadin]] interact with the intestinal immune system.

This may trigger:

- increased [[Intestinal permeability]]
    
- release of [[Zonulin]]
    
- activation of [[T-cell activation]]
    
- production of [[IgA immune response]]
    
- intestinal [[Inflammation]]
    

Over time this immune reaction may lead to:

- [[Villous atrophy]]
    
- nutrient malabsorption
    
- systemic symptoms
    

---

# Symptomatic and silent exposure

Some individuals experience immediate symptoms following gluten exposure.

Common symptoms include:

- abdominal pain
    
- diarrhoea
    
- fatigue
    
- brain fog
    

However, some individuals with [[Coeliac disease]] may experience **silent exposure**, where intestinal damage occurs without noticeable symptoms.

This makes exposure detection particularly important.

---

# Relevance for the scanner

The Gluten Exposure Model informs the evaluation logic used by the scanner platform.

Exposure risk is assessed through:

- [[Ingredient risk engine]]
    
- [[Cross-contamination model]]
    
- [[Scanner risk scoring system]]
    

These systems attempt to identify foods or environments that may introduce gluten exposure.

---

# Role within the vault

This model connects the biological understanding of gluten-triggered immune responses with the practical detection systems used by the Gluten Exposure Scanner platform. 

It links to:

• [[Gluten]]
• [[Coeliac disease]]
• [[Ingredient risk engine]]
• [[Cross-contamination model]]
• [[Scanner risk scoring system]]
• [[Scanner data sources]]

Together these components form the knowledge architecture behind the Glutility platform.

---
## Platform implementation

The biological exposure concepts described here inform the decision logic implemented in the [[Scanner risk scoring system]].

• [[Scanner data sources]]

## Connected Product Systems
- [[Scanner architecture]]
- [[Platform overview]]
- [[Knowledge Scanner Bridge]]
- [[Scanner inputs and outputs]]
## Core Inputs
- Ingredient lists
- Allergen declarations
- Certification status
- Manufacturing context
- Venue handling practices
- User sensitivity context
## Outputs
- Contains gluten
- Cross-contamination risk
- No gluten detected
- Certified gluten-free
- Confidence score
- User-safe explanation
- User guidance
- Recommended next action
