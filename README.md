# Matomo Usage Activity Tracker for OpenAIRE #

A generic usage activity tracker for Matomo platform. The script is based on the Matomo log analytics tool [1]. The script:

1. Parses the Web server log files 
2. Cleans non-legitimate traffic, eg. bots, search engines using the COUNTER Robot list  
3. Records usage activity for metadata and downloaded items from repositories 

Requires python 2.6 or 2.7.

## Quick Install And Run ##

1. Install virtualenv
    $ pip install virtualenv
2. Create a virtual environment for the project
    $ virtualenv -p /usr/bin/python2.7 matomo_tracker
3. Activate the virtual environment:
    $ source matomo_tracker/bin/activate
3. Download COUNTER Robots List: 
 wget https://raw.githubusercontent.com/atmire/COUNTER-Robots/master/COUNTER_Robots_list.json 
4. Download matomo_import_logs.py and matomo.yaml to activated project folder
5. Install the following packages:
    - pip install pyyaml
6. Run the importer
 /usr/bin/python2.7 {logs_folder}


[1] https://matomo.org/docs/log-analytics-tool-how-to/


