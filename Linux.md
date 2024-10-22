<!--
 * @Description: 
 * @Author: FallCicada
 * @Date: 2024-10-21 15:39:23
 * @LastEditors: FallCicada
 * @LastEditTime: 2024-10-21 15:39:28
 * @: 無限進步
-->


* * *

[基本概念](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e5%9f%ba%e6%9c%ac%e6%a6%82%e5%bf%b5)
---------------------------------------------------------------------------------------------------------------------------------

### [简单分类](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e7%ae%80%e5%8d%95%e5%88%86%e7%b1%bb)

1.  **Windows**： 微软公司的操作系统。
2.  **Mac**： 苹果公司的类 Unix 操作系统。
3.  **Linux**： 基于 Linux 内核的类 Unix 操作系统总称，如 Ubuntu 和 CentOS 。

_Unix 是最早的多用户、多任务操作系统。_

* * *

[文件管理](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e6%96%87%e4%bb%b6%e7%ae%a1%e7%90%86)
---------------------------------------------------------------------------------------------------------------------------------

在 Linux 操作系统中，所有被操作系统管理的资源，例如网络接口卡、磁盘驱动器、输入输出设备、普通文件或是目录都被看作是一个文件。

### [文件类型](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e6%96%87%e4%bb%b6%e7%b1%bb%e5%9e%8b)

**Linux 支持 5 种文件类型 ：**

<table><thead><tr><th>文件类型</th><th>描述</th><th>示例</th></tr></thead><tbody><tr><td>普通文件</td><td>存储信息和数据</td><td>代码、可执行文件、图片</td></tr><tr><td>目录文件</td><td>管理文件和子目录</td><td>文件夹</td></tr><tr><td>链接文件</td><td>不同目录下文件共享</td><td>对于每个符号链接，都由系统创建链接文件指向具体位置</td></tr><tr><td>设备文件</td><td>访问硬件设备</td><td>键盘、鼠标</td></tr><tr><td>命名管道</td><td>进程之间的通信</td><td></td></tr></tbody></table>

### [目录结构](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e7%9b%ae%e5%bd%95%e7%bb%93%e6%9e%84)

Linux 文件系统的结构层次鲜明，就像一棵倒立的树，最顶层是其根目录 **/root**：

**常见子目录说明：**

*   **/bin：** 存放二进制可执行文件 (ls、cat、mkdir 等)，常用命令一般都在这里；
*   **/etc：** 存放系统管理和配置文件；
*   **/home：** 存放所有用户文件的根目录，是用户主目录的基点，比如用户 user 的主目录就是 / home/user，可以用~ user 表示；
*   **/usr ：** 用于存放系统应用程序；
*   **/opt：** 额外安装的可选应用程序包所放置的位置。一般情况下，我们可以把 tomcat 等都安装到这里；
*   **/proc：** 虚拟文件系统目录，是系统内存的映射。可直接访问这个目录来获取系统信息；
*   **/root：** 超级用户（系统管理员）的主目录（特权阶级 ^o^）；
*   **/sbin:** 存放二进制可执行文件，只有 root 才能访问。通常存放系统管理员使用的系统级别的管理命令和程序。如 ifconfig 等；
*   **/dev：** 用于存放设备文件；
*   **/mnt：** 系统管理员安装临时文件系统的安装点，系统提供这个目录是让用户临时挂载其他的文件系统；
*   **/boot：** 存放用于系统引导时使用的各种文件；
*   **/lib ：** 存放着和系统运行相关的库文件 ；
*   **/tmp：** 用于存放各种临时文件，是公用的临时文件存储点；
*   **/var：** 用于存放运行时需要改变数据的文件，也是某些大文件的溢出区，比方说各种服务的日志文件（系统启动日志等。）等；
*   **/lost+found：** 这个目录平时是空的，系统非正常关机而留下 “无家可归” 的文件（windows 下叫什么. chk）就在这里。

[基本命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e5%9f%ba%e6%9c%ac%e5%91%bd%e4%bb%a4)
---------------------------------------------------------------------------------------------------------------------------------

