# 📂 创作历史记录 (Song History)

> 记录每次创作的 Style Prompt、歌词、参数配置和结果笔记，方便复用和迭代。

---

## 📋 使用说明

1. 每次完成一首歌的最终版本后，复制下方模板新增一条记录
2. `[成功]` / `[待优化]` / `[放弃]` 三种状态标注
3. 给每条记录打上 `#标签` 便于检索

---

## 🗂️ 创作与协同调优记录模板

```markdown
### [歌曲编号] 歌名 (Version/Iteration) — [状态: 成功/待优化/放弃]

| 维度 | 属性与参数 |
|:---|:---|
| **创作日期** | YYYY-MM-DD |
| **针对模型** | Suno v5.5 (必须标明具体模型版本，便于未来升级隔离) |
| **曲风/乐理** | [J-Pop, Alt-R&B, etc.] |
| **调性/BPM** | [调性] / [BPM] BPM |
| **歌手声线** | [Male/Female] — [例如：F-11 幻梦女声] |
| **用途** | [YouTube / Bilibili / 专辑名 / 单曲] |
| **状态** | [成功] / [待优化] / [放弃] |

#### 1. 人机反馈与参数转化记录 (HITL Translation Log)
*   **创作者的听感反馈**：“[粘贴用户的口头反馈，如：副歌太尖锐、配器太重、唱得太快]”
*   **AI 翻译与调整**：[根据《人机协同留痕SOP》对照表，说明把什么口头要求转化为了什么 Style/Exclude 词汇]

#### 2. 本次所用 Style Prompt（DAW 混音版）
`[粘贴最终 Style Prompt]`

#### 3. 本次所用 Exclude Styles
`[粘贴负面提示词]`

#### 4. 生成结果归因与归档 (Result Attribution)
*   **生成效果评价**：[记录本次生成的优缺点，是否解决上次的问题，有没有爆音/幻觉]
*   **下步建议**：[如：可定稿 / 需在此基础上继续调整BPM]
```

---

## 📝 创作记录

### S001 「蒼い炎 / Blue Flame」— [成功]

| 项目 | 内容 |
|------|------|
| **创作日期** | 2026-03-07 |
| **参考曲目** | Snow Man「One」(2024 Blue Lock ED) |
| **曲风** | J-Pop Slow Ballad × Anime ED Style |
| **调性/BPM** | C Major / 75 BPM |
| **人声** | Female — F-11 幻梦女声 |
| **语言** | Japanese + English hooks |
| **用途** | YouTube / 测试 |
| **状态** | [成功] — 速度控制优化中 |

**Style Prompt（Layer 2 — V3 修正版）**
```
Slow melancholic J-Pop mid-tempo ballad with quiet determination and bittersweet longing. 75 BPM slow deliberate pace with spacious half-time drum feel and restrained orchestral strings. C major.

Ethereal female vocal with crystalline breathy tone and translucent veil-like quality. Soprano with delicate head voice and controlled soft vibrato. Restrained and melancholic in verses with slowly building emotional intensity in chorus. Cool detached delivery with underlying sadness. Clear Japanese diction with natural Japanese-English code-switching. Layered whispered self-harmony in chorus. Ad-libs soft (Ooooh) and quiet (Yeah). Japanese with English.

Grand piano with slow emotive arpeggios and gentle orchestral strings with gradual swells. Minimal electronic percussion with soft kick and brushed texture. Warm ambient synth pads. No upbeat drums. No fast hi-hats.

Warm melancholic EQ. Gentle opto compression. Long plate reverb with ambient decay on vocals. Wide spacious stereo. Soft analog mastering.
```

**Exclude Styles**
```
upbeat and happy and cheerful and bright and fast tempo and energetic and dance and EDM and party and funk and disco and heavy metal and distorted and aggressive and male vocal
```

**歌曲结构**
```
[Intro // 8 bars slow piano] → [Verse 1] → [Pre-Chorus] → [Chorus] → [Verse 2] → [Pre-Chorus] → [Chorus] → [Bridge // whispered] → [Final Chorus] → [Outro // piano fade]
```

