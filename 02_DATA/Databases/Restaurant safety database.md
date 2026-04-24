The Restaurant Safety Database evaluates restaurants and food-service environments for potential exposure to [[Gluten]].

Individuals with [[Coeliac disease]] often face significant risk when eating outside the home due to hidden [[Cross-contamination]] and limited knowledge of gluten-free food preparation in restaurant kitchens.

This system works together with the [[Ingredient risk engine]] and the [[Cross-contamination model]] to determine whether restaurant meals are safe for individuals requiring a strict gluten-free diet.

---

# Restaurant safety evaluation

Restaurants are evaluated using several safety indicators related to gluten exposure.

These include:

- gluten-free menu availability
    
- dedicated gluten-free preparation areas
    
- shared kitchen environments
    
- staff awareness of [[Coeliac disease]]
    
- contamination risks during food preparation
    
- customer safety reports
    

Each indicator contributes to the overall restaurant safety classification.

---

# Dedicated gluten-free kitchens

Restaurants with **fully dedicated gluten-free kitchens** provide the safest environment for individuals with [[Coeliac disease]].

Characteristics include:

- no [[Gluten]] present in the kitchen
    
- dedicated preparation surfaces
    
- separate cooking equipment
    
- separate food storage
    

Possible scanner classification:

SAFE

---

# Shared kitchen environments

Many restaurants operate shared kitchens where both gluten-containing and gluten-free foods are prepared.

Common contamination sources include:

- shared cooking surfaces
    
- shared cutting boards
    
- shared utensils
    
- nearby flour handling
    

These conditions may introduce [[Cross-contamination]].

Possible scanner classification:

CAUTION

---

# Shared fryers

Shared fryers are one of the most common causes of gluten exposure in restaurants.

Example:

[[French fries]] are naturally gluten-free but become unsafe when cooked in the same fryer as breaded foods containing [[Gluten]].

Possible scanner classification:

HIGH RISK

---

# Staff training and awareness

Restaurant staff knowledge plays an important role in preventing gluten exposure.

Indicators include:

- staff understanding of [[Coeliac disease]]
    
- awareness of [[Cross-contamination]]
    
- ability to explain ingredients
    
- willingness to modify dishes safely
    

Restaurants with trained staff are safer for gluten-free dining.

---

# Customer safety reports

The platform may collect reports from users regarding restaurant safety.

Reports may include:

- safe dining experiences
    
- suspected gluten exposure
    
- contamination incidents
    
- inaccurate gluten-free labeling
    

These reports contribute to restaurant safety scores.

---

# Restaurant safety scoring

The scanner may assign an overall safety classification based on multiple factors.

Example categories:

SAFE  
CAUTION  
HIGH RISK  
UNKNOWN

Safety scores may consider:

- kitchen practices
    
- contamination risks
    
- customer reports
    
- certification status
    

---

# Integration with the scanner

When a user searches for or scans a restaurant:

1. the restaurant profile is retrieved
    
2. kitchen safety conditions are evaluated
    
3. contamination risks are assessed using the [[Cross-contamination model]]
    
4. ingredient safety is evaluated using the [[Ingredient risk engine]]
    
5. a final safety classification is returned
    

---

# Biological relevance

Even trace amounts of [[Gluten]] can trigger immune activation in individuals with [[Coeliac disease]].

Relevant biological mechanisms include:

- [[Gliadin]]
    
- [[IgA immune response]]
    
- [[T-cell activation]]
    
- [[Intestinal Inflammation]]
    
- [[Villous atrophy]]
    

This is why strict avoidance of contamination is necessary when dining in restaurants.

---

# Role within the platform

The Restaurant Safety Database is a key component of the scanner architecture.

It works together with:

- [[Ingredient risk engine]]
    
- [[Cross-contamination model]]
    
- [[Product database]]
    
- [[Exposure tracking]]
    

Together these systems form the **Gluten Exposure Scanner platform** used by Glutility.