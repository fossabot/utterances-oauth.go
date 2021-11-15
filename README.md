# utterances-oauth.go

[utterances](https://github.com/utterance) API 的非官方 Golang 实现

![Build Status](https://img.shields.io/github/workflow/status/GizmoOAO/utterances-oauth.go/docker%20build%20&%20push)
![GitHub last commit (branch)](https://img.shields.io/github/last-commit/GizmoOAO/utterances-oauth.go/main)
[![GitHub](https://img.shields.io/github/license/GizmoOAO/utterances-oauth.go)](./LICENSE)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FGizmoOAO%2Futterances-oauth.go.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FGizmoOAO%2Futterances-oauth.go?ref=badge_shield)

中文 | [English](./README-en.md)

# 安装与使用

## 配置

使用前需要在执行目录创建名为 `.env` 的文件. 文件的值请参考下表: [例子](./.env.example)

- BOT_TOKEN: 创建 issues 时使用的 Github 个人令牌, [点这创建](https://github.com/settings/tokens/new?scopes=public_repo)
- CLIENT_ID: [GitHub OAuth web application flow](https://developer.github.com/v3/oauth/#web-application-flow) 使用的 `ClientID`, 创建 Github App 后可以获得.
- CLIENT_SECRET: [GitHub OAuth web application flow](https://developer.github.com/v3/oauth/#web-application-flow) 使用的 `ClientSecret`, 创建 Github App 后可以获得.
- STATE_PASSWORD: 32 位密码, 用于加密 `state`, [点这创建](https://lastpass.com/generatepassword.php).
- ORIGINS: 来源域列表, 用于 [CORS](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Access_control_CORS), 多个来源域使用英文半角逗号分隔.

## 快速部署到 Vercel

点击 deploy 按钮来开始你的部署！

[![Deploy to Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/GizmoOAO/utterances-oauth.go)

## 从源码安装

编译非常简单, 只需要安装好 [Go](https://golang.org/) , 然后执行 `go build` 就可以完成编译. 但在运行前你需要修改好 `.env` 文件.

```bash
git clone https://github.com/GizmoOAO/utterances-oauth.go.git
cd utterances-oauth.go
go build
```

## 使用 Docker

使用 Docker 的方式运行非常简单, 只需要将 `docker-compose.yaml` 文件上传到安装了 Docker 的服务器, 执行下面的命令就可以成功运行.

```bash
docker-compose up -d
```

# 感谢

- [utterance](https://github.com/utterance)

# 许可证

MIT


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FGizmoOAO%2Futterances-oauth.go.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FGizmoOAO%2Futterances-oauth.go?ref=badge_large)