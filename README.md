# 🌍 环游世界小课堂 · World Explorer for Kids

给小学一年级小朋友的世界地理网页，中英文双语，可离线使用。
A bilingual (Chinese + English) world geography web page for Grade 1 kids. Works fully offline.

## 打开方式 · How to open

双击 `index.html`，用任意浏览器打开即可。不需要安装、不需要联网。
Just double-click `index.html` in any browser. No install, no internet needed.

## 功能 · Features

**📚 学习 Learn**
- **24 个国家**，按洲分类（亚洲 / 欧洲 / 非洲 / 北美洲 / 南美洲 / 大洋洲）
- **国家卡片** — 国旗、中英文国名、首都、3 条一年级能懂的小知识、当地「你好」怎么说
- **国家三宝** — 每个国家的 🏛️ 地标建筑、🐾 代表动物、🌸 国花，点一下就会读出名字
- **🌏 3D 地球** — 会自转，可拖动；点国家后地球自动飞过去并插上小旗

**🎮 四个游戏 Games**
- **🎯 地球寻宝** — 「在地球上找到日本！」转动地球找出目标国家，答错会提示所在大洲和方向
- **🐾 动物找家** — 把小动物配对回它的国家，配对成功会说出「袋鼠住在澳大利亚」
- **🚩 国旗配对** — 8 道选国旗的题，答错会显示正确答案
- **🛂 环游世界护照** — 每认识一个新国家就盖一个章，24 个集满有奖状；进度自动保存在浏览器里

**🔊 语音 · 🈳 双语**
- 所有游戏全程中英文朗读（浏览器语音合成），可一键关闭
- 三档语言切换：中英对照 / 纯中文 / 纯英文

## 技术说明 · Notes

- 单文件，零依赖：HTML + CSS + 原生 JavaScript
- 24 面国旗 + 24 个地标建筑全部为内嵌手绘 SVG（Windows 不支持 emoji 国旗，故未使用 emoji）
- 24 种国花由参数化 SVG 生成（花瓣数 / 花瓣形状 / 颜色）
- 地球为 canvas 正射投影（orthographic projection）实时绘制，海陆轮廓为简化坐标数据
- 护照进度存于 `localStorage`，键名 `we_passport_v1`

## 添加国家 · Adding a country

1. 在 `index.html` 的 `COUNTRIES` 数组中照格式加一条（含 `lat` / `lon` 经纬度）
2. 在 `FLAGS` 对象中加上对应的国旗绘制函数
3. 在 `EXTRA` 中加上该国的地标 / 动物 / 国花，地标图形加在 `LM` 对象里
