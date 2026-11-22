# LanguageTool for TOS

LanguageTool checks grammar and spelling through an HTTP API. Install the package for your NAS architecture on TOS 7 with Docker Engine. In a client that supports custom LanguageTool servers, use `http://<NAS IP>:18884/v2` as the API base URL. The package provides an API service.

Use the endpoint from a trusted network. The API accepts text without authentication, so restrict access to the intended clients. For a quick check, replace `NAS-IP` in the command below. The response contains suggested replacements in `matches`.

```sh
curl -fsS 'http://NAS-IP:18884/v2/check' \
  --data-urlencode 'language=en-US' \
  --data-urlencode 'text=I has a book.'
```

## TOS 使用说明

LanguageTool 通过 HTTP API 检查语法与拼写。请在安装了 Docker Engine 的 TOS 7 上选择适合 NAS 架构的安装包。在支持自定义服务的客户端中，将 API 基础地址设为 `http://<NAS IP>:18884/v2`。此包提供 API 服务。

请限制为可信网络内的指定客户端访问。API 接收待检查的文本，无需身份验证。可将上述命令中的 `NAS-IP` 改成 NAS 地址进行检查，返回的 `matches` 中列出了修改建议。

[上游项目 / Upstream](https://github.com/languagetool-org/languagetool) · [镜像构建来源 / Container source](https://github.com/Erikvl87/docker-languagetool) · [HTTP API](https://languagetool.org/http-api/swagger-ui/)
