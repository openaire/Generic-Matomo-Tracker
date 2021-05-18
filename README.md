# Generic Usage Activity Tracker for OpenAIRE #

A generic usage activity tracker for Matomo platform. The script is based on the Matomo log analytics tool [1]. The script:

1. Parses the Web server log files
2. Cleans non-legitimate traffic, eg. bots, search engines using the COUNTER Robot list  
3. Imports usage activity for metadata and downloaded items from repositories to OpenAIRE's Matomo platform.

Requires python 3.

## Quick Install And Run ##

1. Install virtualenv
    `$ pip install virtualenv`
2. Create a virtual environment for the project
    `$ virtualenv -p /usr/bin/python3 matomo_tracker`
3. Activate the virtual environment:
    `$ source matomo_tracker/bin/activate`
4. Download matomo_import_logs.py and matomo.yaml to activated project folder
5. Configure matomo parameters in matomo.yaml
6. Install the following packages:
    - `pip install pyyaml`
7. Run the importer `$python3 matomo_import_logs.py {logs_folder}` or `$python3 matomo_import_logs.py {log_file}`


## Note ##
* The imported logs should be removed from the {logs_folder} to avoid duplication of events.
* Skip the `n` first lines to start parsing/importing data at a given line for the specified log file using -s `n` or --skip=`n` (eg. -s 1000 or --skip=1000 )
* Configure the `LogFileFormat` parameter in yaml for a customized log file format


[1] https://matomo.org/docs/log-analytics-tool-how-to/
