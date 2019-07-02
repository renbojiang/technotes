
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
sudo su
sudo echo "10.35.136.250 git.autodesk.com">>/etc/hosts
sudo su ec2-user
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTkxNTkwMzMxMiwtMTk5MDU0NTY3Ml19
-->