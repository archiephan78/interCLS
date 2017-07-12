## Install software
### Red Hat
#### `rpm -i` <packet.rpm>
+ `-e` : unistall packet 
+ `-U` : install new packet or upgrade
+ `-V` : verifies a packet
+ `-h` : hiển thị hash 
#### `yum` install < packet name >
+ `update/upgrade`
+ `remove`
+ `check-update`
+ `list` ; `search` ; `info`

### Debian 
#### `dpkg -i` <packetfile.deb/packet name>
+ `-r` remove 
+ `-P` purge : xóa packet + config file
+ `-p` information của packet đã cài
+ `I` info packet đã xóa
#### `apt-get` install <packet name>
+ `update`
+ `upgrade`
+ `remove`
+ `autoremove`
+ `autauclean`
#### add software source
 ``` 
     sudo vi /etc/apt/sources.list
     sudo apt-get update
     sudo apt-get install [packetname]
  ```
 
 ##### Hay
  ```
    sudo add-apt-repository deb http://any.com
    sudo apt-key add<downloaded-keyfiles>
   sudo add-apt-repository ppa<lp-user>/<ppa-name>
    sudo apt-get update
   ```
