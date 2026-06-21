---
name: rickc-audio-engineer-public
description: Rickc Audio Engineer Public (通用专业版) — 录音棚级AI音乐创作全流程助手。将混音参数、人声制作、效果器设置转化为结构化提示词，实现专业级音乐输出。当用户需要用 Suno AI 创作高质量音乐、需要精准控制混音/人声/母带效果、或需要生成专业级提示词时使用。
trigger:
  - "Suno 录音棚"
  - "Suno 混音"
  - "曲风创新"
  - "曲风突变"
  - "Genre Mutation"
  - "Genre Innovation"
---

# 🎛️ Rickc Audio Engineer Public (音频工程化精准提示法)

> **核心理念**：把「人声怎么唱 + 混音台怎么调 + 效果器加多少」全部写成结构化、参数化、专业音频术语的指令，让 AI 不凭感觉瞎猜，直接复刻出录音棚级成品。

---

## 📦 资源模块索引

本 Skill 由主文件 + 5 个资源模块组成，可按需调用：

| 模块 | 文件 | 说明 |
| ---- | ---- | ---- |
| 🎵 常用曲风库 | `resources/genre-library.md` | 20+ 曲风的 DAW 参数块预设，按流派分类 |
| 🎤 人声设计库 | `resources/vocal-design-library.md` | 20+ 个人声预设（女声 / 男声 / 对唱 / 合唱） |
| 📝 歌词优化指南 | `resources/lyrics-optimization.md` | 中/英/日/韩四语押韵、发音、现代语感优化 |
| 📈 音乐趋势库 | `resources/music-trends.md` | 全球及各市场流行趋势宏观分析 |
| 📂 创作历史记录 | `resources/song-history.md` | 创作记录模板、标签体系、统计看板 |

> 💡 **调用方式**：在创作过程中，根据需要读取对应资源文件。例如选曲风时读取 `genre-library.md`，设计人声时读取 `vocal-design-library.md`，写歌词时读取 `lyrics-optimization.md`。

---

## 📋 使用流程

### Step 1: 收集创作需求

向用户交互式收集以下信息（未提供的项目使用智能默认值）：

```text
┌──────────────────────────────────────────────┐
│          🎵 Rickc 音频工程创作需求表            │
├──────────────────────────────────────────────┤
│ 1. 歌曲主题/故事：_______________             │
│ 2. 目标流派：_______________                  │
│ 3. 情绪基调：_______________                  │
│ 4. 人声要求：_______________                  │
│ 5. 参考曲目/艺术家风格（可选）：_______________│
│ 6. 歌词语言：中文 / 英文 / 日文 / 韩文 / 混合  │
│ 7. 用途场景：_______________                  │
│ 8. 输出模式偏好：句式描述 / DAW参数块 / 双模式  │
│ 9. 特殊要求：_______________                  │
└──────────────────────────────────────────────┘
```

### Step 2: 调用资源模块

根据需求调用对应模块：

1. **选曲风** → 读取 `resources/genre-library.md`，选择匹配的 `[GENRE]` 预设
2. **选人声** → 读取 `resources/vocal-design-library.md`，选择匹配的 `[VOCAL]` 预设
3. **写歌词** → 读取 `resources/lyrics-optimization.md`，按语言优化押韵和语感
4. **了解趋势** → 读取 `resources/music-trends.md`，确认风格是否符合当前流行
5. **保存记录** → 创作完成后更新 `resources/song-history.md`

### Step 3: 选择提示模式并构建 Style Prompt

本 Skill 提供 **两种提示模式**，适用于不同场景：

| 模式 | 适用场景 | 精度 | 复杂度 |
| ---- | -------- | ---- | ------ |
| **Mode A — 句式描述模式** | 快速创作、通用场景 | ★★★☆☆ | 低 |
| **Mode B — DAW 参数块模式** | 专业制作、精准控音、录音棚级输出 | ★★★★★ | 高 |

> 💡 **推荐策略**：默认使用 **Mode B**（DAW 参数块模式）以获得最大精度。如用户偏好简洁或快速出活，切换 Mode A。两种模式也可融合使用。

---

## 🅰️ Mode A — 句式描述模式（七层结构化模板）

