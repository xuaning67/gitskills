# gitskills
上传全部文件至一个新的仓库
## 配置SSH keys（在本机未曾配置SSH密钥的情况下的操作）
### 新建仓库
在GitHub上新建一个仓库，需要设置的内容有仓库名、是否共享、是否生成Readme
### 生成SSH密钥部分
+ 打开Git Bash 输入以下命令
  - git config --global user.name "GitHub账号名" 回车
  - git config --global user.email "GitHub邮箱"  回车
+ 输入命令：cd ~/.ssh 。此时一般会有密钥生成，如果没有，再次输入以下命令：ssh-keygen -t rsa -C "GitHub注册邮箱"。之后会出现一系列操作，大致是关于ssh文件的位置。可以一直点击回车。这样.ssh文件就会出现在C盘目录下（具体自己找，应该好找）。
+ 找到.ssh文件，打开。
+ 用记事本里面的id_rsa.pub文件。复制里面的全部信息（里面的就是SSH密钥）。
+ 进入Github点击右上角头像，选择setting选项。
+ 点击new SSH Key。在Title框自定义一个名字。
+ 复制的信息粘贴到Key文本框。点击Add SSh Key。
以上则SSH密钥配置成功。
## 上传文件（在已经设置好SSH keys的情况下）
1. 右键需要上传的文件，选择Git bash Here，进入命令行
2. git init //初始化仓库，这时候会发现文件夹中出现一个名为.git的文件
3. 输入 git status //标红部分为当前文件夹中待添加到本地仓库的文件。
4. 输入 git add 文件名（加后缀）  或者  git add --all  。再次输入 git status //刚才显示为红色的文件信息已经变为绿色，表明文件已经被添加到本地仓库。
5. git commit -m "提交信息"  //说明著述，对本次提交添加说明原因
6. 去GitHub上复制仓库地址
7. git remote add origin master GitHub仓库地址。//将本地从仓库关联到GitHub上
8. git pull --rebase origin master //如果远程仓库有README.md文件，执行此操作。大致就是为本地仓库代码目录添加一个README.md文件
9. git push -u origin master //上传命令。  
别忘了刷新GitHub仓库查看。
11111
