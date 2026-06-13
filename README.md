# CSTUserRank — Paper Implementation

## Paper
**"Exploring the Role of Sentiment Analysis with Network and Temporal 
Features for Finding Influential Users in Social Media Platforms"**  
Ishfaq et al. (2024) — Social Network Analysis and Mining

---

## What is this?
This is a Python implementation of the **CSTUserRank** model as part of 
a university course project.

CSTUserRank ranks influential users in social networks by combining:
-  **Network Centralities** — Degree, Closeness, Betweenness, PageRank, Katz, EVC
-  **Sentiment Analysis** — using VADER on user posts and comments
-  **Temporal Weighting** — Simple Exponential Smoothing (β = 0.51)
-  **MCDM + Entropy + TOPSIS** — for final ranking

---


##  Dataset
**Music Community Weblog** from MetaFilter dataset
- 300 most active users
- Directed graph: Commenter → Post Author
- Time span: 2006–2017

---

##  Pipeline
Input Data

↓

Graph Construction (Directed)

↓

6 Classical Centralities (DC, CC, BC, PR, Katz, EVC)

↓

Sentiment Analysis (VADER)

↓

Temporal Weighting (Exponential Smoothing)

↓

8-dimensional MCDM Matrix

↓

Normalization → Entropy Weighting → TOPSIS

↓

Final User Rankings

↓

Evaluation (SIR, Jaccard, Spearman, Ablation)
---

##  Key Results
- CSTUserRank achieves **higher infection rate** in SIR simulation
- **Fewer rank ties** compared to baseline centrality methods
- Spearman correlation shows **distinct ranking** from single-criterion methods

---

##  Technologies Used
- Python 3.x
- NetworkX — graph construction & centralities
- VADER — sentiment analysis
- NumPy / Pandas — data processing
- Matplotlib / Seaborn — visualization
- Scikit-learn — normalization

---

##  Reference
> U. Ishfaq, H. U. Khan, and D. Shabbir,
> *"Exploring the role of sentiment analysis with network and temporal 
> features for finding influential users in social media platforms,"*
> Social Network Analysis and Mining, vol. 15, no. 1, p. 14, 2025.

---

##  Implemented by
**Kimia Malekizadeh**  
University of Science and Culture  
Supervisor: Dr. Baharifard  
June 2026