每一层用句号结尾。用 `and` / `with` 代替逗号（Suno 处理逗号时可能跳过后续内容）。

```text
Genre: [流派描述，含时代和子流派融合，用 and/with 连接].
Style: [曲风特质，旋律走向，编曲风格].
Mood: [情绪基调，情绪变化弧线].
Singer's Voice: [人声类型 + 音色质感 + 演唱技法 + 情感表达].
Instrumentation: [核心乐器（限2-3件）+ 辅助乐器 + 演奏方式].
Production: [空间效果 + 动态处理 + 频率特征 + 音场宽度].
Mastering: [母带方向 + 响度特征 + 整体质感].
```

### Mode A 示例

```text
Genre: Dark cinematic synthwave with 80s retro-futurism and modern electronic production.
Style: Catchy and atmospheric melodies with slow-building tension and dramatic crescendos.
Mood: Melancholic and introspective with a rising sense of hopeful resolve.
Singer's Voice: Intimate female alto with breathy delivery and subtle vibrato and restrained emotional intensity in verses building to powerful chest voice in chorus.
Instrumentation: Pulsing analog bass synth with warm saturation and layered atmospheric pads and tight punchy electronic drums with crisp hi-hats.
Production: Short plate reverb on vocals with long ambient tail on pads and tight parallel compression on drums and wide stereo imaging with clear center vocal placement.
Mastering: Polished modern master with controlled loudness and warm analog character and wide stereo field.
```

---

## 🅱️ Mode B — DAW 参数块模式（录音棚级精准控制）

> 🎯 **本模式核心**：将混音台上每个效果器/处理器的实际参数转化为 Suno 可理解的精准描述。
>
> [!CAUTION]
> **Suno Style Prompt 有 950 字符硬限制（官方标称1000但易超限）！** 完整参数块仅作为创作参考和思维工具，最终粘贴到 Suno 的 Style Prompt 必须压缩到 950 字符以内。
>
> **质量要求**：Style Prompt 必须参考下方 §Mode B 示例中的 **Layer 2 格式**，写成流畅的描述性段落。禁止输出短促的标签拼接式文本。字符数直接影响生成质量，目标 600-850 字符。

### ⚡ 两层输出策略

| 层级 | 用途 | 字符数 |
| ---- | ---- | ------ |
| **Layer 1 — 完整参数块** | 创作参考 / 思维工具 / DAW后期参考 | 不限 |
| **Layer 2 — 压缩粘贴版** | 直接粘贴到 Suno Style Prompt 框 | **≤ 950 字符** |

### 🗜️ 压缩规则（Layer 1 → Layer 2）

1. **删掉 `[SECTION]` 标题头**：Suno 不需要 `[GENRE]` `[VOCAL]` 等标记
2. **合并为流畅句子**：用 `and` / `with` 连接，不换行
3. **删除括号解释**：`(-3dB reduce muddiness)` → 直接删掉
4. **优先级排序**：VOCAL > GENRE > INSTRUMENTATION > Production（混合EQ/压缩/混响/母带为1-2句）
5. **VOCAL 占 40% 字符预算**（最影响成品的参数，但要精简重复形容词）
6. **Production 合并为 1-2 句**：只保留效果器类型名，删掉具体数值（Suno 不精确响应数值参数）
7. **每句用句号结尾**，用 `and` 代替逗号
8. **目标 600-850 字符**（硬限 950。使用丰富的描述性语言填充预算，避免短促标签式拼接。对比：500 字符的 Prompt 比 800 字符的生成质量明显更差）
9. **输出前必须验证字符数**：实际计数，不要估算

### 完整参数块模板（Layer 1 — 创作参考用）

按需选用，**不需要每个 Section 都写**，根据歌曲需求选择关键参数块即可。

