# How to install Papatohu Dashboard

This folder contains all neccessary files to install our dashboard.

Plz follow this steps to open and configure the dashboard:

- download all files to your PC
- start with the backend folder
- execute the file "config_backend.bat" 
- When running the file you will be asked to input some information, but you are free to skip all of it (just press Return to skip an option). When asked if the information is correct, type yes.
- this generates a self-signed certificate. If you deploy the dashboard officially, you should use a proper ssl certifiate!
- execute the file "start_backend.bat" to start the backend
- after that, move to the frontend folder
- unpack the frontend.rar to your favorite destination e.g. at Apache the htdocs folder
- Add following lines in the "httpd-proxy.conf" file of Apache under xampp/apache/conf/extra:
  -  ProxyPass //info.0.json https://xkcd.com/info.0.json
     ProxyPassReverse //info.0.json https://xkcd.com/info.0.json

     ProxyPass //api/random https://zenquotes.io/api/random
     ProxyPassReverse //api/random https://zenquotes.io/api/random

     ProxyPass //getConfig/ https://localhost:8443/getConfig/
     ProxyPassReverse //getConfig/ https://localhost:8443/getConfig/

      ProxyPass //updateConfig/ https://localhost:8443/updateConfig/
      ProxyPassReverse //updateConfig/ https://localhost:8443/updateConfig/

      ProxyPass //tunnelEfaDirect.php https://www.kvv.de/tunnelEfaDirect.php
      ProxyPassReverse //tunnelEfaDirect.php https://www.kvv.de/tunnelEfaDirect.php

      ProxyPass //newsticker.rdf https://www.tagesschau.de/newsticker.rdf
      ProxyPassReverse //newsticker.rdf https://www.tagesschau.de/newsticker.rdf

      ProxyPass //freeplan/ https://api.deutschebahn.com/freeplan/
      ProxyPassReverse //freeplan/ https://api.deutschebahn.com/freeplan/

      ProxyPass //login/ https://localhost:8443/login/
      ProxyPassReverse //login/ https://localhost:8443/login/

      ProxyPass //newUser/ https://localhost:8443/newUser/
      ProxyPassReverse //newUser/ https://localhost:8443/newUser/

      ProxyPass //get/ https://localhost:8443/get/
      ProxyPassReverse //get/ https://localhost:8443/get/
      
- simply start Apache


Have fun,

Your Team Papatohu
