## 如何升级或更新 Debian Pi Aarch64 系统

### 重要：

**我们发布的更新或软件包根据实际情况一般通常采用 tag、zip、tar.gz、xz 的压缩格式发布**

**你必须至少安装了对以上压缩格式软件的支持，强烈建议通过下面的命令一键安装以上所有软件包的支持**

安装过程要求你的树莓派已连接网络并能够访问互联网

```shell
apt update ; apt install tar gzip zip unzip bzip2 xz-utils -y
```
----

### 升级系统固件及驱动

**请前往 [此处](https://pan.baidu.com/s/1-NY_WL5LB0stpxT1wAKSaA)**

* 打开"***Debian-Pi-Aarch64-Kernel-Firmware***"文件夹，

* **下载最新的升级包** (根据年月日判断，如2019-01-02)

> 如：***upkg-2019-01-02-v2019-1.0-u1.zip***

* 上传到你的树莓派系统，解压这个升级包

```shell
unzip upkg-2019-01-02-v2019-1.0-u1.zip

# 注意：这里的 upkg-2019-01-02-v2019-1.0-u1.zip 以你实际下载的文件名为准
```
* 解压完成后执行以下命令

```shell
cd ./upkg
sudo  sh  ./sys_upgrade
```

* **然后重启系统，完成升级**

### 更新系统

更新系统无需额外操作，直接使用最新的**Debian**系统仓库更新即可，通过以下命令进行系统更新

```shell
apt update ; apt upgrade -y
```