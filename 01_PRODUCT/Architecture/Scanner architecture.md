# Gluten Exposure Scanner Architecture

The scanner is the operational layer of the Glutility platform.

Its purpose is to detect gluten exposure risk in food products,
restaurants, and environments for people with coeliac disease.

## Core Components

# Scanner architecture

## Core Components

1. Product barcode scanning  
2. Ingredient risk intelligence  
3. Cross-contamination detection  
4. Restaurant safety database  
5. Personal exposure tracking  


## Scanner Workflow

scan barcode  
→ retrieve product database  
→ analyze ingredient risks  
→ evaluate cross-contamination signals  
→ compute exposure risk  
→ return safety result  


---

## Detailed scanner architecture

## Input layer

The scanner ingests multiple input types:

### 1. Product data
- barcode
- ingredient list
- allergen labels
- manufacturer information

### 2. Restaurant data
- menu items
- preparation methods
- kitchen environment
- cross-contact practices

### 3. Ingredient intelligence
- known gluten-containing substances
- derivative ingredients
- processing risks

### 4. Contamination signals
- shared equipment
- supply chain risks
- handling conditions

### 5. User-specific data
- diagnosis (coeliac / sensitivity)
- tolerance level (if applicable)
- exposure history


## Processing pipeline

The scanner processes data through multiple stages:

1. data normalisation
2. ingredient risk analysis
3. cross-contamination modelling
4. biomedical interpretation
5. risk scoring


## Output layer

The scanner produces:

### 1. Risk classification
- safe
- caution
- high risk

### 2. Risk explanation
- why the product is risky
- which mechanism triggered the risk (ingredient / contamination / environment)

### 3. Flagged elements
- specific ingredients
- preparation risks
- contamination sources

### 4. Confidence score
- high / medium / low
- based on data quality and completeness

### 5. Actionable guidance
- safe to consume / avoid / verify
- suggested precautions (if applicable)


## Downstream usage

### 1. User application
- real-time product scanning
- restaurant safety evaluation
- personalised exposure tracking

### 2. API access (B2B)
- food companies (product validation)
- restaurants (safety scoring)
- retailers (product intelligence)
- health platforms (integration)

### 3. Data products
- aggregated risk datasets
- ingredient risk intelligence
- contamination pattern insights

### 4. Certification layer (future)
- “verified safe” scoring
- partner certification programs
- compliance tools

---

## System dependencies

- [[Scanner data sources]]
- [[Scanner risk scoring system]]
- [[Platform overview]]
## Knowledge Layer
The scanner integrates scientific logic through [[Gluten exposure model]].