# INSTALL MYSQL MAC

###how to locate your 'php.ini' file
the '/' indicate that we want to search from the filesystem root

```
mdfind php.ini
````

###it is possible that apache don't use any php.ini file
you can verify by launching the php command php_info();
look at the field 'Loaded Configuration File' -> it may be written : /etc/php.ini or nothing at all

###how to add the mysql path to PATH environment variable
edit the file '/etc/paths'

```
add the following path : /usr/local/mysql/bin
```

###resolve the socket problem
in /etc/php.ini, verifiy that the following attribute is well set as below

```
mysql.default_socket = /tmp/mysql.sock
```

###usual problem with mysql.sock
php attempt to reach a file located at /var/mysql/mysql.sock but
the file is elsewhere : /tmp/mysql.sock.
create a symbolic link to resolve this php problm
ln -s {dest} {link-name}

```
ln -s /tmp/mysql.sock /var/mysql/mysql.sock
```

#HOW TO RESET ROOT PASSWORD IN MYSQL

###stop mysql service
```
sudo /usr/local/mysql/support-files/mysql.server stop
````

###start mysql deamon in safe mode
```
sudo mysqld_safe --skip-grant-tables
```

###start mysql client mode root
```
mysql -u root
````

###swith to table mysql
```
use mysql
```
###change password with the field 'authentication_string'
```
update user set authentication_string=password('root') where user='root';
```
