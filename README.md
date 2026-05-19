# 🎁 Gift Recommender

> 智能送礼建议 Agent Skill - 在任何场合送出最合适的礼物

[![收录于 JerryKing's Trove](https://img.shields.io/badge/%E6%94%B6%E5%BD%95%E4%BA%8E-JerryKing's%20Trove-blue)](https://github.com/MRLMRML/JerryKing-s-Trove) [![Scenarios](https://img.shields.io/badge/%E5%9C%BA%E6%99%AF-17%2B-red)](#-核心能力) [![Holidays](https://img.shields.io/badge/%E8%8A%82%E6%97%A5-30%2B-green)](#-核心能力) [![Countries](https://img.shields.io/badge/%E5%9B%BD%E5%AE%B6-12%2B-orange)](#-核心能力) [![Taboos](https://img.shields.io/badge/%E7%A6%81%E5%BF%8C-25%2B-purple)](#-核心能力)

---

## 🎯 项目是什么

Gift Recommender 是一个 AI Skill，帮用户在各种场合做出最合适的送礼决策。

**核心理念**：场合精准、关系得体、预算合理、禁忌不踩。

**工作流程**：

```
用户描述场景 → Agent 读取 SKILL.md → 解析维度 → 加载参考 → 生成方案 → 输出
```

---

## ✨ 核心能力

| 维度 | 覆盖范围 | 说明 |
|------|---------|------|
| 🎊 **中国节日** | 30+ | 春节/中秋/端午等传统节日 + 520/七夕/双11等数字寓意节日 + 母亲节/教师节等现代节日 |
| 🎯 **敏感场景** | 17 类 | 求领导提拔/调动、求客户签单、求医生手术、求老师照顾、入学请托、办户口、打官司、介绍工作等 |
| 🌍 **国际送礼** | 12 区域 | 日/韩/俄/东欧/中亚/东南亚/中东/印度/非洲/拉美/大洋洲/西方通用 |
| 💰 **份子钱** | 7 类场合 | 按关系×城市级别矩阵：婚礼/乔迁/生子/升学/丧事/生日/探病 |
| 🚫 **文化禁忌** | 25+ | 物品禁忌(钟/伞/鞋/梨...) + 数字禁忌(忌4/喜6/8) + 颜色/花卉/地区差异 |
| 🔄 **回礼指南** | 全场景 | 时机/价值比例(等价/加码/减码)/话术/禁忌 |
| 📦 **礼物品类** | 8 大类 | 食品/数码/奢侈品/家居/体验/定制/健康/教育，含品牌推荐和价格参考 |
| 💬 **话术切换** | 6 种风格 | 根据场景自动切换：节日温暖/喜事祝贺/商务得体/求人含蓄/丧事克制/回礼谦逊 |

---

## 🚀 使用方式

### 安装 Skill

```bash
git clone https://github.com/MRLMRML/gift-recommender.git \
  ~/.opencode/skills/gift-recommender
```

### 交互示例

```
用户：中秋节给领导送什么礼物好？预算500-1000
AI：为您推荐3个方案：
    ⭐ 方案一（首推）：高档月饼礼盒+茶叶 ¥600-800
       理由：中秋标配，体面不出错
    方案二：阳澄湖大闸蟹礼盒 ¥500-800
    方案三：高档水果+红酒 ¥500-700
    话术："X总，中秋快乐！一点小心意，祝阖家团圆~"
    避雷：不送钟、伞、梨、单数礼
```

```
用户：朋友结婚，份子钱随多少合适？我在北京
AI：普通朋友：¥500-800 | 好友/闺蜜：¥1000-2000
    吉利数字：666、888、1314
    避雷：忌4、忌单数、用新钞
```

```
用户：求领导帮忙调动工作，怎么送礼？
AI：核心策略：借节日之名，循序渐进
    推荐：高档茶叶礼盒 / 名酒 / 购物卡
    金额：¥2000-8000（视关系和难度）
    话术："领导，我在现在岗位学了很多，但家里确实有困难，想请您帮忙指点指点"
    注意：先试探态度，不要贸然送礼
```

---

## 🏗️ 项目结构

```
gift-recommender/
├── SKILL.md                          # AI Skill 文档（Agent 读取）
├── README.md                         # 项目说明
├── LICENSE                           # MIT 许可证
│
└── references/                       # 参考知识库
    ├── cultural-taboos.md            # 文化禁忌速查
    ├── gift-money-guide.md           # 份子钱矩阵
    ├── sensitive-scenarios.md        # 敏感场景指南（17类）
    ├── chinese-holidays.md           # 中国节日指南
    ├── international-gifts.md        # 国际送礼指南（12区域）
    ├── life-events.md                # 人生事件指南
    ├── business-gifts.md             # 商务送礼指南
    ├── return-gifts.md               # 回礼指南
    └── gift-categories.md            # 礼物品类推荐
```

---

## 📄 License

MIT License
