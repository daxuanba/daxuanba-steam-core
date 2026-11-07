<div align="center">
  <img src="logo.png" alt="大轩巴 · daxuanba" width="560">
</div>

# 大轩巴万能内核

> daxuanba-core · 自研 Steamworks 模拟内核 · v1.0.0

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

---

<div align="center">大轩巴 · daxuanba</div>
