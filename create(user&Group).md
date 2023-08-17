This is a markdown file for Exercise on Creating user and groups in Linux systems. 

## EXERCISE

1. create a user, set an expiry date for the user, such that the account expires after 2 weeks. 

2. prompt the user to change password after log-in

3. Attach the user to a group called Altschool.

4. Allow Altschool group to only run cat command on /etc/directory.

5. create another user, make sure the user doesnt have a home directory.


### SOLUTION 

1. create a user using the useradd command 
~~~ 
sudo useradd Rawlings
~~~


To set an expiry date for a specific user, you can use the usermod command followed by the -e flag (expiry flag), then the expiry date in YYYY-MM-DD format, and then the name of the user to set the expiry date in Linux.

~~~
sudo usermod -e 2023-08-31 Rawlings

~~~


![Alt text](<Images/user expiry date.png>)


2. prompt a user to change password after log-in

To prompt a user to change his/her password , the user password must have expired. to force a user password to expire, you make use of the passwd command specifying the -e tag which means expire. 

~~~
passwd -e Rawlings

~~~

![Alt text](<Images/Set user password to expire.png>)


To verify the user's password expiration information, we use the **Chage command**

~~~
chage -l Rawlings
~~~

![Alt text](<Images/passwd change.png>)

3. Attach the user to a group called Altschool.

i. create a new group by using the **groupadd command**

~~~
sudo groupadd Altschool
~~~

ii. Add the user to the new group created using the **usermod command**

~~~
sudo usermod -aG Altschool
~~~

![Alt text](<Images/user added to Altschool Group.png>)

4. Allow Altschool group to only run **cat command** on /etc/directory

This is made possible by editing the sudoer file

![Alt text](<Images/allow Altschool grp run only cat cmd.png>)


5. Create another user make sure this user doesn't have a home directory. 

To create a user without their home directories, **-M** is used example
~~~
useradd -M Chukwudi
~~~
![Alt text](<Images/User without a home directory.png>)