Linux 命令大全：[http://man.linuxde.net/](http://man.linuxde.net/)

### [目录切换命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e7%9b%ae%e5%bd%95%e5%88%87%e6%8d%a2%e5%91%bd%e4%bb%a4)

*   **`cd usr`：** 切换到该目录下 usr 目录
*   **`cd ..（或cd../）`：** 切换到上一层目录
*   **`cd /`：** 切换到系统根目录
*   **`cd ~`：** 切换到用户主目录
*   **`cd -`：** 切换到上一个操作所在目录

### [目录操作命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e7%9b%ae%e5%bd%95%e6%93%8d%e4%bd%9c%e5%91%bd%e4%bb%a4)

1.  **`mkdir 目录名称`：** 增加目录
    
2.  **`ls或者ll`**（ll 是 ls -l 的别名，ll 命令可以看到该目录下的所有目录和文件的详细信息）：查看目录信息
    
3.  **`find 目录 参数`：** 寻找目录（查）
    
    示例：
    
    *   列出当前目录及子目录下所有文件和文件夹: `find .`
    *   在`/home`目录下查找以. txt 结尾的文件名:`find /home -name "*.txt"`
    *   同上，但忽略大小写: `find /home -iname "*.txt"`
    *   当前目录及子目录下查找所有以. txt 和. pdf 结尾的文件:`find . \( -name "*.txt" -o -name "*.pdf" \)`或`find . -name "*.txt" -o -name "*.pdf"`
4.  **`mv 目录名称 新目录名称`：** 修改目录的名称（改）
    
    注意：mv 的语法不仅可以对目录进行重命名而且也可以对各种文件，压缩包等进行 重命名的操作。mv 命令用来对文件或目录重新命名，或者将文件从一个目录移到另一个目录中。后面会介绍到 mv 命令的另一个用法。
    
5.  **`mv 目录名称 目录的新位置`：** 移动目录的位置 --- 剪切（改）
    
    注意：mv 语法不仅可以对目录进行剪切操作，对文件和压缩包等都可执行剪切操作。另外 mv 与 cp 的结果不同，mv 好像文件 “搬家”，文件个数并未增加。而 cp 对文件进行复制，文件个数增加了。
    
6.  **`cp -r 目录名称 目录拷贝的目标位置`：** 拷贝目录（改），-r 代表递归拷贝
    
    注意：cp 命令不仅可以拷贝目录还可以拷贝文件，压缩包等，拷贝文件和压缩包时不 用写 - r 递归
    
7.  **`rm [-rf] 目录`:** 删除目录（删）
    
    注意：rm 不仅可以删除目录，也可以删除其他文件或压缩包，为了增强大家的记忆， 无论删除任何目录或文件，都直接使用`rm -rf` 目录 / 文件 / 压缩包
    

### [文件操作命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e6%96%87%e4%bb%b6%e6%93%8d%e4%bd%9c%e5%91%bd%e4%bb%a4)

1.  **`touch 文件名称`:** 文件的创建（增）
    
2.  **`cat/more/less/tail 文件名称`** 文件的查看（查）
    
    *   **`cat`：** 查看显示文件内容
    *   **`more`：** 可以显示百分比，回车可以向下一行， 空格可以向下一页，q 可以退出查看
    *   **`less`：** 可以使用键盘上的 PgUp 和 PgDn 向上 和向下翻页，q 结束查看
    *   **`tail-10` ：** 查看文件的后 10 行，Ctrl+C 结束
    
    注意：命令 tail -f 文件 可以对某个文件进行动态监控，例如 tomcat 的日志文件， 会随着程序的运行，日志会变化，可以使用 tail -f catalina-2016-11-11.log 监控 文 件的变化
    
3.  **`vim 文件`：** 修改文件的内容（改）
    
    vim 编辑器是 Linux 中的强大组件，是 vi 编辑器的加强版，vim 编辑器的命令和快捷方式有很多，但此处不一一阐述，大家也无需研究的很透彻，使用 vim 编辑修改文件的方式基本会使用就可以了。
    
    **在实际开发中，使用 vim 编辑器主要作用就是修改配置文件，下面是一般步骤：**
    
    vim 文件 ------> 进入文件 -----> 命令模式 ------> 按 i 进入编辑模式 -----> 编辑文件 -------> 按 Esc 进入底行模式 -----> 输入：wq/q! （输入 wq 代表写入内容并退出，即保存；输入 q! 代表强制退出不保存。）
    
4.  **`rm -rf 文件`：** 删除文件（删）
    
    同目录删除：熟记 `rm -rf` 文件 即可
    

### [文件压缩命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e6%96%87%e4%bb%b6%e5%8e%8b%e7%bc%a9%e5%91%bd%e4%bb%a4)

**1）打包并压缩文件：**

Linux 中的打包文件一般是以. tar 结尾的，压缩的命令一般是以. gz 结尾的。

而一般情况下打包和压缩是一起进行的，打包并压缩后的文件的后缀名一般. tar.gz。 命令：**`tar -zcvf 打包压缩后的文件名 要打包压缩的文件`** 其中：

z：调用 gzip 压缩命令进行压缩

c：打包文件

v：显示运行过程

f：指定文件名

比如：假如 test 目录下有三个文件分别是：aaa.txt bbb.txt ccc.txt，如果我们要打包 test 目录并指定压缩后的压缩包名称为 test.tar.gz 可以使用命令：**`tar -zcvf test.tar.gz aaa.txt bbb.txt ccc.txt`或：`tar -zcvf test.tar.gz /test/`**

**2）解压压缩包：**

命令：tar [-xvf] 压缩文件

其中：x：代表解压

示例：

1 将 / test 下的 test.tar.gz 解压到当前目录下可以使用命令：**`tar -xvf test.tar.gz`**

2 将 / test 下的 test.tar.gz 解压到根目录 / usr 下:**`tar -xvf test.tar.gz -C /usr`**（- C 代表指定解压的位置）

### [操作权限命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e6%93%8d%e4%bd%9c%e6%9d%83%e9%99%90%e5%91%bd%e4%bb%a4)

操作系统中每个文件都拥有特定的权限、所属用户和所属组。权限是操作系统用来限制资源访问的机制，在 Linux 中权限一般分为读 (readable)、写(writable) 和执行 (excutable)，分为三组。分别对应文件的属主(owner)，属组(group) 和其他用户(other)，通过这样的机制来限制哪些用户、哪些组可以对特定的文件进行什么样的操作。通过 **`ls -l`** 命令我们可以 查看某个目录下的文件或目录的权限

示例：在随意某个目录下`ls -l`

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAACbklEQVRoQ+2aMU4dMRCGZw6RC1CSSyQdLZJtKQ2REgoiRIpQkCYClCYpkgIESQFIpIlkW+IIcIC0gUNwiEFGz+hlmbG9b1nesvGW++zxfP7H4/H6IYzkwZFwQAUZmpJVkSeniFJKA8ASIi7MyfkrRPxjrT1JjZ8MLaXUDiJuzwngn2GJaNd7vyP5IoIYY94Q0fEQIKIPRGS8947zSQTRWh8CwLuBgZx479+2BTkHgBdDAgGAC+fcywoyIFWqInWN9BSONbTmFVp/AeA5o+rjKRJ2XwBYRsRXM4ZXgAg2LAPzOCDTJYQx5pSIVlrC3EI45y611osMTHuQUPUiYpiVooerg7TWRwDAlhSM0TuI+BsD0x4kGCuFSRVzSqkfiLiWmY17EALMbCAlMCmI6IwxZo+INgQYEYKBuW5da00PKikjhNNiiPGm01rrbwDwofGehQjjNcv1SZgddALhlJEgwgJFxDNr7acmjFLqCyJuTd6LEGFttpmkYC91Hrk3s1GZFERMmUT01Xv/sQljjPlMRMsxO6WULwnb2D8FEs4j680wScjO5f3vzrlNJszESWq2LYXJgTzjZm56MCHf3zVBxH1r7ftU1splxxKYHEgoUUpTo+grEf303rPH5hxENJqDKQEJtko2q9zGeeycWy3JhpKhWT8+NM/sufIhBwKI+Mta+7pkfxKMtd8Qtdbcx4dUQZcFCQ2I6DcAnLUpf6YMPxhIDDOuxC4C6djoQUE6+tKpewWZ1wlRkq0qUhXptKTlzv93aI3jWmE0Fz2TeujpX73F9TaKy9CeMk8vZusfBnqZ1g5GqyIdJq+XrqNR5AahKr9CCcxGSwAAAABJRU5ErkJggg==)

