# Bash

#### 查看目录下所有文件大小
`du -sh * `
#### 删除文件夹
`rm -r <dir>`
#### mac/linux下txt中文乱码
`iconv -c -f GB2312 -t UTF-8 凡人修仙转.txt >> 凡人修仙转2.txt`


#### 创建别名
```
vim ~/.zshrc
alias ns='nvidia-smi'
alias gitamp="git add . ; git commit -m 'new'; git push"
source ~/.zshrc
```