```text
[GENRE]
primary: [主流派]
fusion: [融合元素]
era: [时代/年代参考]
tempo: [BPM 或 节奏描述]
key: [调性，如 Cm / F major / Am]

[VOCAL]
type: [male/female] vocal
style: [风格参考描述，不用艺术家名字，用特质描述]
language: [演唱语言]
tone: [音色关键词，逗号分隔]
register: [音域偏好: soprano/alto/tenor/baritone]
technique: [演唱技法: breathy/belting/falsetto/vibrato 等]
delivery: [演唱态度: intimate/detached/passionate/aggressive]
special: [特殊要求，如咬字、颤音、气声等细节]
high notes: [高音处理方式]
ad-libs: [即兴装饰: 有/无/风格]

[INSTRUMENTATION]
core: [核心乐器1] and [核心乐器2]
support: [辅助乐器]
texture: [底层纹理/氛围铺垫]
avoid: [需要避免的乐器]

[MIXING]
quality: [混音品质描述: studio master / lo-fi / live room 等]
spatial: [空间感: stereo / 3D immersive / mono-focused]
export: [输出规格: 48kHz 24-bit / 44.1kHz 16-bit 等]

[EQ]
highpass: [高通滤波频率，如 80Hz]
cut: [需要衰减的频段和原因，如 200-400Hz reduce muddiness]
boost: [需要提升的频段和 dB 值，如 2.5k-6k +2~3dB presence]
character: [整体 EQ 特征: bright / warm / neutral / dark]

[COMPRESSION]
type: [压缩器类型: analog / opto / VCA / FET / digital]
ratio: [压缩比: 2:1 / 3:1 / 4:1 等]
attack: [起音速度: slow / medium / medium-fast / fast]
release: [释放速度: slow / medium / fast / auto]
goal: [压缩目标: transparent / punchy / glued / squashed]
parallel: [并行压缩: 有/无/比例]

[SATURATION]
type: [饱和类型: tape / tube / analog / transistor]
amount: [饱和度: subtle / moderate / heavy]
character: [特征描述: warmth / grit / crunch]
caution: [注意事项，如 avoid distorting specific elements]

[REVERB]
type: [混响类型: plate / hall / room / chamber / spring]
predelay: [预延迟: 10-60ms 范围]
decay: [衰减时间: 0.5-5s 范围]
mix: [干湿比: 10-50% 范围]
layer: [叠加层: 如 +long ambient reverb 10-20% mix]
vocal: [人声专属混响设置]
instruments: [乐器混响设置]

[DELAY]
type: [延迟类型: stereo slap / pingpong / tape echo / analog]
time: [延迟时间: ms 值或节奏同步 1/8 / dotted 1/4]
feedback: [反馈量: 5-50% 范围]
filter: [延迟滤波: dark / bright / filtered]
mix: [延迟干湿比]

[DOUBLING]
style: [加倍方式: chorus / double-tracking / ADT / haas]
width: [宽度效果: subtle / moderate / wide]
application: [应用位置: vocal / guitars / synths]

[DE-ESSER]
active: [是否启用: yes/no]
frequency: [作用频段: 4-8kHz 范围]
intensity: [强度: light / moderate / heavy]

[MASTERING]
loudness: [目标响度: -14 LUFS streaming / -9 LUFS loud]
stereo: [立体声宽度: narrow / standard / wide / immersive]
limiter: [限制器设置: transparent ceiling / brick-wall]
character: [母带特征: warm analog / clean digital / punchy modern]
headroom: [预留空间: -1dB / -0.3dB / 0dB true peak]
```

---

### Mode B 示例 — 梦幻流行女声

#### Layer 1：完整参数块（创作参考 / DAW 后期用）

```text
[GENRE]
primary: dream pop
fusion: trip-hop undertones and ambient electronic textures
era: modern with 90s dreampop nostalgia
tempo: 78 BPM slow ethereal groove
key: Em

[VOCAL]
type: female vocal
style: ethereal and airy with detached floating presence
language: English
tone: delicate and breathy and magnetic
register: alto to soprano with effortless transitions
technique: breathy head voice with controlled vibrato and occasional falsetto
delivery: detached and mysterious with emotional distance and cool elegance
special: emphasize crystal-clear diction
high notes: crystal-clear sustain with no strain
ad-libs: minimal ethereal (Ooooh) (Mmmm)

[INSTRUMENTATION]
core: atmospheric synth pads with warm analog texture and acoustic fingerstyle guitar with reverb shimmer
support: subtle electronic percussion with brushed textures
texture: ambient granular pad layers with tape hiss
avoid: heavy distorted guitars and aggressive drums

[EQ] highpass: 80Hz / cut: 200-400Hz -3dB / boost: 2.5k-6k +2dB / boost: 10k+ +2dB / character: bright airy
[COMPRESSION] opto LA-2A 2:1 medium-fast attack / transparent / parallel 20%
[REVERB] plate 2.5s 30% + ambient tail 15% / predelay 30ms
[DELAY] pingpong dotted 1/4 / feedback 20% / dark filter / mix 18%
[MASTERING] -14 LUFS / wide stereo / warm analog / -1dB true peak
```

