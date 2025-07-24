# Install Rapid7 Agent on Windows

This was originally for integrating as a [Ludus](https://ludus.cloud) role but should work stand-alone without any modification
- Copy installer image to files directory
- Update defaults/main.yml with filename (r7_agent_installer_image)

* For stand alone usage
To store install token, create the file ~/secrets.yml and populate the 'r7_customer_agent_key' variable with your Rapid7 customer agent key:
```
r7_customer_agent_key: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

* For Ludus usage, this file must be in the ludus user home directory (typically /home/ludus).

# Ludus Howto
* On your ludus host, clone the repo

```git clone https://github.com/mikepell007/ludus_r7_agent.git```
* Download the installer image from the provider and copy into the files folder

```cp agentInstaller-x86_64.msi ludus_r7_agent/files```
* Edit ludus_r7_agent/defaults/main.yml and change *r7_agent_installer_image* to the name of the .msi downloaded earlier
* Install the role (*-g* is optional if you want it installed for all users)

```ludus ansible role add -g -d ludus_r7_agent```
* Edit/create **/home/ludus/secrets.yml** (sudo or from a root proxmox shell) and change *r7_customer_agent_key* to your specific key from R7

```r7_customer_agent_key: <put your key here>```
* Add the ludus_r7_agent role to your Windows hosts in your range configuration.  Use ludus_r7_agent/r7.yaml as a guide.  
