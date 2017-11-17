# Linux

### 用户管理

- 添加用户

  ```bash
  sudo useradd ykg -m # -m is to create the home dir for this user
  sudo passwd ykg
  sudo adduser ykg sudo # add user to sudo group
  ```

### 文件系统

- `/usr` 目录
   
   > Pronounced as “user,” but this subdirectory does not contain user files.

   >  `/usr` is a large directory hierarchy that looks a little like the root. 

   > The bulk of the Linux system resides in  `/usr` .

   > The primary reason that the root does not contain the complete system is to **keep space requirements low**.

- 获取`symbolic link file`本身的内容

  ```bash
  readlink *<foo>*  # -n for no-newline
  ```

### 关机/重启

  ```shell
  shutdown -h now # 关机，h表示halt程序
  shutdown -r     # 重启，r表示reboot程序
  ```

### 网络

- 应用更新后的配置

  ```shell
  ifdown eth0; ifup eth0;  # (re)initialize the network interface
  ```

- 修改IP地址、掩码、网关、DNS

  ```shell
  ifconfig eth0 *<address>* *<netmask>*
  route add default gw *<gw-address>*
  ```

  IP/MASK/GW可以修改`/etc/network/interfaces`文件
  DNS的设置是直接修改`/etc/resolv.conf`文件

- DHCP

  ```
  allow-hotplug eth0
  iface eth0 inet dhcp
  ```

- 静态IP

  ```
  allow-hotplug eth0
  iface eth0 inet static
  address 192.168.11.100
  netmask 255.255.255.0
  gateway 192.168.11.1
  ```

- 参考资料
  [Debian Reference -- Network setup][1]




[1]: http://www.debian.org/doc/manuals/debian-reference/ch05.en.html
