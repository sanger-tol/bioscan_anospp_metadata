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


## Update code

If code needs to be updated, follow these steps
```bash
# go to code directory
cd bioscan_anospp_metadata
# remove changes made to notebooks - this will erase execution info 
git checkout -- work/*.ipynb
# pull changes from github
git checkout main
git pull
# update Nominatim user agent name - insert your preferred username 
sed -e -i 's/bioscanManifestTest/bioscan_am60/' work/validate_partner_manifest_dev.ipynb
```

Once done, change 