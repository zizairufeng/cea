## About

**`campushpere-auth-simplified`** 使用交互式的配置程序，实现了学工系统的登录，返回的 `cookie` 可直接用于学工系统或今日校园相关验证，基于此可以开发更多强大工具集 ( 例如本项目提供的 [今日校园自动签到] 示例 )

## Prerequisites

- NodeJs
- Git

## Get started

1. 安装此项目

```sh
git clone https://git.io/JL4oc
cd campushpere-auth-simplified && chmod +x init.js
```

2. 初始化学校及用户

- 学校配置:

  ```sh
  ./init.js -s
  ```

- 用户配置:

  ```sh
  ./init.js -u

  ```

- 使用文件配置用户: 根目录下创建 `userConf.yml`, 参考以下示例:

  ```yml
  # 支持多用户配置,用多数组实现
  - username: 11111111
    password: 1
    alias: beetcb
  - username: 22222222
    password: 2
    alias: beet
  ```

2. 工具构建:
   你可以基于本项目完成相应工具开发, 本项目提供 **今日校园自动签到** 示例：
   执行主程序可自动签到

```sh
node index.js
```

## Features

- 交互式配置: `campushpere-awesome-auth` 提供交互式的命令行完成 用户 及 学校 的配置，同时也支持使用 `yml` 文件来配置
- 验证持久化: 缓存验证信息于 cookie , 只在失效时更新

## Thanks

登录中加密过程大量参考 [wisedu-unified-login-api](https://github.com/ZimoLoveShuang/wisedu-unified-login-api) 项目，在此感谢

## Disclaimer

`campushpere-auth-simplified` 用于学习和研究 NodeJs，请勿商用或非法使用。作者: `[beetcb](https://www.beetcb.com)`, 邮箱: `i@beetcb.com`