#### Layer 2：压缩粘贴版（直接粘贴到 Suno ≤ 950 字符）

```text
Dream pop with trip-hop undertones and ambient electronic textures. 78 BPM ethereal groove in Em.

Ethereal female vocal with delicate breathy magnetic tone. Alto to soprano with effortless transitions. Breathy head voice with controlled vibrato and occasional falsetto. Detached and mysterious with cool elegance. Crystal-clear diction. Ad-libs (Ooooh) (Mmmm). English.

Atmospheric synth pads with warm analog texture and fingerstyle guitar with reverb shimmer. Subtle electronic percussion. Ambient granular pad layers. No distorted guitars.

Bright airy EQ. Opto compression transparent. Plate reverb with ambient tail. Pingpong delay. Wide stereo. Warm analog mastering.
```

> 💡 **上面的 Layer 2 约 550 字符**。建议在此基础上进一步丰富 Genre 融合描述和 Vocal 细节，目标达到 700-850 字符以获得最佳效果。注意 VOCAL 段落应占全部字符的 40% 左右，这是正确的优先级。

---

## 📊 DAW 参数速查 — 常用预设

### 🎤 人声预设

> 完整预设库见 `resources/vocal-design-library.md`

| 预设名称 | EQ | Compression | Reverb | Delay | 特征 |
| -------- | -- | ----------- | ------ | ----- | ---- |
| **温暖亲密** | cut 3-5k -2dB / boost 200Hz +1dB | opto 2:1 slow attack | room 0.8s 20% | slap 30ms 10% | 近距离收音感 |
| **空灵飘渺** | boost 10k+ +3dB / cut 300Hz -3dB | opto 2:1 medium | plate+hall 2.5s 35% | pingpong 1/4 20% | 梦幻悬浮感 |
| **力量型** | boost 2-4k +3dB / boost 100Hz +2dB | FET 4:1 fast attack | hall 1.5s 15% | slap 40ms 8% | 冲击力与厚度 |
| **烟嗓慵懒** | cut 5k -1dB / boost 800Hz +1dB | opto 3:1 medium | chamber 1.2s 25% | tape 200ms 15% | 暖厚磁性 |
| **电子处理** | boost 6k+ +4dB / cut 200Hz -4dB | VCA 6:1 fast | shimmer 3s 40% | pingpong 1/8 30% | 未来感处理声 |
| **RAP/说唱** | boost 3-5k +4dB / highpass 120Hz | FET 4:1 fast fast | room 0.5s 10% | slap 20ms 5% | 硬朗前置 |

### 🎹 风格混音预设

> 完整曲风库见 `resources/genre-library.md`

| 风格 | EQ 特征 | Compression | Reverb | 整体特征 |
| ---- | ------- | ----------- | ------ | -------- |
| **Lo-fi / Chill** | rolloff 12k / boost 400Hz | heavy 6:1 slow | room 1s 30% + vinyl | 温暖复古颗粒感 |
| **EDM / Dance** | boost 8k+ +3dB / sub 40Hz | sidechain 8:1 | short 0.3s 10% | 能量冲击感 |
| **R&B / Soul** | warm mids 500Hz +2dB / silk 10k | opto 3:1 smooth | plate 2s 25% | 丝滑温柔 |
| **摇滚** | boost 3k +3dB / tight low 80Hz | parallel 4:1 punchy | room 1.2s 20% | 粗犷有力 |
| **古典/管弦** | flat neutral / air 12k +1dB | minimal 1.5:1 | concert hall 3.5s 30% | 自然宽广 |
| **流行** | boost 2-4k +2dB / clean 200Hz | opto 2.5:1 transparent | plate 1.5s 20% | 清晰甜美 |
| **Ambient** | rolloff 2k / boost sub 60Hz +3dB | none or 1.5:1 | infinite 6s+ 60% | 沉浸氛围 |
| **Jazz** | warm 300Hz +1dB / gentle air 8k | opto 2:1 very slow | chamber 1.8s 20% | 温暖现场感 |

