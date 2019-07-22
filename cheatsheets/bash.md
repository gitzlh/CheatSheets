## 文件
#### 查看目录下所有文件大小
`du -sh * `
#### 删除文件夹
`rm -r <dir>`
## Git

#### 远程项目clone到本地
`git clone git@github.com:gitzlh/CheatSheets.git`
#### 本地修改push到远程
```
git add .
git commit -m 'comments' #-m 后面的是修改信息，必须写
git push
```
#### 远程修改pull到本地
```
git stash
git pull
```
#### 远程与本地均修改，本地无法push
- 强行覆盖远程
```
git push -u origin +master
```
- 每次本地修改时，先git pull
