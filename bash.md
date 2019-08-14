# Bash

#### 查看目录下所有文件大小
`du -sh * `
#### 删除文件夹
`rm -r <dir>`
#### mac/linux下txt中文乱码
`iconv -c -f GB2312 -t UTF-8 凡人修仙转.txt >> 凡人修仙转2.txt`

#### 根据文件名寻找文件
`find . -name "word2vec*" # 当前目录下寻找包含word2vec的文件` 
#### 创建别名
```
vim ~/.zshrc
alias ns='nvidia-smi'
alias gitamp="git add . ; git commit -m 'new'; git push"
source ~/.zshrc
```

#### 截取文件中间某些行

```
sed -n '100,200p' filename 
```
