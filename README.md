# garlock-chronology

| Step                                    |         In          |                Code |                Out |
|-----------------------------------------|:-------------------:|--------------------:|-------------------:|
| 1. Create event PDFs                    | Age_Constraints.csv | MCMC/KDE or gauss() |     Site_Event.csv |
| 2. Combine event PDFs                   |   Site_Event.csv    |          Sum of KDE |   combined_PDF.csv |
| 3. Detect peaks                         |  combined_PDF.csv   |          find_peaks | extracted_PDFs.csv |
| 4. Multiply PDFs intersecting each peak | extracted_PDFs.csv  |          Sum of KDE |      final_PDF.csv |
| 5. Visualize data                       |   final_PDF.csv     |         Matplotllib |        .png figure |