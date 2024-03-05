# get-public-ip

Objective: A bash script that acts as a simple dynamic DNS service to update configured domain records to reflect the dynamically allocated IP address for the host server.

This aim of the script is to have it fulfill the following tasks:
 - Check for the existance of it's configuration file used to store sensitive values (ignored by Git)
    - Or perhaps have it check for environmenttal variables configured for the purpose of this script in PATH?

 - Use the OpenDNS resolver to retrieve the server's public-facing IP address

 - Compare the most recently retrieved IP address with the last IP address stored in the configuration to check for a value change
    - If the values differ
        - Update the IP address in Cloudflare
        - Log the change in a logfile
        - Add the value in the Google Sheet Log

    - If the values are the same
        - Log the check in the logfile, but note that nothing changed


        
