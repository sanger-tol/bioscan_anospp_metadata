# bioscan_anospp_metadata

Partner metadata handling for BIOSCAN and ANOSPP projects

## Setup

To set up, execute in terminal

```bash
git clone git@github.com:amakunin/bioscan_anospp_metadata.git
cd bioscan_anospp_metadata
conda env create -f work/env.yml
conda activate bioscan_metadata_dev
mkdir results
```

Copy manifest to validate somewhere in `results` directory

To run, execute in terminal

```
jupyter notebook
```

Then, in browser at `localhost:8888`, 
- navigate to `work/validate_bioscan.ipynb` or `work/validate_anospp.ipynb`
- run all cells - note this will take a while on the first time as NCBI Taxonomy is downloaded to `work/taxdump.tar.gz`
- in the first cell of "Validation" section, replace `fn` value with path to your manifest
- running the cell should yield the validation report 

NB keep track of `user_agent` value in `Nominatim` function for geocoding
