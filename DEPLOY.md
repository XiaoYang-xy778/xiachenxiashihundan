# 部署到 GitHub Pages

仓库：`XiaoYang-xy778/xia-chenxiao-is-a-jerk`
预期网址：https://xiaoyang-xy778.github.io/xia-chenxiao-is-a-jerk/

## 方式 A：命令行（已在本机仓库初始化好后）

```bash
git add -A
git commit -m "夏辰骁是混蛋.COM"
git branch -M main
git remote add origin https://github.com/XiaoYang-xy778/xia-chenxiao-is-a-jerk.git
git push -u origin main
```

然后在仓库 Settings → Pages → Source 选 `Deploy from a branch`，分支 `main`、目录 `/ (root)`。

## 方式 B：纯网页上传

1. 新建 public 仓库 `xia-chenxiao-is-a-jerk`
2. Add file → Upload files，把 `index.html` 和 `.nojekyll` 拖进去
3. Settings → Pages → main / root

## 注意

- `.nojekyll` 必须保留，否则 GitHub 会跳过下划线开头的文件（本站暂时没有，但保留更稳）。
- 无需构建，没有依赖，也没有外部请求。
