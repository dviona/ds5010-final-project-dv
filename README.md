# Ecology Through Data: Forest Cover Type Analysis

An exploratory data analysis of 581,012 forest land parcels in Colorado's Roosevelt National Forest, investigating how elevation, soil, sunlight, and terrain shape the distribution of seven tree species across four wilderness areas.

**Course:** DS 5010 · Introduction to Programming for Data Science · Northeastern University  
**Dataset:** [Covertype](https://archive.ics.uci.edu/dataset/31/covertype) — UCI Machine Learning Repository (581,012 records, 54 features)

---

## About This Project

Most analyses of the Covertype dataset treat it as a classification benchmark — load the data, run a model, report accuracy. This project takes a different approach: it treats the dataset as an **ecological field study**, asking not just *what* patterns exist, but *why* they exist.

Every question is interpreted through the lens of forest ecology — explaining species distributions using concepts like elevational zonation, microclimate effects of slope aspect, soil-moisture relationships, and ecological niche theory. 

### Highlights

- **Ecological niche width analysis** quantifying which tree species are habitat generalists vs. specialists
- **Simpson's Diversity Index** computed per wilderness area to measure biodiversity
- **Topographic Moisture Index** engineered from slope, aspect, and hydrology distance
- **Climatic zone feature engineering** from USFS soil taxonomy codes — a mapping referenced in the UCI documentation but never implemented in existing analyses
- **Polar rose diagram** of slope aspect preferences by species
- **Radar chart fingerprints** comparing the ecological identity of four wilderness areas
- **ANOVA with Bonferroni-corrected post-hoc testing** on elevation across all seven cover types

---

## Project Structure

```
ds5010-final-project/
├── covertype_analysis.ipynb   # Main notebook — 25 questions with code, visualizations, and analysis
├── helpers.py                 # Reusable ecological classification functions (Q1–Q5)
├── config.py                  # Color palette, species/area name mappings, matplotlib rcParams
├── soil_lookup.py             # Soil type → USFS ELU → climatic/geological zone mapping
├── presentation/              # Video presentation slides and exported figures
├── requirements.txt           # Python dependencies
└── README.md
```

---

## Questions Overview

### Act 1 — Ecological Toolkit & Exploration (Q1–Q10)
Custom ecological classification functions (elevation zones, solar exposure, topographic moisture, compass/aspect binning, fire proximity) followed by foundational EDA using pandas and NumPy.

### Act 2 — Deep Dive & Visualization (Q11–Q20)
Targeted analysis of extreme terrain, roadway proximity as a human impact proxy, hillshade asymmetry, hydrology geometry, and rare soil associations. Visualizations include elevation KDE distributions, wilderness area heatmaps, polar aspect diagrams, elevation-slope scatter plots, and solar gradient heatmaps.

### Act 3 — Ecological Niche Analysis (Q21–Q25)
A connected five-question arc: statistical hypothesis testing (ANOVA) → niche width quantification → climatic zone feature engineering → ecological outlier detection → wilderness area fingerprint synthesis.

---

## Key Findings

*Section updated after analysis is complete.*

---

## How to Run

```bash
git clone https://github.com/[your-username]/ds5010-final-project-dv.git
cd ds5010-final-project-dv
pip install -r requirements.txt
jupyter notebook covertype_analysis.ipynb
```

---

## Tools & Libraries

Python · pandas · NumPy · Matplotlib · Seaborn · SciPy · ucimlrepo

---

## Dataset Citation

Blackard, J. (1998). Covertype [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C50K5N

---

## Author

**Debbie** — MS Data Science (Align), Northeastern University · Khoury College of Computer Sciences  