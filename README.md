# Symbiota
- https://github.com/BU-Spark/se-Symbiota-portal
- https://github.com/BU-Spark/se-symbiota-vagrant
## Create Database used PHPmyAdmin
![image](https://user-images.githubusercontent.com/79159894/197318314-401f6339-6580-427e-8174-cb84855c7b5b.png)

## Create User
![image](https://user-images.githubusercontent.com/79159894/197319621-6eb62a72-e4c0-4cf2-8bbd-ece5ab791ace.png)

## Run the SQL script to create table and insert data

- db_schema-1.0.sql
- db_schema_patch-1.1.sql, db_schema_patch-1.2.sql

## Modify PHP File Name
- Rename /config/symbini_template.php to /config/symbini.php.
- Rename /config/dbconnection_template.php to /config/dbconnection.php.
- Rename /index_template.php to index.php.
- Rename header_template.php to header.php, and footer_template.php to footer.php
- Rename head_template.php to head.php
- Rename usagepolicy_template.php to usagepolicy.php


## Symbiota vagrant
- https://github.com/BU-Spark/se-symbiota-vagrant

## Stuck in this issue --- vagrant up : The following SSH command responded with a non-zero exit status.

Not found the solution yet.
 ``` 
cd symbiota-vagrant
vagrant up
 ```
  ```
vagrant plugin update vagrant-vbguest
 ```
- Reference
- https://github.com/hashicorp/vagrant/issues/1659

