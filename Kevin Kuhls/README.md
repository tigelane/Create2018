#WS47B - Yes, You C'Ansible


# BYOD Requirements

## Prereqs
This workshop will require several components:

* Infrastructure devices - You will receive credentials during the session to access your own dcloud infrastructure pod.
* A developer workstation with Ansible and git loaded. There are several options for this listed by preference:
  * Run our developer container locally using Docker, and your preferred text editor
  * Use the Ubuntu host in your dcloud pod. Access will require either VPN with AnyConnect or Openconnect (preferred) or via https Guacamole client
  * Run Ansible natively on your Linux or OSX workstation. Due to the workshop time constraints, we will most likely not be able to assist with any troubleshooting if you choose this option.

## Setup information


### Docker container:
This option is ideal for users using OSX, Linux, or Windows 10 with virtualization support. This typically excludes Home edition, laptops without virtualization support enabled, and Windows 8 and older.

* Install [Docker for Mac](https://docs.docker.com/engine/installation/mac/) or [Docker for Windows](https://docs.docker.com/engine/installation/windows/) or [Docker for Linux ](https://docs.docker.com/engine/installation/linux/ubuntu/)
* Install your preferred text editor. Popular options include PyCharm, Sublime, Atom, TextWrangler, vim, Notepad++

Once installed, we will walk you through downloading and running our developer container during the workshop.


### Ubuntu jumphost:
This option works best with a local VPN client, but can work without if needed.

* With VPN:
  * Install [Cisco AnyConnect](https://devnetsandbox.cisco.com/Docs/VPN_Access/AnyConnect_Installation_Guide.pdf) or OpenConnect
  * Install VNC client such as [RealVNC](https://www.realvnc.com/en/connect/download/viewer/)
* Without VPN:
  * Install a modern web browser


### Local Install:
This option will assume you have OSX or Linux, and have a solid knowledge of package management for your platform.

* Install Ansible 2.5
Install git
* Install [Cisco AnyConnect](https://devnetsandbox.cisco.com/Docs/VPN_Access/AnyConnect_Installation_Guide.pdf) or OpenConnect
* Install your preferred text editor. Popular options include PyCharm, Sublime, Atom, TextWrangler, vim

###Pods:
* [Pod3](https://v132user1:d44cbc@portal.vpod132.dc-05.com:8443/dcloud)
* [Pod4](https://v187user1:2d0919@portal.vpod187.dc-05.com:8443/dcloud)
* [Pod5](https://v198user1:62a971@portal.vpod198.dc-05.com:8443/dcloud)
* [Pod6](https://v215user1:b59ffd@portal.vpod215.dc-05.com:8443/dcloud)
* [Pod7](https://v206user1:ce5a54@portal.vpod206.dc-05.com:8443/dcloud)
* [Pod8](https://v194user1:dc9af3@portal.vpod194.dc-05.com:8443/dcloud)
* [Pod9](https://v242user1:92451@portal.vpod242.dc-05.com:8443/dcloud)
* [Pod10](https://v335user1:5aa769@portal.vpod335.dc-05.com:8443/dcloud)
* [Pod11](https://v413user1:f09cce@portal.vpod413.dc-05.com:8443/dcloud)
* [Pod12](https://v449user1:2ff00f@portal.vpod449.dc-05.com:8443/dcloud)
* [Pod13](https://v458user1:56379a@portal.vpod458.dc-05.com:8443/dcloud)
* [Pod14](https://v617user1:e2b404@portal.vpod617.dc-05.com:8443/dcloud)
* [Pod15](https://v659user1:cba86d@portal.vpod659.dc-05.com:8443/dcloud)
* [Pod16](https://v788user1:80e493@portal.vpod788.dc-05.com:8443/dcloud)
* [Pod17](https://v416user1:a0d5bf@portal.vpod416.dc-05.com:8443/dcloud)
* [Pod18](https://v653user1:1cf3ce@portal.vpod653.dc-05.com:8443/dcloud)
* [Pod19](https://v914user1:323626@portal.vpod914.dc-05.com:8443/dcloud)
* [Pod20](https://v998user1:7fa1b9@portal.vpod998.dc-05.com:8443/dcloud)
* [Pod21](https://v982user1:73e30f@portal.vpod982.dc-05.com:8443/dcloud)
* [Pod22](https://v1060user1:b849df@portal.vpod1060.dc-05.com:8443/dcloud)
* [Pod23](https://v1071user1:ed74f6@portal.vpod1071.dc-05.com:8443/dcloud)
* [Pod24](https://v1133user1:7b4c0f@portal.vpod1133.dc-05.com:8443/dcloud)
* [Pod25](https://v1123user1:b6075f@portal.vpod1123.dc-05.com:8443/dcloud)
* [Pod26](https://v1267user1:d2b8fa@portal.vpod1267.dc-05.com:8443/dcloud)
* [Pod27](https://v1315user1:1b97af@portal.vpod1315.dc-05.com:8443/dcloud)
* [Pod28](https://v1390user1:b892ab@portal.vpod1390.dc-05.com:8443/dcloud)
* [Pod29](https://v1410user1:858221@portal.vpod1410.dc-05.com:8443/dcloud)
* [Pod30](https://v1461user1:ed93c8@portal.vpod1461.dc-05.com:8443/dcloud)


### Setup:

* docker pull kuhlskev/ansible_vpn:1.0
### Windows: 
* docker run -it --rm --privileged –v %cd%:/home/docker kuhlskev/ansible_vpn:1.0
### OSX/Lin: 
* docker run -it --rm --privileged –v "$(pwd)":/home/docker kuhlskev/ansible_vpn:1.0
