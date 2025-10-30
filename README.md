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
git filter-repo --path bootstrap-5.3.7-dist.zip --invert-paths --force
```
