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
![image](https://user-images.githubusercontent.com/79159894/197408786-d8a8ccc2-a59d-4c2c-b6a4-6d5f41e63d3c.png)

Not found the solution yet.
``` 
cd symbiota-vagrant
vagrant up
```
```
vagrant plugin update vagrant-vbguest
```
 
 Not help
 ``` 
 vagrant halt/suspend
 vagrant reload
 ``` 
- Reference
- https://github.com/hashicorp/vagrant/issues/1659

## Check the existing key
- list all files that contains existing key 
 ``` 
ls -al ~/.ssh
 ``` 
 ![image](https://user-images.githubusercontent.com/79159894/198750117-2aefda71-626b-4dd6-a1ce-5ee62902bb99.png)
- File name that supprot git hub public key:
  - id_rsa.pub
  - id_ecdsa.pub
  - id_ed25519.pub
### Reference
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys

## Generate the SSH key
 ``` 
ssh-keygen -t rsa 
 ``` 
- Open file at C:\Users\debra/.ssh/id_rsa, public key store in it.
![image](https://user-images.githubusercontent.com/79159894/198750322-9b3f9736-5d8d-49cb-971e-a09a754fe20d.png)
### Reference
https://inchoo.net/dev-talk/how-to-generate-ssh-keys-for-git-authorization/

## Use ssh to connect the server through vscode
1. ctrl + shift + p opend command of vscode
2. select SSH-Remote Host: Connect to host
3. select configure SSH Host, configure file will be opened
4. add host name and infromation below into the file.
 ``` 
 Host herbaria
    HostName 54.86.117.232
    User debrah
    IdentityFile C:\Users\debra\.ssh\id_ed25519
 ``` 
 
5. After that, ctrl + shift + p opend command of vscode
6. select SSH-Remote Host: Connect to host, then we can see the Host herbaia in the selections
7. Clik it and new window will pop out and the green left corner will start run opening remote.
8. Then click the exploer and open folder and ok, we can have the all symbiota file on the server.
