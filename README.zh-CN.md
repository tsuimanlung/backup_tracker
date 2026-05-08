# Backup Tracker · 备份记录追踪

基于 Web 的每日备份录入与统计工具。纯 HTML/CSS/JS 实现，无需构建步骤、无需框架、无需后端。数据通过 localStorage 完全存储在浏览器本地。

## 功能

- **每日录入** — 记录备份的系统、类型、状态、数据量、耗时、操作人、来源路径、介质、卷标/序列号及备注
- **数据锁定** — 锁定单条记录或一键锁定当前筛选出的所有记录，防止误编辑或误删除
- **统计图表** — 成功率趋势、每日分布柱状图、各系统成功率、状态分布饼图（基于 ECharts）
- **历史筛选** — 按日期范围、系统和状态筛选记录
- **Excel 导入** — 支持 `.xls` / `.xlsx` 文件导入，自动识别表头
- **Excel 模板下载** — 生成空白模板供离线收集数据
- **深色科幻 UI** — 粒子动画背景、发光效果、扫描线叠加

## 使用方法

1. 浏览器打开 `index.html`（或访问[在线站点](https://tsuimanlung.github.io/backup_tracker/)）
2. 填写备份信息，点击 **Save** 保存
3. 切换到 **History** 标签页查看、筛选、锁定或删除记录
4. 切换到 **Statistics** 标签页查看可视化分析

所有数据保存在浏览器 localStorage 中，不会发送到任何服务器。

## 数据字段

| 字段 | 说明 |
|---|---|
| Date | 备份执行日期 |
| System | 备份系统（12 个预定义选项） |
| Type | Full / Incremental / Differential / Snapshot |
| Status | Success / Fail / Partial / In Progress |
| Data Size | 例如 `256.3 GB` |
| Duration | 例如 `1h 23m` |
| Operator | 备份操作人 |
| Source Path | 备份来源路径（默认 `D:\ACH Shared`） |
| Media | External HDD / NAS / Tape Drive / Object Storage / Optical Disc / Other |
| Volume Label | My Book 1 / My Passport / 2020-My Book |
| Volume SN | 70C4-4CBE / 56C3-C608 / 020E-E18E |
| Note | 备注信息 |

## 技术栈

- [ECharts](https://echarts.apache.org/) — 图表库
- [SheetJS (xlsx)](https://sheetjs.com/) — Excel 导入与模板生成
- localStorage — 数据持久化

## 许可证

MIT
