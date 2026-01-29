## Code Trends, Quantified: Mapping the Programming Language Ecosystem

**BA820: Unsupervised Machine Learning | Team 14**

---

###  Project Motivation:
As Business Analytics students, we work with Python daily but realized we were only seeing a fraction of the full programming landscape. This project emerged from wanting to look beyond the hype, by using data analysis to understand the actual ecosystem rather than just the noise. We're mapping the scale of languages that exist, from historical systems to modern releases, and using that data to separate genuine industry impact from marketing noise. 
The goal is straightforward: to identify which languages actually matter and spot emerging trends worth paying attention to. Major stakeholders would be Chief Technology Offiers(CTOs), Product Managers, School Educators, Mentors and Students.

---

###  The Data
This project utilizes a comprehensive metadata repository of over **4,000 programming languages**. This dataset is unique because it treats mathematical notations, ancient numeral systems, and modern syntax as a single continuous lineage of human logic.

#### Data Structure & Composition
* **Scope:** 4,303 entries with 49 technical, community, and economic features.
* **Feature Categories:** * **Technical:** Syntax patterns (assignment operators, comment tokens), file types, and case sensitivity.
    * **Social:** GitHub stars, forks, Wikipedia daily views, and language rank.
    * **Economic:** Job postings (where HTTP and SQL currently lead) and estimated user populations.
      
---

###  Research Questions

#### 1. The Market Discovery
* **Focus:**  Do programming languages naturally cluster into distinct groups based on shared technical features (syntax patterns, file types) and community signals (GitHub activity, Wikipedia view)

#### 2. Economic Strategy
* **Focus** Can we segment programming languages into distinct "Market Archetypes": specifically "Hype Driven" (high GitHub stars/subscribers, low job counts) vs. "Silent" (low social hype, high job counts and user estimates)

#### 3. Risk Mitigation
* **Focus:** Can we detect "Ghost Languages" technologies with significant cultural visibility (high Wikipedia views and rankings) but virtually no real employment ecosystem?

#### 4. Success Pillars Optimization
* **Focus:** Among the 49 technical metadata features we have (syntax patterns, file types, naming conventions), which ones actually predict how long a language survives and remains relevant in the long run?

---

###  Planned Analysis
* **Preprocessing:** Log-transforming skewed community metrics and handling high-missingness technical columns.
* **Clustering:** Applying **K-Means** and **Hierarchical Clustering** to define market segments and technical lineages.
* **Dimensionality Reduction:** Using **Principal Component Analysis (PCA)** to simplify the feature space and identify core variance.

---

###  Repository Structure
* `data/`: Raw and processed versions of the PLDB dataset.
* `notebooks/`: 
    * `EDA_Primary_Dataset.ipynb`: Comprehensive exploratory analysis and visualizations.
* `reports/`: Documentation for project milestones and the final proposal.


------

## Backup Project: Decoding Bob Ross Paintings

**BA820: Unsupervised Machine Learning | Team 14**

---

###  Project Motivation
Bob Ross's *The Joy of Painting* is an unusual phenomenon representing the confluence of art, education, and visual consistency on a large scale. While his paintings appear uniform in style at first glance, the series contains significant variation in color usage, composition, and subject matter. Because this dataset represents paintings as abstract concepts (binary indicators for colors and elements) rather than raw pixels, it creates a unique opportunity to analyze artistic patterns at scale.

From a business perspective, discovering the latent structure in this data can revolutionize content organization for media archives and art education platforms. Identifying visual templates and "styles" enables:
* **Recommendation Systems:** Suggesting episodes based on preferred visual "moods."
* **Curriculum Design:** Organizing art education tracks by composition complexity.
* **Thematic Curation:** Creating structured archives for streaming or digital galleries.

---

###  Preliminary EDA Insights
Our initial analysis of the painting metadata revealed several key structural patterns:

1. **Palette Skewness:** The distribution of `num_colors` is highly skewed. While most paintings rely on a consistent core set, a "long tail" of paintings uses much richer, complex sets of colors.
2. **Co-occurrence Bundles:** Landscape elements (trees, mountains, water) are not randomly placed; they tend to co-occur in repeatable "composition bundles" or templates.
3. **Composition Density:** There is a significant range in complexity—some paintings are sparse while others are dense with elements—suggesting a deliberate stylistic choice across the series.
4. **Non-Linear Evolution:** Using the `chronological_order` variable, we found that while combinations change, there is no simple linear trend in palette size, implying style evolves in waves throughout the series.

---

###  Research Questions

#### 1. Style Discovery (The "Palette vs. Subject" Type)
* **Focus:** Do paintings cluster more effectively based on their **color palette structure** or the specific **landscape elements** depicted? 

#### 2. Structural Evolution (The "Composition vs. Matter" Type)
* **Focus:** Do paintings at different points in the chronological order differ more in **composition structure** (density/complexity) than in their actual **subject matter**?.

#### 3. Contrast Analysis (The "Light vs. Dark" Type)
* **Focus:** Are there distinct painting clusters defined solely by **contrast intensity** (light vs. dark color mixes), independent of the season or year?

#### 4. Template Identification (The "Element Bundle" Type)
* **Focus:** Are there recurring **"element bundles"** that appear together far more often than expected given their individual frequencies?

---

###  Repository Structure
* `data/`: Raw binary indicators for colors and landscape elements.
* `notebooks/`: 
    * `EDA_Backup_Dataset.ipynb`: Exploratory analysis of artistic features.
* `reports/`: Proposal documentation and project synthesis.
