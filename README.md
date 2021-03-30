# Parkinson's Gittis Collab

These code files were used to train Gaussian process (GP) regressions (and linear regressions) on the various datasets generated by Teresa Spix. 

## Overview of the files
### "Regressions_LeaveOutCopies_first2DataSets_PredictOnRaw_CompareToAvg-Testing-NoDupes-afterlooxv.ipynb":
This file was used to train linear regressions with a linear kernel and interacting terms on the first set of PV and Lhx6 data. This file also generated output files used in "gpeTest_leaveAllOut_rawpred_compareavg_FINAL-NoDupes-afterlooxv.Rmd".

### "Regressions_LeaveOutCopies_all3DataSets_PredictOnRaw_CompareToAvg-Testing-NoDupes-afterlooxv.ipynb":
This file was used to train linear regressions with a linear kernel and interacting terms on all the PV and Lhx6 data. This file also generated output files used in "gpeTest_leaveAllOut_rawpred_compareavg_allThreeDataSet_FINAL-NoDupes-afterlooxv.Rmd".

### "gpeTest_leaveAllOut_rawpred_compareavg_FINAL-NoDupes-afterlooxv.Rmd"
This R file was used to train GP regressions on separated PV and Lhx6 data in the first round of data. The input files came from "Regressions_LeaveOutCopies_first2DataSets_PredictOnRaw_CompareToAvg-Testing-NoDupes-afterlooxv.ipynb". The output files are evaluated in "calculateCoeffs_GPs.ipynb".

### "gpeTest_leaveAllOut_rawpred_compareavg_allThreeDataSet_FINAL-NoDupes-afterlooxv.Rmd"
This R file was used to train GP regressions on separated all the PV and Lhx6 data. The input files came from "Regressions_LeaveOutCopies_first2DataSets_PredictOnRaw_CompareToAvg-Testing-NoDupes-afterlooxv.ipynb". The output files are evaluated in "calculateCoeffs_GPs.ipynb".

### "calculateCoeffs_GPs.ipynb"
This file was used to calculate the correlation coefficients between the GP regressions and the averaged actual responses. The input files are generated from "gpeTest_leaveAllOut_rawpred_compareavg_FINAL-NoDupes-afterlooxv.Rmd" and "gpeTest_leaveAllOut_rawpred_compareavg_allThreeDataSet_FINAL-NoDupes-afterlooxv.Rmd".

### "collectData_AndreasWay.Rmd"
This file was used to generate the artificial data points to test the GP regressions and see which points they predicted have the largest differences.

## Packages needed
For Python 3, these packages are needed:
### pandas
### math
### numpy
### sys
### sklearn
### copy
### xlsxwriter
### scipy

For R, these packages are needed (I ran this on R 3.6):
### kernlab
### ggplot2

## Data Files
The raw starting data files are included here. When starting with "Regressions_LeaveOutCopies_first2DataSets_PredictOnRaw_CompareToAvg-Testing-NoDupes-afterlooxv.ipynb" or Regressions_LeaveOutCopies_all3DataSets_PredictOnRaw_CompareToAvg-Testing-NoDupes-afterlooxv.ipynb", replace where the file names are read in with the path to where you downloaded the files or where your data are. 