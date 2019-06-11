# cgxSubOptimal
Enable or disable sub optimal re-evaluation

Instructions:

* Install python3
* Install cloudgenix python sdk : pip3 install cloudgenix
* Setup authentication as listed below
* Create a csv file with the example at devicelist.csv
* run the script using: python3 cgxSubOptimal.py --all --enable
* You can also specify a text file with a list to site names, each site in its own line, that will be affected by the script: python3 cgxSubOptimal.py --site_file sites.txt --enable

cgxSubOptimal.py looks for the following for AUTH, in this order of precedence:

* --email or --password options on the command line.
* CLOUDGENIX_USER and CLOUDGENIX_PASSWORD values imported from cloudgenix_settings.py
* CLOUDGENIX_AUTH_TOKEN value imported from cloudgenix_settings.py
* X_AUTH_TOKEN environment variable
* AUTH_TOKEN environment variable
* Interactive prompt for user/pass (if one is set, or all other methods fail.)

Exmpale:
```
bash$ ./cgxSubOptimal.py  --site_file sites.txt --enable
INFO:cgxSIPalg:Death Valley at Death Valley is being configured
INFO:cgxSIPalg:-- already have fcconfig
INFO:cgxSIPalg:-- updating fcconfig entry
INFO:cgxSIPalg:None at Dan Home is being configured
INFO:cgxSIPalg:-- already have fcconfig
INFO:cgxSIPalg:-- updating fcconfig entry
```