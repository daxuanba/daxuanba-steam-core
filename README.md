<div align="center">
  <img src="logo.png" alt="大轩巴 · daxuanba" width="560">
</div>

# 大轩巴万能内核

> daxuanba-core · 自研入库内核 · v1.0.0

[大轩巴入库器mini](https://github.com/daxuanba/daxuanba-Injector-mini) 唯一内置的入库内核。
文件分发型：不注入、不常驻、不需要 Steam 客户端运行。

## 它是什么

按游戏 exe 的位数（x64 / x86），把对应架构的内核文件放进游戏 exe 同目录，
由游戏自己加载：

| 64 位 | 32 位 |
| --- | --- |
| `steam_api64.dll` / `daxuanba64.dll` | `steam_api.dll` / `daxuanba.dll` |

另有 `dwmapi.dll` / `xinput1_4.dll` 辅助模块，导出 1000+ Steamworks 接口。

## 特点

- **单内核**：不需要 GreenLuma / SteamTools / OpenSteamTool，也不存在多套内核互相打架
- **双架构**：自动识别游戏 exe 是 32 位还是 64 位，选对应 DLL
- **清单驱动**：读取 Steam `config/lua/appid_*.lua`，自动识别 AppID / DLC / 成就
- **配置**：`daxuanbacore.toml`（优先）或 `daxuanba.json`
- **不常驻**：没有后台服务，不往 Steam 目录塞代理 DLL

## 使用

通过入库器 mini 的「内核」页一键安装，或手动把对应位数的 DLL 复制到游戏 exe 所在目录。
首次使用建议先备份游戏目录。

## 配套应用：大轩巴入库器mini

[大轩巴入库器mini](https://github.com/daxuanba/daxuanba-Injector-mini) 是配套的 Windows 桌面工具，
一个 exe 双击即用：

- 内核一键安装 / 卸载 / 状态检查
- 免费游戏走 Steam 官方接口真入库（提交前后复查真实账号库）
- 用户名 + 密码 + 邮箱验证码登录
- 扫 Steam 清单目录，识别每个游戏由哪个工具写入
- 有 DLC 才显示小按钮，弹窗看原图标与真实拥有状态
- 应用启动即自动开启网络加速

程序数据统一放 `%APPDATA%\DaXuanBa\DXB-Mini`，程序目录只留一个 exe。


---

<div align="center">大轩巴 · daxuanba</div>
