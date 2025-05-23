
创建
git init： 创建新仓库：
git clone /path/to/repository：克隆本地仓库
git clone username@host:/path/to/repository：克隆远程仓库

工作流
你的本地仓库由 git 维护的三棵“树”组成：
第一个是你的 `工作目录`，它持有实际文件；
第二个是 `暂存区（Index）`，它像个缓存区域，临时保存你的改动；
最后是 `HEAD`，它指向你最后一次提交的结果。

**添加和提交**
==git add .==/git add (filename)：添加文件到暂存区/解决冲突后使用!
==git commit -m== "代码提交信息"：将暂存区的内容提交到本地仓库

替换本地改动
==git checkout .==/git checkout (filename)：取消暂存区文件

推送改动
git remote add origin (Your Github URL)：将远程仓库与本地仓库关联起来
==git push origin master==：将本地仓库 `master` 分支的内容推送到远程仓库 `origin`

分支
git checkout -b branch_x：创建一个叫做“feature_x”的分支，并切换过去
git branch -d branch_x：把新建的分支删掉， `-D` （强制删除）选项
git push origin branch_x：将分支推送到远端仓库
git checkout master：切换回主分支

更新与合并
git fetch：更新代码库
git pull ：更新你的本地仓库至最新改动
git merge branch_x：合并其他分支到你的当前分支（先切需要合入的分支，例如 master）
git diff ：(source_branch) (target_branch)：预览差异
git status ：对比本地文件状态和仓库中的状态





