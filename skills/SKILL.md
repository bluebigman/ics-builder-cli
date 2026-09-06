# 日历 ICS 工具箱（ics-builder-cli）

生成 .ics 日历事件/解析日历文件/多日历找空闲时段。纯本地文件处理，不同步任何云日历。

本工具仅做本地数据/文本处理，不采集任何个人信息。

## 命令
| 命令 | 用途 |
|---|---|
| `ics-builder status` | 自检（返回含 ok） |
| `ics-builder auth` | 校验可用（本地工具无需密钥） |
| `ics-builder unAuth` | 清除本地状态 |
| `ics-builder create <标题> <开始> [结束] [--desc 描述] [--file 路径]` | 生成事件（开始 YYYY-MM-DD[ HH:mm]） |
| `ics-builder parse <文件.ics>` | 解析日历事件清单 |
| `ics-builder free <文件1.ics> <文件2.ics> …` | 多日历找空闲窗口 |

所有命令输出 JSON：`{"code":0|1,"ok":true|false,"data":...,"error":"人类可读错误"}`。

## AI 使用指引
用户要安排会议/导入日历 → create（保存用 --file）；查档期用 parse/free。
