### Run A Service without sudo permission. (Suppose service name is docker)

```
sudo usermod -aG docker ${USER}
```
User will need to re-login or type the following command to take the effect of above command
```
su - ${USER}
```
