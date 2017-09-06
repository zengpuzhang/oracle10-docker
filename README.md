# Oracle-xe-10g in Docker
====================

This project is based on Kristian Du's <kristian.du@gmail.com> project [dkfi/docker-oracle-xe-10g](https://github.com/dkfi/docker-oracle-xe-10g) which is also based
on the work done by Wei-Ming Wu <wnameless@gmail.com> on
[wnameless/docker-oracle-xe-11g](https://github.com/wnameless/docker-oracle-xe-11g)

Oracle Express Edition 10g Release 2 (10.2.0.1) 32-bit on Debian 7.0 Wheezy.


## Usage

```console
docker-compose up -d
```

Connect database with following setting:

```
hostname: localhost
port: 49161
username: system
password: oracle
```

For example, connect to database with sqlplus:

```console
sqlplus system/oracle@localhost:49161
```

Password for SYS & SYSTEM
```
oracle
```

Login by SSH

```console
ssh root@localhost -p 49160
password: admin
```

Login to web administrator on a browser:
```
http://localhost:49162/apex
```

## Run SQL Scripts
This Docker container shares a volume located at /scripts. 
You can run scripts inside of the oracle system by first SSHing, launching SQL plus, then using the script command: 

```console
ssh root@localhost -p 49160
sqlplus
@scripts/example.sql
```
