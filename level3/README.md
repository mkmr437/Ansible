Write a playbook.yml under /home/thor/ansible directory on jump host, an inventory file is already present 
under /home/thor/ansible directory on jump host itself. Using this playbook accomplish below given tasks:


1.Create an empty file /opt/devops/blog.txt on app server 1; its user owner and group owner should be tony. 
  Create a symbolic link of source path /opt/devops to destination /var/www/html.


2. Create an empty file /opt/devops/story.txt on app server 2; its user owner and group owner should be steve.
   Create a symbolic link of source path /opt/devops to destination /var/www/html.


3. Create an empty file /opt/devops/media.txt on app server 3; its user owner and group owner should be banner.
   Create a symbolic link of source path /opt/devops to destination /var/www/html.




# Managing ACL's
## There are some files that need to be created on all app servers in Stratos DC. The Nautilus DevOps team want these files to be owned by user root only however, they also want that the app specific user to have a set of permissions on these files. All tasks must be done using Ansible only, so they need to create a playbook. Below you can find more information about the task

Create a playbook named playbook.yml under /home/thor/ansible directory on jump host, an inventory file is already present under /home/thor/ansible directory on Jump Server itself.

### Create an empty file blog.txt under /opt/data/ directory on app server 1. Set some acl properties for this file. Using acl provide read '(r)' permissions to group tony (i.e entity is tony and etype is group).


### Create an empty file story.txt under /opt/data/ directory on app server 2. Set some acl properties for this file. Using acl provide read + write '(rw)' permissions to user steve (i.e entity is steve and etype is user).


### Create an empty file media.txt under /opt/data/ on app server 3. Set some acl properties for this file. Using acl provide read + write '(rw)' permissions to group banner (i.e entity is banner and etype is group).
