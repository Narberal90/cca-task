# Canonical Correlation Analysis (CCA) for Hotel Reviews

## Description
This project implements the Canonical Correlation Analysis (CCA) algorithm to analyze the relationship between review text properties (length of negative and positive reviews) and hotel rating indicators (reviewer score and average score).

## Requirements
- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - scikit-learn

## Setting Up the Environment

Follow these steps to set up the environment:

1. **Create a virtual environment:**
    ```bash
    python -m venv venv
    ```

2. **Activate the virtual environment:**
    - On Windows:
      ```bash
      venv\Scripts\activate
      ```
    - On macOS/Linux:
      ```bash
      source venv/bin/activate
      ```

3. **Install the required dependencies:**

    ```
    pip install -r requirements.txt
    ```

## File Structure
- `archive.zip` — data with hotel reviews.
- `cca_analysis.ipynb` — Jupyter notebook to perform the analysis.
- `README.md` — user instructions.

## Usage

1. Open the `cca_analysis.ipynb` notebook.
2. Run the code.

## Algorithm Details

1. **Data Loading and Preprocessing**:
   - The CSV file with reviews is read from the specified path.
   - "No Negative" and "No Positive" values are replaced with NaN.
   - Lengths of negative and positive reviews are calculated.
   - Rows with missing important values (reviewer score, average score, negative and positive review lengths) are dropped.

2. **Canonical Correlation Analysis**:
   - Two sets of variables are used:
     - X: Length of negative and positive reviews.
     - Y: Reviewer score and average hotel score.
   - The data is standardized using `StandardScaler`.
   - The `CCA` class from the `scikit-learn` library is used to compute canonical variables and correlations between the two sets of variables.

3. **Visualization**:
   - Scatter plots are generated for the two canonical components, showing the relationship between review text properties (lengths of reviews) and ratings (reviewer score and average score).
   - The correlation values for each canonical component are printed in the console for reference.

