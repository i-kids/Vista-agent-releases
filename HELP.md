# Vista 使用与连接帮助

电脑运行原生 CLI 和 Vista Desktop，手机通过 Vista Mobile 或浏览器连接电脑网关。模型地址、模型ID和凭据由使用者在电脑配置，手机不需要登录官方 Codex App。

## 下载与安装

[下载 Vista Desktop 0.1.0-preview.1](https://github.com/i-kids/Vista-agent-releases/releases/tag/v0.1.0-preview.1)，按电脑平台选择：

- Mac Apple Silicon（M 系列）：macOS-arm64.dmg，或同架构 ZIP。
- Mac Intel：macOS-x64.dmg，或同架构 ZIP。
- Windows x64：Windows-x64-Setup.exe；免安装使用同平台 ZIP。

Mac 打开 DMG 后将 Vista Desktop.app 拖入“应用程序”；Windows 运行 Setup.exe。
在电脑准备原生 Codex CLI 并配置自己的模型接入，然后打开 Vista Desktop 启动网关，再连接手机。
版本页同时提供 SHA256SUMS 用于核对下载内容。当前为人工更新预览版，Mac 为 ad-hoc 签名、未公证，Windows 未正式代码签名；应用内自动更新及原生手机发行尚未开放。

## LAN

手机与电脑连接同一可信网络，在 Vista Desktop 启动网关后使用界面显示的地址或配对码。登录信息以该电脑实际生成内容为准，不存在公开通用密码。English: use the gateway URL shown by your own desktop on the same trusted network.

## Quick

临时 Cloudflare 入口用于已明确允许的临时连接；使用软件中显示的实际HTTPS地址。不要把配对码或登录密码发到问题反馈中。入口失效后重新查看电脑状态，不盲目重复发送任务。

## Cloudflare

固定域名需由维护者先配置 Cloudflare Tunnel 与DNS。示例域名 `vista.example.com` 不是在线服务；应使用你自己的域名。配置操作参考[Cloudflare官方文档](https://developers.cloudflare.com/cloudflare-one/networks/connectors/cloudflare-tunnel/)。

## Server

服务器入口需要正确的HTTPS证书和反向代理；先核对已有站点和端口，保留原服务。仅SSH连接不等于手机可直接访问网关。参考[Caddy官方文档](https://caddyserver.com/docs/running)。

## NAS

NAS与服务器相同，需要实际可达且证书正确的HTTPS反向代理。保留原NAS管理入口和站点，不因连接Vista覆盖其他服务。

## External

已有Tailscale或反向代理时，使用维护者明确提供的访问地址。Tailscale必须在同一tailnet中连接并具备相应访问权限，参考[Tailscale官方帮助](https://tailscale.com/docs/how-to/quickstart)。软件中的允许域名列表不会自动创建隧道或配置DNS。

## Updates

唯一Vista发行页为[本仓库Releases](https://github.com/i-kids/Vista-agent-releases/releases)。仅在Vista签名清单和实际发行物就绪后启用相应更新能力。人工更新模式只提示维护者提供新版，不会自动下载或替换程序。保留旧版及数据备份，更新不应改变原CLI账号和项目目录。

## Privacy

反馈请提供平台、Vista版本、失败步骤和脱敏错误；不要上传API Key、登录密码、配对码、聊天历史、SSH私钥、签名密钥或私人源码。English: never post credentials, pairing codes, private source or chat history in public issues.

