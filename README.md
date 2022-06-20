# How to install Papatohu Dashboard

This folder contains all neccessary files to install our dashboard.

You need Java 16 or higher to run the backend and Appache (e.g. XAMPP) to run the frontend.

Plz follow this steps to open and configure the dashboard:

- download all files to your PC
- start with the backend folder
- execute the file "config_backend.bat" 
- When running the file you will be asked to input some information, but you are free to skip all of it (just press Return to skip an option). When asked if the information is correct, type yes.
- this generates a self-signed certificate. If you deploy the dashboard officially, you should use a proper ssl certifiate!
- execute the file "start_backend.bat" to start the backend
- after that, move to the frontend folder
- move all files in the folder to your favorite destination e.g. at Apache the htdocs folder
- replace the httpd.conf in xammp/apache/conf with /Frontend - xammp configuration/httpd.conf
- replace the httpd-proxy.conf in xammp/apache/conf/extra with /Frontend - xammp configurationin/httpd-proxy.conf
      
- simply start Apache


Have fun,

Your Team Papatohu
