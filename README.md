# Install Rapid7 Agent on Windows

This was originally for integrating as a [Ludus](https://ludus.cloud) role but should work stand-alone without any modification
- Copy installer image to files directory
- Update tasks/main.yml with filename

* For stand alone usage
To store install token, create the file ~/secrets.yml and populate the 'r7_customer_agent_key' variable with your Rapid7 customer agent key:
```
r7_customer_agent_key: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

* For Ludus usage, this file must be in the ludus user home directory (typically /home/ludus).
