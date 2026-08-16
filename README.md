# 🌍 环游世界小课堂 · World Explorer for Kids

给小学一年级小朋友的世界地理网页，中英文双语，可离线使用。
A bilingual (Chinese + English) world geography web page for Grade 1 kids. Works fully offline.

## 打开方式 · How to open

双击 `index.html`，用任意浏览器打开即可。不需要安装、不需要联网。
Just double-click `index.html` in any browser. No install, no internet needed.

## 功能 · Features

- **24 个国家** — 按洲分类（亚洲 / 欧洲 / 非洲 / 北美洲 / 南美洲 / 大洋洲）
- **国家卡片** — 国旗、中英文国名、首都、3 条一年级能懂的小知识、当地「你好」怎么说
- **🔊 朗读** — 用浏览器语音读出国名（中文 + 英文）
- **🌏 3D 地球** — 会自转，可拖动；点国家后地球自动飞过去并插上小旗；地球上的白点也可直接点选
- **🈳 语言切换** — 中英对照 / 纯中文 / 纯英文
- **🎮 国旗小游戏** — 8 道选国旗的题，答错会显示正确答案，最后给分

## 技术说明 · Notes

- 单文件，零依赖：HTML + CSS + 原生 JavaScript
- 24 面国旗全部为内嵌手绘 SVG（Windows 不支持 emoji 国旗，故未使用 emoji）
- 地球为 canvas 正射投影（orthographic projection）实时绘制，海陆轮廓为简化坐标数据

## 添加国家 · Adding a country

1. 在 `index.html` 的 `COUNTRIES` 数组中照格式加一条（含 `lat` / `lon` 经纬度）
2. 在 `FLAGS` 对象中加上对应的国旗绘制函数
