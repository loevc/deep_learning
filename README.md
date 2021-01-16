# deep_learning
note the study proccess
> 为表述清晰，在掌握英文之前，尽量使用中文

# 首先是关于环境的安装和配置
这里使用的结构是

ubuntu16.04

CUDA + cuDNN + Anaconda + PyCharm

CUDA 是基于Nvidia显卡的 我所使用的是 GEFORCE RTX 2060 (notebooks）

查看显卡信息
```
$ lspci | grep -i nvidia
```

```
$ nvidia-smi
```
> 若无显示 则说明显卡驱动尚未安装

在nvidia官网下载对应版本的驱动

在ubuntu16.04中 会默认安装nouveau驱动

禁用nouveau驱动

$ sudo vim /etc/modprobe.d/blacklist.conf 
> 在最后加上 
```
blacklist nouveau
options nouveau modeset=0
```
update (because aborted nouveau)
```
$ sudo update-initramfs -u 
```

reboot the ubuntu 

verity nouveau 是否禁用成功

```
$ lsmod | grep nouveau
```
若无显示 则成功




##  alt + ctrl + f1  进入命令行模式

that will ask you type **account**&**passwd**
i login by loevc(my usr name)



close the graph surface
```
$sudo service lightdm stop
```


if installed nvidia drivers
```
$ sudo apt-get remove nvidia-*
```


cd path that saving the nvidia drivers




 





















