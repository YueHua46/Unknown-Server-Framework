# Unknown Server Framework

<p align="center">
  <img src="docs/assets/usf.jpg" alt="USF" width="720" />
</p>

<p align="center">
  <strong>基于 Minecraft Bedrock Edition ScriptAPI 的生存辅助与服务器管理框架</strong>
</p>

<p align="center">
  <a href="docs/README_en.md">English</a>
  ·
  <a href="docs/README_tw.md">繁體中文</a>
  ·
  <a href="https://github.com/microsoft/minecraft-scripting-samples/tree/main/ts-starter">项目框架参考</a>
</p>

---

## 项目简介

Unknown Server Framework（USF）适用于 Minecraft BE 官方服务端（BDS）、个人存档、LLSE 和 Realms，定位为生存辅助向的服务器管理插件。

> 当前仓库版本可能落后于最新发布版本，也可能比最新发布版本更新。插件所有版本请以 YYTZ666/usfdown 仓库内文件为准。

| 项目       | 信息                                     |
| ---------- | ---------------------------------------- |
| 最新版本   | **USF0.8.0F**                            |
| 作者       | EarthDLL（USFrameTeam）                  |
| 维护       | USFrameTeam                              |
| 社区贡献者 | XiaoXiaoYang、Antonbin、小洋骢、Ice_rink |
| 特别鸣谢   | 交流群全体成员                           |

## 官方资源

| 类型             | 地址                                                                           |
| ---------------- | ------------------------------------------------------------------------------ |
| 所有版本         | [YYTZ666/usfdown](https://github.com/YYTZ666/usfdown/tree/main/files/main)     |
| MineBBS          | [minebbs.com/threads/usf.17109](https://www.minebbs.com/threads/usf.17109/)    |
| KLPBBS           | [klpbbs.com/thread-131213-1-1.html](https://klpbbs.com/thread-131213-1-1.html) |
| USFrameTeam 官网 | [usframeteam.top](https://www.usframeteam.top/)                                |
| USF 文档主站     | [usfdoc.pages.dev](https://usfdoc.pages.dev/)                                  |
| USF 文档域名     | [usfdocs.usframeteam.top](https://usfdocs.usframeteam.top/)                    |
| USF 文档备用     | [docs.usframeteam.top](https://docs.usframeteam.top/)                          |

## 下载站

| 类型     | 域名                      |
| -------- | ------------------------- |
| 主域名   | `d.usframeteam.top`       |
| 跳转域名 | `usfdown.usframeteam.top` |
| 备用域名 | `usfdown.zuyst.top`       |

---

## 功能概览

USF 已实现传送系统、群组系统、领地系统、公告功能、管理功能等核心模块。

### 传送系统

- 返回死亡点
- 玩家 TP
- 固定传送点（管理员设定）
- 世界共享点（玩家设定）
- 个人传送点
- 群组共享点
- 随机传送
- Home 功能

### 群组系统

- 群组历史消息
- 群组内聊天
- 领地共享

### 领地系统

- 设置开放成员 / 队伍
- 设置公共领地

### 公告功能

- 多公告
- 顶置公告
- 新成员公告

### 管理功能

- 背包检查
- 视角跟踪
- 管理领地
- 封禁实体
- 编辑管理员
- 编辑封禁名单
- 禁言 / 屏蔽
- 设置头衔

## 插件设置

- 设置进服提示语
- 设置游戏辅助功能
- 日志系统
- 计分板默认值
- 积分系统
- 血量显示
- 玩家名格式修改
- 聊天显示格式修改
- 传送点、领地、群组设置
- 插件内置命令设置
- 插件主菜单打开方式设置

---

## 开发方式

| 项目     | 说明                           |
| -------- | ------------------------------ |
| 前提     | 已安装 Node.js 和 npm          |
| 安装依赖 | `npm install`                  |
| 源码位置 | `scripts/`、`scripts/modules/` |
| 行为包   | `behavior_packs/`              |
| 日志服务 | `log-server/`                  |

常用流程：

1. 在项目根目录执行 `npm install`。
2. 修改 `scripts/` 下的 TypeScript 源文件。
3. 执行 `npm run build` 编译并打包脚本。
4. 按需使用 `npm run local-deploy`、`npm run mcaddon` 或手动部署到目标服务器。

## 构建方式

| 命令                         | 说明                           |
| ---------------------------- | ------------------------------ |
| `npm run build`              | 编译 TypeScript 并生成脚本产物 |
| `npm run build:production`   | 生产构建                       |
| `npm run lint`               | 运行项目代码检查               |
| `npm run clean`              | 清理构建产物                   |
| `npm run local-deploy`       | 本地监听、构建并部署           |
| `npm run mcaddon`            | 打包为 mcaddon                 |
| `npm run mcaddon:production` | 生产模式打包为 mcaddon         |

部署时，将构建后的行为包文件上传到目标服务器，或使用生成的包文件导入到对应 Minecraft 环境。
