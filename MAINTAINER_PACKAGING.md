# Host Release 打包说明（维护者）

> 在 **私有开发仓库** 构建，上传到 **ChaiSniffer-Public** 的 GitHub Releases。

---

## 1. 构建 Windows Host

```powershell
cd native-host
powershell -NoProfile -ExecutionPolicy Bypass -File .\build-host.ps1
```

确认存在：

- `native-host/host.exe`
- `native-host/bin/ffmpeg.exe`
- `native-host/host.cmd`
- `native-host/setup-bridge.cmd`
- `native-host/com.browser_mpv_bridge.json`

---

## 2. 组装发布 zip

建议文件名：`ChaiSniffer-Host-Windows-x64-v0.9.14.zip`

zip 根目录结构：

```text
ChaiSniffer-Host-Windows-x64-v0.9.14/
  README.txt          # 简短：解压 → setup-bridge.cmd → 粘贴扩展 ID
  native-host/
    host.cmd
    host.exe
    setup-bridge.cmd
    com.browser_mpv_bridge.json
    bin/ffmpeg.exe
    （不要包含 bridge-settings.json 或用户数据）
```

**不要** 打包：Python 源码、`.pytest_cache`、开发用 `host.py`（可选保留 host.py 仅当未冻结时 — 发布版应仅 exe）。

---

## 3. 创建 GitHub Release

1. 仓库：`K-O-N-B/ChaiSniffer-Public`
2. Tag：`host-v0.9.14`（与扩展版本对应）
3. Title：`Windows Native Host v0.9.14`
4. 正文：复制 `RELEASE_NOTES/v0.9.14.md` 中 Host 部分
5. 上传 zip 作为 Release asset

---

## 4. 商店扩展包

商店仅提交 **`extension/`** 目录打包的 zip（不含 native-host 源码）。

打包前确认 `install_links.js` 指向 Public 仓库。

---

## 5. 校验清单

- [ ] `setup-bridge.cmd` 在新机器可登记 Native Messaging
- [ ] 设置页 **运行完整自检** 全部 ✓
- [ ] B 站分轨或公开 HLS 测试下载成功
- [ ] Release 页链接与扩展内「打开 GitHub 下载页」一致
