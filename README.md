# modulome_sc_acitivity_inference

Activity inference pipeline for the _S. cerevisiae_ iModulon structure: https://github.com/jtburrows/modulome_sc_sbrg.git


Using the activity inference notebook, activities for new data can be inferred using the iModulon structure.

## Required Data
### Required data from iModulon Structure:
- ICA Data object module_sc.json
- train_counts.csv (length-normalized counts for original data in ICA decomposition)

This data can be found in the Zenodo Repository for this work or attached in the release for this package.

### Required data as new input:
- test_counts.csv (counts data for new input (preferably lenght-normalized))
- test_log_tpm.csv (lop_tpm data for new input qc and testing in notebook)
- test_metadata.csv (metadata for new data)

The metadata needs to include sample names as an index which match the columns of test_counts.csv. It also needs to include the columns for condition, project, and reference_condition for normalization of the data. An example of appropriate data is prorvided in the above linked zenodo and in the repository release.

Running the notebook will calculate activities from the data and generate basic plots enabling downstream analysis.

### Environment Creation
Using conda, install environoment with the following command: `conda env create -f environment.yml`
