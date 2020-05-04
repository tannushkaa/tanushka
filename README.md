version: '3.1' 
services: 
db: 
image: mariadb 
volumes: - /etc/mysql/config.d 
restart: always 
environment: 
MYSQL_ROOT_PASSWORD: example 
adminer:
 image: 
adminer 
restart: always 
ports: - 8080:8080 
version: '3.1' 
services: 
drupal: 
image: 
drupal:
8-apache ports: - 8080:80 
volumes: - /var/www/html/modules - /var/www/html/profiles - /var/www/html/themes 
# this takes advantage of the feature in Docker that a new anonymous 
# volume (which is what we're creating here) will be initialized with the 
# existing content of the image at the same location - /var/www/html/sites 
restart: always 
postgres: 
image: 
postgres:10 
environment: 
