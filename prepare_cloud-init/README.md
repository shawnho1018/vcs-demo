### Ubuntu 18.04 Guest Preparation for vSphere environment
This project is to demonstrate how to properly clean up OS instance for cloud-init. This template has been tested against
* Ubuntu 18.04
* vSphere 6.7U2
* Cloud Assembly (SaaS) version on 2019/07/01
The idea comes from [this link](https://jimangel.io/post/create-a-vm-template-ubuntu-18.04/)

#### How to use this project?
1. Please install freshly from Ubuntu 18.04 iso file: The tested iso version is ubuntu-18.04.2-live-server-amd64.iso.
2. `Git clone` or Simply add this `cleanup.sh` file into the resulting VM. 
3. Using vSphere mechanism to convert VM to Template.
4. Use this template as the basis of vCloud Assembly template.  

Compared to earlier work (as shown in the previous link), I add an input to allow customized hostname as follows:
```
sed -i 's/preserve_hostname: true/preserve_hostname: false/g' /etc/cloud/cloud.cfg
```
