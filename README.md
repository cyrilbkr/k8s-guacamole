# k8s-guacamole
Apache Guacamole for Kubernetes

This configuration launch one deployment for Guacd on serviceport 4822 and one deployment for Guacamole on serviceport 8080. 

You need a Mysql/Mariab server already up and runnng to host the Guacamole database. 

Default login/password : guacadmin/guacadmin

## How to 

### Create & initialize database
Create a new Mysql/Maria database with a login/password and source it with the sql script : 

    source < boostrapdb.sql
    
### Configure 

Edit deployment.yml and modify database,user and password var :

    - name: MYSQL_HOSTNAME
    value: "xxxxx"
    - name: MYSQL_DATABASE
    value: "xxxxx"
    - name: MYSQL_USER
    value: "xxxxx"
    - name: MYSQL_PASSWORD
    value: "xxxxx"

### Launch 

    kubectl create -f k8s-guacamole/


