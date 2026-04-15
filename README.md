# Size-Exclusion Chromatography Processing and Percent Collapse Calculation
Python notebooks for processing LabSolutions size-exclusion chromatography exports, generating molecular weight chromatograms, and calculating polymer percent collapse.

## Files

- `DMFGPC_process_directory.ipynb` — processes and plots DMF size-exclusion chromatography traces
- `aqSEC_process_directory.ipynb` — processes and plots aqueous size-exclusion chromatography traces
- `collapse_directory.ipynb` — compares matched DMF and aqueous traces and calculates percent collapse

Example input data and example output plots are also included in this repository.

## What the code does

These notebooks:
- read raw LabSolutions `.txt` exports
- extract chromatogram data from the relevant detector
- extract the calibration curve from the same file
- convert retention time to apparent molecular weight
- subtract a blank trace
- normalize the signal
- generate processed chromatogram plots

The collapse workflow also:
- matches DMF and aqueous files by sample name
- identifies the peak molecular weight in each solvent
- calculates percent collapse
- exports a summary Excel file of percent collapse values

## Input format

The code is written for LabSolutions text exports containing detector chromatograms and calibration curve tables. An example file is included in the repository and shows the expected format.

## How to use

Open the notebook you want to run and edit the input paths in the user settings cell:
- data directory
- blank file
- output file name
- plot range

Then run all cells.

## Outputs

Depending on the notebook, outputs include:
- processed chromatogram plots
- CSV files of processed traces
- PDF comparison plots
- Excel summary file with percent collapse values

## Notes

- The code assumes the LabSolutions export format used in the example data.
- DMF and aqueous files should have matching filenames for collapse analysis.
- Example data and example plots are included so the workflow can be checked before using new data.
