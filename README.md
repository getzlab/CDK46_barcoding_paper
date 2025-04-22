# CDK46_barcoding_paper

This repository contains code necessary to reproduce the results for the Whole Exome Sequencing data in the CDK4/6 barcoding paper.

## Running the mutation analysis

Run the "comut_plot.ipynb" notebook. This will generate three output files: "CDK46_barcoding_CoMut_maf.maf", "CDK46_barcoding_CoMut_cgc_anno.tsv" and "CDK46_barcoding_CoMut_patho_anno.tsv". These files can then be used as input to [Morpheus](https://software.broadinstitute.org/morpheus), which is a matrix visualizationn tool. The server takes in a MAF file and optional annotation files for samples (columns) and mutations (rows). Steps to generate the CoMut plot using Morpheus are outlined below:

* Make basic CoMut plot: Upload 'CDK46_barcoding_CoMut_OncoKB_maf.maf' to the Morpheus server
* Annotate mutations: Click on File -> Open. Upload 'CDK46_barcoding_CoMut_cgc_anno.tsv'. In 'Open file action', select 'Annotate rows' and click 'OK'. Leave default settings in 'Select Fields To Match On' and click 'OK' again. Follow the same set of steps again for uploading 'CDK46_barcoding_CoMut_patho_anno.tsv'.

## Running copy number analysis

Run the "copy_number_heatmap.ipynb" notebook.
