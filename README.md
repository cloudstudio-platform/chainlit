---
name: Chainlit
description: >-
  Build Python LLM apps in minutes ⚡️
  Chainlit lets you create ChatGPT-like UIs on top of any Python code in minutes! Some of the key features include intermediary steps visualisation, element management & display (images, text, carousel, etc.) as well as cloud deployment.
author:
  name: Chainlit
  avatar: https://avatars.githubusercontent.com/u/128686189?s=64&v=4
contributors: 
  - name: willydouhard
    avatar: https://avatars.githubusercontent.com/u/13104895?s=64&v=4
  - name: constantinidan  
    avatar: https://avatars.githubusercontent.com/u/16107237?s=64&v=4
language:
  - language: TypeScript
    percentage: 58.0
  - language: Python
    percentage: 41.5
star: '574'
fork: '201'
url: https://github.com/cloudstudio-platform/chainlit
banner: ./images/quick-start.png
icon: https://cs-res.codehub.cn/vscode/node.svg
video: ./images/Chainlit.mov
license: Apache-2.0
order: 18
---

# 欢迎来到 Chainlit 👋

**在几分钟内构建python LLM 应用程序 ⚡️**

Chainlit 可让您在几分钟之内就在任何Python代码上创建类似于ChatGPT的UI!一些关键功能包括中间步骤的可视化，元素的管理和现实（图像，文本，轮播等）以及云部署

[![](https://dcbadge.vercel.app/api/server/ZThrUxbAYw?style=flat)](https://discord.gg/ZThrUxbAYw)
[![Twitter](https://img.shields.io/twitter/url/https/twitter.com/chainlit_io.svg?style=social&label=Follow%20%40chainlit_io)](https://twitter.com/chainlit_io)
[![CI](https://github.com/Chainlit/chainlit/actions/workflows/ci.yaml/badge.svg)](https://github.com/Chainlit/chainlit/actions/workflows/ci.yaml)

## 安装

打开终端并运行:

```bash
$ pip install chainlit
$ chainlit hello
```

如果 `hello app`现在在您的浏览器中是打开的状态，则表示您已准备就绪!

## 📖 文档

请参阅[此处](https://docs.chainlit.io) 以获取有关一下内容的完整文档:

- 入门（安装，简单示例）
- 例子
- 参考（完整的API文档）

## 🚀 快速开始

### 🐍 python代码

使用以下代码 `demo.py` 创建一个新文件:
```python
import chainlit as cl


@cl.on_message  # this function will be called every time a user inputs a message in the UI
def main(message: str):
    # this is an intermediate step
    cl.Message(author="Tool 1", content=f"Response from tool1", indent=1).send()

    # send back the final answer
    cl.Message(content=f"This is the final answer").send()
```

现在您就可以运行它了！
```
$ chainlit run demo.py -w
```


<img src="/images/quick-start.png" alt="Quick Start"></img>



### 🔗 和 LangChain

查看我们与LangChain的即插即用[集成](https://docs.chainlit.io/langchain)

## 🛣 路线图
- [ ] 新的UI元素（电子表格，视频，轮播）
- [ ] 通过组件的框架来创建您自己的UI元素
- [ ] 基于DAG的思想链接口
- [ ] 在提示场景中支持更多的 LLMs 
- [ ] 应用程序部署

使用 Github issues or on [Discord](https://discord.gg/ZThrUxbAYw)告诉我们您希望在Chainlit中添加哪些内容.

## 💁 贡献

作为快速发展领域中的一项开源计划，我们欢迎您的贡献，无论是通过添加新的功能还是改进文档。

有关如何贡献的详细信息，请参阅[此处](.github/CONTRIBUTING.md).

## 许可
Chainlit 是开源的，并根据[Apache 2.0](LICENSE)许可证获得许可
