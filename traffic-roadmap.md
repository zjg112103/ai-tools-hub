# AI 工具箱网站 - 流量优化待办清单

> 唯一目的：上线后吸引流量。按优先级排序，从见效快到见效慢。
> 最后更新：2026-05-15

---

## ✅ 已完成

- [x] 15 个工具详情页（chatgpt, deepseek, claude, chatglm, kimi, midjourney, stable-diffusion, klingai, cursor, copilot, notion-ai, doubao, tongyi, dalle, runway）
- [x] 4 个排行榜页面（AI对话 / AI绘画 / AI编程 / AI视频）
- [x] sitemap.xml（所有页面收录）
- [x] robots.txt
- [x] 首页排行榜入口按钮
- [x] 首页工具对比功能
- [x] 详情页互相链接（推荐替代工具）

---

## 🔥 P0 - 最高优先级（1-2 天内完成）

### 1. 对比专题页
**为什么重要**：用户搜"ChatGPT vs DeepSeek"、"可灵 vs Runway"这种对比词的非常多，搜索意图明确，转化率高。

**要做的事**：
- [x] `compare/chatgpt-vs-deepseek.html` → ChatGPT 和 DeepSeek 全面对比
- [x] `compare/midjourney-vs-stable-diffusion.html` → AI 绘画两大巨头对比
- [x] `compare/cursor-vs-copilot.html` → AI 编程工具对比
- [x] `compare/klingai-vs-runway.html` → AI 视频工具对比
- [x] `compare/deepseek-vs-chatglm.html` → 国产免费 AI 对比
- [x] `compare/kimi-vs-deepseek.html` → 读论文 vs 编程，两个免费工具对比
- [x] 每个页面做成横向深度对比：表格 + 结论 + 推荐
- [x] 更新 sitemap 加入对比页

**每个对比页包含**：
- 标题含两个工具名（SEO）
- 核心指标对比表格（价格、中文、国内可用、代码、写作等）
- 按场景推荐（什么场景选A、什么场景选B）
- 链接回各自的详情页

---

### 2. Google Search Console 提交
**为什么重要**：这是免费搜索流量最重要的入口。提交后 Google 开始索引页面，通常 1-2 周后开始有搜索展现。

**要做的事**：
- [ ] 用 Google 账号登录 https://search.google.com/search-console
- [ ] 添加网站 `https://my-ai-tools-hub.netlify.app/`
- [ ] 验证方式：HTML 标签验证（在首页 head 里加 meta 标签）
- [ ] 提交 sitemap：`https://my-ai-tools-hub.netlify.app/sitemap.xml`
- [ ] 等待 Google 索引（1-2 周）

---

### 3. 首页结构化数据（JSON-LD）
**为什么重要**：帮助 Google/Bing 更好理解网站内容，搜索结果可能显示星级、面包屑等富文本，点击率更高。

**要做的事**：
- [x] 在首页 `<head>` 加 JSON-LD Schema.org 标记
- [x] 类型：`WebSite` + `ItemList`（工具列表）
- [x] 包含网站名称、URL、描述
- [x] 详情页也加 `SoftwareApplication` + `AggregateRating`
- [x] 排行榜和对比页加 `Article` schema

---

## 📈 P1 - 高优先级（1 周内）

### 4. 博客/教程文章
**为什么重要**：长期流量最大的来源。教程类文章覆盖长尾搜索词，持续带来流量。

**要写的文章**：
- [ ] `blog/free-ai-tools-2026.html` → "2026 年 15 个免费 AI 工具推荐（不用花一分钱）"
- [ ] `blog/ai-tools-no-vpn.html` → "不用翻墙也能用的 AI 工具汇总（国内直接访问）"
- [ ] `blog/midjourney-beginner-guide.html` → "AI 绘画入门：从零开始学 Midjourney"
- [ ] `blog/ai-coding-tools-compare.html` → "AI 编程工具对比：Cursor vs Copilot vs TRAE"
- [ ] `blog/ai-video-tools-guide.html` → "AI 视频生成入门：5 个工具让你做出短视频"
- [ ] `blog/best-ai-for-students.html` → "学生必备 AI 工具：论文/编程/学习全部免费"
- [ ] `blog/best-ai-for-work.html` → "上班族 AI 工具推荐：写邮件/做PPT/翻译提效"

**每篇文章**：1500-2500 字，覆盖长尾搜索词，内容可复用详情页素材。

---

### 5. Open Graph + 社交分享优化
**为什么重要**：用户分享到微信/微博/知乎时显示好看的预览卡片，提升点击率。

**要做的事**：
- [ ] 所有页面 `<head>` 加 Open Graph 标签（og:title, og:description, og:image, og:url）
- [ ] 设计一个默认分享图（1200x630px），可以用 AI 生成
- [ ] 加 Twitter Card 标签
- [ ] 加微信分享缩略图支持

---

### 6. 百度搜索优化
**为什么重要**：国内用户主要用百度，百度对中文内容友好。