第一列的内容的信息解释如下：

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAACbklEQVRoQ+2aMU4dMRCGZw6RC1CSSyQdLZJtKQ2REgoiRIpQkCYClCYpkgIESQFIpIlkW+IIcIC0gUNwiEFGz+hlmbG9b1nesvGW++zxfP7H4/H6IYzkwZFwQAUZmpJVkSeniFJKA8ASIi7MyfkrRPxjrT1JjZ8MLaXUDiJuzwngn2GJaNd7vyP5IoIYY94Q0fEQIKIPRGS8947zSQTRWh8CwLuBgZx479+2BTkHgBdDAgGAC+fcywoyIFWqInWN9BSONbTmFVp/AeA5o+rjKRJ2XwBYRsRXM4ZXgAg2LAPzOCDTJYQx5pSIVlrC3EI45y611osMTHuQUPUiYpiVooerg7TWRwDAlhSM0TuI+BsD0x4kGCuFSRVzSqkfiLiWmY17EALMbCAlMCmI6IwxZo+INgQYEYKBuW5da00PKikjhNNiiPGm01rrbwDwofGehQjjNcv1SZgddALhlJEgwgJFxDNr7acmjFLqCyJuTd6LEGFttpmkYC91Hrk3s1GZFERMmUT01Xv/sQljjPlMRMsxO6WULwnb2D8FEs4j680wScjO5f3vzrlNJszESWq2LYXJgTzjZm56MCHf3zVBxH1r7ftU1splxxKYHEgoUUpTo+grEf303rPH5hxENJqDKQEJtko2q9zGeeycWy3JhpKhWT8+NM/sufIhBwKI+Mta+7pkfxKMtd8Qtdbcx4dUQZcFCQ2I6DcAnLUpf6YMPxhIDDOuxC4C6djoQUE6+tKpewWZ1wlRkq0qUhXptKTlzv93aI3jWmE0Fz2TeujpX73F9TaKy9CeMk8vZusfBnqZ1g5GqyIdJq+XrqNR5AahKr9CCcxGSwAAAABJRU5ErkJggg==)