**配置笔记**
- ✅ `slow deliberate melancholic bittersweet spacious` — 有效控制情绪
- ✅ `No upbeat drums. No fast hi-hats.` — 明确排除快鼓
- ✅ 歌词每行 3-8 音节 + `...` 停顿控制速度
- ❌ `groovy / catchy / driving / energy` — 会推快变欢乐，避免使用
- ❌ 歌词每行超过 12 音节 — 会导致 Suno 加速
- 💡 如仍过快，BPM 进一步降到 68-70 + 加 `extremely slow and spacious`
- 💡 和声如不够厚，在 Chorus 歌词加 `(三声部和声 Ooh-Aah)` 标注

**主题** 再次见到你 / 坚定的梦想 / 蓝色火焰意志

**标签** #JPop #Ballad #Female #Japanese #AnimeED #SlowBurn #EtherealStyle

---

### S002 「Credit Roll (深夜アニメ OST)」 — [状态: 成功]

| 维度 | 属性与参数 |
|:---|:---|
| **创作日期** | 2026-05-20 |
| **针对模型** | Suno v5.5 |
| **曲风/乐理** | Cinematic Felt Piano Instrumental |
| **调性/BPM** | C Major / 70 BPM |
| **歌手声线** | 无 (Instrumental) |
| **用途** | 专辑《深夜アニメ (Midnight Anime)》收尾轨 (Track 10) |
| **状态** | [成功] |

#### 1. 人机反馈与参数转化记录 (HITL Translation Log)
*   **创作者的听感反馈**：“最后一轨希望是彻底的平静和留白，像黑屏职员表滚动一样，不要有任何歌手哼唱或电子合成器打扰，钢琴的音色要很温暖、有老唱片的感觉。”
*   **AI 翻译与调整**：
    - 针对“彻底的平静，无哼唱”：在歌词框填充结构标签序列，并在 Style Prompt 中标明 `no vocals, pure acoustic instrumental`，且 Exclude 框填入 `vocals, singing, voice` 进行双保险；
    - 针对“老唱片感觉，钢琴温暖”：在 Style Prompt 加入 `Warm analog felt grand piano with mechanical hammer noise. Subtle vinyl crackle and tape hiss.` 并辅以 `Warm lo-fi EQ` 调色；
    - 针对“留白，不要电子乐”：Exclude 排除 `heavy synths, electronic, drums, percussion`，BPM 锚定为缓慢的 `70 BPM`。

#### 2. 本次所用 Style Prompt（DAW 混音版）
`Cinematic solo piano instrumental. 70 BPM slow deliberate pace. Warm analog felt grand piano with mechanical hammer noise. Subtle vinyl crackle and tape hiss. Gentle underlying string swells in the background. Long atmospheric plate reverb. Warm lo-fi EQ. Soft analog mastering. No vocals, pure acoustic instrumental.`

#### 3. 本次所用 Exclude Styles
`vocals, singing, voice, drums, percussion, heavy synths, upbeat, electronic, rock, epic, fast`

#### 4. 生成结果归因与归档 (Result Attribution)
*   **生成效果评价**：Suno 完美压制了人声幻觉，钢琴具有极佳的毛毡阻尼感 and 机械杂音，背景弦乐进入的节点符合 [Energy: Medium] 的结构标记。
*   **下步建议**：已定稿，通过 `one-click-archive` 分发至本地 G 盘归档并同步飞书。

---

## 📊 统计看板

| 统计项 | 数值 |
|--------|------|
| **总创作数** | 2 |
| **成功率** | 100% |
| **最常用曲风** | J-Pop Ballad / Cinematic Felt Piano |
| **最常用人声** | Female |
| **最常用语言** | Japanese + English |

---

## 🔧 成功参数词汇库

根据历次创作积累，以下词汇经验证有效：

### ✅ 让歌曲变慢/忧郁

```
slow / deliberate / melancholic / bittersweet / restrained / spacious
laid-back / half-time feel / minimal percussion / brushed texture
```

### ✅ 让歌曲变快/欢乐

```
groovy / driving / energetic / catchy / punchy / upbeat
tight hi-hats / syncopated rhythm / dance-ready
```

### ✅ 人声空灵感

```
ethereal / crystalline / veil-like / translucent / breathy head voice
delicate vibrato / glass-like / floating / detached
```

### ❌ 需要 Exclude 的词汇（欢快快歌）

```
upbeat and happy and cheerful and fast tempo and energetic and dance and EDM
```

### ❌ 需要 Exclude 的词汇（忧郁慢歌）

```
upbeat and happy and fast and dance and energetic and aggressive
```
