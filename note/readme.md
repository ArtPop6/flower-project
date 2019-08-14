# a flower project
1. 当出现"could not read from remote respository.please make sure you have the correct access rights and the respository exists"错误时。
- push没有权限，未设置公钥。
- 在.git文件加上 git bash here，输入ssh-keygen -t rsa -C "2017118621@qq.com"，一路enter再输入cat ~/.ssh/id_rsa.pub查看密钥，再将该密钥值输入至github再直接提交。