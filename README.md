# AI服装库 Pages

AI服装库（AI Costume Gallery）的 GitHub Pages 静态页面仓库，用于托管隐私政策和用户协议，供 HarmonyOS 应用市场上架审核使用。

## 应用信息

- 应用名称：AI服装库（AI Costume Gallery）
- 包名：com.xmgod.aifashionlibrary
- 版本：1.1.0（versionCode 1001000）
- 平台：HarmonyOS（API 26 / HarmonyOS 6.0.0(20)+），phone · tablet · 2in1
- 年龄分级：3+｜免费 · 无广告 · 无内购
- 应用源码工程：`/Users/kuku/Documents/Code/HarmonyOS/Apps/ai-costume-gallery-cn`（目录名沿用立项仓库名，不是产品名）

## 关键合规事实

页面正文与下列实现事实一一对应，修改应用时需同步核对：

- `entry/src/main/module.json5` 没有 `requestPermissions` 这个键，包括网络权限；全工程无任何网络 API 引用，`oh-package.json5` 的 `dependencies` 是空对象。应用完全离线运行。
- 本地数据（应用设置、衣橱收藏与备注、最近浏览 / 最近复制 / 搜索记录 / 标签使用次数、工坊草稿）存放在应用沙箱私有目录的关系型数据库与 preferences 文件里，未加密、不上云、不参与备份同步。
- 相册写入只在保存搭配卡时通过系统 `SaveButton` 安全控件触发一次性临时授权；文件导出走 `DocumentViewPicker`，目录由用户选定。
- 不提供 AI 生成合成服务：提示词工坊是检索 + 固定规则模板拼装，相同输入必得相同输出，运行时不调用模型，不产出图片 / 音频 / 视频。界面与文案统一避免「生成」措辞。
- 无账号体系、无广告、无内购、无第三方统计 / 推送 / 崩溃上报 SDK。
- 随包 600 条服装条目、126 个标签与中 / 英 / 日三语文案独立编写；随包参考图版权归原站、仅用于展示，缺图回退代码绘制的矢量剪影；交互机制参考 `Brilliant666/ai-costume-gallery-cn`（代码 MIT、中文译文 CC BY 4.0），在应用内「关于」页与随包 `notice.md` 署名。

## 页面与正本

- `docs/index.html`：GitHub Pages 首页，中文 / English 切换，隐私政策 / 用户协议切换。
- `privacy-policy.md`：中文隐私政策。
- `privacy-policy-en.md`：English privacy policy.
- `terms-of-service.md`：中文用户协议。
- `terms-of-service-en.md`：English terms of service.

四份 Markdown 是协议正本，`docs/index.html` 内的四个正文块（zh/en × privacy/terms）与之一一对应
（隐私政策 10 节、用户协议 11 节），页面不是自动生成物：改正文必须同步改两边。

## 部署说明

仓库已配置 `.github/workflows/pages.yml`，推送到 `main` 分支后自动部署 `docs/` 目录。

GitHub Pages 需在仓库 Settings -> Pages 中将 Source 设置为 `GitHub Actions`。

公开入口：

- 协议中心首页：https://tomkuku588-bot.github.io/aifashionlibrary/
- 隐私政策直达：https://tomkuku588-bot.github.io/aifashionlibrary/?doc=privacy
- 用户协议直达：https://tomkuku588-bot.github.io/aifashionlibrary/?doc=terms
- 英文版直达：在以上地址追加 `&lang=en`

AGC 提审时「隐私政策 URL」填写隐私政策直达地址。

## 与应用内文本的关系

应用内展示的是 `entry/src/main/resources/rawfile/legal/*.md`（中文正本 + 日文概要），由
`scripts/make_legal_html.py` 转出 `docs/上架素材_20261030/legal/*.html`。本仓库页面是按 AGC
审核口径重写的正式版本，内容比应用内更全（含存储位置、删除方式、免责、争议解决等章节），
但结论必须一致：零权限、零联网、数据不出本机、不提供 AI 生成合成服务。

两边任一变动时同步核对：

- 应用内同意门 key `Agreements.CONSENT_KEY` 的后缀即文档版本；改正文就改日期，触发全量重新征求同意。
- 本页面头部元信息里的「更新日期 / 生效日期」与应用内版本号保持一致（当前 2026-11-01）。

## 已知风险

协议页托管在境外 GitHub Pages（`tomkuku588-bot.github.io`），不是已备案域名。应用侧文档
（`docs/上架素材_20261030/AGC上架信息.md` 第三节）把这一条列为待确认风险：提审前需二选一
——迁到已备案域名，或确认华为接受境外托管的协议页。这个坑与页面内容无关，换仓库不会消失。

## 关联远程

```
git remote add origin git@github.com:tomkuku588-bot/aifashionlibrary.git
git push -u origin main
```
