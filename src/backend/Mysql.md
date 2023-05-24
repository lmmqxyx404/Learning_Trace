# watch out
first you must start the mysql service, then you can connect it.

# In windows,first you must start up mysql service
net start mysql
net stop mysql

# add big files(my.ini)
max_allowed_packet=64M

# some frequent command
The operations of most databases are similar to the tables;
## create a table
CREATE TABLE IF NOT EXISTS `player`(
   `player_id` VARCHAR(40) ,
   `part_id` VARCHAR(40) ,
   `job_name` VARCHAR(40) ,
   `charac_name` VARCHAR(40) ,
   `uin` VARCHAR(40) ,
   `contact_uin` VARCHAR(40)
)ENGINE=InnoDB DEFAULT CHARSET=utf8;

## link the mysql
mysql -u root -p

##
show databases;
## 
use tablename;
select database();

## create a table
create table tablename(
  id type(4 length ) not null primary key auto_increment,
  year date
)                     
: create a table

## import a mysql
source pathname; //The path should be originated from the root 

## crud operation in a table
drop table tablename  //delete the table
truncate table table_name // clear a table
insert into tablename values (value); // create
delete from tablename where condition;  //delete
update tablename set attr='new value',… where condition  //update
```
update type set icon="<SmileOutlined />" where Id=3;
update type set icon="<LikeOutlined />" where Id=99;

```
select * from tablename where condition  //Retrieve
## rename
rename table previous tablename to latest tablename;
## exit
exit
## show mysql port
show global variables like 'port';
show global variables like '%secure_file_priv%';

## export data to outfile "D:\mine.xls"
before you export, tou must set the secure_file_priv=''
```select * from table_name into outfile "D:\mine.xls";```

watch out:
when you attempt to import a backup sql to a new environment, you should install mysql.
Then you should create a database and use it.At last, you can use source command.