> 下面将详细讲解文件的类型、Linux 中权限以及文件有所有者、所在组、其它组具体是什么？

**文件的类型：**

*   d： 代表目录
*   -： 代表文件
*   l： 代表软链接（可以认为是 window 中的快捷方式）

**Linux 中权限分为以下几种：**

*   r：代表权限是可读，r 也可以用数字 4 表示
*   w：代表权限是可写，w 也可以用数字 2 表示
*   x：代表权限是可执行，x 也可以用数字 1 表示

**文件和目录权限的区别：**

对文件和目录而言，读写执行表示不同的意义。

对于文件：

<table><thead><tr><th>权限名称</th><th>可执行操作</th></tr></thead><tbody><tr><td>r</td><td>可以使用 cat 查看文件的内容</td></tr><tr><td>w</td><td>可以修改文件的内容</td></tr><tr><td>x</td><td>可以将其运行为二进制文件</td></tr></tbody></table>

对于目录：

<table><thead><tr><th>权限名称</th><th>可执行操作</th></tr></thead><tbody><tr><td>r</td><td>可以查看目录下列表</td></tr><tr><td>w</td><td>可以创建和删除目录下文件</td></tr><tr><td>x</td><td>可以使用 cd 进入目录</td></tr></tbody></table>

**需要注意的是超级用户可以无视普通用户的权限，即使文件目录权限是 000，依旧可以访问。** **在 linux 中的每个用户必须属于一个组，不能独立于组外。在 linux 中每个文件有所有者、所在组、其它组的概念。**

