## Automatic migration and setup

To migrate Wordpress instances between different servers:
1. Open up a terminal and navigate to the Local Deployment directory.
2. Edit the uploads.ini file to increase the upload_max_filesize to 300MB. This can be changed back after setup.
3. run the command
```shell
sudo docker-compose up -d
```
4. In a web browser enter the url localhost:8000 to access the WordPress site.
5. Set up WordPress
6. In the WordPress dashboard navigate to Plugins -> Add New
7. Search for the plugin: All-in-One WP Migration. Install and activate.
8. In the WordPress dashboard navigate to All-in-One WP Migration -> Import
9. Select Import from File and select the WPRESS file from the wordpress_content directory.
10. Update the email address to your email address.

## Login details
- username: admin
- password: inethi
