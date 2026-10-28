# Vista Desktop + Vista Mobile

Vista 的公开发行与更新入口。此仓库只维护公开帮助、经过维护者确认的安装包和签名更新清单；源码在独立的私人仓库维护。

- [下载和版本说明](https://github.com/i-kids/Vista-agent-releases/releases)
- [使用与连接帮助](HELP.md)
- [问题反馈](https://github.com/i-kids/Vista-agent-releases/issues)

已发布 [Vista Desktop 0.1.0-preview.2 桌面预览版](https://github.com/i-kids/Vista-agent-releases/releases/tag/v0.1.0-preview.2)，提供 macOS Apple Silicon、macOS Intel 和 Windows x64 安装包、Vista Ed25519 签名更新清单及 SHA256SUMS。preview.1 用户需先人工安装一次 preview.2；preview.2 已启用 Vista 自有桌面更新通道，安装新版仍由用户点击确认。Mac 为 ad-hoc 签名、未公证，Windows 未正式代码签名；正式平台签名与原生手机发行暂缓。

更新制品使用 `Vista-Desktop-*` / `Vista-Mobile-*` 名称，桌面签名清单为 `vista-update.json`。客户端不会要求用户提供源码仓库的 GitHub 令牌，也不使用 CMB 上游发布物替代 Vista 更新。

## Open-source attribution

Vista 基于 [Codex Mobile Bridge](https://github.com/try2love/codex-mobile-bridge) 的 MIT 许可代码。原作者版权及第三方声明随对应发行物保留；品牌与发行渠道变更不改变这些归属。