---

## 🎤 人声制作参数词库

> 完整开箱即用预设见 `resources/vocal-design-library.md`

### 人声类型

| 类别 | 可用参数 |
| ---- | -------- |
| **性别** | `Male Vocal` / `Female Vocal` / `Androgynous Voice` |
| **音域** | `Soprano` / `Alto` / `Tenor` / `Baritone` / `Bass` |
| **角色** | `Lead Vocal` / `Backing Vocals` / `Choir` / `Diva Solo` / `Duet` |
| **年龄感** | `Youthful Voice` / `Mature Voice` / `Weathered Voice` / `Children's Vocals` |

### 音色质感

| 风格 | 参数术语 |
| ---- | -------- |
| **温暖** | `warm and velvety tone` / `rich and full-bodied` |
| **空灵** | `ethereal and angelic` / `delicate and airy` |
| **沙哑** | `deep and husky` / `smoky and gritty` / `raspy` |
| **力量** | `powerhouse vocal` / `soaring and dynamic` / `belting` |
| **亲密** | `whispery and intimate` / `breathy and close-mic` / `ASMR-like` |
| **磁性** | `magnetic and captivating` / `velvety and seductive` |
| **清冷** | `cool and detached` / `crystal-clear and thin` |
| **电子** | `processed with subtle auto-tune` / `vocoder effect` / `metallic and robotic` |

### 演唱技法

| 技法 | 提示词 |
| ---- | ------ |
| **咬字** | `clear consonants and no mumbles` / `precise diction` / `strong rolled R` |
| **气息** | `breathy delivery` / `controlled breath support` / `airy and floating` |
| **颤音** | `subtle vibrato` / `wide vibrato` / `no vibrato straight tone` |
| **转音** | `smooth melismatic runs` / `gospel-style vocal riffs` |
| **力度变化** | `verse intimate and chorus defiant` / `pianissimo to fortissimo arc` |
| **特殊** | `falsetto` / `head voice` / `chest voice` / `vocal fry` / `throat singing` |
| **极端** | `death growl` / `guttural` / `screaming` / `pig squeals` |

### 情感表达

| 情感 | 参数术语 |
| ---- | -------- |
| **悲伤** | `melancholic and yearning` / `tearful and vulnerable` |
| **欢乐** | `bright and joyful` / `celebratory and exuberant` |
| **愤怒** | `aggressive and intense` / `raw and confrontational` |
| **冷静** | `cool and detached` / `stoic and restrained` |
| **深情** | `passionate and sensual` / `tender and loving` |
| **神秘** | `mysterious and distant` / `enigmatic and ethereal` |

---

## 🎹 乐器精确描述词库

### 核心原则

> ⚠️ **每首歌限 2-3 件核心乐器**，辅助乐器 1-2 件。过多乐器会导致混音混杂。

### 键盘/钢琴

| 乐器 | 精确描述 |
| ---- | -------- |
| **原声钢琴** | `grand piano with natural resonance` / `upright piano with intimate character` |
| **电钢琴** | `Rhodes piano with warm tremolo` / `Wurlitzer piano with gritty edge` |
| **合成器** | `analog Moog bass synth` / `Juno-60 pad` / `Prophet-5 lead` / `FM digital bell synth` |
| **风琴** | `Hammond B3 organ with Leslie speaker` / `church pipe organ` |

### 吉他

| 乐器 | 精确描述 |
| ---- | -------- |
| **木吉他** | `acoustic fingerstyle guitar` / `nylon string classical guitar` / `steel-string strumming` |
| **电吉他** | `clean Telecaster arpeggios` / `overdriven Les Paul power chords` / `Jazzmaster with chorus` |
| **特殊** | `slide guitar with bluesy tone` / `12-string acoustic shimmer` |

### 低音

