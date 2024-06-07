### Git的安装

```
brew install git

# 更改全局用户名和邮箱
git config --global user.name "Your New Username"
git config --global user.email "yournewemail@example.com"

# 更改本地仓库的用户名和邮箱
git config user.name "Your New Username"
git config user.email "yournewemail@example.com"
```

###  常用指令

```
git add .
git commit -m "update message"
git push
git status
git fetch
git pull 
```

###  fetch && pull

```
git fetch
功能：git fetch 从远程仓库下载所有分支的最新提交和更新，但不会合并这些更新到你当前的工作分支。它只是将这些更新存储在本地的远程分支中。
用法：git fetch [remote]，例如 git fetch origin。
结果：不会修改你的工作目录或当前分支，只是更新了本地的远程跟踪分支。你需要手动合并或查看这些更新。

git pull
功能：git pull 是 git fetch 和 git merge 的组合。它从远程仓库下载更新，并自动尝试将这些更新合并到你当前的工作分支。
用法：git pull [remote] [branch]，例如 git pull origin main。
结果：下载并合并远程更新到当前分支。如果有冲突，需要手动解决冲突。
```

