# DevOps_Ansible_Vagrant
For this project, a Shell Script was used together with Vagrant and Ansible for automation of the database, web and monitor servers of the book Devops in practice: delivery of reliable and automated software, followed by Danilo Sato.

To use this project it is necessary to install VirtualBox on the website: https://www.virtualbox.or/wiki/Downloads, Vagrant on the website: https://www.vagrantup.com/downloads and Ansible on the website: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

Access the virtual machine by executing the following commands: $ vagrant ssh db $ mysql -u root -p -e "SHOW DATABASES" enter the password: secret $ mysql -u loja -p loja_schema -e "select database(), user()" enter the password: lojasecret

To check the web server, simply access the following sites in your browser: http://192.168.33.12:8080/devopsnapratica/ http://192.168.33.12:8080/devopsnapratica/admin/ to log in at http://192.168.33.12:8080/devopsnapratica/admin/ just put in Username: admin and Password: admin

To check the monitoring server, simply access the following website in your browser: http://192.168.33.14/nagios3/ by entering the username: nagiosadmin and password: secret or directly accessing the link http://nagiosadmin:secret@192.168.33.14/nagios3 remembering that this is not a secure way of access, to check if everything is correct it is possible to navigate through the left side menu for Services and Host Groups to access the monitoring of services and host groups.
