ssh-keygen
eval $(ssh-agent -s)
ssh-add <(cat ~/.ssh/id_rsa | tr -d '\r')
echo "$SSH_PRIVATE_KEY" | ssh-add -


### In case Error Permissions 0644 are too open for the <Private_Key> use the below command to set the permissions
sudo chmod 600 <path_to_private_key>


## Github Use SSH KEY
Using a specific private key for a git repository. If you want to use that key for all repositories. Then use --global tag
```
git config --local core.sshCommand "/usr/bin/ssh -i /home/me/.ssh/id_rsa_foo"
```

```
git clone -c core.sshCommand="/usr/bin/ssh -i /home/me/.ssh/id_rsa_foo" git@github.com:me/repo.git
```

### Configure You User's Name and User's Email info
To Configure Email and User's Name for Specific Repository. Type the following commands in the projects root directory.
1. `git config --local user.name "Your Name"
2. `git config --local user.email "Your Email"

To configure this globally on your machine. Type the above commands any where on your machine. Just replace `--local` with `--global`
