# 🎤 Suno AI 人声设计库 (Vocal Design Library)

> 本库提供开箱即用的 `[VOCAL]` 参数块预设，按性别 × 风格维度组织。选择后直接粘贴到 Style Prompt 中使用。

---

## 📋 速查矩阵

| 风格 | 女声预设 | 男声预设 |
|------|---------|---------| 
| 空灵梦幻 | `F-01` 仙女音 | `M-01` 云端少年 |
| 温暖甜美 | `F-02` 暖糖嗓 | `M-02` 邻家暖男 |
| 冷酷疏离 | `F-03` 冰川女王 | `M-03` 暗夜行者 |
| 烟嗓磁性 | `F-04` 午夜爵士 | `M-04` 威士忌嗓 |
| 力量爆发 | `F-05` 燃系歌姬 | `M-05` 摇滚猛兽 |
| 清冷知性 | `F-06` 文艺女青年 | `M-06` 诗人低语 |
| 甜酷混合 | `F-07` 辣妹音 | `M-07` 街头少年 |
| 古典质感 | `F-08` 歌剧花腔 | `M-08` 古典男高 |
| 电子处理 | `F-09` 赛博女声 | `M-09` 数字幽灵 |
| 说唱/念白 | `F-10` 说唱女王 | `M-10` Flow 大师 |
| 空灵节奏感 | `F-11` 幻梦女声 | — |

---

## 👩 女声预设 (Female Presets)

### F-01 仙女音（空灵梦幻）

```text
[VOCAL]
type: female vocal
style: ethereal and dreamy with angelic floating quality
language: [按需填写]
tone: crystal-clear and delicate and airy and otherworldly
register: soprano with effortless high notes
technique: breathy head voice with light vibrato and whispered transitions
delivery: detached and mysterious and floating above the music
special: glass-like high notes with natural shimmer and soft consonants
high notes: crystal-clear sustain with no strain and gentle fade
ad-libs: ethereal (Ooooh) and (Ahhh) with reverb bloom
```

**适配曲风**：Dream Pop / Ambient / 古风 / Cinematic  
**参考音色方向**：王菲式疏离空灵 / Enya 式天籁

### F-02 暖糖嗓（温暖甜美）

```text
[VOCAL]
type: female vocal
style: warm and sweet with honey-toned intimacy
language: [按需填写]
tone: round and warm and sweet and gentle and slightly nasal charm
register: alto to mid-soprano comfort zone
technique: clear chest voice with smooth transitions and gentle vibrato at phrase endings
delivery: sincere and tender and close-to-ear warmth
special: smile-in-voice quality and soft legato phrasing
high notes: warm and round without sharpness
ad-libs: gentle (Mmm) and (La la la)
```

**适配曲风**：C-Pop / J-Pop / Indie Pop / 民谣  
**参考音色方向**：田馥甄式温柔 / IU 式清甜

### F-03 冰川女王（冷酷疏离）

```text
[VOCAL]
type: female vocal
style: icy and commanding with cold glamour
language: [按需填写]
tone: thin and sharp and metallic edge and controlled coolness
register: mid-range with cutting high notes
technique: straight tone with minimal vibrato and precise staccato phrasing
delivery: emotionally detached and superior and calculating
special: each word pronounced with deliberate precision and razor-sharp diction
high notes: piercing and controlled with steel-like clarity
ad-libs: minimal and sharp (Ha) or silence
```

**适配曲风**：Synthpop / K-Pop (girl crush) / Dark Pop  
**参考音色方向**：CL 式霸气 / Grimes 式冷电子

### F-04 午夜爵士（烟嗓磁性）

```text
[VOCAL]
type: female vocal
style: smoky jazz with late-night lounge magnetism
language: [按需填写]
tone: husky and smoky and warm and magnetic and slightly gravelly
register: low alto with sultry lower register
technique: breathy delivery with lazy phrasing and behind-the-beat timing
delivery: seductive and world-weary and effortlessly cool
special: vocal fry at phrase endings and whispered asides
high notes: restrained and smoky without losing warmth
ad-libs: spoken-word asides and breathy (Yeah) and (Mmm)
```

**适配曲风**：Jazz / Neo-Soul / R&B / Bossa Nova  
**参考音色方向**：Billie Holiday 式烟嗓 / Amy Winehouse 式爵士灵魂

