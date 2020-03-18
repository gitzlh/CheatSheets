# Bash

## 文件

#### 查看目录下所有文件大小
`du -sh * `
#### 删除文件夹
`rm -r <dir>`
#### mac/linux下txt中文乱码
`iconv -c -f GB2312 -t UTF-8 凡人修仙转.txt >> 凡人修仙转2.txt`

#### 根据文件名寻找文件
`find . -name "word2vec*" # 当前目录下寻找包含word2vec的文件` 


#### 截取文件中间某些行

```
sed -n '100,200p' filename 
```
#### 打乱文件的行


```
shuf input_file.txt -o  output_file.txt
```

#### cat追加文件内容
```
cat test > test1  # test的内容粘贴到test1，test1原有内容被覆盖
```
```
cat test >> test1  # test的内容追加到test1，test1原有内容被覆盖

```

## 服务器

#### 上传
```
scp  /home/me/Desktop/test.txt  user_name@192.168.0.0:/home/zlh/.ssh    #文件
scp  -r /home/me/Desktop/test  user_name@192.168.0.0:/home/zlh/.ssh  #文件夹
```
#### 下载
```
scp -P 21111 user_name@192.168.0.0:/opt/test.txt  /home/me/Desktop
scp -P 21111 -r user_name@192.168.0.0:/opt/test  /home/me/Desktop #-P指定端口

```
#### 免密登录
```
ssh-keygen -b 4096 -t rsa # 客户端：生成私钥、公钥；.ssh文件下已经有则不需要；
scp ~/.ssh/id_rsa.pub user@192.168.0.0:~/.ssh  # 客户端：复制公钥到服务器
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys # 服务器端：追加公钥内容到authorized_keys；若无此文件可直接copy
vim ~/ssh/config  # 客户端：设置别名、端口，格式如下：
    # HostName icl
    # Port 234
    # User zlh
    # IdentityFile ~/.ssh/id_rsa

```
## 网络

#### HTTP下载 -单个文件
```
wget https://repo.anaconda.com/archive/Anaconda3-2019.10-MacOSX-x86_64.sh
```
#### FTP下载 -单个文件
```
wget --ftp-user=xxx --ftp-password=xxx ftp://cf.pku.edu.cn:21/123.zip  # 会在当前目录新建名为123的目录
```

#### FTP下载 -文件夹
```
wget -nH -m --ftp-user=xxx --ftp-password=xxx ftp://cf.pku.edu.cn:21/123/  # 会在当前目录新建名为123的目录
```
## python
#### 查看python版本
```
python --version
```
#### 查看python位置
```
which python
```
#### 改变PYTHONPATH
```
export PYTHONPATH=$PYTHONPATH:～/DST
python3.7 models/HDST_BERT/train_HDST.py
```
export用来设置环境变量；多个路径之间用冒号进行分割

然后直接在该路径（DST）下执行命令

#### nohup服务器后台运行程序
```
nohup python3 train.py > log.txt &
```


## 其他
#### 创建命令别名
```
vim ~/.zshrc
alias ns='nvidia-smi'
alias gitamp="git add . ; git commit -m 'new'; git push"
source ~/.zshrc
```

