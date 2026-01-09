<file name=0 path=/Users/kurtis/Desktop/Data-Science-Project-Template/README.md># [Aerial Imagery Urban Land Analysis]

**One-liner:** Aerial Imagery Urban Land Analysis, Intended to assist sustainable urban planning efforts.

## Overview
This project analyzes high-resolution aerial imagery features to classify urban land-cover types in a remote-sensing context. Using data containing spectral, shape, and texture features extracted from segmented aerial images, I explored relationships among predictors and prepared the data for modeling. I implemented clustering, dimensionality reduction, and supervised classification methods, including k-Nearest Neighbors and Random Forests. The final outputs include trained classification models, visualizations of feature structure and clustering behavior, and performance evaluations for both multi-class and binary land-cover classification tasks.

## Key Results
- [Result 1: The Random Forest classifier achieved 84.7% accuracy (κ = 0.823) on the nine-class land-cover classification task and 93.3% accuracy with an AUC of 0.992 on the binary split, indicating strong overall predictive performance and substantial agreement beyond chance. This suggests that the extracted aerial imagery features capture meaningful signal for urban land-cover classification, particularly when class boundaries are conceptually well defined.]
- [Result 2: The most influential predictors were spectral reflectance features (NDVI, Mean_R, Mean_NIR) and texture variability metrics (SD_R, SD_NIR, GLCM3), while shape features played a complementary role. This highlights that surface material properties and local heterogeneity are more discriminative than geometric shape alone for distinguishing urban land-cover types in aerial imagery.]
- [Result 3: Collapsing the nine land-cover classes into a binary Vegetation vs. Non-Vegetation target substantially improved model performance and interpretability. The Random Forest achieved 93.3% accuracy, 0.905 F1 score, and a near-perfect AUC of 0.992, demonstrating that the feature set is highly effective at distinguishing broad land-cover categories even when finer object-level separation is more challenging.]

## Repo Structure
- `data/` – local data (not committed)
  - `data/raw/` – original, immutable data
  - `data/cleaned/` – processed data created by scripts/notebooks
- `notebooks/` – exploration + storytelling (EDA, results)
- `src/` – reusable Python functions (preprocessing, features, modeling)
- `scripts/` – runnable scripts (pipeline entry points)
- `reports/` – figures + final outputs
- `env/` – environment and dependency files

## Getting Started -  Setup

### Option A — Python (VS Code, venv + pip)

Run these in Terminal from the repo as the root directory (cd ~path):

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r env/requirements.txt
```

### 1) Clone
```bash
git clone [REPO_URL]
cd [REPO_NAME]
```

### Option B — R (RStudio, renv)

<!-- Added note for R setup instructions -->
Run these in R console from the repo as the root directory:

```r
install.packages("renv")
renv::restore()
```