**要做的事**：
- [ ] 百度站长平台提交网站（https://ziyuan.baidu.com）
- [ ] 添加百度统计代码（了解访客数据）
- [ ] 确保页面 title 和 description 包含核心中文关键词
- [ ] 页面之间互相链接（百度爬虫靠链接发现页面）
- [ ] 等百度账号配额恢复后提交站点

---

## 🎯 P2 - 中期优化（持续）

### 7. 用户评分功能
**为什么重要**：页面有互动 → 用户停留时间更长 → SEO 排名更好。评分本身是搜索结果亮点。

**要做的事**：
- [ ] 工具卡片和详情页加评分组件（1-5 星 + 简短评价）
- [ ] 数据存在 localStorage（不依赖后端）
- [ ] 显示平均评分和评价数量
- [ ] 详情页的 JSON-LD 加 AggregateRating

---

### 8. 工具收藏功能
**为什么重要**：用户收藏后下次会回来 → 增加回访率 → 搜索引擎认为网站有价值。

**要做的事**：
- [ ] 工具卡片加"收藏"按钮
- [ ] 收藏列表存在 localStorage
- [ ] 首页加"我的收藏"筛选
- [ ] 收藏数量显示在页面某处

---

### 9. 每周 AI 工具速报
**为什么重要**：让用户有理由经常回来，覆盖"最新 AI 工具"时效性搜索词，百度/Google 喜欢持续更新的网站。

**要做的事**：
- [ ] 创建 `weekly/` 目录
- [ ] 每周更新一期（手动或半自动）
- [ ] 内容：本周新工具、工具更新、行业动态
- [ ] 首页加"本周速报"入口

---

### 10. 更多详情页
**为什么重要**：每个详情页都是一个独立的 SEO 页面，覆盖不同的搜索词。

**待做的详情页**：
- [ ] Gemini（Google 出品，搜索量高）
- [ ] Grok（马斯克出品，话题性强）
- [ ] 即梦 AI（国产 AI 绘画，免费）
- [ ] LiblibAI（国产 SD 平台）
- [ ] Seedance（字节 AI 视频）
- [ ] TRAE（字节 AI IDE，完全免费）
- [ ] Replit AI（在线编程平台）
- [ ] Pika（AI 视频工具）
- [ ] Jasper AI（AI 营销写作）
- [ ] Copy.ai（AI 文案）
- [ ] MiniMax（国产 AI）
- [ ] 讯飞星火（科大讯飞 AI）

---

## 📊 网站技术优化

### 11. 页面加载速度
- [ ] 检查首页加载速度（Google PageSpeed Insights）
- [ ] 压缩 CSS/JS（目前是内联的，已经比较轻量）
- [ ] 图片懒加载（如果后续加图片的话）
- [ ] Netlify CDN 已经自带，速度应该可以

### 12. 移动端体验
- [ ] 检查排行榜页面在手机上的显示
- [ ] 检查详情页在手机上的显示
- [ ] 确保所有按钮可点击、文字可读

### 13. 404 页面
- [ ] 创建友好的 404 页面
- [ ] 包含"返回首页"和搜索框

### 14. 网站图标
- [ ] 设计一个 favicon.ico（可以用 AI 生成）
- [ ] 加到所有页面的 `<head>` 里

---

## 📈 数据追踪

### 15. 访客分析
- [ ] 添加 Google Analytics（了解访客来源和行为）
- [ ] 或用百度统计（国内更准确）
- [ ] 追踪：每日访客、热门页面、搜索词、跳出率

### 16. 搜索表现监控
- [ ] Google Search Console 看搜索展现和点击
- [ ] 百度站长平台看索引量和关键词排名
- [ ] 每周记录数据变化

---

## 💡 内容策略

### 17. 长尾关键词覆盖
思路：不要只做"AI工具"这种大词（竞争太激烈），多做长尾词：
- "ChatGPT 怎么注册"
- "DeepSeek 免费吗"
- "可灵 AI 和 Runway 哪个好"
- "不用翻墙的 AI 工具"
- "学生免费 AI 工具"
- "AI 绘画 Prompt 怎么写"

每个长尾词写一个页面或文章，积少成多。

### 18. 竞品差异化
和其他 AI 工具导航网站（AI Bot、ToolAI 等）相比，我们的差异化：
- ✅ 工具对比功能（其他站没有）
- ✅ 详细评测页面（其他站只有卡片）
- ✅ 排行榜页面（其他站没有）
- ✅ 全部中文、面向国内用户
- 计划：对比专题页（其他站没有）
- 计划：教程博客（其他站没有）

---

## 📋 执行顺序建议

| 批次 | 内容 | 预计时间 |
|------|------|---------|
| 第 1 批 | 对比专题页（6 个） | 半天 |
| 第 2 批 | Google Search Console + 结构化数据 | 1-2 小时 |
| 第 3 批 | 博客文章（先写 2-3 篇） | 半天 |
| 第 4 批 | Open Graph + 百度优化 | 1-2 小时 |
| 第 5 批 | 用户评分 + 收藏功能 | 2-3 小时 |
| 第 6 批 | 更多详情页（持续） | 每个半小时 |
| 持续 | 每周速报 + 更多博客 | 每周 1-2 小时 |
