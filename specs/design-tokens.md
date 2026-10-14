# 零压画铺 · 设计变量规范 (Design Tokens)

> 所属：零压画铺 Chill Sketch Hub　｜　上级文档：[prd.md](../prd.md)
> 说明：本文是视觉的「单一事实来源」。所有组件与页面均引用此处的变量，改主题只需改这里。

## 1. 颜色 (Color)

### 1.1 基础色板

| 变量 | 色值 | 名称 / 用途 |
| --- | --- | --- |
| `--color-paper` | `#FAF7F0` | 墙面 / 页面底色 |
| `--color-paper-alt` | `#F3EEE3` | 卡片底 / 次级底色 |
| `--color-surface` | `#FEFBF5` | 浮起卡片 / 弹层底（比纸略亮，非纯白） |
| `--color-sage` | `#8A9A7B` | 主色（招牌绿） |
| `--color-sage-deep` | `#6B7F5E` | 主色-深（按压 / 强调文字） |
| `--color-sage-soft` | `#DCE3D5` | 主色-浅底（选中背景） |
| `--color-wood` | `#C9A87C` | 木质（招牌 / 木牌） |
| `--color-wood-light` | `#D9C4A0` | 牛皮纸（标签 / 胶带） |
| `--color-orange` | `#E08A4B` | 暖橘（营业灯 / 主要行动点） |
| `--color-orange-deep` | `#D96B4A` | 番茄（强调按压 / 警示） |
| `--color-yellow` | `#F2E2A8` | 手账点缀-黄 |
| `--color-pink` | `#E8C4C4` | 手账点缀-粉 |
| `--color-seal` | `#C15B45` | 印章朱红（打卡 / 完成） |
| `--color-seal-gold` | `#D9A441` | 金章（第 5 次强烈肯定 / 超额赞扬叠加） |
| `--color-ink` | `#4A4238` | 正文文字 |
| `--color-ink-soft` | `#7A6F63` | 次要文字 / 说明 |
| `--color-line` | `#E3DACB` | 分割线 / 描边 |

### 1.2 语义别名（组件优先引用这层）

| 变量 | 指向 | 用途 |
| --- | --- | --- |
| `--bg` | `--color-paper` | 页面背景 |
| `--surface` | `--color-surface` | 卡片 / 弹层背景 |
| `--text` | `--color-ink` | 主文字 |
| `--text-muted` | `--color-ink-soft` | 次要文字 |
| `--brand` | `--color-sage` | 品牌主色 |
| `--accent` | `--color-orange` | 强调 / 行动点 |
| `--border` | `--color-line` | 描边 / 分割 |

### 1.3 用色规则

- **绿色为主、木色打底、暖橘只做小面积点亮**（招牌灯、印章、关键按钮）。
- 避免纯黑 `#000` 与纯白 `#FFF`；文字禁用纯黑，用 `--color-ink`。
- 单个屏幕内品牌色系建议不超过 3 种主色块，保持"温和纸感"。

## 2. 字体 (Typography)

> 中文字体文件体积大。策略：**正文走系统字体**（保证离线流畅），**仅标题 / 落款引入轻量 Web Font**（子集化后通常 < 300KB）。

| 变量 | 字体栈 | 用途 |
| --- | --- | --- |
| `--font-title` | `"站酷快乐体", "LXGW WenKai", "PingFang SC", "Microsoft YaHei", sans-serif` | 招牌 / 页面标题 |
| `--font-hand` | `"Ma Shan Zheng", "LXGW WenKai", cursive` | 落款 / 日期 / 便签手写感 |
| `--font-body` | `system-ui, -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif` | 正文 / 界面文字 |

### 字号与行高

| 变量 | 值 | 用途 |
| --- | --- | --- |
| `--fs-display` | `28px / 1.25` | 页面招牌标题 |
| `--fs-h1` | `22px / 1.3` | 区块大标题 |
| `--fs-h2` | `18px / 1.35` | 小节标题 / 卡片标题 |
| `--fs-body` | `15px / 1.6` | 正文 |
| `--fs-small` | `13px / 1.5` | 标签 / 辅助说明 |
| `--fs-tiny` | `11px / 1.4` | 导航文字 / 角标 |

## 3. 间距 (Spacing)

以 4px 为基准步进。

| 变量 | 值 | 典型用途 |
| --- | --- | --- |
| `--sp-1` | `4px` | 图标与文字间隙 |
| `--sp-2` | `8px` | 标签内、元素紧密间距 |
| `--sp-3` | `12px` | 卡片内小间距 |
| `--sp-4` | `16px` | 卡片内边距 / 页面左右边距 |
| `--sp-5` | `20px` | 区块内边距 |
| `--sp-6` | `24px` | 区块之间 |
| `--sp-8` | `32px` | 大区块分隔 |
| `--sp-10` | `40px` | 页面顶部 / 底部留白 |

