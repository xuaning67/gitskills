# gitskills
上传全部文件至一个新的仓库
在已经设置好SSH keys的情况下
第一步：右键需要上传的文件，选择Git bash Here，进入命令行
第二步：git init初始化仓库，这时候会发现文件中出现一个名为.git的文件
第三步：git commit -m "提交信息"  //这个地方还不清楚是什么含义
第四步：git remote add origin master GitHub仓库地址。该操作应该就是本地同GitHub的连接
第五步：git pull --rebase origin master 。这是啥我也还不知道
第六步：git push -u origin master。 同样不知道这是啥，但是到目前为止基本算是上传成功。
