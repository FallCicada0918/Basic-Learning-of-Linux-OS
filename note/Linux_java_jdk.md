<!--
 * @Description: 
 * @Author: FallCicada
 * @Date: 2024-10-22 16:02:45
 * @LastEditors: FallCicada
 * @LastEditTime: 2024-10-22 16:05:10
 * @: 無限進步
-->
在Linux系统上安装JDK（Java Development Kit）1.8，你可以通过多种方式来完成。下面我将指导你如何使用软件包管理器来进行安装。这里以常见的Ubuntu/Debian和CentOS/RHEL为例。

### Ubuntu/Debian

1. 打开终端。

2. 添加OpenJDK的存储库。对于Ubuntu 20.04及更高版本，可以使用以下命令：
   ```bash
   sudo apt update
   sudo apt install openjdk-8-jdk
   ```
   如果你需要Oracle JDK而不是OpenJDK，你可能需要从Oracle官网下载并手动安装，因为版权原因，Oracle JDK通常不会包含在官方存储库中。

3. 验证安装：
   ```bash
   java -version
   ```
   这应该会显示JDK版本信息，并且确认是1.8版本。

javac
### 手动安装

如果你需要特定版本的Oracle JDK，并且它没有包含在你的Linux发行版的默认仓库中，你可能需要手动下载并安装JDK。以下是基本步骤：

1. 访问Oracle官方网站或使用其他可信来源下载JDK 1.8的tar.gz文件。

2. 下载后，在终端中切换到下载目录，并解压tar.gz文件：
   ```bash
   tar -xzf jdk-8uXXX-linux-x64.tar.gz
   ```

3. 将解压后的目录移动到一个合适的目录，例如`/usr/lib/jvm`：
   ```bash
   sudo mv jdk1.8.0_XXX /usr/lib/jvm/
   ```

4. 设置环境变量。编辑`~/.bashrc`或`/etc/profile`文件，添加如下行：
   ```bash
   export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_XXX
   export PATH=$JAVA_HOME/bin:$PATH
   ```

5. 使更改生效：
   ```bash
   source ~/.bashrc
   ```
   或者如果是编辑的`/etc/profile`：
   ```bash
   source /etc/profile
   ```

6. 最后验证安装：
   ```bash
   java -version
   ```

请根据你的具体Linux发行版和需求选择合适的方法进行安装。如果遇到任何问题，请随时询问！在Linux系统上安装JDK（Java Development Kit）1.8，你可以通过多种方式来完成。下面我将指导你如何使用软件包管理器来进行安装。这里以常见的Ubuntu/Debian和CentOS/RHEL为例。

### Ubuntu/Debian

1. 打开终端。

2. 添加OpenJDK的存储库。对于Ubuntu 20.04及更高版本，可以使用以下命令：
   ```bash
   sudo apt update
   sudo apt install openjdk-8-jdk
   ```
   如果你需要Oracle JDK而不是OpenJDK，你可能需要从Oracle官网下载并手动安装，因为版权原因，Oracle JDK通常不会包含在官方存储库中。

3. 验证安装：
   ```bash
   java -version
   ```
   这应该会显示JDK版本信息，并且确认是1.8版本。

### CentOS/RHEL

1. 打开终端。

2. 安装必要的工具：
   ```bash
   sudo yum install -y yum-utils
   ```

3. 添加并安装JDK。对于OpenJDK，可以使用以下命令：
   ```bash
   sudo yum install -y java-1.8.0-openjdk-devel
   ```

4. 验证安装：
   ```bash
   java -version
   ```
   同样地，这会显示你的JDK版本，并确认其为1.8。

### 手动安装

如果你需要特定版本的Oracle JDK，并且它没有包含在你的Linux发行版的默认仓库中，你可能需要手动下载并安装JDK。以下是基本步骤：

1. 访问Oracle官方网站或使用其他可信来源下载JDK 1.8的tar.gz文件。

2. 下载后，在终端中切换到下载目录，并解压tar.gz文件：
   ```bash
   tar -xzf jdk-8uXXX-linux-x64.tar.gz
   ```

3. 将解压后的目录移动到一个合适的目录，例如`/usr/lib/jvm`：
   ```bash
   sudo mv jdk1.8.0_XXX /usr/lib/jvm/
   ```

4. 设置环境变量。编辑`~/.bashrc`或`/etc/profile`文件，添加如下行：
   ```bash
   export JAVA_HOME=/usr/lib/jvm/jdk1.8.0_XXX
   export PATH=$JAVA_HOME/bin:$PATH
   ```

5. 使更改生效：
   ```bash
   source ~/.bashrc
   ```
   或者如果是编辑的`/etc/profile`：
   ```bash
   source /etc/profile
   ```

6. 最后验证安装：
   ```bash
   java -version
   ```

请根据你的具体Linux发行版和需求选择合适的方法进行安装。如果遇到任何问题，请随时询问！