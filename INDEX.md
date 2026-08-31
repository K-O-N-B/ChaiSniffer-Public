# 对外公布资料包（审核用）

本目录内容用于发布到 **公开仓库** `https://github.com/K-O-N-B/ChaiSniffer-Public`，与私有开发仓 `ChaiSniffer` 分离。

## 文件清单

| 文件 | 用途 |
|------|------|
| [README.md](README.md) | 公开仓库首页 |
| [PRIVACY.md](PRIVACY.md) | 隐私政策（商店必填 URL） |
| [docs/zh-CN/INSTALL_HOST.md](docs/zh-CN/INSTALL_HOST.md) | Host 安装说明（简体） |
| [docs/TEST_ENV.md](docs/zh-CN/TEST_ENV.md) | 测试环境与支持平台 |
| [RELEASE_NOTES/v0.9.16.md](RELEASE_NOTES/v0.9.16.md) | 扩展 0.9.16 更新说明 |
| [store/EDGE_SUBMISSION_CHECKLIST.md](store/EDGE_SUBMISSION_CHECKLIST.md) | **Edge 上架步骤清单** |
| [store/EDGE_PARTNER_FIELDS.md](store/EDGE_PARTNER_FIELDS.md) | Partner Center 字段复制区 |
| [store/EDGE_STORE_LISTING.md](store/EDGE_STORE_LISTING.md) | Edge 商店中英文描述 |
| [store/EDGE_REVIEW_NOTES.md](store/EDGE_REVIEW_NOTES.md) | 认证说明（给审核员） |
| [store/SCREENSHOT_CAPTIONS.md](store/SCREENSHOT_CAPTIONS.md) | 截图内容与 caption |
| [store/PERMISSIONS_JUSTIFICATION.md](store/PERMISSIONS_JUSTIFICATION.md) | 权限对照表 |
| [RELEASE_NOTES/v0.9.14.md](RELEASE_NOTES/v0.9.14.md) | 首版 Release 说明 |
| [MAINTAINER_PACKAGING.md](MAINTAINER_PACKAGING.md) | Host zip 打包与上传步骤 |
| [REPO_SETUP.md](REPO_SETUP.md) | 创建公开仓库并 push |

## 当前版本（2026-08-31）

| 组件 | 版本 |
|------|------|
| 扩展 | **0.9.16**（Edge 商店提交准备中） |
| Windows 辅助应用 | **host-v0.9.14.1**（[Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/tag/host-v0.9.14.1)） |
| 扩展提交 zip（本地） | `../dist-release/ChaiSniffer-Extension-v0.9.16.zip` |

## 审核要点

1. **仓库名**：`ChaiSniffer-Public`；扩展内链接已指向本仓。
2. **闭源**：本目录不含扩展/Host 源码，仅文档与 Release 资产说明。
3. **v0.9.16** 新增浮动图标开关，**无新增 manifest 权限**。
4. **图1 灰色「柴嗅」**：Edge 浏览器固定 UI，**无法**改为链接；替代：设置页与右键菜单「柴嗅 · 项目主页」。

## Edge 上架 — 你需亲自完成

见 [store/EDGE_SUBMISSION_CHECKLIST.md](store/EDGE_SUBMISSION_CHECKLIST.md)：

1. Partner Center 账号与创建产品  
2. 上传 `ChaiSniffer-Extension-v0.9.16.zip`  
3. 截取 5 张截图（说明见 SCREENSHOT_CAPTIONS.md）  
4. 粘贴 EDGE_PARTNER_FIELDS / EDGE_REVIEW_NOTES 文案  
5. 提交审核  

文案与权限说明已由维护者文档准备好，**审核即可**。
