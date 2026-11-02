# Municipal Profiles and Social Leader Killings in Colombia

An application of Principal Component Analysis (PCA) to municipal fiscal, territorial, and rural credit indicators in Colombia. The notebook reduces 15 variables to three components and examines their association with recorded killings of social leaders.

The PCA calculations are written explicitly with NumPy to show the underlying linear algebra.

## Analysis

The notebook:

1. Builds municipal indicators using averages for 2016–2022, including population density and per capita fiscal and credit variables.
2. Applies log transformations to selected variables and standardizes the data.
3. Constructs the covariance matrix and calculates its eigenvalues and eigenvectors.
4. Projects the data onto three principal components and examines explained variance, loadings, and variable contributions.
5. Relates the components to killings of social leaders aggregated over 2018–2023, using plots and OLS regressions with and without departmental fixed effects. Standard errors are clustered by department.

It also checks that component variances match their eigenvalues and that the components are uncorrelated. The regressions describe associations between municipal profiles and violence.

## Files

- `PCA_1.ipynb`: data preparation, PCA, visualizations, and regressions.
- `panel_tierras_violencia_final.csv`: municipal panel used in the analysis.

## How to run

Install the dependencies:

```bash
pip install pandas numpy matplotlib seaborn statsmodels
```

Keep the CSV file in the same folder as `PCA_1.ipynb`. Open the notebook in Jupyter or VS Code and run the cells in order.

## Author

Daniel Ricardo Amaya Alba
