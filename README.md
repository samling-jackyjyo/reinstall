# reinstall
一个一键重装脚本

#### 亮点:
```
使用官方安装方式，非第三方 dd 镜像，更安全（也提供 dd 功能）
支持 BIOS/EFI 机器，支持 ARM 机器
可能是第一个支持在 1g 内存上安装 红帽 7/8/9 系列的脚本
可能是第一个支持重装到 ubuntu 22.04 的脚本
可能是第一个支持重装到 alpine 的脚本
可能是第一个支持重装到 Windows 的脚本（不算 dd 的话）
```
#### 使用:
```
下载:
curl -O https://raw.githubusercontent.com/bin456789/reinstall/main/reinstall.sh

安装 Linux: 
bash reinstall.sh centos-7 (或其他系统)

安装 Windows:
bash reinstall.sh windows --iso=https://example.com/zh-cn_windows_10_enterprise_ltsc_2021_x64_dvd_033b7312.iso --image-name='Windows 10 Enterprise LTSC 2021'

dd:
bash reinstall.sh dd --img=https://example.com/xxx.gz

重启:
reboot
```
#### 支持重装到:
```
centos-7/8/9 (centos 8/9 为 stream 版本)
alma-8/9
rocky-8/9
fedora-37/38
ubuntu-20.04/22.04
alpine-3.16/3.17/3.18
debian-10/11
windows (见下方注意事项)
dd
```
#### Windows 注意事项:
```
支持 x64 BIOS, x64 UEFI，测试成功的系统有 7 10 11 2022
经测试不支持甲骨文云的 ARM
安装 Windows 需要以下参数
--iso           iso 链接，不需要提前添加 virtio 驱动
--image-name    系统全名，不区分大小写，两边要有引号，例如：
                'Windows 7 Ultimate'
                'Windows 10 Enterprise LTSC 2021'
                'Windows 11 Pro'
                'Windows Server 2022 SERVERDATACENTER' 
                
提示：iso 链接可以到 https://archive.org 上面找
```
#### 内存要求:
```
debian 384M
centos/alma/rocky/fedora 1G
alpine ?
ubuntu ?
windows 1G
```
#### 网络要求:
```
要求有 IPv4、DHCPv4
```
#### 默认用户名 / 密码:
```
root            123@@@
administrator   123@@@
````
#### todo:
```
测试 Xen
添加 Xen Windows 驱动
使用 Cloud Images
````
