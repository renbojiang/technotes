# CI Operation

 ## Update resolve.conf
 ssh to acadci-manager.ecs.ads.autodesk.com and then
 - run ```sudo su``` to switch to root
 - edit /etc/dhcp/dhclient.conf to remove **domain-server** and **domain-search** from it
 - run ```dhclient eth0```
 - run ```cat /etc/resolve.conf``` to verify there is no **search ecs.ads.autodesk.com** in the conf file
 
 
  

