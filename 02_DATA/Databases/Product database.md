The Product Database stores the product-level information required for barcode-based [[Gluten]] exposure assessment.

When a user scans a product barcode, the scanner retrieves a product record from the database and evaluates the product using the [[Ingredient risk engine]] and the [[Cross-contamination model]].

This database is one of the core components of the scanner architecture and supports product safety analysis for individuals with [[Coeliac disease]].

---

# Purpose of the product database

The Product Database allows the platform to identify and evaluate packaged food products.

Its main purposes are:

- barcode recognition
- product identification
- ingredient retrieval
- allergen assessment
- gluten exposure analysis
- contamination risk interpretation

This system supports the first stage of the scanner workflow.

---

# Core product record

Each product should have a structured record.

A product record may include:

- barcode
- product name
- brand
- product category
- ingredient list
- allergen statement
- gluten-free claim
- certification status
- oats present
- manufacturer
- country
- language of label
- contamination warnings
- source of data
- last verification date

These fields allow the scanner to analyze both direct ingredients and contamination risks.

---

# Barcode field

The barcode is the key identifier used by the scanner.

Examples include:

- EAN
- UPC

When a barcode is scanned, the platform uses it to retrieve the corresponding product record.

This field is essential for product lookup.

---

# Product identification

The scanner should identify the following basic product information:

- product name
- brand
- category
- package size
- market or country

This information helps users confirm that the scanned item is the correct product.

It also helps distinguish regional variations of the same brand.

---

# Ingredient list

The ingredient list is one of the most important fields in the database.

It should preserve the ingredient text as shown on the product label.

The ingredient list is then evaluated by the [[Ingredient risk engine]].

Examples of ingredient-level triggers include:

- [[Wheat]]
- [[Barley]]
- [[Rye]]
- malt extract
- modified starch
- oats

This is one of the primary inputs for product risk classification.

---

# Allergen statement

The allergen statement provides additional safety information beyond the ingredient list.

Examples include:

- contains wheat
- may contain wheat
- produced in a facility that also processes wheat
- gluten-free

This field supports contamination and allergen interpretation.

---

# Gluten-free claim

Products may contain packaging claims related to gluten status.

Examples include:

- gluten-free
- no gluten-containing ingredients
- certified gluten-free

These claims must be interpreted carefully and should not automatically override contamination data unless certification is verified.

---

# Certification status

Certification status is important for determining confidence in product safety.

Possible values may include:

- certified gluten-free
- not certified
- unknown certification status

If a product is certified gluten-free, this may affect the final risk result in combination with ingredient and contamination analysis.

---

# Oats field

Products containing oats require special handling.

Oats do not naturally contain [[Gluten]], but they are frequently affected by [[Cross-contamination]].

The database should therefore record:

- oats present
- certified gluten-free oats
- unknown oat status

This field is especially important for scanner accuracy.

---

# Contamination warnings

The database should capture manufacturer contamination warnings.

Examples include:

- may contain wheat
- produced on shared equipment
- made in a facility that processes wheat, barley, or rye

These warnings are evaluated using the [[Cross-contamination model]].

---

# Source of product data

Each product record should indicate where the data came from.

Possible sources include:

- manufacturer label
- manufacturer website
- public food database
- user-submitted data
- manual review

This allows the platform to assign confidence levels to product records.

---

# Verification and freshness

Product formulations can change over time.

Each product record should therefore store:

- last verification date
- verification source
- confidence level

This helps prevent outdated product information from being treated as current.

---

# Product evaluation workflow

When a user scans a barcode:

1. the barcode is matched to a product record
2. the ingredient list is retrieved
3. the [[Ingredient risk engine]] evaluates ingredient-level risk
4. contamination warnings are evaluated using the [[Cross-contamination model]]
5. certification and gluten-free claims are reviewed
6. a final product safety classification is returned

---

# Possible scanner classifications

The scanner may return one of the following product classifications:

- SAFE
- CAUTION
- HIGH RISK
- UNKNOWN

These classifications are based on the combined interpretation of:

- ingredients
- allergen statements
- contamination warnings
- certification status
- data confidence

---

# Role within the platform

The Product Database is the barcode lookup and product intelligence layer of the scanner system.

It works together with:

- [[Scanner architecture]]
- [[Ingredient risk engine]]
- [[Cross-contamination model]]
- [[Restaurant safety database]]
- [[Exposure tracking]]

Together these systems form the **Gluten Exposure Scanner platform** used by Glutility.