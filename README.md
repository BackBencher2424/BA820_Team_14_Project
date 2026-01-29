## Code Trends, Quantified: Mapping the Programming Language Ecosystem
**BA820: Unsupervised Machine Learning | Team 14**

---

##  Project Motivation: The Architecture of Human-Computer Interaction
Programming languages are the intersection of human logic and industrial demand. With over 4,000 languages in existence, the ecosystem is too vast for manual categorization. This project applies Unsupervised Machine Learning to discover hidden structures—evolutionary lineages, technical similarity clusters, and the "hype-utility" gap—that define the modern programming landscape. 

By analyzing the "Long Tail" of data, we move beyond simple popularity ranks to provide actionable insights for EdTech curriculum development, career ROI assessment, and technical risk management for CTOs.

[Image of a network graph of programming language relationships]

---

##  The Data
The project utilizes a rich metadata repository of over 4,000 programming languages sourced from the PLDB.
* **Scope:** 49 features including syntax metadata, community metrics, and economic indicators.
* **Structured Indicators:** Features include file extensions, comment styles, case sensitivity, GitHub stars, Wikipedia views, and job postings.
* **Why this data?** Unlike traditional datasets that focus on a few "superstar" languages, this dataset represents the entire ecosystem as abstract, measurable concepts, allowing us to analyze the "long tail" of the industry.

---

##  Why Unsupervised Learning?
The programming language market lacks pre-defined labels for "Market Archetypes" or "Structural Families." We use unsupervised methods to let the data reveal its own latent structure, which is essential for:
1.  **Discovery:** Finding "Hidden Families" without the bias of popularity.
2.  **Anomaly Detection:** Identifying "Ghost Languages" that defy typical market correlations.
3.  **Dimensionality Reduction:** Simplifying 49 variables into core "Success Pillars" that drive language longevity.

[Image of K-Means clustering algorithm partitioning data points]

---

##  Research Questions

### 1. The "Blue Ocean" Market Discovery (Clustering)
* **Question:** Do programming languages naturally cluster into distinct "Hidden Families" based on shared technical features (syntax, file types) and community signals?
* **Motivation:** EDA showed that GitHub stars and job counts are extremely right-skewed. We want to see if the "Long Tail" of overlooked languages shares structural DNA with successful ones.
* **Decision Impact:** Helps EdTech companies identify niche markets to develop specialized curricula, moving away from saturated spaces like Python/Java.
* **Surprise:** If legacy languages (pre-1980) cluster with modern cloud-native languages based on engagement patterns.

### 2. The "Hype vs. Utility" Strategy (Clustering)
* **Question:** Can we segment the market into distinct "Market Archetypes"—specifically "Social Darlings" (high hype, low jobs) vs. "Silent Giants" (low hype, high infrastructure)?
* **Motivation:** Scatter plots reveal a massive disconnect where high "stargazing" does not translate to employment.
* **Decision Impact:** Acts as a risk-assessment tool for CTOs to distinguish between "fads" and "stable tools" before committing to a tech stack migration.
* **Surprise:** If corporate-backed languages generate significantly more social "noise" than actual industrial deployment compared to grassroots languages.

### 3. The "Ghost Language" Phenomenon (Anomaly Detection)
* **Question:** Can we mathematically isolate "Ghost Languages"—technologies with high "Social Presence" (Wikipedia) but near-zero "Economic Infrastructure" (Jobs)?
* **Motivation:** The median for `number_of_jobs` is 0, yet the `language_rank` varies widely. This "all talk, no walk" imbalance is a clear statistical anomaly.
* **Decision Impact:** Protects students and professionals from investing time in "Academic Icons" that have failed to cross over into the industry.
* **Surprise:** Finding a language in the top 10% of Wikipedia views that is a total outlier with zero recorded jobs.



### 4. Structural Success Pillars (PCA)
* **Question:** Which combination of the 49 metadata features (syntax, identifiers) explains the most variance in a language's long-term survival?
* **Motivation:** The dataset is high-dimensional with many correlated features; we need to reduce this noise to find the core drivers of technical longevity.
* **Decision Impact:** Allows language designers to understand which technical specs are most associated with a language surviving its first decade.
* **Surprise:** If "Metadata Completeness" (having a domain name) explains more variance than actual syntax features.



---

##  Planned Analysis
* **Preprocessing:** Log-transforming skewed community metrics and handling high-missingness technical columns.
* **Clustering:** Applying **K-Means** and **Hierarchical Clustering** to define market segments and technical lineages.
* **Anomaly Detection:** Utilizing **Isolation Forests** or **DBSCAN** to detect the "Ghost Language" phenomenon.
* **Dimensionality Reduction:** Using **Principal Component Analysis (PCA)** to simplify the feature space and identify core variance.

---

## 📂 Repository Structure
* `data/`: Raw and processed versions of the PLDB dataset.
* `notebooks/`: 
    * `EDA_Primary_Dataset.ipynb`: Comprehensive exploratory analysis and visualizations.
    * `Modeling_Final.ipynb`: Implementation of clustering and anomaly detection logic.
* `reports/`: Documentation for project milestones and the final proposal.
