# 对外公布资料包（审核用）

本目录内容用于发布到 **公开仓库** `https://github.com/K-O-N-B/ChaiSniffer-Public`，与私有开发仓 `ChaiSniffer` 分离。

## 文件清单

| 文件 | 用途 |
|------|------|
| [README.md](README.md) | 公开仓库首页 |
| [PRIVACY.md](PRIVACY.md) | 隐私政策（商店必填 URL） |
| [docs/INSTALL_HOST.md](docs/INSTALL_HOST.md) | Host 安装说明 |
| [docs/TEST_ENV.md](docs/TEST_ENV.md) | 测试环境与支持平台 |
| [store/EDGE_STORE_LISTING.md](store/EDGE_STORE_LISTING.md) | Edge 商店中英文描述、审核备注 |
| [store/PERMISSIONS_JUSTIFICATION.md](store/PERMISSIONS_JUSTIFICATION.md) | 权限对照表 |
| [RELEASE_NOTES/v0.9.14.md](RELEASE_NOTES/v0.9.14.md) | 首版 Release 说明模板 |
| [MAINTAINER_PACKAGING.md](MAINTAINER_PACKAGING.md) | Host zip 打包与上传步骤 |
| [REPO_SETUP.md](REPO_SETUP.md) | 创建公开仓库并 push 的一次性步骤 |

## 审核要点

1. **仓库名**：建议 `ChaiSniffer-Public`（可改，改后需同步 `extension/install_links.js`）。
2. **闭源**：本目录不含扩展/Host 源码，仅文档与 Release 资产说明。
3. **扩展 v0.9.14** 已将设置页、Popup、右键菜单链接指向公开仓。
4. **图1 灰色「柴嗅」**：Edge 浏览器固定 UI，**无法**改为链接；替代方案见设置页「安装与使用须知」与右键菜单「柴嗅 · 项目主页」。

## 你审核后可执行

见 [REPO_SETUP.md](REPO_SETUP.md) 创建 GitHub Public 仓库并 push；再按 [MAINTAINER_PACKAGING.md](MAINTAINER_PACKAGING.md) 上传第一个 Host Release。
