# 公开仓库创建指南（审核用）

> 本文档仅供维护者使用，用于把 `public-release/` 内容发布到 **对外公布专用仓库**。  
> **请勿**将私有开发仓库 `K-O-N-B/ChaiSniffer` 设为 Public。

---

## 推荐仓库

| 项 | 值 |
|---|---|
| **仓库名** | `ChaiSniffer-Public` |
| **公开 URL** | https://github.com/K-O-N-B/ChaiSniffer-Public |
| **用途** | 用户文档、隐私政策、Windows Host 安装包 Release |
| **不包含** | 扩展源码、Host Python 源码（闭源分发） |

---

## 一次性创建步骤

1. 在 GitHub 新建 **Public** 仓库：`ChaiSniffer-Public`（不要勾选 README，本目录已备好）。
2. 在本机 `MPV-Bridge/public-release/` 目录执行：

```powershell
cd G:\00_Develop-Projects-NZ\009_MPV_Bridge\MPV-Bridge\public-release
git init -b main
git add README.md PRIVACY.md docs store RELEASE_NOTES MAINTAINER_PACKAGING.md
git commit -m "Initial public release documentation"
git remote add origin https://github.com/K-O-N-B/ChaiSniffer-Public.git
git push -u origin main
```

3. 在 GitHub **Releases** 上传第一个 **Windows 本机组件** zip（打包方法见 `MAINTAINER_PACKAGING.md`），Tag 建议 `host-v0.9.14`。
4. 确认扩展 `install_links.js` 中的 `GITHUB_REPO` 已指向 `ChaiSniffer-Public`（v0.9.14 起默认已改）。
5. 商店上架时，隐私政策 URL 填：  
   `https://github.com/K-O-N-B/ChaiSniffer-Public/blob/main/PRIVACY.md`

---

## 与私有开发仓的关系

| 仓库 | 可见性 | 内容 |
|------|--------|------|
| `ChaiSniffer` | Private | 完整源码、开发文档、测试 |
| `ChaiSniffer-Public` | **Public** | 安装说明、隐私政策、Host 二进制 Release、商店文案 |

扩展内所有「下载 Host / 安装说明 / 项目主页」链接均指向 **Public** 仓库。
