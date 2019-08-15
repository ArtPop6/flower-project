# flower-project
- git出现"Updates were rejected because the tip of your current branch is behind"的问题
1. 主要是因为远程仓库与本地仓库冲突的问题
2. 使用git pull 将仓库一致后再push

- 当push时出现"could not read from remote respository.please make sure you have the correct access rights and the respository exists"错误时
1. 主要是没有设置密钥
2. 在.git文件处Git bash here输入命令"ssh-keygen -t rsa -C "2017118621@qq.com",一路enter再输入"cat ~/.ssh/id_rsa.pub"得到密钥再从github上new ssh。

- 当push时出现Everything up-to-date但远程仓库并未修改的解决策略
1. 新建一个分支new
2. 在这个分支上new添加修改后的文件git add ,git commit -m
3. 切换到master分支，合并分支 git merge new
4. 删除new分支


