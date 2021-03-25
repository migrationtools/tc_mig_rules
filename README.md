# tc_mig_rules
This repository contains xml rules that are used by the red hat migration toolkit to scan weblogic applications and provide recommendations for migrating it to tomcat.
Copy the xml rules to your {user.home}/.mta/rules folder.

Pre-requisites:
You should have downloaded and installed mta cli tool, version 5.1.0 or later.
You can get it at:
https://developers.redhat.com/products/mta/download

These rules have been tested against version 5.1.0.

To generate the migration report:
Open a command window 
Navigate to the mta cli/bin folder.
Run:

mta-cli --input <your_wl_app>\target\<your_wl.ear/your_wl.war> --output <your_mta_output_folder> --target tomcat --overwrite --batchmode

The tool takes a minute or two to scan the war/ear and generate the report in the output folder
Navigate to the output folder <your_mta_output_folder> and open up index.html to get your report.