| 乐器 | 精确描述 |
| ---- | -------- |
| **贝斯** | `fingerstyle bass with round tone` / `slap bass` / `fretless bass with mwah` |
| **合成低音** | `analog sub bass` / `wobble dubstep bass` / `808 bass` |

### 鼓/打击

| 乐器 | 精确描述 |
| ---- | -------- |
| **原声鼓** | `acoustic drums with realistic feel` / `brushed jazz drums` / `powerful rock kit` |
| **电子鼓** | `crisp TR-808 drums` / `punchy TR-909 kicks` / `glitchy IDM percussion` |
| **打击** | `congas and bongos` / `tabla` / `cajón` / `orchestral timpani` |

### 弦乐/管乐

| 乐器 | 精确描述 |
| ---- | -------- |
| **弦乐** | `lush string section` / `solo cello with emotional vibrato` / `pizzicato strings` |
| **管乐** | `warm flugelhorn solo` / `bright trumpet section` / `saxophone with breathy tone` |
| **木管** | `haunting flute melody` / `clarinet with rich lower register` |

### 民族/特色

| 乐器 | 精确描述 |
| ---- | -------- |
| **东亚** | `guzheng (古筝)` / `erhu (二胡) with emotional vibrato` / `pipa (琵琶)` / `dizi (笛子)` |
| **其他** | `sitar with shimmering resonance` / `kalimba` / `steel drum` / `didgeridoo` |

---

## 📐 歌曲结构 Metatags

### 基础结构标签

需注意：**起播完播率至关重要，前奏必须极短抓耳 (如 <10s)**。为了保证生成长度大于 3 分钟，应把时间堆在中间和结尾（避免过早使用 `[Outro]` 或 `[End]`，而是增加第二/三段主歌以及专门的加长乐器独奏）。

```text
[Intro // Catchy 5s hook / immediate vocal]  [Verse 1]  [Pre-Chorus]  [Chorus]  
[Extended Instrumental Break / Guitar Solo]  [Verse 2]  [Pre-Chorus]  [Chorus]  
[Bridge]  [Drop / Breakdown]  [Final Chorus]  [Outro // Long 30s fade out]  [End]
```

### 高级结构控制（内嵌技术指令）

> 🚨 **AI Agent 宿主模型执行避坑指南 (Anti-Laziness Warning)**
> **极易踩坑点**：LLM 在批量生成多首歌曲的歌词时，极易出于“偷懒”或“简化输出”的本能，只输出基础标签（如只写 `[Chorus]`）而丢弃至关重要的 `//` 内嵌指令。
> **强制要求**：Agent 在任何生成排版歌词的任务中，**必须强制**在每一个结构标签内添加 `// 音乐指令`（例如 `[Chorus // heavy sub bass, wide stereo pads]`）。如果不加，Suno 会完全靠瞎猜配器，导致最终成品丧失工业级控制力。**绝对不允许输出光秃秃的 `[Chorus]` 等基础标签。**
```text
[Intro // Ambient pad build with rising synth]
[Verse 1] [// sparse arrangement with piano and subtle drums]
[Pre-Chorus] [// build intensity with layered strings]
[Chorus] [// full arrangement explosion with choir harmonies]
[Bridge] [// stripped back to solo vocal and piano]
[Outro // fade out with reverb tail]
```

### 能量控制标签

```text
[Energy: Low]  |  [Energy: Medium → High]  |  [Energy: Explosive]  |  [Energy: Drop to silence]
```

### 歌词内嵌控制

| 技巧 | 语法 | 示例 |
| ---- | ---- | ---- |
| **大写强调** | `WORD` | `I WILL NOT FALL` — 加大音量/强度 |
| **延长元音** | `Ooooh` / `Yeaaah` | 创作抓耳旋律 |
| **括号背景声** | `(text)` | `Main lyrics (Ethereal backing vocals)` |
| **括号音效** | `(effect)` | `(record scratching)` / `(thunder)` |
| **星号音效** | `*effect*` | `*glass breaking*` / `*crowd cheering*` |
| **技术指令** | `//` | `// tempo change` — 不会被唱出 |
| **人声标注** | `[Tag]` | `[whispering]` / `[screaming]` / `[spoken word]` |

---

