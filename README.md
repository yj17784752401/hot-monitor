# AI 热点监控工具


## 、项目介绍

这是一套以 **AI 编程实战** 为核心的项目教程，基于 Express 5 + React 19 + OpenRouter + Socket.io，用 AI 编程的方式从 0 到 1 开发一个《AI 热点监控工具》，带你亲身体验 AI Vibe Coding 的完整工作流，学会用 AI 快速做出实用的提效工具！


![](https://pic.yupi.icu/1/image-20260304102630302.png)

输入要监控的关键词，系统自动从 Twitter、Bing、HackerNews、搜狗、B 站等 **8+** 个信息源聚合抓取内容，利用 AI 进行真假识别和相关性分析，并通过 WebSocket 实时推送和邮件通知用户。此外，还将热点监控能力封装为 **Agent Skills 技能包**，让 Cursor、VSCode Copilot、Claude Code 等 AI 编程工具也能直接使用。


既然如此，**不如做一个更通用的工具**。

这就是 AI 热点监控工具的起点：让 AI 帮你盯热点，第一时间获取优质信息！

![](https://pic.yupi.icu/1/AI%E7%83%AD%E7%82%B9%E7%9B%91%E6%8E%A7%E5%AF%B9%E8%AF%9D%E6%A1%86.jpg)



### 6 大核心能力

1）配置监控关键词，支持激活 / 暂停。

![](https://pic.yupi.icu/1/image-20260304102804249.png)



2）AI 自动从 8+ 数据源抓取和分析热点，利用 AI 进行查询扩展、真假识别、相关性分析和智能摘要。

![](https://pic.yupi.icu/1/image-20260304103025682.png)



3）多维度筛选和排序，按来源、重要性、时间范围筛选，按热度、相关性、时间排序。

![](https://pic.yupi.icu/1/image-20260304103219366.png)



4）全网搜索，输入关键词从多个数据源聚合搜索。

![](https://pic.yupi.icu/1/image-20260304103824666.png)



5）实时通知，WebSocket 实时推送 + 邮件通知。

![](https://pic.yupi.icu/1/image-20260304104139285.png)



6）Agent Skills 技能包，安装后在 Cursor、VSCode Copilot、Claude Code 中都能直接使用。

![](https://pic.yupi.icu/1/1772099941189-4fb78679-12ac-4b92-a7b4-b5b4645b09d4.png)




### 前置条件

- Node.js ≥ 18（推荐 20 LTS）
- 一个 [OpenRouter API Key](https://openrouter.ai/settings/keys)（必需，用于 AI 分析）


# 后端
cd server
npm install
npx prisma generate
npx prisma db push

# 前端
cd ../client
npm install
```

### 2. 配置环境变量

```bash
cp server/.env.example server/.env
```

编辑 `server/.env`，至少填入 OpenRouter API Key：

```bash
OPENROUTER_API_KEY=sk-or-v1-你的key
# Twitter API Key（可选）
TWITTER_API_KEY=你的key
```

### 3. 启动服务（两个终端）

```bash
# 终端 1：启动后端（端口 3001）
cd server && npm run dev

# 终端 2：启动前端（端口 5173）
cd client && npm run dev
```

访问 **http://localhost:5173** ，输入关键词即可开始监控热点 🔥

| 服务 | 地址 |
|------|------|
| 前端页面 | http://localhost:5173 |
| 后端 API | http://localhost:3001 |
| 数据库管理 | `cd server && npx prisma studio`（可选） |



