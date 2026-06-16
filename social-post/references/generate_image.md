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
6. **輸出位置與命名**
   - 生成後的圖片一律集中放 `/Users/fishtv/Development/book/social-post/photo/`
   - 若使用者有指定主標題，檔名直接用主標題
   - 例：`諾蘭:說未來很可怕，但我們還有選擇.png`
   - 若本次工具無法直接寫檔，也要先依這個檔名規則生成，後續存檔沿用同名
7. **封面比例預設**
   - 若本次是「封面圖」，預設使用 `16:9` 橫式構圖
   - 目標尺寸固定為 `1920x1080`
   - 除非使用者明確指定別的比例
   - 生成後必須檢查實際像素；若工具輸出不是 `1920x1080`，要後處理成正確尺寸後再交付
8. **變體命名**
   - 若同一張封面要做多個版本，檔名尾碼加流水號
   - 例：`諾蘭:說未來很可怕，但我們還有選擇1.png`
   - 下一版接續：`諾蘭:說未來很可怕，但我們還有選擇2.png`
9. **差異型主題優先構圖**
   - 若文章核心在講前後對比、混亂與整理、阻力與清開，優先做視覺上可一眼看懂的 `A/B 對比圖`
   - 對比可以是左右分區、前後兩個狀態，或同一人物面對兩種工作環境

## Prompt 範本

```text
Create a premium editorial-style social post image for a Traditional Chinese post.

Format:
16:9 horizontal cover, 1920x1080.

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
