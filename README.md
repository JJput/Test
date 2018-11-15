# Git指令集

#### 显示配置信息命令
    git config 

#### 创建仓库
    git init

#### 添加"xx"文件/文件夹到暂存区
    git add xx
 
#### 添加当前目录下全部文件/文件夹到暂存区
    git add -A
    //注意-A大写
#### 查看暂存区状态
    git status

## 提交更新到本地仓库
    
#### 从暂存区更新至本地仓库
    git commit

#### -a 全部
    
    git commit -a

#### -m "" 加上备注信息
    
    git commit -m ""

#### 查看日志（历史提交）

    git log
    
## 版本还原

#### 直接还原至”上一次提交本地仓库“版本

    git reset --hard HEAD

#### 根据SHA1码来指定还原(至少输入前4位)

    git reset --hard xxxx
    //SHA1码可以通过git log查看


## 添加远程仓库-GutHub

#### 通过SSH添加
    git remote add origin git@github.com:GitHub用户名/远程库名+".git"
    
    例如：GitHub userName:JJput  repository:JJUtils
         git remote add origin git@github.com:JJput/JJUtils.git

#### 将本地仓库更新的内容提交到远程仓库
##### 第一次 要加 "-u”
    git push -u origin master  
##### 以后    
    git push origin master

#### 将远程仓库拉取下来
    git pull --rebase origin master


### GitHub建好空项目后的指令

    echo "# JJUtils" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:JJput/JJUtils.git
    git push -u origin master

## 移除

    git rm