## 4. 圆角 (Radius)

| 变量 | 值 | 用途 |
| --- | --- | --- |
| `--radius-sm` | `8px` | 标签 / 小控件 |
| `--radius-md` | `12px` | 按钮 / 输入框 |
| `--radius-lg` | `16px` | 卡片 |
| `--radius-xl` | `24px` | 弹层 / 大卡片 |
| `--radius-pill` | `999px` | 药丸按钮 / 标签 |

## 5. 阴影 (Shadow)

暖色阴影（取自 `--color-ink`），避免生硬的冷灰黑影。

| 变量 | 值 | 用途 |
| --- | --- | --- |
| `--shadow-card` | `0 2px 8px rgba(74,66,56,.08)` | 普通卡片 |
| `--shadow-sign` | `0 6px 16px rgba(74,66,56,.16)` | 招牌 / 木牌 |
| `--shadow-float` | `0 8px 24px rgba(74,66,56,.18)` | 悬浮按钮 / 弹层 |

## 6. 动效 (Motion)

| 变量 | 值 | 用途 |
| --- | --- | --- |
| `--dur-fast` | `160ms` | 微交互（按压、勾选） |
| `--dur` | `240ms` | 常规过渡（切换、展开） |
| `--dur-slow` | `360ms` | 入场 / 弹层 |
| `--ease-out` | `cubic-bezier(.22,.61,.36,1)` | 通用减速 |
| `--ease-bounce` | `cubic-bezier(.34,1.56,.64,1)` | 回弹（印章 / 撒花） |

## 7. 布局 (Layout)

| 变量 | 值 | 用途 |
| --- | --- | --- |
| `--nav-h` | `56px` | 底部导航高度 |
| `--safe-b` | `env(safe-area-inset-bottom, 0px)` | 全面屏底部安全区 |
| `--safe-t` | `env(safe-area-inset-top, 0px)` | 全面屏顶部安全区 |
| `--content-max` | `480px` | 内容区最大宽度（桌面居中，模拟手机） |
| `--touch-min` | `44px` | 最小可点击区域 |

## 8. 参考实现（CSS 变量）

```css
:root {
  /* 颜色 */
  --color-paper: #FAF7F0;
  --color-paper-alt: #F3EEE3;
  --color-surface: #FEFBF5;
  --color-sage: #8A9A7B;
  --color-sage-deep: #6B7F5E;
  --color-sage-soft: #DCE3D5;
  --color-wood: #C9A87C;
  --color-wood-light: #D9C4A0;
  --color-orange: #E08A4B;
  --color-orange-deep: #D96B4A;
  --color-yellow: #F2E2A8;
  --color-pink: #E8C4C4;
  --color-seal: #C15B45;
  --color-seal-gold: #D9A441;
  --color-ink: #4A4238;
  --color-ink-soft: #7A6F63;
  --color-line: #E3DACB;

  /* 语义别名 */
  --bg: var(--color-paper);
  --surface: var(--color-surface);
  --text: var(--color-ink);
  --text-muted: var(--color-ink-soft);
  --brand: var(--color-sage);
  --accent: var(--color-orange);
  --border: var(--color-line);

  /* 字体 */
  --font-title: "站酷快乐体", "LXGW WenKai", "PingFang SC", "Microsoft YaHei", sans-serif;
  --font-hand: "Ma Shan Zheng", "LXGW WenKai", cursive;
  --font-body: system-ui, -apple-system, "PingFang SC", "Microsoft YaHei", sans-serif;

  /* 间距 */
  --sp-1: 4px;  --sp-2: 8px;  --sp-3: 12px; --sp-4: 16px;
  --sp-5: 20px; --sp-6: 24px; --sp-8: 32px; --sp-10: 40px;

  /* 圆角 */
  --radius-sm: 8px; --radius-md: 12px; --radius-lg: 16px;
  --radius-xl: 24px; --radius-pill: 999px;

  /* 阴影 */
  --shadow-card: 0 2px 8px rgba(74,66,56,.08);
  --shadow-sign: 0 6px 16px rgba(74,66,56,.16);
  --shadow-float: 0 8px 24px rgba(74,66,56,.18);

  /* 动效 */
  --dur-fast: 160ms; --dur: 240ms; --dur-slow: 360ms;
  --ease-out: cubic-bezier(.22,.61,.36,1);
  --ease-bounce: cubic-bezier(.34,1.56,.64,1);

  /* 布局 */
  --nav-h: 56px;
  --safe-b: env(safe-area-inset-bottom, 0px);
  --safe-t: env(safe-area-inset-top, 0px);
  --content-max: 480px;
  --touch-min: 44px;
}
```