### F-05 燃系歌姬（力量爆发）

```text
[VOCAL]
type: female vocal
style: powerful diva with explosive dynamic range
language: [按需填写]
tone: rich and full-bodied and resonant and soaring
register: wide range from chest voice lows to belted soprano highs
technique: powerful belting with controlled vibrato and dynamic crescendos
delivery: passionate and defiant and emotionally unleashed
special: goosebump-inducing build from whisper to full power and riffing on sustained notes
high notes: powerful sustained belt with wide vibrato and emotional release
ad-libs: gospel-style runs and (Woah-oh-oh) and (Yeah-eah-eah)
```

**适配曲风**：Power Ballad / Pop Rock / Gospel / Musical  
**参考音色方向**：邓紫棋式高音爆发 / Adele 式灵魂力量

### F-06 文艺女青年（清冷知性）

```text
[VOCAL]
type: female vocal
style: literary and understated with intellectual cool
language: [按需填写]
tone: slightly thin and clear and clean and bookish warmth
register: mid-range comfortable alto
technique: spoken-singing hybrid and natural unpolished phrasing and conversational
delivery: introspective and thoughtful and like reading poetry aloud
special: intentionally imperfect and charming in its rawness
high notes: avoided or approached gently without pushing
ad-libs: spoken-word fragments and gentle humming (Hmm)
```

**适配曲风**：Indie Folk / 民谣 / Singer-Songwriter  
**参考音色方向**：陈绮贞式文艺 / Phoebe Bridgers 式低调

### F-07 辣妹音（甜酷混合）

```text
[VOCAL]
type: female vocal
style: sweet yet fierce with playful attitude
language: [按需填写]
tone: bright and sharp and slightly nasal and cheeky
register: mid to high soprano with punchy delivery
technique: staccato rhythmic delivery and rap-sing hybrid and attitude-loaded phrasing
delivery: confident and flirtatious and unbothered
special: switching between cute and fierce within phrases
high notes: sharp and bright and short punchy hits
ad-libs: (Uh-huh) and (Let's go) and cheeky spoken asides
```

**适配曲风**：K-Pop / EDM Pop / Trap Pop / Dance Pop  
**参考音色方向**：BLACKPINK LISA 式辣酷 / Doja Cat 式百变

### F-08 歌剧花腔（古典质感）

```text
[VOCAL]
type: female vocal
style: operatic soprano with classical training and purity
language: [按需填写]
tone: pure and round and resonant and vibrant with classical projection
register: full soprano range with coloratura agility
technique: classical bel canto with controlled vibrato and legato lines
delivery: grand and emotive and theatrical
special: ornamental trills and runs and perfect pitch control
high notes: soaring and effortless with full operatic projection
ad-libs: classical vocalise (Ah-ah-ah) runs
```

**适配曲风**：Classical Crossover / Cinematic / Neoclassical / Musical  

### F-09 赛博女声（电子处理）

```text
[VOCAL]
type: female vocal
style: cyberpunk processed vocal with digital aesthetics
language: [按需填写]
tone: thin and metallic and auto-tuned and glitchy and futuristic
register: mid-range with pitch-shifted sections
technique: monotone delivery with sudden pitch jumps and vocoder blending
delivery: robotic and emotionless and AI-like detachment
special: heavy auto-tune with hard-tune effect and glitch interruptions
high notes: pitch-shifted and crystallized
ad-libs: glitched fragments and stuttered syllables
```

**适配曲风**：Hyperpop / EDM / Future Bass / Synthwave  

### F-10 说唱女王（Rap/念白）

```text
[VOCAL]
type: female vocal
style: fierce rapper with sharp flow and lyrical precision
language: [按需填写]
tone: sharp and aggressive and clear and punchy
register: mid-range spoken with occasional melodic hooks
technique: rapid-fire delivery and complex rhythmic flow and hard consonants
delivery: confident and dominant and street-smart
special: razor-sharp diction and rhythmic variety and breath control
high notes: melodic hook sections with attitude
ad-libs: (Skrrt) and (Aye) and (Woo) and spoken drops
```

**适配曲风**：Trap / Hip-Hop / K-Rap / C-Rap  

### F-11 幻梦女声（空灵节奏感）

