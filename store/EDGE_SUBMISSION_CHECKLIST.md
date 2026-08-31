# Edge 商店提交清单（维护者）

> **扩展版本：** 0.9.16  
> **提交包路径（本地）：** `MPV-Bridge/dist-release/ChaiSniffer-Extension-v0.9.16.zip`  
> **Partner Center：** https://partner.microsoft.com/dashboard/microsoftedge/overview

---

## 一、你需要亲自完成的（AI 无法代劳）

| 步骤 | 说明 |
|------|------|
| 1 | 注册 / 登录 [Microsoft Partner Center](https://partner.microsoft.com/dashboard) |
| 2 | 创建扩展产品 → 上传 **zip 包**（见上路径） |
| 3 | 上传 **截图**（见 [SCREENSHOT_CAPTIONS.md](./SCREENSHOT_CAPTIONS.md)，至少 1 张，建议 5 张） |
| 4 | 上传 **商店图标** 128×128（可用 `extension/icons/dog-128.png`） |
| 5 | 填写文案（复制 [EDGE_PARTNER_FIELDS.md](./EDGE_PARTNER_FIELDS.md)） |
| 6 | 提交审核；若被拒，按邮件意见修改后重新提交 |
| 7 | **上架后**：打开商店版扩展 → 设置 → 复制 **新扩展 ID** → 更新公开文档中的「商店 ID」说明（如有固定示例） |

---

## 二、已准备好的材料（可直接复制）

| 文件 | 用途 |
|------|------|
| [EDGE_PARTNER_FIELDS.md](./EDGE_PARTNER_FIELDS.md) | Partner Center 各字段中英文正文 |
| [EDGE_STORE_LISTING.md](./EDGE_STORE_LISTING.md) | 完整描述、分类、审核备注 |
| [EDGE_REVIEW_NOTES.md](./EDGE_REVIEW_NOTES.md) | 认证测试步骤（给审核员） |
| [PERMISSIONS_JUSTIFICATION.md](./PERMISSIONS_JUSTIFICATION.md) | 权限用途对照 |
| [SCREENSHOT_CAPTIONS.md](./SCREENSHOT_CAPTIONS.md) | 截图内容与 caption |
| [../PRIVACY.md](../PRIVACY.md) | 隐私政策 URL（商店必填） |

---

## 三、提交前自检

- [ ] zip 内根目录有 `manifest.json`，`version` 为 `0.9.16`
- [ ] zip **不含** `tools/`、`.git`、源码注释外的开发文件
- [ ] 本地侧载 zip 加载后：Popup 正常、设置页可打开、浮动图标开关有效
- [ ] 隐私政策 URL 在浏览器可打开（未登录 GitHub 也可访问 raw 或 blob 页）
- [ ] Host Release 页可下载（审核员可能点链接）

---

## 四、上架后与 Host 的关系

1. 用户从 **Edge 商店** 安装扩展 → 得到 **商店固定扩展 ID**
2. 用户从 GitHub 下载 Host → `setup-bridge.cmd` → **必须粘贴商店 ID**
3. 侧载测试 ID **≠** 商店 ID；文档 [INSTALL_HOST.md](../docs/zh-CN/INSTALL_HOST.md) 已说明

---

## 五、常见拒审与应对

| 原因 | 应对 |
|------|------|
| 权限过宽 | 附 [PERMISSIONS_JUSTIFICATION.md](./PERMISSIONS_JUSTIFICATION.md)；说明嗅探需观察网络请求 |
| Native Messaging | 说明 Host **不在扩展包内**，用户自愿从 GitHub 安装；符合 1.2.3 |
| 版权 / 下载 | 描述中强调「仅处理有权保存的内容」「不绕过 DRM」 |
| 无法验证功能 | 在认证说明中提供 Host 安装步骤 + 公开测试页建议 |
