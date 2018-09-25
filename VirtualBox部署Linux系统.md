[TOC]

# VirtualBox部署Linux系统

​	在JavaEE的课程中,需要学员对Linux系统的有初步的认识.课程要求学员在虚拟机上进行安装Linux系统,虚拟机大多是Vmware.Vmware虚拟机功能上强大,使用过的人都是认可的,但是...有点时候Vmware也会出现异常情况.

- 情况一 : 虚拟机安装不上

  ![](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537667506817.png)

- 情况二 : Linux系统安装不上

  ![](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537667734800.png)

  ------

  ​	还有其他诸多类的情况,我们无法开始Linux学习的伟大事业.那么这个时候可以使用另一个虚拟机软件

  VirtualBox.下面开始对VirtualBox进行讲解.

  

## (一) VirTualBox简介

​	VirtualBox 是一款开源[虚拟机软件](https://baike.baidu.com/item/%E8%99%9A%E6%8B%9F%E6%9C%BA%E8%BD%AF%E4%BB%B6/9003764)。VirtualBox 是由德国 Innotek 公司开发，由Sun Microsystems公司出品的软件，使用[Qt](https://baike.baidu.com/item/Qt)编写，在 Sun 被 [Oracle](https://baike.baidu.com/item/Oracle) 收购后正式更名成 Oracle VM VirtualBox。 

​	VirtualBox号称是最强的免费虚拟机软件，它不仅具有丰富的特色，而且性能也很优异！它简单易用，可虚拟的系统包括Windows（从Windows 3.1到Windows10、Windows Server 2012，所有的Windows系统都支持）、Mac OS X、Linux、[OpenBSD](https://baike.baidu.com/item/OpenBSD)、[Solaris](https://baike.baidu.com/item/Solaris/3517)、IBM OS2甚至[Android](https://baike.baidu.com/item/Android)等操作系统！ 使用者可以在VirtualBox上安装并且运行上述的这些操作系统！ 

> ​    VirtualBox官网:[https://www.virtualbox.org/]()
>
> ​    官方最新版本 : 5.2

![1537666510740](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537666510740.png)



## (二) VirtualBox的安装

### 一.打开安装软件,点击下一步

![](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669222889.png)

### 二.更换安装路径

![1537669410172](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669410172.png)

![1537669476504](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669476504.png)

### 三.选择对应选项,进行下一步

![1537669567085](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669567085.png)

### 四.点击`是`,开始安装

![1537669633187](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669633187.png)

### 五.点击`安装`,进行软件的安装

![1537669691231](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669691231.png)

![1537669747405](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669747405.png)

> ​	安装时会有提示安装Oracle的总线程控制器,点击  `安装`

### 六.安装完毕,点击`完成`进行安装向导

![1537669949731](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537669949731.png)

### 七.在打开的软件界面中,进行全局设置

![1537670237795](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537670237795.png)

### 八.在全局设置中的常规中,更改安装虚拟机安装的路径

![1537670492726](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537670492726.png)

### 九.在热键中,更改虚拟机切除热键(跟据个人习惯自由设定)

![1537670772614](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537670772614.png)

### 十.在扩展中安装VirtualBox扩展包vbox-extpack

​	针对安装的不同的Virtualbox版本,应安装与之对应的`vbox-extpack`扩展包

   -  查看VirtualBox版本

   ![1537672059198](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672059198.png)

   ![1537672133448](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672133448.png)
     
   - 在官网下载对应的版本

     ![1537672315743](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672315743.png)

     > ​	安装地址 : [https://www.virtualbox.org/wiki/Downloads]()

   - 在扩展中进行安装

     ![1537672447518](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672447518.png)

     ![1537672535428](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672535428.png)

     ![1537672577278](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672577278.png)

     ![1537672691704](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672691704.png)

     ![1537672752202](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537672752202.png)

   > 为什么要安装此扩展包呢?
   >
   > ​ 当关闭虚拟机，再次打开虚拟机的时候，无法打开报错！ 

   

​      

## (三) VirtualBox安装Centos6.5

​	在安装虚拟前,我们需要开启BIOS中的虚拟化技术(重点),如果不开启会出现下面的错误提示.

> ​	百度经验 : [https://jingyan.baidu.com/article/335530daa55d7e19cb41c3c2.html]()

![1537677867170](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537677867170.png)



### 一.新建Virtual虚拟系统

![1537678299376](C:\Users\Simple\AppData\Local\Temp\1537678299376.png)

### 二.选择Centos系统版本

![1537679017860](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537679017860.png)

> ​	在VirtualBox中没有对应的Centos,但在Red Hat中可以直接使用Centos版本的Linux,所以在版本中选择Red Hat-64bit(我们安装的Centos是64位的)

### 三.分配系统内存

![1537679860527](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537679860527.png)

> 至少分配1GB内存（或者2G内存），支持图形界面显示
> 对于Centos的安装大致可以安装两种模式:
> 	1.纯命令行模式(类似windows的Dos系统)
>         2.桌面模式(类似与windows操作系统)
>
> 不同的模式,可以分配不同的内容空间(此次演示桌面版)
> 	1.512MB的内存不能支持图形界面。
> 	2.1024MB（或者2048MB内存）的内存可以支持图形界面。

### 四.创建虚拟硬盘

![1537680500517](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537680500517.png)

![1537680660517](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537680660517.png)

![1537680711259](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537680711259.png)

![1537680793503](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537680793503.png)

> ​	虚拟硬盘可以分配大一些 ，之前的设置中可以动态调整硬盘的内容。

![1537681016845](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537681016845.png)

### 五.Linux安装前的设置

- ​	设置系统属性

![1537681161634](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537681161634.png)

- ​	设置处理器个数

![1537681334669](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537681278277.png)

> ​	在系统的处理中,可以针对自己的电脑选择处理器的个数,这里分配1个处理器

- ​	设置内存

  ![1537681611010](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537681611010.png)

	 ​	由于此次将安装Centos桌面版,显存可以设置32MB以上,这里设置为32MB

	 ​	设置安装镜像位置

![1537681952369](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537681952369.png)

![1537682287958](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537682287958.png)

- ​	设置网络(重点)

![1537682491509](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537682491509.png)

> ​	上图的这是的作用可以让虚拟机可以连接上互联网(要保证主机能够上网)



![1537842638431](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537842638431.png)

> ​	上图的配置可以使主机和虚拟机相互通信



​	在虚拟机的网络配置中,主要有三种配置方式:

​		1）  NAT ： 虚拟机电脑 通过 外部主机进行上网，但是虚拟机电脑没有独立ip地址，只能由虚拟机电脑连接外部主机，外部主机不能主动连接虚拟机 .`外部主机能上网，虚拟机就能上网!!!` 

​		2）  桥接： 虚拟机电脑，会和外部主机在局域网注册一台物理机，会和主机在局域网有同一个网段ip ，互相访问，虚拟机上网通过局域网交换机进行上网 （虚拟机和外部主机属于同一IP网段，同时连接路由器进行上网）

​		3）  Host-only: 虚拟机会产生一个虚拟ip，和主机进行互相通信，此时虚拟机只能和主机通信，外部电脑无法访问 虚拟机 ，`虚拟机不能上网！`

> 桥接 : 可以让外部的电脑访问，即外部电脑都可以访问虚拟机服务器
> NAT：表示虚拟机可以访问本机电脑
> Host-only：表示本机电脑和虚拟机可以互相访问，但是别人无法访问虚拟机

### 六.Centos6.5的安装

- ​	启动Centos的安装,并切换到缩放模式


![1537683190386](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537683190386.png)

![1537683466039](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537683466039.png)

​                                	![1537683722941](https://github.com/FlippyGO/VirtureBox/blob/master/img/153768351601.png)

- ​	进入的Centos的安装步骤

![1537683388391](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537683388391.png)

- ​	选择Skip，跳过media测试 

![1537684335763](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537684335763.png)

- ​	开始Centos的安装

![1537684406772](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537684406772.png)

- ​	语种的选择(生成环境尽量采用英文版,避免软件对中文的不兼容)

![1537684479890](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537684479890.png)

- ​	键盘选择默认的就可以了(美式键盘)

![1537684610562](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537684610562.png)

- ​	选择基本存储设备(选择默认)

  ![1537684776626](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537684776626.png)

- ​    格式化数据的提示,这里选择 `Yes,dicard any data`

![1537684855707](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537684855707.png)

- ​	修改主机域名,这里可以根据自己的喜好进行修改,但不要有中文和特殊字符

![1537685174094](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537685174094.png)

- ​	设置网络

![1537686550817](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537685174093.png)

- ​	对网络进行设置为开机启动

![1537686689609](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537686689609.png)

![1537686887422](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537686887422.png)

- ​	选择时区为上海

![1537687013834](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537687013834.png)

- ​	设置超级账号Root的密码

![1537687164488](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537687164488.png)

> ​	如果密码过于简单,会有提示.但是如果不是正式环境就直接点击 `Use Anyway`
>
> ![1537687323651](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537687323651.png)

- ​	给系统进行分盘

![1537687787218](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537687787218.png)

> 图上的的各个选项解释 : 
>
> ​	1.Use All Space :删除硬盘上的所有分区(这将包含Windows的NTFS分区和VFAT或者其他操作系统的分区信息)
>
> ​	2.Replace Existing Linux System : 替换之前的linux系统安装时的分区,不会对其他分区数据删除.
>
> ​	3.Shrink Current System : 调整当前分区
>
> ​	4.User Free Space : 保留当前的数据和分区并安装到未使用的存储驱动器上
> 		注意 : 必须要保留足够的空间
>
> ​	5.Create Custom Layout : 自定义对存储设备进行分区.项目环境一般会自动分区.

- ​	磁盘进行分区

  | 分区名字 | 分区大小                                                   |
  | :------: | :--------------------------------------------------------- |
  |  /boot   | 存放Linux相关的程序,比如引导装载程序等,建议大小为150MB     |
  |    /     | 系统根目录,所有的目录都挂在这个目录下,建议大小5GB以上      |
  |   /usr   | 存放系统的应用程序,相关数据较多,建议大小3GB                |
  |   /var   | 存放系统经常变化的数据和日志文件,建议大小1GB以上           |
  |   swap   | 虚拟内存,建议是物理内存的1~2倍                             |
  |  /home   | 存放用户数据,是普通用户的宿主目录,建议将剩下的空间全部分配 |

  ![](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689460383.png)

- 给Boot进行分区

![1537690186234](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689537733.png)

![1537690206873](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689962495.png)

- ​	给 / 分配空间

![1537690120712](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537690120712.png)

![1537690186234](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689537733.png)

![1537690585319](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537690423065.png)

- ​	给swap分配空间

![1537690559965](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537690559965.png)

![1537690186234](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689537733.png)

![1537690735631](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537690735631.png)

- ​	给/usr分配空间

![1537690960410](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537690960410.png)

![1537690186234](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689537733.png)

![1537691051280](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537691051280.png)

- ​	给/var分配空间

![1537691135065](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537691135065.png)

![1537690186234](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689537733.png)

![1537691240372](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537691240372.png)

- ​	给/home分配空间

![1537691314891](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537691314891.png)

![1537690186234](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537689537733.png)

![1537691431985](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537691431985.png)

- ​	分区后的结果

![1537691485426](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537691485426.png)

- ​	重新启动系统

![1537692219259](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537692219259.png)

- ​	分区后,需要进行分区的格式化

![1537692286196](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537692286196.png)

![1537692371682](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537692371682.png)

- ​	格式化完毕,下一步

![1537692442923](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537692442923.png)

- ​	此次我们安装迷你桌面版(这个版要比桌面版预装的软件少)

![1537692585542](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537692585542.png)

> ​	各个类型的解释:
>
> |             类型             | 解释                                                         |
> | :--------------------------: | ------------------------------------------------------------ |
> |           Desktop            | 基本的桌面系统,包括常用的桌面软件,如文件查看工具等....       |
> |       Minimal Desktop        | 基本的桌面系统,但软件较少                                    |
> |            Mnimal            | 基本的系统,不包含任何可选的软件包                            |
> |         Basic Server         | 基本系统系统,不包含桌面                                      |
> |       DataBase Server        | 基本的系统平台,加上Mysql和PostgreSQL数据库,无桌面            |
> |          Web Server          | 基本的系统平台,加上PHP Web Server,还有Mysql 和PostgreSQL数据库的客户端,无桌面 |
> |         Virtual Host         | 基本系统夹虚拟平台                                           |
> | Soft Development Wrokstation | 软件包较多,虚拟化平台,桌面环境,开发工具                      |
>



- ​	系统安装完毕,重新启动

![1537693237295](https://github.com/FlippyGO/VirtureBox/blob/master/img/1537693237295.png)





