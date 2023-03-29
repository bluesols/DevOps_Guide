1. Add a new User `adduser username`
2. List all users `cat /etc/passwd`
3. Add a group `groupadd mygroup`
4. Add user to group `usermod -aG group_cicd github`
5. Delete a group `groupdel mygroup`
6. Create a directory if doesn't exists `mkdir -p path`
7. `chown github_user:sites -R /var/www/html`
8. Check permissions for a specific directory `ls -l <path>`
9. `id root` or `id` to get group, user ids details of any user or current user
10. `grep <search_word> <file_path>` to search a word from file
11. 


We are using `github_user` user for all github ci/cd deployments. This user is a member of `sites_group` group. And this group has all necessary permissions to files, folders and services

