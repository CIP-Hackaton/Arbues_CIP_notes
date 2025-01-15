# README for variedad_caracteristicas

## Required Files

1. **`Variedad_a_Caracteristicas_28.csv`**
   - Contains qualitative and quantitative characteristics of potato varieties.
   - Key columns:
     - Variety: Name of the variety.
     - Late blight (LB): Resistance to late blight.
     - Predominant tuber flesh color: Predominant color of tuber flesh.
     - Tuber shape depth of eyes: Depth of tuber eyes.
     - Dry matter (%): Percentage of dry matter.
     - Growing period highland: Growing period in highlands.

2. **`caracteristicas.csv`**
   - Contains extended data on potato varieties, with additional characteristics.
   - Key columns:
     - Similar to those in `Variedad_a_Caracteristicas_28.csv`, with the addition of:
       - Predominant tuber skin color: Predominant color of tuber skin.
       - General tuber shape: General shape of the tuber.

3. **`Variedad_a_Caracteristicas_28_numeric (1).csv`**
   - Numeric version of `Variedad_a_Caracteristicas_28.csv`.
   - Categorical columns converted to binary or numerically encoded variables:
     - Late blight (LB): Encoded as 0, 1, 2, 3.
     - Predominant tuber flesh color and Tuber shape depth of eyes: Encoded as dummy variables.

---

## Internal Workflows

1. **Cleaning and Conversion:**
   - Basic data cleaning in columns.
   - Conversion of categorical values to numeric for quantitative analysis.

2. **Grouping and Filtering:**
   - Grouping by variety to consolidate common characteristics.
   - Inclusion of additional columns in `caracteristicas.csv` for more detailed analysis.

3. **Output:**
   - Processed qualitative and quantitative data exported in CSV format.

---

## Final Exports

- **Generated files:**
  1. `Variedad_a_Caracteristicas_28.csv`: Raw data on characteristics.
  2. `caracteristicas.csv`: Extended data with additional characteristics.
  3. `Variedad_a_Caracteristicas_28_numeric (1).csv`: Numeric version for quantitative analysis.
