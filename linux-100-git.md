# git init 初始化本地main仓库
git config --global init.defaultBranch main

```shell
git init 
```

# 关联到remote仓库
```shell
git remote add linux100 https://github.com/GitJumping/my-linux-practise-100.git
```

## 异常（远程是空仓库）

```shell
git push -u linux100 main                                                                                                                                                                                                                                          2024.11.17-12:48:53
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/GitJumping/my-thinking-in-spring.git'
```

```shell
# 远程 main不存在，先在本地创建分支
git checkout -b main
git push linux100 main
# 依然报错
```

```shell
git status
git add .
git commit -m 'init'
git push
git push --set-upstream linux100 main
# 推送成功
```

# 给远程仓库设置token

```shell
# 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
git remote set-url linux100 https://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@github.com/GitJumping/my-linux-practise-100.git
```

# 这一步好像很重要
```shell
git pull
git pull linux100 main
```

# pull之后继续，然后提交
```shell
git status

git add .

git commit -m 'batch test'

git push -u linux100 main

```

# 后面的步骤备用
git pull origin main

git config pull.rebase false

git config --global http.version HTTP/1.1
git config --global core.protectNTFS false

git config --global http.proxy http://proxy-server:8118
git config --global https.proxy http://proxy-server:8118

git config --global http.postBuffer 524288000
git config --global core.longpaths true
