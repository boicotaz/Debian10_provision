# Debian10_provision
Ansible scripts to provision a Debian 10 enviroment with nginx and mysql server container.

### Execute Ansible scripts
From the root of the repository execute the following command <br/>
`ansible-playbook -i invetories/remote entrypoint.yml -u root -k` <br/>
It will prompt for root's user credentials. <br/>

### Mysql Container Information
Instructions for using the deployed mysql services directly by the Debian-10 system. <br/><br/>

Firstly, acquire the root password by executing the following as the root user <br/>
`docker logs mysql-server 2>&1 | grep GENERATED` <br/><br/>

Finally, connect to mysql by providing the generated root password, acquired in the previous step </br>
`docker exec -it mysql-server mysql -u root -p`