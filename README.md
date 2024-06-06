# garlock-chronology
[![DOI](https://zenodo.org/badge/811452867.svg)](https://zenodo.org/doi/10.5281/zenodo.11508484)

| Step                                    |         In          |         Code         |                         Out |
|-----------------------------------------|:-------------------:|:--------------------:|----------------------------:|
| 1. Create event PDFs                    | Age_Constraints.csv | MCMC/KDE or gauss()  | Site_Event.csv (event PDFs) |
| 2. Combine event PDFs                   |   Site_Event.csv    |      Sum of KDE      |            combined_PDF.csv |
| 3. Detect peaks                         |  combined_PDF.csv   |      find_peaks      |          extracted_PDFs.csv |
| 4. Multiply PDFs intersecting each peak | extracted_PDFs.csv  |      Sum of KDE      |               final_PDF.csv |
| 5. Visualize data                       |   final_PDF.csv     |     Matplotllib      |                 .png figure |

## STEP 1 -- Create PDFs

Create probability density functions for each event at each site

### Example input file -- Age_Constraints.csv

| event |     site      | min_age | min_err | max_age | max_err | confidence |
|-------|:-------------:|--------:|--------:|---------|---------|------------|
| EPP-W | El Paso Peaks |         |         |         |         |            |
| EPP-U | El Paso Peaks |         |         |         |         |            |
| EPP-R | El Paso Peaks |         |         |         |         |            |
| EPP-Q | El Paso Peaks |         |         |         |         |            |
| EPP-K | El Paso Peaks |         |         |         |         |            |
| EPP-F | El Paso Peaks |         |         |         |         |            |
| EP-A  |  Echo Playa   |         |         |         |         |            |
| EP-B  |  Echo Playa   |         |         |         |         |            |
| EP-C  |  Echo Playa   |         |         |         |         |            |
| EP-D  |  Echo Playa   |         |         |         |         |            |
