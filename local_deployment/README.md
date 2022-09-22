## Manual migration and setup

To migrate Wordpress instances between different servers:
1. Compress wp-content folder from the the WordPress content directory. The exported database named wordpress can be found in the same directory.
2. Startup a new mariadb container.
3. Import database from step 1. (make sure the URL is updated to the current URL being used in the database. This can be changed easily pre-import by editing the file.)
4. Edit the volumes in the docker-compose so that your new wordpress instance uses the wp-content folder from step 1 and link it to your new mariadb container.
5. Start up the wordpress docker container.
6. Update the email address to your email.

## Automatic migration and setup

To migrate Wordpress instances between different servers:
1. Open up a terminal and navigate to the Local Deployment directory.
2. Edit the uploads.ini file to increase the upload_max_filesize to 300MB. This can be changed back after setup.
3. run the command
'''
sudo docker-compose up -d
'''
4. In a web browser enter the url localhost:8000 to access the WordPress site.
5. Set up WordPress
6. In the WordPress dashboard navigate to Plugins -> Add New
7. Search for the plugin: All-in-One WP Migration. Install and activate.
8. In the WordPress dashboard navigate to All-in-One WP Migration -> Import
9. Select Import from File and select the WPRESS file from the WordPress Content directory.
10. Update the email address to your email address.

## Login details
- username: admin
- password: inethi