# WalleX——可跨链区块链钱包/An Blockchain Wallet Enabling cross Chains Swap

## 一、安装环境要求/Env Requirements

1. 操作系统：**Linux系统**（Ubuntu等）/ OS: Linux(maybe BSD based or MacOS works)
2. 软件服务：Python 3.0、Truffle等 / Service: Python3 and Truffle

## 二、安装过程/Installation   

1. 安装Python3.0和Truffle；Installation of Python3 and Truffle.
2. 根据requirements.txt文件安装运行所需的模块； Installation of other components referencing requirements.txt.
   ````
   pip install -r requirements.txt
   ````

## 三、经典使用流程/Typical Usage

1. 本地搭建以太坊私有网络/Local Chain
    - 使用Ganache在本地搭建以太坊私有网络/Deploy via Ganache
2. 运行WalleX系统/Launch Wallex Service
    - 启动WEB服务器/Launch Web server
        - 在文件的根目录，执行下述命令启动WEB服务器：
            ````
            export FLASK_APP=blockchain.py
            flask run
            ````
    - 进入WalleX系统界面/Access to webpage via browser
        - 服务器运行时，在Web浏览器的地址栏中输入服务器运行地址，即可进入WalleX系统界面。
 
## 四、数据库重置/Reset User DB
1. 在文件的根目录，执行下述命令进入python shell：
   ````
    export FLASK_APP=blockchain.py
    flask shell
   ````
2. 在shell中执行下属命令重置数据库：
   ````
   from app import db
   db.drop_all()
   db.create_all()
   ````
