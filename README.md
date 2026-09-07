# Warp Loves Anyone

[English](#english) | [简体中文](#zh-cn)

<a id="english"></a>
## English

An Xposed module (libxposed API 102) that forces apps of your choice through the Cloudflare WARP tunnel, and makes the Cloudflare apps' dark mode follow the system setting.

### Features

- Force any package through WARP: blocks selected packages from being added to the VPN's disallowed applications list
- "Force proxy list" entry injected into the apps' Settings → Advanced → Connection options (native-style list with per-app remove, plus a multi-select app picker with icons)
- "Follow system theme" switch injected into Settings → Advanced; when on, the apps' dark theme toggle is managed by the system
- Scope: `com.cloudflare.onedotonedotonedotone`, `com.cloudflare.cloudflareoneagent`

### Requirements

- A libxposed-compatible framework with API 102 support (e.g. LSPosed 2.x+)

### Usage

1. Enable the module in LSPosed (scope is fixed to the two Cloudflare apps)
2. Manage the force proxy list inside the apps: Settings → Advanced → Connection options
3. Reconnect the VPN to apply the list

### Build

Source: https://github.com/Baidaofu/WarpLovesanyone

```bash
./gradlew assembleRelease
```

<a id="zh-cn"></a>
## 简体中文

[English](#english) | [简体中文](#zh-cn)

一个 Xposed 模块(libxposed API 102):让任意 App 的流量强制走 Cloudflare WARP 隧道,并让 Cloudflare App 的暗色模式跟随系统设置。

### 功能

- 强制任意包名走 WARP:阻止所选包名进入 VPN 的「排除应用」列表
- 在 App 的 设置 → 高级 → 连接选项 内注入「强制代理列表」入口(原生风格列表 + 图标多选选择器)
- 在 设置 → 高级 内注入「跟随系统主题」开关;开启后 App 的深色主题由系统代管
- 作用域:com.cloudflare.onedotonedotonedotone、com.cloudflare.cloudflareoneagent

### 要求

- 支持 libxposed API 102 的框架(如 LSPosed 2.x+)

### 使用

1. 在 LSPosed 中启用模块(作用域固定为上述两个 App)
2. 在 App 内管理强制代理列表:设置 → 高级 → 连接选项
3. 修改列表后断开并重连 VPN 生效

### 构建

源码:https://github.com/Baidaofu/WarpLovesanyone

```bash
./gradlew assembleRelease
```

## License

Same as the upstream project: [WarpLovesPlayStore](https://github.com/BruceZhang1993/WarpLovesPlayStore) (MIT).
