## Install iNethi

To install the iNethi environment ensure that you use a seperate server such as an Intel NUC or a Virtual Machine. Do not install on your host machine as you might not be able to access the internet. For more info visit the iNethi [master-builder repo](https://github.com/iNethi/master-builder)

1. In the root directory run the command:
```shell
git clone https://github.com/iNethi/master-builder
```
2. Run the  command and follow the installation steps
```shell
sudo ./build_all.sh
```

## Automatic Migration and Setup

To migrate Wordpress instances between different servers:
1. Transfer the inethi-monetization folder to the server.
2. Edit the uploads.ini file to increase the upload_max_filesize to 300MB. This can be changed back after setup.
3. run the command
```shell
sudo ./local_build.sh
```
4. In a web browser enter the url radio.inethilocal.net to access the WordPress site.
5. Set up WordPress
6. In the WordPress dashboard navigate to Plugins -> Add New
7. Search for the plugin: All-in-One WP Migration. Install and activate.
8. In the WordPress dashboard navigate to All-in-One WP Migration -> Import
9. Select Import from File and select the WPRESS file from the wordpress_content directory.
10. Update the email address to your email address.

## Login details
- username: admin
- password: inethi

## Additional Information

If you are unble to access these services from a host machine you will need to manually resolve the dns requests.
For Linux or macOS machines add run the command:
```shell
sudo nano /etc/host
```
Add the ip address of the server running the iNethi environment and the domain name of the service to the file seperated by a tab. For example:
- <server ip> radio.inethilocal.net

For Windows users open Notepad and run it as an administrator. 
- Select File -> Open and search the for directory C:\Windows\System32\drivers\etc.
- Select All Files in the File Explorer and open the hosts file.
Add the ip address of the server running the iNethi environment and the domain name of the service to the file seperated by a tab. For example:
- <server ip> radio.inethilocal.net

To update the domain name edit the .env file and change the TRAEFIK_API_RULE_WORDPRESS.
