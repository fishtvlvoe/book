# Phase 2-Image：配圖 / 生圖

何時跑：使用者說「配圖」「生圖」「幫這篇做圖」「封面圖」，或在文案定稿後未明確拒絕圖片時。

## 核心原則

1. 圖是為文案服務，不是反過來
2. 先抓文案主命題，再翻成畫面
3. 優先讀 `image_prompt_profile.md`
4. 若有公司 CI，先套 CI，再套 Fish 個人風格

## 步驟

1. **先讀文案**
   - 找出最重要的一句話
   - 判斷這篇屬於：觀點型 / 工作流型 / 書摘型 / 情緒反思型
2. **讀 `image_prompt_profile.md`**
   - 先用 Fish 個人預設
   - 若有品牌區塊，套品牌限制
3. **產出 1-3 組 prompt**
   - 一組穩健版
   - 一組更有視覺感版
   - 一組偏品牌 / 公司 CI 版（若有）
4. **預設主動問**
   - 文案定稿後補一句：
   - `要不要順手幫這篇生一張配圖？`
5. **若使用者說要**
   - 直接交 prompt
   - 若當前環境可直接生圖，就用 prompt 產圖

## Prompt 範本

```text
Create a premium editorial-style social post image for a Traditional Chinese post.

Core message:
「（這篇文最重要的一句話）」

Visual concept:
（用 2-4 句描述畫面，不要只重複標題）

Style:
realistic photography, thoughtful workspace atmosphere, soft natural light, restrained composition, premium editorial look, clean negative space for headline, not generic AI poster

Brand / CI constraints:
（若有品牌色、品牌物件、品牌禁忌，寫在這裡）

Avoid:
overly futuristic neon tech aesthetic, cluttered layout, cheap startup hero look, exaggerated lens flare, fake hands, unreadable typography
```

## 什麼情況不該硬做圖

- 文案還沒定稿
- 還不知道這篇重點是什麼
- 品牌 CI 還沒給，但使用者明確要求品牌一致
- 只是為了湊圖，沒有畫面理由
