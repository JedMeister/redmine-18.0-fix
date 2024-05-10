This is a destructive script to deal with a freshly installed Redmine appliance
which suffers from inital MariaDB database corruption on reboot.

Warning - this will wipe all MariaDB database, including Redmine.
-----------------------------------------------------------------

Database data you wish to keep should be recovered and backed up **BEFORE**
running this script!

The user will be asked to reset Redmine password & email and set a password for
the (new) 'mariadb_admin' MariaDB account (for use in Webmin).

All MariaDB data will be nuked and MariaDB will be reconfigured to a fresh
install state. Required DBs abd DB users will be recreated and appropriate
permissions granted. The Redmine DB structure will be reloaded and Redmine will
be as per a fresh install. Webmin will be reconfigured to use the
'mariadb_admin' DB user and the password will be pre-filled.

To download and run:

	wget https://raw.githubusercontent.com/JedMeister/redmine-18.0-fix/master/redmine-fix
	chmod +x redmine-fix
	./redmine-fix
