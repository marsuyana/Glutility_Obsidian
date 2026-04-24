
---

## Core architecture pages

- [[Platform overview]]
    
- [[Scanner architecture]]
    
- [[Scanner system diagram]]
    
- [[Scanner data sources]]
    
- [[Scanner risk scoring system]]
    

---

## Project objective

The goal of the Glutility platform is to reduce accidental gluten exposure by analysing:

- packaged food products
    
- restaurant environments
    
- ingredient compositions
    
- contamination environments
    
- personal exposure history
    

The system combines biomedical knowledge with real-world food data to generate safety evaluations for users.

---

## System architecture overview

The platform is organised into several layers.

Each layer has a distinct role within the system.

---

## System layers

### Biomedical knowledge layer

Defines how gluten affects the human body and enables medically grounded interpretation of exposure.

### Data infrastructure layer

Handles ingestion, storage, and structuring of product, ingredient, and environmental data.

### Scanner intelligence layer

Processes inputs and evaluates gluten risk using multiple analytical models.

### User interaction layer

Delivers results, explanations, and recommendations to the user.

### Learning & feedback layer

Improves system accuracy over time through user data and real-world validation.
--- 

# Biomedical knowledge layer

The biomedical ontology defines how gluten exposure affects individuals with coeliac disease.

Key ontology pages include:

- [[Gluten]]
- [[Gliadin]]
- [[Coeliac disease]]
- [[Zonulin]]
- [[Tight junctions]]
- [[Intestinal permeability]]
- [[Cytokines]]
- [[Gut microbiome]]

These pages form a structured biomedical knowledge graph inside Obsidian.

The knowledge graph allows the system to connect biological mechanisms with food exposure scenarios.

---

# Gluten exposure model

The page [[Gluten exposure model]] links biomedical knowledge with the scanner logic.

It connects:

• gluten biology  
• immune response mechanisms  
• contamination pathways  
• platform evaluation systems

This page acts as the conceptual bridge between science and software.

---

# Scanner intelligence layer

The scanner evaluates food safety using three core systems.

### Ingredient risk engine

The [[Ingredient risk engine]] analyses ingredients found in food products.

It classifies ingredients into categories such as:

• gluten containing  
• gluten free  
• conditional risk  

Examples of high-risk ingredients include:

• wheat  
• barley  
• rye  
• malt  

---

### Cross-contamination model

The [[Cross-contamination model]] evaluates environmental contamination risks.

Examples include:

• shared fryers  
• shared utensils  
• flour dust environments  
• manufacturing line contamination  

This model captures real-world exposure scenarios that are not visible in ingredient lists.

---

### Scanner risk scoring system

The [[Scanner risk scoring system]] integrates information from multiple sources and produces a safety classification.

Possible outputs:

• SAFE  
• PROCEED WITH CAUTION  
• HIGH RISK  
• UNKNOWN  

The scoring logic also considers data reliability and confidence levels.

---

# Data infrastructure layer

The scanner relies on structured information sources.

These are documented in:

[[Scanner data sources]]

Key data inputs include:

### Product data

• barcode databases  
• ingredient lists  
• allergen declarations  
• manufacturer information  

### Ingredient knowledge

• regulatory definitions  
• gluten containing grains  
• ingredient terminology  

### Contamination intelligence

• restaurant preparation environments  
• manufacturing processes  
• food safety research  

### Restaurant safety information

• self-reported safety practices  
• gluten-free certification programmes  
• community reports  

### User-generated intelligence

Users may contribute:

• product corrections  
• contamination warnings  
• restaurant reports  

This information helps improve scanner accuracy.

---

# Platform systems

The platform includes several modules.

Core systems:

- [[Product database]]
- [[Ingredient risk engine]]
- [[Cross-contamination model]]
- [[Restaurant safety database]]
- [[Exposure tracking]]
- [[Scanner risk scoring system]]

These systems together form the evaluation pipeline.

---

# Scanner evaluation pipeline


The resulting evaluation informs the user whether a food product or environment is safe.


---

# Knowledge graph structure

The Obsidian vault functions as a structured biomedical and platform knowledge graph.

It contains two major domains:

### Biomedical ontology

Describes biological mechanisms and disease pathways.

### Platform architecture

Describes scanner logic, data sources, and evaluation systems.

Separating these layers allows scientific knowledge to evolve independently from the software implementation.

---

# Current development status

The following components are already implemented in the knowledge system:

Biomedical ontology pages  
Gluten exposure model  
Ingredient risk engine  
Cross-contamination model  
Scanner risk scoring system  
Scanner system diagram  
Scanner data sources  
Product database structure  
Restaurant safety database structure  
Exposure tracking module  

This forms the foundational architecture of the platform.

---

# Future modules

The architecture supports additional modules such as:

• recipe safety analysis  
• restaurant safety intelligence  
• personalised exposure tracking  
• dietary recommendation systems  

These modules will reuse the same knowledge and data layers.

---

# Strategic importance of the architecture

This architecture enables the platform to:

• integrate biomedical knowledge with food data  
• evaluate real-world contamination risks  
• scale across global food databases  
• support multiple platform modules  

The scanner therefore acts as the core intelligence layer of the Glutility ecosystem.

---

# Next development priorities

Immediate priorities include:

• implementing the scanner evaluation algorithm  
• integrating product barcode databases  
• expanding ingredient classification datasets  
• developing restaurant safety intelligence  

These steps will allow the first functional scanner prototype to be built.

---

# Summary

The Glutility platform combines biomedical knowledge, structured food data, and risk modelling to create a gluten exposure intelligence system.

The current knowledge vault already defines the architecture required to build the scanner and future platform modules.

