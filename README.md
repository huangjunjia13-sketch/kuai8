# 快乐8开奖记录抓取器 V1

静态网页版，可直接部署到 GitHub Pages。

## 功能
- 调用灰鸟免费彩票 API 的快乐8（`klb`）历史接口
- 自动分页抓取
- 按年份筛选（默认 2026）
- 校验每期是否为 20 个不重复的 01–80 号码
- 网页预览
- 导出 `快乐8_2026.csv`
- CSV 字段：`issue,date,n1,...,n20`

## GitHub Pages
把本目录文件上传到仓库根目录，Settings → Pages → Deploy from a branch → main / root。

## 重要
这是纯前端版本。浏览器是否能直接抓取，取决于数据接口是否允许跨域（CORS）。
如果 GitHub Pages 打开后日志显示 `Failed to fetch` / `CORS`，需要增加一个 Cloudflare Worker / Pages Function 代理接口；前端解析和 CSV 导出部分无需重写。

数据接口文档：
https://api.huiniao.top/
