## 查找大文件

```bash
git rev-list --objects --all | git cat-file --batch-check='%(objectname) %(objecttype) %(objectsize) %(rest)' | sort -k3 -n -r | head -n 20
```

## 在 python 环境中安装 filter-repo

```bash
uv venv .venv && source .venv/bin/activate
uv pip install git-filter-repo
```

## 删除历史中的大文件

```bash
git filter-repo --path installer --invert-paths --force
```

git remote add origin https://github.com/malen/delete-large-file-from-history.git
git push --set-upstream origin develop

### 非常关键

git push origin -f --all


https://www.notion.so/Azure-Functions-6ed753b22ac547a182f9750c1fd1ddc7?source=copy_link
