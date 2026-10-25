# copper capstone (a.k.a. me vs messy trade data)

This is me cleaning up trade data for my capstone project.
The raw files are in `data/`, the cleaned exports are in `output/`, and the two notebooks are where the cleanup happened.

## what’s in here

### notebooks

- `copper-analysis1.ipynb`  
	Reads `copper-duty_annual.csv`, does the whole transpose/reset-index/rename-columns routine, splits `Commodity` into `HTS Code` and `Product Name`, then exports cleaned annual duty data.

- `copper-analysis2.ipynb`  
	Similar workflow, but for customs value data from `copper-customs-value_annualized.csv`, then exports a cleaned customs value file.

### data/ (raw-ish inputs)


- Raw files are Census/USA Trade Online exports and include a source line + giant column headers.
- `copper-customs-value_annualized.csv` — raw customs value pull (very wide format, 8 lines).
- `copper-customs-value_monthly.csv` — monthly customs value pull (same weird shape, 8 lines).
- `copper-duty_annual.csv` — raw annual duty pull (8 lines).
- `copper-duty-values-by_month.csv` — monthly duty pull (8 lines).
- `drive-download-20261015T172316Z-1-001.zip` — downloaded archive from Drive.
- `drive-download-20261015T172316Z-1-001/` — extracted folder from the zip (currently basically empty except system metadata).

### output/ (cleaned exports)

- `export-copper-customs_value-monthly.csv` — cleaned long-ish customs value dataset (1,827 lines).
- `export-copper-duty-annual.csv` — cleaned annual duty dataset (167 lines).

