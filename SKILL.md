---
name: world-cup-cal-subscription
description: |
  帮助球迷一键订阅 2026 美加墨世界杯完整赛程日历（iCal/.ics），自动同步到
  iPhone、Mac、Android、Google 日历、Outlook 等，每日自动更新比分与赛果。
---

# 世界杯赛程日历订阅助手

帮助用户把 2026 FIFA 世界杯全部赛程同步到手机/电脑日历，无需部署、无需编程。

- 上游项目: https://github.com/lizijing98/world-cup-cal
- 发现来源: https://www.v2ex.com/t/1212567
- 许可: ISC
- GitHub Stars: 25+
- 语言: JavaScript (Node.js)
- CI: GitHub Actions 每日自动拉取 football-data.org 数据并重新生成 .ics 文件

## 用户场景

当用户想要：

- 把 2026 世界杯全部 104 场比赛一次性导入日历 App
- 用 iPhone/Mac/Android 自带日历订阅世界杯赛程
- 在 Google 日历或 Outlook 中添加世界杯赛程
- 不想手动逐场添加，希望订阅后自动更新比分和赛果
- 选择 CDN 订阅地址（jsdelivr）或 GitHub raw 地址
- 了解 iCal 订阅的工作原理和更新频率设置建议

## 订阅地址

### 推荐地址（CDN，全球可用）

```
https://cdn.jsdelivr.net/gh/lizijing98/world-cup-cal@master/WorldCupSchedule.ics
```

### 备用地址（GitHub raw，部分地区需代理）

```
https://raw.githubusercontent.com/lizijing98/world-cup-cal/master/WorldCupSchedule.ics
```

## 操作指南

### iPhone / Mac

1. 打开「设置」→「日历」→「账户」→「添加账户」→「其他」
2. 选择「添加已订阅的日历」
3. 粘贴上方 CDN 订阅地址
4. 建议将刷新频率改为「每天」

### Google 日历

1. 打开 Google 日历网页版
2. 点击左侧「其他日历」旁的 + 号 →「通过 URL 添加」
3. 粘贴订阅地址，点击「添加日历」

### Outlook

1. 打开 Outlook 日历
2. 选择「添加日历」→「从 Internet 订阅」
3. 粘贴订阅地址

## 日历内容

每条日历事件包含：

- 比赛标题：主队 vs 客队（含国旗 emoji）
- 开始/结束时间：UTC 时间，日历 App 自动转本地时区
- 比赛阶段：小组赛 / 淘汰赛轮次
- 比分：已完赛的自动更新最终比分
- 更新时间戳

## 输入

- 用户的设备类型和日历 App（iPhone/Android/Mac/Google/Outlook/飞书等）
- 是否需要代理（决定推荐哪个订阅地址）
- 可选：时区偏好、感兴趣的球队

## 输出

- 具体的订阅操作步骤（适配用户的设备和日历 App）
- 正确的订阅 URL
- 刷新频率设置建议
- 常见问题排查（订阅失败、时区不对、事件不更新等）
