## Change Default IP Address in Docker Container

To change the default IP address used by Docker containers, follow these steps:


```
sudo -i
vim /etc/docker/daemon.json
```
Edit the Configuration:

```
{
  "bip":"192.168.1.1/24"
}
```
Restart Docker:

`sudo systemctl restart docker` <br>
OR <br>
`service docker restart`
