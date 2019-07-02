
## Amazon Linux AMI 2018.03.0 (HVM)
- Docker Installation
```bash
sudo yum install docker
sudo gpasswd -a ${USER} docker
sudo reboot
# sudo usermod -a -G docker $USER
```
- Fix unresolved: git.autodesk.com 
```bash
sudo echo "10.35.136.250 git.autodesk.com">>/etc/hosts
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5OTA1NDU2NzJdfQ==
-->