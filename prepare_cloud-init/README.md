### Ubuntu 18.04 Guest Preparation for vSphere environment
This project is to demonstrate how to properly clean up OS instance for cloud-init. This template has been tested against
* Ubuntu 18.04
* vSphere 6.7U2
* Cloud Assembly (SaaS) version on 2019/07/01
The idea comes from [this link](https://jimangel.io/post/create-a-vm-template-ubuntu-18.04/)

#### I add an input to allow customized hostname as follows:
```
sed -i 's/preserve_hostname: true/preserve_hostname: false/g' /etc/cloud/cloud.cfg
```
