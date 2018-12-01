**学习Git与github教程**

---

**一、提交项目到github**

- 工作区——>add——>暂存区——>（commit）——>本地仓库——>push——>远程仓库

- 远程仓库——>clone、pull、fetch——>本地仓库——>reset——>暂存区——>minxed——>工作区

   

  ***方式一：***

  1.在github上建立一个空的远程仓库
  2.将远程仓库克隆到本地(git clone 网址)
  3.在本地向仓库添加内容
  4.将工作区的内容添加到暂存区（git add .）
  5.将暂存区的内容提交到本地仓库(git commit -m "提交说明")
  6.将本地仓库的内容推送到远程仓库（git push origin master）



​	***方式二：***（适合没有网的时候）

​       1.在本地初始化仓库（git init）
​       2.向本地仓库添加内容
​       3.将工作区的内容增添到暂存区(git add .)
​       4.将暂存区的内容提交到本地仓库(git commit -m "提交说明")
​       5.有网的时候在github上面建立一个空的仓库
​       6.本地仓库和远程仓库建立联系（git remote add origin 网址）
​       7.将本地仓库的内容推送到远程仓库（git push origin master）



---



**二、Git之版本管理**

- 创建一个文件在本地仓库：touch 文件名

- 向文件中写入内容：echo 内容 >> 文件名

- 查看文件中的内容：cat 文件名

- 清空暂存区（保存在工作区），也可以理解为撤销：git rm --cache 文件名

- 将暂存区的内容提交到本地仓库：git commit -m "add a.md file"

- 查看过去的（历史的）某个版本：git log(git log --oneline）

- 查看所有（过去未来的）版本和操作记录：git reflog

- 回到过去某个版本：

  - git reset --hard 版本号（清除所有信息）
  - git reset --soft 版本号（暂存区还有内容）
  - git reset --mixed 版本号（工作区还有内容）

- 给当前版本添加版本标签：git tag 标签号

- 给历史版本添加标签：git tag 标签号 版本号

- 添加有备注的版本标签：git tag -a 标签号 -m "备注"

- 查看标签：git tag

- 显示标签的详细信息：git show 标签号

- 删除标签：git tag -d 要删除的标签号

- 对比版本之间的差异：git diff 前版本号 后版本号

- 将本地仓库某标签名推送到远程仓库：git push origin 标签号

- 将本地仓库所有标签推送到远程仓库：git push origin --tag

- 删除标签，先删除本地仓库标签，再删除远程仓库标签：git push origin :refs/tags/版本号 


---



**三、Git之团队合作**

- 集中式方式：（和SVN类似）

- fork+Pull Resquests方式

   

  ---


**四、Git之快速学习Markdown**

- Markdown使用工具（typora）
  - 常用命令：
    - Ctrl+B:变粗
    - Ctrl+i:变斜体
    - Ctrl+B+I:变粗变斜体
    -  --- 表示直线
    - 插入链接：[主页]（链接地址）
    - 插入图片:Ctrl+shift+i

---



**五、Git之搭建个人博客**

**1.安装环境**

- 安装Git
- 安装Node.js环境
- 安装Hexo博客框架（npm install -g hexo）

**2.搭建博客**

- 初始化：hexo init

- 生成静态文件：hexo g (hexo generate)

- 启动服务器本地预览：hexo s (hexo sever)

- 新建一篇博客：hexo new 博客名

- Hexo配置：_config_yml文件

- 配置公钥（ssh-keygen -t rsa -C "账户邮箱"）

- 添加git上传的插件：npm install --save hexo-deployer-git

- 部署github：hexo d (hexo deploy)

- 下载博客主题：git clone 博客主题仓库

  注：修改服务器端口：hexo s -p 端口号

