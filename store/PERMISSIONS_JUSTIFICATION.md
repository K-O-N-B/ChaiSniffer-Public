# 权限说明（商店审核 / 用户透明）

扩展 Manifest V3 权限与 **仅本地用途** 对照。

| 权限 | 用途 | 数据是否上传 |
|------|------|--------------|
| `nativeMessaging` | 与已安装的本机 Host 交换下载/播放指令 | 否 |
| `webRequest` | 观察网络请求以嗅探 m3u8/mpd/媒体 URL | 否 |
| `storage` | 保存用户设置（嗅探开关、站点规则等） | 否（浏览器本地 sync/local） |
| `cookies` | 读取 **当前页面** Cookie 写入本机请求 | 否 |
| `contextMenus` | 扩展图标右键菜单（设置、项目主页） | 否 |
| `tabs` | 获取当前标签页、打开设置/工具页 | 否 |
| `webNavigation` | 页面导航时刷新嗅探上下文 | 否 |
| `alarms` | 保持 Service Worker 活跃（低频率） | 否 |
| `scripting` | 在页面注入嗅探脚本（与 content_scripts 配合） | 否 |
| `downloads` | 浏览器侧下载辅助（主下载由 Host 完成） | 否 |
| `declarativeNetRequest` | 可选：模拟移动端 UA 规则 | 否 |
| `declarativeNetRequestWithHostAccess` | 同上，需 host 权限 | 否 |
| `host_permissions: http(s)://*/*` | 在所有站点嗅探（用户可配置黑白名单） | 否 |
| `host_permissions: file:///*` | 本地 HTML 文件页面测试 | 否 |

**Content scripts** 在页面主世界注入钩子以捕获媒体地址与可选深度搜钥（默认关闭）。不修改页面 UI，不向远程服务器发送页面内容。

**本机 Host** 不在扩展包内；用户从 GitHub Releases 自行安装，扩展仅通过 Native Messaging 与其通信。
