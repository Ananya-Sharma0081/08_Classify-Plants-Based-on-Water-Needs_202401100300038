# Plant Water Need Classifier

## Description
This project builds a machine learning model to classify plants into water‑need categories (low, medium, high) based on environmental features.

## Problem Statement
Different plants have varying water requirements influenced by sunlight, soil type, and watering frequency. The goal is to predict a plant’s water‑need category automatically to optimize plant care.

## Dataset
- **File**: `plants.csv`
- **Columns**:
  - `sunlight_hours` (float): Average daily sunlight hours
  - `watering_freq_per_week` (int): Watering frequency per week
  - `soil_type` (categorical): sandy, loamy, clay
  - `water_need` (target categorical): low, medium, high

## Installation
1. Clone the repository:
   ```bash
   git clone <repo_url>
   cd plant-water-need-classifier
   ```
2. Create a virtual environment and install dependencies:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

## Usage
1. Place `plants.csv` in the project root.
2. Run the training script:
   ```bash
   python train.py
   ```
3. The script will output model metrics in the console and save the trained model as `plant_classifier.pkl`.

## Methodology
1. **Preprocessing**
   - Load data with pandas
   - Encode categorical features (`soil_type`, `water_need`) using LabelEncoder
2. **Balancing**
   - Apply SMOTE to address class imbalance
3. **Training**
   - Split data (80% train, 20% test)
   - Train a Gradient Boosting Classifier
4. **Evaluation**
   - Use accuracy, precision, recall, and F1‑score to assess performance

## Results
- **Accuracy**: 0.48
- **Classification Report**:
  - High: precision=0.50, recall=0.50, f1=0.50
  - Low: precision=0.33, recall=0.38, f1=0.35
  - Medium: precision=0.60, recall=0.55, f1=0.57

## Objectives
- Encode and preprocess environmental features
- Balance target classes with SMOTE
- Train and evaluate a Gradient Boosting model
- Provide data‑driven recommendations for plant watering

## References
1. Chawla et al., 2002. SMOTE: Synthetic Minority Over‑sampling Technique.
2. Friedman, 2001. Greedy Function Approximation: A Gradient Boosting Machine.
3. scikit‑learn GradientBoostingClassifier Documentation.
4. pandas Documentation.

---
*Prepared for academic presentation.*