## ⚙️ 高级参数设置

### Suno 平台设置建议

| 参数 | 推荐值 | 说明 |
| ---- | ------ | ---- |
| **Mode** | Custom Mode | 分离歌词和风格，精准控制 |
| **Model Version** | V5.5 (最新版) | 官方: help.suno.com · 2026年3月发布，最低 V4.5 |
| **Vocal Gender** | Male / Female | 必须手动选中指定性别 |
| **Lyrics Mode** | Manual | 手动控制歌词结构，防止AI乱编 |
| **Weirdness** | 50 (官方默认) | 官方: 0-100, 50=normal。社区稳定推荐 20-40（较低值=更一致，较高值=更多随机性）|
| **Style Influence** | 80 | 官方: 0-100, Loose→Strong。社区锁定风格推荐 70-90 |
| **Exclude Styles** | 必须填写 | 加入负面提示词以精准避坑 |
| **Instrumental** | 按需选择 | 纯音乐时勾选 |

### 精准速度/情绪控制对照表

| 控制维度 | 让 Suno 变慢/忧郁 | 让 Suno 变快/欢乐 |
| -------- | ----------------- | ----------------- |
| **速度关键词** | `slow` `deliberate` `spacious` `laid-back` | `groovy` `driving` `energetic` `catchy` |
| **情绪关键词** | `melancholic` `restrained` `bittersweet` | `bright` `cheerful` `upbeat` `fun` |
| **BPM 策略** | 写比目标**低 5-7**（想要 82 就写 75） | 写实际值即可 |
| **歌词密度** | 每行 **3-8 音节** + `...` 停顿 | 每行 10-15 音节 |
| **鼓组描述** | `minimal soft` `brushed` `half-time` | `tight punchy` `crisp hi-hats` |
| **Exclude** | `upbeat / happy / fast / dance / energetic` | `slow / ballad / ambient / sad` |

### 语言策略

> 💡 **风格描述和参数块用英文，歌词用目标语言**（Suno 对英文音频术语理解更准确）
>
> 歌词押韵和语感优化详见 `resources/lyrics-optimization.md`

### 无母带输出（用于后期 DAW 处理）

```text
UNMASTERED pre-master rough mix: zero compression (track/bus/master) and zero limiting/maximizer and zero clipping and zero saturation/exciter and zero stereo widening — do not make it loud or mastered; keep wide dynamics and leave lots of headroom (peaks ≤ -10 to -8 dB). ZERO muddiness: no low-mid buildup (especially 150–600 Hz) and no boxiness and no boom and no rumble; keep the low end tight and clean with clear separation and a dry/flat mix that's easy to EQ and master later in my DAW.
```

### 🎛️ 外部 AI 母带处理基准参数（针对流媒体 Loudness 的标准流程）

- **Target Loudness Mode**: Streaming Standard (e.g. YouTube Loudness)
- **Target Loudness (dB)**: -9
- **Ceiling Mode**: True Peak (15kHz Lowpass)
- **Ceiling (dBFS)**: -0.5
- **Oversampling**: 2x (Slow)
- **Automatic Mastering**: Enabled (Level 0.5)
- **Output Format**: WAV(16bit)
- **Sampling Rate**: 44.1kHz
- **Low Cut Freq**: 20 Hz
- **High Cut Freq**: 20000 Hz
- **Advanced Options**: Preserve Bass (Checked), Mastering Algorithm (V2 Latest)

---

## 🔄 制作工作流

### Phase 1: 基础生成

1. 选择模式（Mode A 句式描述 / Mode B DAW 参数块）
2. 从资源模块调取曲风预设 + 人声预设
3. 构建 Style Prompt + 编写歌词（参考歌词优化指南）
4. 设置参数（Custom Mode + V5.5 + Weirdness 50 官方默认）
5. 生成 2-4 个版本，选择最佳 Foundation

### Phase 2: 迭代优化

1. 使用 **Extend** 从最佳版本继续创作
2. 使用 **Replace Section** 精准修复弱段落
3. 使用 **Remix** 探索同歌词不同风格
4. **每次只改一个变量**（乐器 / 情绪 / 人声 / 效果器参数）

### Phase 3: 风格锁定