```text
[VOCAL]
type: female vocal
style: ethereal and crystalline with translucent veil-like quality and rhythmic versatility
language: Japanese with English hooks
tone: crystal-clear and breathy and delicate and glass-like and translucent shimmer
register: soprano with effortless high register
technique: breathy head voice with delicate controlled vibrato and natural Japanese-English code-switching and rhythmic precision in verses
delivery: cool and detached in verses building to passionately resolute in chorus
special: glass-like sustained high notes and clear Japanese diction and layered self-harmony in chorus
high notes: crystal-clear sustain with ethereal shimmer and no strain
ad-libs: soft (Ooooh) and whispered (Yeah yeah yeah) and harmony layers (Ahhh)
```

**适配曲风**：J-Pop Slow Ballad / Alt R&B / Melodic Future Bass  
**参考方向**：空灵日韩曲风

---

## 👨 男声预设 (Male Presets)

### M-01 云端少年（空灵梦幻）

```text
[VOCAL]
type: male vocal
style: ethereal boy-like purity with delicate floating quality
language: [按需填写]
tone: light and airy and pure and slightly androgynous
register: high tenor with easy falsetto access
technique: breathy falsetto with gentle head voice and floating delivery
delivery: innocent and dreamy and weightless
special: seamless chest-to-falsetto transitions and pure gentle tone
high notes: effortless falsetto with crystalline clarity
ad-libs: gentle (Ooh) and sustained falsetto hums
```

**适配曲风**：Dream Pop / Indie / R&B / Ambient  
**参考音色方向**：林宥嘉式空灵 / Jeff Buckley 式纯净

### M-02 邻家暖男（温暖亲切）

```text
[VOCAL]
type: male vocal
style: warm and approachable with genuine emotional warmth
language: [按需填写]
tone: warm and round and friendly and comforting and slightly husky
register: mid-range baritone to tenor comfort zone
technique: natural delivery with gentle vibrato and conversational phrasing
delivery: sincere and heartfelt and like talking to an old friend
special: smile-in-voice warmth and natural breath sounds add intimacy
high notes: warm and soft without strain
ad-libs: gentle spoken asides and (Hmm) and (Yeah)
```

**适配曲风**：C-Pop / Folk / Singer-Songwriter / Acoustic  
**参考音色方向**：毛不易式温暖 / Ed Sheeran 式亲和

### M-03 暗夜行者（冷酷疏离）

```text
[VOCAL]
type: male vocal
style: dark and brooding with mysterious edge
language: [按需填写]
tone: deep and dark and resonant and shadowy and magnetic
register: low baritone with haunting low notes
technique: controlled low register and whispery verses and restrained power
delivery: menacing calm and emotionally guarded and dangerous stillness
special: spoken-word sections with low resonance and dramatic pauses
high notes: rarely used and when used full of tension and strain
ad-libs: low spoken whispers and breathing sounds
```

**适配曲风**：Dark Pop / Gothic / Trip-Hop / Synthwave  
**参考音色方向**：The Weeknd 式暗黑 / Hozier 式深沉

### M-04 威士忌嗓（烟嗓磁性）

```text
[VOCAL]
type: male vocal
style: weathered and soulful with lived-in character
language: [按需填写]
tone: gravelly and warm and smoky and aged and textured
register: mid-baritone with gritty lower range
technique: raspy delivery with lazy blues phrasing and emotional weight
delivery: world-weary and wise and effortlessly cool
special: vocal cracks add authenticity and sandpaper texture on consonants
high notes: strained and raw with emotional power
ad-libs: gravelly (Mmm) and spoken asides and bluesy moans
```

**适配曲风**：Blues / Rock / Jazz / Country / Folk  
**参考音色方向**：Leonard Cohen 式沧桑 / Tom Waits 式粗粝

### M-05 摇滚猛兽（力量爆发）

```text
[VOCAL]
type: male vocal
style: explosive rocker with raw power and intensity
language: [按需填写]
tone: powerful and gritty and aggressive and soaring
register: wide range with powerful tenor belts
technique: hard belting with aggressive vibrato and screaming dynamics
delivery: defiant and furious and cathartic emotional release
special: controlled screams and raw power notes and primal energy
high notes: screamed or belted with full force and grit
ad-libs: screams and (YEAH) and (COME ON) and growls
```

**适配曲风**：Rock / Metal / Punk / Alternative  

