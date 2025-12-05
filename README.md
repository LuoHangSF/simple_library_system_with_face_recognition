## 一、说明

UI库用的是Pyside6，数据库用的是MySQL 9.0

## 二、如何运行

### (1) 准备环境

#### 1. 安装MySQL 9

具体详见[此处](https://blog.csdn.net/weixin_47406082/article/details/131867849?ops_request_misc=elastic_search_misc&request_id=07270aba3dd70d5c957d1c89d6a97f3b&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-131867849-null-null.142^v102^pc_search_result_base9&utm_term=mysql%E5%AE%89%E8%A3%85&spm=1018.2226.3001.4187)，安装后请设置好自己的用户名密码和端口号。

#### 2. 配置MySQL

使用`mysql -u root -p --default-character-set=utf8mb4`登录MySQL，同时需要在`./database/connector.py`里修改你设置的MySQL的用户名、密码和端口号。

#### 3. 配置数据库

登录MySQL后，在MySQL命令行运行`./main_bookdb6.sql`里面的所有SQL语句（或者直接在命令行输入`SOURCE main_bookdb6.sql`以批量执行）。运行后会创建一个bookdb数据库，里面保存了图书管理系统需要的信息，里面初始化了一个管理员（帐号和密码都是admin）、一个用户（用户信息在sql文件里面自己找）和几本书籍

#### 4. 安装Python

如何安装Python也自行百度，我的本机环境是Python 3.10。和3.10相差不大应该也可以。

注意安装的时候一定要勾选**加入环境变量**（如果你会创建Python虚拟环境就不用）

#### 5. 配置dlib包的前置环境

为了保证`dlib`包能够正常安装，需要提前在windows上配置cmake和boost，具体详见[这里](https://blog.csdn.net/weixin_47406082/article/details/131867849?ops_request_misc=elastic_search_misc&request_id=07270aba3dd70d5c957d1c89d6a97f3b&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-131867849-null-null.142^v102^pc_search_result_base9&utm_term=mysql%E5%AE%89%E8%A3%85&spm=1018.2226.3001.4187)

#### 6. 配置Python虚拟环境

创建虚拟环境后，运行`pip install -r requirement.txt`

### (2) 运行程序

在项目目录进入控制台，输入`python main.py`回车即可。

如果你前面使用虚拟环境安装Python的包，注意一定要在虚拟环境里运行，否则会报错。

### 
