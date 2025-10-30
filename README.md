## 查找大文件

git rev-list --objects --all | git cat-file --batch-check='%(objectname) %(objecttype) %(objectsize) %(rest)' | sort -k3 -n -r | head -n 20

## 删除历史中的 node_modules 目录

git filter-repo --path node_modules --invert-paths --force
