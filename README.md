# wireshark-ubuntu-installation

# Add the stable official PPA. To do this, go to terminal by pressing Ctrl+Alt+T and run:
```
sudo add-apt-repository ppa:wireshark-dev/stable

```

# Update the repository:
```
sudo apt-get update

```

# Install wireshark 2.0:
```
sudo apt-get install wireshark

```


# Run wireshark:
```
sudo wireshark

```

- If you get an error couldn't run /usr/bin/dumpcap in child process: Permission Denied, go to the terminal again and run:
```
sudo dpkg-reconfigure wireshark-common

```

- Say YES to the message box. This adds a wireshark group. Then add user to the group by typing

```
sudo adduser $USER wireshark

```

- Then restart your machine and open Wireshark. It works. Good Luck.
- Open terminal and type the commands:
```
    sudo apt-get install wireshark
    sudo dpkg-reconfigure wireshark-common
    sudo adduser $USER wireshark
    wireshark
```
- If you getting wireshark running error, so close it and then just do the following:
```
    Go to usr/share/wireshark
    Open init.lua with a text editor
    Change disable_lua = false to disable_lua = true
```
