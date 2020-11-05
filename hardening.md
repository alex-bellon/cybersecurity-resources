# Hardening

## Linux
- [How to Secure a Linux Server](https://github.com/imthenachoman/How-To-Secure-A-Linux-Server)

## SQL
- https://medium.com/linode-cube/5-essential-steps-to-hardening-your-mysql-database-591e477bbbd7
- https://www.techrepublic.com/article/how-to-harden-mysql-security-with-a-single-command/
- https://www.tecklyfe.com/harden-mysql-server/

### [5 Steps to hardedning your MySQL database](https://medium.com/linode-cube/5-essential-steps-to-hardening-your-mysql-database-591e477bbbd7)
- Setup with `mysql_secure_installation` - takes care of most of this for you!
- Set strong passwords and change default passwords
  - `sudo mysqladmin password`
  - Unfortunately, MySQL runs background tasks as that root user. These tasks will break once you set a password, unless you take the additional step of hard-coding the password into the /root/.my.cnf file:
  ```
  [mysqladmin]
  user = root
  password = yourpassword
  ```
  Make sure to restrict access to that file
  ```
  $ sudo chown root:root /root/.my.cnf
  $ sudo chmod 0600 /root/.my.cnf
  ```
- Remove unnecessary users
  - Remove anonymous user
  ```sql
  > drop user “”@”localhost”;
  > flush privileges;
  ```
- Only grant access to the needed databases
  ```sql
  > grant all privileges on mydb.* to someuser@”localhost” identified by ‘astrongpassword’;
  > flush privileges;
  ```
  - You can also grant specific privileges (select, drop, delete, etc.)
- Enable TLS
  - Once you have valid certs, add this to my.cnf
  ```
  [mysqld]
  ssl-ca=/path/to/ca.crt
  ssl-cert=/path/to/server.crt
  ssl-key=/path/to/server.key
  ```
  - Also, make sure the SSL cipher suites are strong ones

### [Harden MySQL Server](https://www.tecklyfe.com/harden-mysql-server/)
- Set connection error limit
  - Bans people after `x` failed login attempts
  - Edit the configuration file `my.cnf` and set `max_connect_errors`:
    - `max_connect_errors = 5`
- Disable load data local infile
  - The LOAD DATA LOCAL INFILE command allows users, or an attacker, to read local files and even access other files on the operating system.
  - Edit the configuration file `my.cnf` and set `local-infile`:
    - `local-infile=0`
- Disable show databases
  - Edit `my.cnf` and add `skip-show-database` to the `[mysqld]`` section:
  ```
  [mysqld]
  skip-show-database
  ```
- Bind MySQL to localhost
  - Edit `my.cnf`:
    - `bind-address = 127.0.0.1`
- Privilege hardening
  - Each application that uses MySQL should have its own user that only has limited privileges and only has access to the databases it needs to run.
  - Never use `ALL TO ..`
  - Never use % for a hostname
  - Application user permissions should be restrictive as possible
  - Only allow super privileges to dba accounts, and localhost
  - Never ever give users global privileges, except for root, backup user, monitoring user, replication user
  - Take extra caution when granting SUPER or FILE privileges: SUPER can modify runtime configuration and become other users, FILE allows reading or writing files as MySQL process
- Rename root user
  ```mysql
  RENAME USER 'root'@'localhost' TO 'foobar'@'localhost';
  FLUSH PRIVILEGES;
  ```

## Tools
- [flan](https://github.com/cloudflare/flan) - Flan Scan is a lightweight network vulnerability scanner.