1. 找到满意风格 → 保存为 **Persona**
2. 使用 **Cover** 功能探索风格变体
3. 记录成功的参数块组合

### Phase 4: 后期加工（可选）

1. 导出音频到 DAW（FL Studio / Ableton / Logic）
2. 分离 Stems（鼓/贝斯/人声/乐器）
3. 精细混音 + 母带处理

### Phase 5: 记录归档

1. 更新 `resources/song-history.md`，保存 Style Prompt / 歌词 / 参数 / 笔记
2. 标注可复用的配置组合

---

## 📦 完整提示词生成输出格式

为用户完成分析后，按以下格式输出最终方案：

```text
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🎵 SUNO 音频工程化精准提示词方案
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

📌 歌曲概述
──────────────────────────────────────────
[主题] | [流派] | [情绪] | [人声类型]
[目标效果简述，一句话]

📝 Style Prompt — Layer 2 压缩版（直接粘贴到 Suno，≤ 950 字符）
──────────────────────────────────────────
[参考下方 §Mode B 示例的 Layer 2 格式：流畅段落式描述]
[4 段式结构：Genre(含BPM/Key) → Vocal(40%预算，多句) → Instrumentation → Production(短促句)]
[目标 600-850 字符]
（约 XXX 字符）

📝 Style Prompt — Layer 1 完整参考版（创作参考 / DAW 后期）
──────────────────────────────────────────
[完整 DAW 参数块，不受字数限制]

🎶 Lyrics（粘贴到 Suno "Lyrics" 框）
──────────────────────────────────────────
[含 Metatags 和内嵌控制的完整歌词]

⚙️ Suno 参数设置
──────────────────────────────────────────
Mode: Custom
Model: V5.5
Weirdness: 50
Style Influence: 80
Exclude Styles: [按 Mood 填写负面提示词]
Instrumental: [是/否]

🎛️ AI母带基准参数（针对流媒体平台定制）
──────────────────────────────────────────
Target Loudness: -9 dB (Streaming Standard)
True Peak: -0.5 dBFS (15kHz Lowpass)
Oversampling: 2x (Slow)
Automatic Mastering: Level 0.5
Output: WAV (16-bit) / 44.1kHz
Low Cut: 20 Hz / High Cut: 20000 Hz
Preserve Bass: Yes / Mastering Alg: V2 (Latest)

💡 迭代优化建议
──────────────────────────────────────────
1. [第一优先级优化方向]
2. [第二优先级优化方向]
3. [备选风格探索建议]

📂 归档信息
──────────────────────────────────────────
标签: #genre #mood #language #usage
建议保存至: resources/song-history.md

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## 🧠 常见问题快速参考

| 问题 | 解决方案 |
| ---- | -------- |
| 音质浑浊 | `[EQ] cut: 200-400Hz -3dB` + `[MIXING] clean separation` |
| 人声不清晰 | `[VOCAL] special: clear consonants` + `[EQ] boost: 2-5k +2dB` |
| 风格不一致 | 使用 Persona 功能锁定 + 每次只改一个参数块变量 |
| 逗号后被忽略 | 全部改用 `and` / `with` 连接 |
| 技术指令被唱出 | 在指令前加 `//` 符号 |
| 母带过度压缩 | 使用「无母带输出」提示词 或 `[MASTERING] headroom: -6dB` |
| 混响太糊 | 降低 `[REVERB] mix: 15%` + 增加 `predelay: 40ms` |
| 人声被淹没 | `[COMPRESSION] parallel: 30%` + `[EQ] boost: 3k +2dB` |
| 能量太平 | `[Energy: Low → High]` + 分段描述不同动态处理 |
| 齿音/R失真 | `[DE-ESSER] frequency: 5-7kHz intensity: light` |
| 歌词押韵不好 | 参考 `resources/lyrics-optimization.md` 对应语言的押韵指南 |
| 不确定用什么曲风 | 查看 `resources/genre-library.md` 速查索引 |
| 生成太快/太欢乐 | 加 `slow deliberate melancholic restrained` + Exclude `upbeat happy energetic` |
| 生成太慢/太忧郁 | 加 `groovy driving energetic catchy` + 提高 BPM 值 |
