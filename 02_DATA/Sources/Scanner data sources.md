This page defines the external and internal information sources used by the Gluten Exposure Scanner to evaluate gluten exposure risk.

The Gluten Exposure Scanner relies on multiple data sources to evaluate the safety of food products and restaurant environments for individuals with [[Coeliac disease]].

These sources provide the raw information used by the platform’s evaluation systems.

The scanner integrates data used by:

- [[Product database]]
- [[Ingredient risk engine]]
- [[Cross-contamination model]]
- [[Restaurant safety database]]
- [[Exposure tracking]]
- [[Scanner risk scoring system]]

Together these systems form the information layer of the scanner.

---

# Product data sources

Product information is primarily obtained from packaged food labels and food databases.

Examples include:

- product barcode data
- ingredient lists
- allergen declarations
- gluten-free certification labels
- manufacturer information

Possible external sources include public food databases and manufacturer product catalogues.

---

# Ingredient knowledge sources

Ingredient risk interpretation relies on scientific and regulatory knowledge about gluten-containing ingredients.

Examples include:

- known gluten-containing grains such as [[Wheat]], [[Barley]], and [[Rye]]
- ingredient terminology used in food labelling
- food regulatory definitions
- allergen disclosure rules

This information supports the logic of the [[Ingredient risk engine]].

---

# Contamination knowledge sources

The [[Cross-contamination model]] relies on knowledge of real-world contamination environments.

Examples include:

- shared production lines
- shared manufacturing facilities
- restaurant kitchens
- shared fryers
- flour dust environments
- shared utensils

These contamination scenarios are derived from food safety practices and real-world restaurant workflows.

---

# Restaurant safety data

Restaurant safety information may be obtained from:

- restaurant self-reported safety practices
- user-submitted safety reports
- gluten-free certification programmes
- community feedback

These signals populate the [[Restaurant safety database]].

---

# User-generated data

Users may contribute data to improve the scanner ecosystem.

Examples include:

- product corrections
- restaurant safety reports
- contamination warnings
- exposure tracking logs

This information feeds into [[Exposure tracking]] and helps refine the scanner’s risk evaluation.

---

# Data reliability

Each data source has a different reliability level.

Examples:

High reliability:

- manufacturer product labels
- certified gluten-free programmes
- regulatory databases

Medium reliability:

- manufacturer websites
- restaurant declarations

Lower reliability:

- community submissions
- unverified user reports

These reliability levels influence the scoring logic described in the [[Scanner risk scoring system]].

---

# Role within the platform

The Scanner Data Sources page defines where the scanner obtains the information needed to evaluate gluten exposure risk.

This data layer supports:

- [[Product database]]
- [[Ingredient risk engine]]
- [[Cross-contamination model]]
- [[Restaurant safety database]]
- [[Exposure tracking]]

Together these systems power the Gluten Exposure Scanner platform used by Glutility.
This data layer supplies the information required by the Gluten Exposure Scanner to evaluate food safety for individuals living with coeliac (celiac) disease.