### M-06 诗人低语（清冷知性）

```text
[VOCAL]
type: male vocal
style: soft-spoken intellectual with poetic grace
language: [按需填写]
tone: soft and delicate and slightly nasal and literary
register: mid-range with intimate volume
technique: spoken-singing and whispered verses and literary phrasing
delivery: contemplative and melancholic and privately emotional
special: ASMR-like closeness and deliberate slow pacing
high notes: gentle and avoided or whispered
ad-libs: whispered words and sighs and long pauses
```

**适配曲风**：Indie / Art Pop / Ambient / 民谣  
**参考音色方向**：Bon Iver 式私密 / 李健式知性

### M-07 街头少年（甜酷混合）

```text
[VOCAL]
type: male vocal
style: street-smart swagger with melodic sensitivity
language: [按需填写]
tone: bright and youthful and slightly nasal and cocky
register: mid-tenor with auto-tune melodic hooks
technique: rap-sing hybrid and melodic flow and catchy hook delivery
delivery: confident and carefree and effortlessly cool
special: auto-tune on melodic sections and hard rap on verses
high notes: auto-tuned soaring hooks
ad-libs: (Yeah) and (Skrrt) and (Woo) and ad-lib stacks
```

**适配曲风**：Trap / Hip-Hop / K-Pop / C-Rap  

### M-08 古典男高（古典质感）

```text
[VOCAL]
type: male vocal
style: classical tenor with operatic projection and warmth
language: [按需填写]
tone: brilliant and resonant and warm and powerful and ringing
register: full tenor range with thrilling top notes
technique: bel canto with sustained legato and controlled vibrato and dynamic range
delivery: grand and noble and emotionally sweeping
special: ringing high C and powerful sustained phrases
high notes: brilliant and ringing with full operatic power
ad-libs: classical vocalise
```

**适配曲风**：Classical Crossover / Opera / Musical / Cinematic  

### M-09 数字幽灵（电子处理）

```text
[VOCAL]
type: male vocal
style: digitally processed with futuristic alien quality
language: [按需填写]
tone: distorted and glitchy and pitch-shifted and alien
register: varied with pitch-shifting across octaves
technique: vocoder-heavy and monotone base with digital artifacts
delivery: cold and mechanical and post-human
special: extreme auto-tune and bit-crushing and formant shifting
high notes: digitally generated overtones
ad-libs: robotic stutters and data-stream sounds
```

**适配曲风**：Hyperpop / Experimental Electronic / IDM  

### M-10 Flow 大师（Rap/念白）

```text
[VOCAL]
type: male vocal
style: versatile rapper with complex flow patterns
language: [按需填写]
tone: clear and punchy and rhythmically precise and authoritative
register: mid-range spoken with melodic hook sections
technique: multisyllabic rhymes and variable speed and syncopated flow
delivery: commanding and storytelling and rhythmically inventive
special: internal rhyme patterns and double-time sections and breath control mastery
high notes: melodic chorus hook sections
ad-libs: (Uh) and (Yeah) and (What) and (Let's go) and hype stacks
```

**适配曲风**：Hip-Hop / Trap / Boom Bap / C-Rap  

---

## 🎭 特殊人声预设

### DU-01 男女对唱 (Duet)

```text
[VOCAL]
type: male and female duet
style: romantic call-and-response with harmonized choruses
language: [按需填写]
tone: contrasting warmth (male warm baritone) and (female bright soprano) that blend in harmony
register: male mid-range and female upper range with overlapping sweet spot
technique: alternating verses and harmonized chorus and occasional unison
delivery: intimate conversation between two voices and emotional chemistry
special: [Male Vocal] tag on male verses and [Female Vocal] tag on female verses
high notes: female leads high notes with male harmony support
ad-libs: overlapping (Ooh) and responded echoes
```

### CH-01 合唱团 (Choir)

```text
[VOCAL]
type: mixed choir
style: full choral ensemble with layered harmonies
language: [按需填写]
tone: rich and layered and powerful and immersive
register: full SATB range (soprano alto tenor bass)
technique: block harmonies and antiphonal call-response and crescendo builds
delivery: unified grand and sweeping and cathedral-filling
special: choir enters gradually and builds to full power at climax
high notes: sopranos soar above full ensemble
ad-libs: wordless choir (Ooh) and (Ahh) layers
```