*   **所有者**
    
    一般为文件的创建者，谁创建了该文件，就天然的成为该文件的所有者，用 ls ‐ahl 命令可以看到文件的所有者 也可以使用 chown 用户名 文件名来修改文件的所有者 。
    
*   **文件所在组**
    
    当某个用户创建了一个文件后，这个文件的所在组就是该用户所在的组 用 ls ‐ahl 命令可以看到文件的所有组 也可以使用 chgrp 组名 文件名来修改文件所在的组。
    
*   **其它组**
    
    除开文件的所有者和所在组的用户外，系统的其它用户都是文件的其它组
    

> 我们再来看看如何修改文件 / 目录的权限。

**修改文件 / 目录的权限的命令：`chmod`**

示例：修改 / test 下的 aaa.txt 的权限为属主有全部权限，属主所在的组有读写权限， 其他用户只有读的权限

**`chmod u=rwx,g=rw,o=r aaa.txt`**

![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADIAAAAyCAYAAAAeP4ixAAACbklEQVRoQ+2aMU4dMRCGZw6RC1CSSyQdLZJtKQ2REgoiRIpQkCYClCYpkgIESQFIpIlkW+IIcIC0gUNwiEFGz+hlmbG9b1nesvGW++zxfP7H4/H6IYzkwZFwQAUZmpJVkSeniFJKA8ASIi7MyfkrRPxjrT1JjZ8MLaXUDiJuzwngn2GJaNd7vyP5IoIYY94Q0fEQIKIPRGS8947zSQTRWh8CwLuBgZx479+2BTkHgBdDAgGAC+fcywoyIFWqInWN9BSONbTmFVp/AeA5o+rjKRJ2XwBYRsRXM4ZXgAg2LAPzOCDTJYQx5pSIVlrC3EI45y611osMTHuQUPUiYpiVooerg7TWRwDAlhSM0TuI+BsD0x4kGCuFSRVzSqkfiLiWmY17EALMbCAlMCmI6IwxZo+INgQYEYKBuW5da00PKikjhNNiiPGm01rrbwDwofGehQjjNcv1SZgddALhlJEgwgJFxDNr7acmjFLqCyJuTd6LEGFttpmkYC91Hrk3s1GZFERMmUT01Xv/sQljjPlMRMsxO6WULwnb2D8FEs4j680wScjO5f3vzrlNJszESWq2LYXJgTzjZm56MCHf3zVBxH1r7ftU1splxxKYHEgoUUpTo+grEf303rPH5hxENJqDKQEJtko2q9zGeeycWy3JhpKhWT8+NM/sufIhBwKI+Mta+7pkfxKMtd8Qtdbcx4dUQZcFCQ2I6DcAnLUpf6YMPxhIDDOuxC4C6djoQUE6+tKpewWZ1wlRkq0qUhXptKTlzv93aI3jWmE0Fz2TeujpX73F9TaKy9CeMk8vZusfBnqZ1g5GqyIdJq+XrqNR5AahKr9CCcxGSwAAAABJRU5ErkJggg==)

上述示例还可以使用数字表示：

chmod 764 aaa.txt

**补充一个比较常用的东西:**

假如我们装了一个 zookeeper，我们每次开机到要求其自动启动该怎么办？

1.  新建一个脚本 zookeeper
2.  为新建的脚本 zookeeper 添加可执行权限，命令是:`chmod +x zookeeper`
3.  把 zookeeper 这个脚本添加到开机启动项里面，命令是：`chkconfig --add zookeeper`
4.  如果想看看是否添加成功，命令是：`chkconfig --list`

### [用户管理命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e7%94%a8%e6%88%b7%e7%ae%a1%e7%90%86%e5%91%bd%e4%bb%a4)

Linux 系统是一个多用户多任务的分时操作系统，任何一个要使用系统资源的用户，都必须首先向系统管理员申请一个账号，然后以这个账号的身份进入系统。

