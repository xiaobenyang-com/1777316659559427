# 随机数生成服务器 Random Generator

一款符合MCP协议的加密安全随机数生成服务器，适用于AI应用、LLM及其他需要高质量随机数的系统。
An encrypted and secure random number generation server that complies with the MCP protocol, suitable for AI applications, LLMS, and other systems that require high-quality random numbers.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| generate_random_integer | Generate cryptographically secure random integers within a specified range |
| generate_random_float | Generate cryptographically secure random floating-point numbers |
| generate_random_bytes | Generate cryptographically secure random bytes |
| generate_uuid | Generate a cryptographically secure UUID (v4) |
| generate_random_string | Generate a cryptographically secure random string |
| generate_random_choice | Randomly select items from a given list using cryptographically secure randomness |
| generate_random_boolean | Generate cryptographically secure random boolean values |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659559427](https://mcp.xiaobenyang.com/inspector/1777316659559427)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659559427](https://mcp.xiaobenyang.com/inspector/1777316659559427)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "随机数生成服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659559427/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "随机数生成服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659559427/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "随机数生成服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659559427",
          },
          "transport": "stdio"
        }
      }
}

```
