# MassageBLT

外单项目，已删除，转移到国内gitee.com个人私有仓库，以此标记


彻底清除Github上某个文件的历史 参考下文
http://blog.csdn.net/ysy950803/article/details/53383582




git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch FILE_PATH' --prune-empty --tag-name-filter cat -- --all

git push origin master --force

rm -rf .git/refs/original/

git reflog expire --expire=now --all

git gc --prune=now

git gc --aggressive --prune=now

其中里面的FILE_PATH为文件路径，如果想删除所有的文件，直接填 *  ，比如 * 或者 Hello/*


