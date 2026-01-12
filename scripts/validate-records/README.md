This script can be used to validate a directory of JSON files against a Sinai Manuscripts Data Portal schema.

# Installation

The preferred installation method is to use [Poetry](https://python-poetry.org/). Please refer to Poetry documentation for guidance on setting up this tool on your system.

Once Poetry has been added, it can be used to set up a virtual environment and install the dependencies for the migration script.

Clone this repository, then navigate to it in your terminal and run:

 `poetry install`

 # Use

 Once installed, use poetry to run the script, e.g.:

 `poetry run src/validate_records.py msobj`

 A record type **must** be specified as a command-line argument. Valid options are: "agents", "works", "msobjs", "layers", "txtunits", or "export". The script will prompt for a valid type if it is not supplied.

 The script will then prompt for an input directory where the data files may be found. After validation is performed, the script will prompt for the path to an output file. If none is provided, the default will be to save a `log.json` file in the working directory.

 This output file contains a JSON representation of the results of validation, reporting the specific validation errors for each file. **Only records that are invalid will be included in the log file**.