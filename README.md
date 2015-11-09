# ansible-weblogic-fmw-infra-12c-R2
Ansible playbook for deploy and create a WebLogic 12c R2 Domain with Oracle Fusion Middleware Infrastructure automatically

Vagrant configuration included. You can download it and test it with vagrant running from folder:

$ vagrant up

You can connect to Enterprise Manager using http://192.168.56.14:7001/em using weblogic/welcome1.

Playbook includes the following roles:
- linux-wls
- linux-jdk
- fmw-software
- fmw-domain
- node-manager
- start-admin-server
- fmw-managed-server

linux-wls:
This role configures the Linux system with requirements to run the WebLogic domain.

linux-jdk:
This role configures the Linux system with JDK8

fmw-software:
This role installs the the Fusion Middleware Software 12c R2

fmw-domain:
This role creates and configures a Domain with Fusion Middleware software

node-namager:
This role configures and starts the Nodemanager. It also configures systemd to start automatically the nodemanager after restart

start-admin-server:
This starts the Admin server using nodemanager for the first time. Creates some initial configuration like boot.properties file

fmw-manager-server:
This role creates and starts a managed server with JRF template. (Ready to host ADF or other Fusion Middleware applications)

More information here:

http://unversioned.blogspot.gr/2015/11/using-ansible-to-install-weblogic-12c.html