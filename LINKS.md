# 链接说明

## 你应该分享哪个？

| 场景 | 用哪个链接 |
|------|------------|
| **寂缠弹 BD 在线看** | [GitHub Pages 入口](https://chalo0518-ctrl.github.io/CLADOS_POE2_BDG-UILDING/) → 寂缠弹 → Excel 网页版 |
| **Grim Pillars 在线看** | OneDrive（快）或 GitHub Pages 入口 |
| 展示 **脚本自动更新** 的最新版 | GitHub Pages 入口 |
| 对方要 **离线保存** | 入口页「下载 xlsx」 |

## 链接地址

### 1. OneDrive 主版本（作者可编辑，链接持有人可查看）

https://1drv.ms/x/c/20757cbe6409b71c/IQAuwDWMX5s2Q629DnZOk56CAQjLHfR0KpY-5ODw5Qv3xxA?e=JsUmJO

- 你在 OneDrive 里改的内容在这里
- GitHub 自动同步 **不会** 更新这个文件

### 2. GitHub Pages 入口（汇总所有 BD）

https://chalo0518-ctrl.github.io/CLADOS_POE2_BDG-UILDING/

含 **Grim Pillars Oracle** 与 **寂缠弹 Blood Mage** 两份指南，均可一键 Excel 网页版打开。

### 3. 公开仓库

https://github.com/chalo0518-ctrl/CLADOS_POE2_BDG-UILDING

## 维护提醒

- 改机制/技能/装备：在私有仓改脚本 → 推送 → GitHub 版自动更新
- 改 OneDrive FAQ：**合并回 GitHub**（见下方）
- 以后若做阶段 3：可在 OneDrive 版对 FAQ 列开放指定人编辑

## OneDrive → GitHub 合并

在 OneDrive 编辑后：

1. 下载 xlsx → 上传到私有仓 `docs/incoming/onedrive_snapshot.xlsx` 并提交  
   **或** Actions → **Merge OneDrive to GitHub** → Run workflow  
2. 脚本提取 **常见问题** 等列 → 写入 `docs/faq/overrides.yaml`  
3. 重新生成 xlsx 并同步公开仓  

本地命令：

```bash
python3 scripts/merge_onedrive_to_github.py --file docs/incoming/onedrive_snapshot.xlsx --regenerate
```

可选：`--mode full` 用 OneDrive 文件整体替换 `docs/Grim_Pillars_Oracle_BD指南.xlsx`。
