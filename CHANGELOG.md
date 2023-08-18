# Changelog 

## 0.3.0

- add bioscan manifest v3 support and set it as template, v2 input still supported
- amend STS output to match v3 manifest, allowing for both v2 and v3 manifests conversion into the same STS output
- regex validations for all format-sensitive fields including dates, reimplement date comparison
- date cleanup from time addition by Excel-to-pandas conversion 
- validate identifier against contributors
- validate input filename
- continued error message clarifications
- logic updates, bug fixes, general refactoring
- tested on backlog pre-release

## 0.2.0

- added new logic for better adherence to SOPs - non-breaking spaces removal, catch lot validation, what three words validation, gal inference from plate ID prefix
- initial work on error message text standartisation
- introduce DEBUG messages to separate state reports from summary stats
- plate expansion after validation to preserve refs to SERIES
- logic updates, bug fixes, general refactoring

## 0.1.0

- major code re-structuring to separate shared functions from bioscan manifest v.2 and anospp manifest v.4 validations
- added manifest SOPs as points of reference for validation
- extended testing of validation functions by inclusion of test datasets with errors into template manifests
- added contributors tab validation
- added generation of xlsx for STS, embedded validation version in the filename
- added and modified checks logic, improved reporting, generic refactoring

## 0.0.1a

Initial version of bioscan manifest v.1 validation. Core functionality developed here.