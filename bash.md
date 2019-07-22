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
- git add把要提交的所有修改放到暂存区（Stage），git commit一次性把暂存区的所有修改提交到分支。
[git](img/gitadd.jpg)
[](img/gitcommit.jpg)
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

#### 查看项目状态
- 要随时掌握工作区的状态，使用`git status`命令。

- 如果`git status`告诉你有文件被修改过，用`git diff`可以查看修改内容。

#### 版本回退
- 回退到上一个版本
`git reset --hard HEAD^`
- 根据版本号回退
`git reset --hard 1094a`
- 上一个版本就是HEAD^，上上一个版本就是HEAD^^，往上100个版本写成HEAD~100。

end

