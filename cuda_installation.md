```
wget https://developer.download.nvidia.com/compute/cuda/10.1/Prod/local_installers/cuda_10.1.243_418.87.00_linux.run
sudo sh cuda_10.1.243_418.87.00_linux.run
```
install failed

查看cuda与显卡驱动版本

https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html

此次选择不安装驱动，安装成功！（软连接为更新）


关于切换版本的方法

建议使用.run文件安装

> accept
if 之前安装了更高版本的驱动  -> 则此次不安装驱动
toolkit -> yes
  location => default
  update symplic -> no
  install samples -> yes

安装完成后在/usr/local/下可以看见
cuda-10.0
cuda-10.1
cuda

switch method
将 ~/.bashrc 下与cuda相关的路径都改为/usr/local/cuda   而不使用 /usr/local/cuda-10.0 or /usr/local/duda-10.1
此时  切换版本只需要更新软链接即可
切换至10.0
rm -rf /usr/local/cuda 
ln -s /usr/local/cuda-10.0 /usr/local/cuda
切换至10.1
rm -rf /usr/local/cuda 
ln -s /usr/local/cuda-10.1 /usr/local/cuda




