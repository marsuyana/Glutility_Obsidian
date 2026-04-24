

The Ingredient Risk Engine evaluates food ingredients for **gluten exposure risk** in individuals with coeliac disease.

It detects:

- direct gluten sources
    
- hidden gluten derivatives
    
- ambiguous ingredients that may contain gluten
    
- ingredients that require certification verification
    

The engine assigns a **risk classification** to each ingredient when evaluating scanned food products.

---

## Risk classification framework

The scanner uses four internal classifications:

- SAFE
    
- CAUTION
    
- HIGH RISK
    
- UNKNOWN
    

These classifications are used by the scanner algorithm when evaluating ingredient lists from barcode scans.

---

# Primary gluten sources

These grains **contain gluten proteins** and are unsafe for people with coeliac disease.

They trigger an automatic **HIGH RISK** classification.

- wheat → [[Gluten]]
    
- barley → [[Gluten]]
    
- rye → [[Gluten]]
    
- spelt → [[Gluten]]
    
- durum → [[Gluten]]
    
- semolina → [[Gluten]]
    
- kamut → [[Gluten]]
    
- triticale → [[Gluten]]
    

---

## Wheat family grains

Several grains are simply **varieties of wheat** and therefore contain gluten.

These include:

- spelt
    
- durum
    
- semolina
    
- kamut
    

Although labels may use these names instead of "wheat", they still contain gluten proteins.

---

# Hidden gluten ingredients

These ingredients often contain gluten but may not be obvious to consumers.

They trigger a **HIGH RISK** classification.

- barley malt
    
- malt extract
    
- malt flavoring
    
- wheat starch
    
- hydrolyzed wheat protein
    
- wheat germ
    
- wheat bran
    

Manufacturers sometimes use these derivatives in processed foods where gluten is not immediately obvious.

---

# Conditional risk ingredients

These ingredients may be safe or unsafe depending on processing methods or certification.

They trigger a **CAUTION** classification unless verified.

- oats
    
- modified starch
    
- dextrin
    
- caramel color
    
- yeast extract
    
- natural flavors
    

The scanner should prompt users to verify certification or manufacturing details.

---

# Certification override logic

Some ingredients normally considered risky may be safe when processed to remove gluten and certified under regulatory standards.

Example:

- wheat starch that has been processed and certified gluten-free (<20 ppm).
    

If a product is verified as **certified gluten-free**, the scanner may downgrade risk to SAFE.

---

# Scanner evaluation workflow

When a product barcode is scanned:

1. The ingredient list is retrieved.
    
2. Each ingredient is evaluated by the Ingredient Risk Engine.
    
3. Known gluten sources trigger HIGH RISK.
    
4. Ambiguous ingredients trigger CAUTION.
    
5. Certified gluten-free products may override certain risks.
    
6. The scanner produces a final safety result.
    

---

# Biological context

Gluten exposure can activate immune responses in genetically susceptible individuals.

Key biological mechanisms include:

- [[Gliadin]]
    
- [[IgA immune](https://chatgpt.com/c/69b7105e-ad1c-8385-ac34-8213ada29abb)]()

## Evaluation Context
Ingredient interpretation should align with [[Gluten exposure model]].