用户的账号一方面可以帮助系统管理员对使用系统的用户进行跟踪，并控制他们对系统资源的访问；另一方面也可以帮助用户组织文件，并为用户提供安全性保护。

**Linux 用户管理相关命令:**

*   `useradd 选项 用户名`: 添加用户账号
*   `userdel 选项 用户名`: 删除用户帐号
*   `usermod 选项 用户名`: 修改帐号
*   `passwd 用户名`: 更改或创建用户的密码
*   `passwd -S 用户名` : 显示用户账号密码信息
*   `passwd -d 用户名`: 清除用户密码

useradd 命令用于 Linux 中创建的新的系统用户。useradd 可用来建立用户帐号。帐号建好之后，再用 passwd 设定帐号的密码．而可用 userdel 删除帐号。使用 useradd 指令所建立的帐号，实际上是保存在 / etc/passwd 文本文件中。

passwd 命令用于设置用户的认证信息，包括用户密码、密码过期时间等。系统管理者则能用它管理系统用户的密码。只有管理者可以指定用户名称，一般用户只能变更自己的密码。

**用户组**

每个用户都有一个用户组，系统可以对一个用户组中的所有用户进行集中管理。不同 Linux 系统对用户组的规定有所不同，如 Linux 下的用户属于与它同名的用户组，这个用户组在创建用户时同时创建。

用户组的管理涉及用户组的添加、删除和修改。组的增加、删除和修改实际上就是对 / etc/group 文件的更新。

**Linux 系统用户组的管理相关命令:**

*   `groupadd 选项 用户组` : 增加一个新的用户组
*   `groupdel 用户组`: 要删除一个已有的用户组
*   `groupmod 选项 用户组` : 修改用户组的属性

### [其他常用命令](#/%E7%90%86%E8%AE%BA%E5%9F%BA%E7%A1%80/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/linux?id=%e5%85%b6%e4%bb%96%e5%b8%b8%e7%94%a8%e5%91%bd%e4%bb%a4)

*   **`pwd`：** 显示当前所在位置
    
*   `sudo + 其他命令`：以系统管理者的身份执行指令，也就是说，经由 sudo 所执行的指令就好像是 root 亲自执行。
    
*   **`grep 要搜索的字符串 要搜索的文件 --color`：** 搜索命令，--color 代表高亮显示
    
*   **`ps -ef`/`ps -aux`：** 这两个命令都是查看当前系统正在运行进程，两者的区别是展示格式不同。如果想要查看特定的进程可以使用这样的格式：**`ps aux|grep redis`** （查看包括 redis 字符串的进程），也可使用 `pgrep redis -a`。
    
    注意：如果直接用 ps（（Process Status））命令，会显示所有进程的状态，通常结合 grep 命令查看某进程的状态。
    
*   **`kill -9 进程的pid`：** 杀死进程（-9 表示强制终止。）
    
    先用 ps 查找进程，然后用 kill 杀掉
    
*   **网络通信命令：**
    
    *   查看当前系统的网卡信息：ifconfig
    *   查看与某台机器的连接情况：ping
    *   查看当前系统的端口使用：netstat -an
*   **net-tools 和 iproute2 ：** `net-tools`起源于 BSD 的 TCP/IP 工具箱，后来成为老版本 Linux 内核中配置网络功能的工具。但自 2001 年起，Linux 社区已经对其停止维护。同时，一些 Linux 发行版比如 Arch Linux 和 CentOS/RHEL 7 则已经完全抛弃了 net-tools，只支持`iproute2`。linux ip 命令类似于 ifconfig，但功能更强大，旨在替代它。更多详情请阅读[如何在 Linux 中使用 IP 命令和示例](https://linoxide.com/linux-command/use-ip-command-linux)
    
*   **`shutdown`：** `shutdown -h now`： 指定现在立即关机；`shutdown +5 "System will shutdown after 5 minutes"`：指定 5 分钟后关机，同时送出警告信息给登入用户。
    
*   **`reboot`：** **`reboot`：** 重开机。**`reboot -w`：** 做个重开机的模拟（只有纪录并不会真的重开机）。