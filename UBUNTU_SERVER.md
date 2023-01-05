### Run A Service without sudo permission for the current user. (Suppose service name is docker)

```
sudo usermod -aG docker ${USER}
```
User will need to re-login or type the following command to take the effect of above command
```
su - ${USER}
```

### Give all permissions to a specific foler and sub folers to all the users
```
sudo chmod -R a+rwx path
```

### Cheat Sheet
1. List available users `cut -d: -f1 /etc/passwd`
2. Add new user `sudo useradd user_name`
