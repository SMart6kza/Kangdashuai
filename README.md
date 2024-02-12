## Kangdashuai
关于window10电脑 许许多多文件乱码的问题：
是因为电脑在区域里面开启了 beta版本（在区域 管理 更改系统区域设置里面）把这个勾去掉就好了。
![屏幕截图 2024-02-04 164518](https://github.com/SMart6kza/Kangdashuai/assets/80021817/f6d22d30-9034-46da-b7fa-6845ff048902)


##可视化大屏项目实现思路一：
  #先利用CSS 和 html文件将主界面搭建出来。（基本框架出来）
  再用js文件填充echarts 图表。




##再给 centos7装载图形化界面的时候。
首先用 sudo yum groupinstall "KDE Plasma Workspaces"
      sudo yum groupinstall "GNOME Desktop"
    选择适合centos的图形界面（版本）
然后安装完成后。如果报错
：安装过程如遇报错：Transaction check error:
file /boot/efi/EFI/centos from install of fwupdate-efi-12-5.el7.centos.x86_64 conflicts with file from package grub2-common-1:2.02-0.65.el7.centos.2.noarch
用 yum upgrade -y 只升级所有包，不升级软件和系统内核。

然后最好在虚拟机里面使用。安装

然后如果：
sudo reboot 重新启动后。
命令行启动界面没有自动切换为图形化界面。
就用 startx 来启动。


如果您不想使用GUI界面，可以切换回命令行界面。在CentOS或其他使用systemd的Linux发行版上，可以通过以下命令设置默认的目标为多用户文本模式：
sudo systemctl set-default multi-user.target
就会有这样的代码产生：

![Uploading 屏幕截图 2024-02-12 163734.png…]()




然后重启系统，系统将在没有启动GUI的情况下启动到命令行模式。您也可以在不重启的情况下临时切换到文本模式，使用如下命令：
sudo systemctl isolate multi-user.target

这样就都可以使用了。


