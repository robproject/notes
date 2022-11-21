---
id: enjb2w7wdyo2wyg7ek23500
title: Frappe Framework
desc: ''
updated: 1660082665282
created: 1640382050940
---
## Custom App
General rules:
1. Position important and mandatory fields in top left
2. Have less than 6 fields in a section
3. Default values
4. All related items in dashboard
5. Section headings designate new sections
6. Avoid buttons; fetch automatically on select instead. If required, place in toolbar
7. Functions and methods need to be less than 10 lines of code. Anything larger needs to become a class.

Doctype Naming Is Title Case And Singular
Child Table Naming requires the parent doctype to be named, followed by the relation

Field Names Are Title Case, Link Name == Doctype Name
Table names are plural, only relation.
Vars must be descriptive

### Creating Doctypes
Don't check 'custom?' as this is only for users without access to server-side operations
<https://discuss.erpnext.com/t/custom-checkbox/6386/3>


### User Translations
Javascript user traslation   
`__("sample translation")  `

Python user translation  
`_("sample translation") `

### WebApp Architecture
![](/assets/images/2021-12-24-13-42-25.png)


## Developer Setup
### Docker Dev Setup  
Setup and add user according to instructions below
![[computer.docker#wsl-setup,1:#*]]

https://github.com/frappe/frappe_docker/tree/main/development

Inside of each bench:
	./env/bin/pip install honcho

If stuck on screen "your system is being updated…"
bench set-config maintenance_mode 0

From <https://discuss.erpnext.com/t/oyour-system-is-being-updated-please-refresh-again-after-a-few-moments-after-running-bench-migrate/40197/26

bench use mysite.localhost
after site creation, logout then login as admin

### URL
mysite.localhost:8000  

### DB Restore with files in frappe-bench/
bench --site [mysite] restore [db.sql]  
bench --site [mysite] set-admin-password [password]

### Dev Setup from Azure VHD
From Debian server, installed via easyinstall script
1. Use Azure storage explorer to download vhd
2. Create hyper-v VM, same ram, default network adapter
3. Remove SSL to access from browser Instructions
```
	   1. bench config dns_multitenant off
	   2. bench setup nginx
	   3. sudo service nginx reload
```	
	   From <https://discuss.erpnext.com/t/remove-ssl-setup-and-return-to-port-based-multitenancy/44234> 
	
4. Sudo apt-get install samba
5. Su root, smbpasswd -a erpadmin
6.  vim /etc/samba/smb.conf
	[newshare]
	path = /home/
	browseable = yes
	read only = no  
	guest ok = yes
7. Su erpadmin  
8. Sudo chmod -R 777 /home
9. Host - network discovery/sharing turn on
10. Login via erpadmin@erpnextvm (or other vm name), password


## Docker Production Setup
### Traefik Config
TRAEFIK_DOMAIN=traefik.your_site.com
EMAIL=your_email@your_site.com
HASHED_PASSWORD={filled}


## Common Commands
### New Site
bench new-site mysite.localhost --mariadb-root-password 123 --admin-password admin --no-mariadb-socket