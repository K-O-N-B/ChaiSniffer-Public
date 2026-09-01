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
| [store/EDGE_SUBMISSION_CHECKLIST.md](store/EDGE_SUBMISSION_CHECKLIST.md) | Edge 上架步骤清单（**已过审**） |
| [store/CHROME_SUBMISSION_CHECKLIST.md](store/CHROME_SUBMISSION_CHECKLIST.md) | **Chrome Web Store 提交清单** |
| [store/CHROME_STORE_LISTING.md](store/CHROME_STORE_LISTING.md) | Chrome 商店描述字段 |
| [store/CHROME_PRIVACY_FIELDS.md](store/CHROME_PRIVACY_FIELDS.md) | Chrome Privacy 页复制区 |
| [store/CHROME_TEST_INSTRUCTIONS.md](store/CHROME_TEST_INSTRUCTIONS.md) | Chrome 审核测试说明 |
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
| 扩展 | **0.9.16**（**Edge 已过审**；Chrome 提交中） |
| Windows 辅助应用 | **host-v0.9.14.1**（[Releases](https://github.com/K-O-N-B/ChaiSniffer-Public/releases/tag/host-v0.9.14.1)） |
| 扩展提交 zip（本地） | `../dist-release/ChaiSniffer-Extension-v0.9.16.zip` |
| Edge CRX ID | `obmiddjkfcfikepdognkecmjkecpiia` |

## 审核要点

1. **仓库名**：`ChaiSniffer-Public`；扩展内链接已指向本仓。
2. **闭源**：本目录不含扩展/Host 源码，仅文档与 Release 资产说明。
3. **v0.9.16** 新增浮动图标开关，**无新增 manifest 权限**。
4. **图1 灰色「柴嗅」**：Edge 浏览器固定 UI，**无法**改为链接；替代：设置页与右键菜单「柴嗅 · 项目主页」。

## Edge 上架 — 已完成

**v0.9.16 已过审。** Edge CRX ID：`obmiddjkfcfikepdognkecmjkecpiia`  
请在公开 README / 设置文案中使用商店安装链接（Partner Center 公布后）。

## Chrome Web Store — 你需亲自完成

见 [store/CHROME_SUBMISSION_CHECKLIST.md](store/CHROME_SUBMISSION_CHECKLIST.md)：

1. 注册 Chrome Web Store 开发者（一次性 **$5**）→ https://chrome.google.com/webstore/devconsole  
2. New item → 上传 `ChaiSniffer-Extension-v0.9.16.zip`  
3. 截图用 `dist-release/store-assets/v0.9.16-edge/`（已是 1280×800）  
4. 粘贴 `CHROME_STORE_LISTING` / `CHROME_PRIVACY_FIELDS` / `CHROME_TEST_INSTRUCTIONS`  
5. Submit for review  

文案与 Edge 过审材料一致，Chrome 侧可直接复用。
