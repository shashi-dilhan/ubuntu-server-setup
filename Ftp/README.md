# FTP Accounts & Users

## User groups

Create a user group

    $ sudo groupadd new_group_name
    
Delete user group

    $ sudo groupdel group_name
    
Add user to a group

    $ sudo adduser user_name user_group
    
Delete user from group

    $ sudo deluser user_name user_group
    
Check user groups

    $ sudo vim /etc/group
    
## FTP user create

Add user

    $ adduser user1
    
Set home directory for the user

    $ sudo usermod -d /var/www/test -m user1
    
Block shell access for the user

    $ usermod -s /sbin/nologin user1
    
Set folder permissions

    $ chown -R user1:www-data html
    
[Tutorial](https://www.youtube.com/watch?v=A1czbNwd2R4&t=0s&index=14&list=PLxfL_LqcdOLzc7xGcqrv4Hw_5uucdQx35)