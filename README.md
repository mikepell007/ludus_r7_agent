# Install SentinelOne Agent on Windows

This was originally for integrating as a [Ludus](https://ludus.cloud) role but should work stand-alone without any modification
- Copy installer image to files directory
- Update tasks/main.yml with filename

* For stand -lone usage
To store install token, create the file ~/secrets.yml and populate the 'sentinel_one_install_token' variable with your Sentinel One install token:
```
sentinel_one_install_token: xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

* For Ludus usage, this file must be in the ludus user home directory (typically /home/ludus).
