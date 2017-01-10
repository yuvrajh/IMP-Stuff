# IMP-Stuff


cat all.txt | awk -F ">" '{print $1'} | awk -F "<" '{print $2'}

:%s/old-text/new-text/g


########Prepend file
sed -i '1s;^;#Auther:\tYuvraj Hole\n#Emp-Code:\t16302\n;' input.txt

sed -i '1s;^;############### Auther:\tYuvraj Hole ################\n################ Emp-Code:\t16302 ###############\n;' mysql.cfg.bkp

Whole Word Subsitution

:s/\<his\>/her/

:1,10s/helo/hello/g


++++++++++DOCKER++++++++++++++++

docker run -it --dns=8.8.8.8 --dns-search="mydomain.local" --name="mycontainer3" -v /local_vol -v /home/tcox/docker/mydata:/remote_vol docker.io/ubuntu:latest /bin/bash

https://aws.amazon.com/blogs/security/how-to-automatically-tag-amazon-ec2-resources-in-response-to-api-events/

##http://docs.sonarqube.org/display/PLUG/LDAP+Plugin#LDAPPlugin-Configuration


sonar.security.realm=LDAP
#Made it false so that every time it will go to AD only for authentication
sonar.security.savePassword=false
ldap.url=ldap://172.27.173.209:3268
ldap.bindDn=CN=Yuvraj Hole,CN=Users,DC=evolvingsols,DC=com
ldap.bindPassword=Rediff%$21
#changed to domain name instead of ip
ldap.realm=evolvingsols.com


# User Configuration
ldap.user.baseDn=cn=Users,dc=Evolvingsols,dc=com
ldap.user.request=(&(objectClass=user)(sAMAccountName={login}))
ldap.user.realNameAttribute=cn
ldap.user.emailAttribute=mail



++++Ubuntu static IP+++++++

auto eth0
iface eth0 inet static
address 172.27.59.25/24
gateway 172.27.59.1
dns-nameservers 172.27.172.12 172.27.172.10
