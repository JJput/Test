# Git

#### 显示配置信息命令
    git config 

#### 添加仓库
    git init

#### 添加"xx"文件/文件夹到暂存区
    git add xx

## 提交当前暂存区的更新至本地仓库
    
    git commit

#### -a 全部
    
    git commit -a

#### -m "" 加上备注信息
    
    git commit -m ""

#### 查看状态 （暂存区）

    git status

#### 查看日志

    git log

//添加远程仓库
git remote add origin https://github.com/iOSZZW/myGit

//移除
git rm

/*********版本还原*********/
//上一个版本
git reset --hard HEAD

//根据SHA1码来指定还原(至少输入前4位)
git reset --hard xxxx


//撤销对工作区"git.txt"的修改
git checkout -- git.txt


/*********GutHub*********/
//添加远程仓库
git remote add origin git@github.com:GitHub用户名/远程库名.git

//将本地仓库更新的内容提交到远程仓库
//第一次 要加 "-u"
git push -u origin master  
//以后
git push origin master

//将远程仓库拉取下来
git pull --rebase origin master



echo "# JJUtils" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:JJput/JJUtils.git
git push -u origin master

