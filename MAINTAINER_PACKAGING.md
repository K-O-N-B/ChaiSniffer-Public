# Host Release 打包说明（维护者）

> 在 **私有开发仓库** `ChaiSniffer` 构建，上传到 **ChaiSniffer-Public** 的 GitHub Releases。  
> 交接摘要见私有仓 `docs/HANDOFF.md`。

---

## 1. 构建 Windows Host

```powershell
cd native-host
powershell -NoProfile -ExecutionPolicy Bypass -File .\build-host.ps1
```

确认存在：

- `native-host/host.exe`
- `native-host/bin/ffmpeg.exe`
- `native-host/bin/cacert.pem`（若构建脚本已拷贝）
- `native-host/host.cmd`
- `native-host/setup-bridge.cmd`
- `native-host/com.browser_mpv_bridge.json`

---

## 2. 组装发布 zip

建议文件名：`ChaiSniffer-Host-Windows-x64-v0.9.17.zip`

zip 根目录结构：

```text
ChaiSniffer-Host-Windows-x64-v0.9.17/
  README.txt
  native-host/
    host.cmd
    host.exe
    setup-bridge.cmd
    setup-bridge.ps1
    com.browser_mpv_bridge.json
    bin/ffmpeg.exe
    bin/cacert.pem
```

**禁止打包：** 任意 `*.py`、`bridge-settings.json`、`.use-python-host`、`.tasks/`、`.cache/`、用户数据。

**校验：**

- `host.exe` SHA256 与构建产物一致（v0.9.17：`E54CB8466C7B962593724F31C7541404047038FCE893E744000D4D02D58F5B24`）
- zip 内 `*.py` 数量为 0
- 可选：Native Messaging 帧测 `PING` / `CONFIGURE_DOWNLOAD_DIR`

---

## 3. 创建 GitHub Release

1. 仓库：`K-O-N-B/ChaiSniffer-Public`
2. Tag：`host-v0.9.17`（与扩展主版本对齐）
3. Title：`Windows Native Host + Extension v0.9.17`
4. 正文：见 `RELEASE_NOTES/v0.9.17.md` / 私有 `dist-release/RELEASE-host-v0.9.17.md`
5. 上传：`ChaiSniffer-Host-Windows-x64-v0.9.17.zip`；可选附带侧载用 `ChaiSniffer-Extension-v0.9.17.zip`

---

## 4. 商店 / 侧载扩展包

- 内容：`extension/` 目录（**含 JS**，商店运行必需）
- **不含** Host Python 源码
- 打包前确认 `install_links.js` 指向本 Public 仓库 Releases
- Edge 提交清单：`store/EDGE_SUBMISSION_CHECKLIST.md`

商店审核期间可用侧载包自测；**侧载扩展 ID ≠ 商店 ID**，需分别 `setup-bridge`。

---

## 5. 校验清单

- [ ] `setup-bridge.cmd` 在新机器可登记 Native Messaging
- [ ] 设置页 **运行完整自检** 全部 ✓
- [ ] 下载目录设置可保存；成片写入该目录
- [ ] fMP4 / 公开 HLS 成片体积正常（非空壳）
- [ ] Release 页链接与扩展内「打开 GitHub 下载页」一致
