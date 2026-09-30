# CSV Predictor (Desktop Machine Learning Tool)

A lightweight desktop application built with Python and PyQt5 that automates tabular classification workflows. The tool dynamically generates graphical user interfaces from loaded datasets, trains Scikit-Learn pipelines, and executes single-record inference or batch file predictions.

---

## Key Features

* **Dynamic UI & Form Generation:** Automatically scans CSV column headers, detects feature types (numerical vs. categorical), and constructs tailored input forms and target selector dropdowns.
* **Automated Data Preprocessing:** Builds an end-to-end `scikit-learn` pipeline utilizing `ColumnTransformer` with `StandardScaler` for continuous variables and `OneHotEncoder` for categorical factors.
* **Live Diagnostic Metrics:** Outputs performance evaluations directly within the GUI, rendering precision, recall, f1-score, and support metrics via `classification_report`.
* **Interactive Single-Record Inference:** Allows manual input adjustment to compute immediate class predictions and calculated probability percentages.
* **Model Serialization:** Exports and loads trained pipelines alongside target encoders via `joblib` for deployment reuse.
* **Automated Batch CSV Scoring:** Ingests unlabelled tabular files, validates column dependencies, and appends `prediction` and `probability(%)` outputs directly into an exported CSV.
* **Portable Windows Binary:** Compiled into a standalone `.exe` using PyInstaller, running without external Python or library dependencies.

---

## Tech Stack & Architecture

* **GUI Framework:** PyQt5
* **Machine Learning & Pipelines:** Scikit-Learn (Logistic Regression, ColumnTransformer, Preprocessing)
* **Data Processing:** Pandas, NumPy
* **Serialization:** Joblib
* **Packaging:** PyInstaller

---

## Installation & Usage

### Option 1: Standalone Windows Binary (No Python Required)
1. Go to the **[Releases](../../releases)** tab on this repository.
2. Download `CSV_Predictor.exe`.
3. Double-click the executable to launch the app directly.

### Option 2: Run from Source
1. Clone the repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/<repo-name>.git
   cd <repo-name>
