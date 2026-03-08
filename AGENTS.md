# AGENTS.md - Educational Slides Project

## Project Overview
- **Purpose**: Create English teaching slides from academic abstracts for Taiwanese university students (EFL learners)
- **Format**: Reveal.js HTML presentations
- **Output**: HTML files hosted on GitHub Pages

## Source Files
- `abstract*.txt` - Academic paper abstracts (EdTech/AI in Education)

## New Style: 逐句解析 (Sentence-by-Sentence)

### Slide Structure (per abstract)
1. **Title slide** - English title + Chinese translation
2. **Highlights** - Research key points (中英對照)
3. **Sentence解析** (每句 2 頁):
   - **Page A**: 英文句子 + 中文翻譯 + 單字表 (Vocabulary)
   - **Page B**: 文法說明 (Grammar)
4. **Summary** - 總結

### 字體設定
- 基礎字體: **36px** (放大以便閱讀)
- 中文翻譯: 0.85em (紅色標示)
- 標題 h2: 1.5em
- 標題 h3: 1.2em (藍色)
- 列表: 0.9em

### CSS 樣式
```css
.reveal { font-size: 36px; }
.chinese { color: #e74c3c; font-size: 0.85em; }
.vocab-table { font-size: 0.7em; }
.grammar-box { background: #e8f6f3; border-left: 5px solid #1abc9c; }
.sentence-box { background: #f8f9fa; border-left: 5px solid #3498db; }
.verb-highlight { background-color: #ffeb3b; padding: 2px 6px; border-radius: 3px; }
```

### HTML 結構範例
```html
<!-- 句子 + 單字 -->
<section>
    <h3>Sentence N 句子解析</h3>
    <div class="sentence-box">
        <p><strong>英文句子 <span class="verb-highlight">核心動詞</span></strong></p>
        <p class="chinese">中文翻譯</p>
    </div>
    <div class="vocab-box">
        <table class="vocab-table">
            <!-- 單字表格 -->
        </table>
    </div>
</section>

<!-- 文法說明 -->
<section>
    <h3>Sentence N 文法</h3>
    <div class="grammar-box">文法說明</div>
</section>
```

## 資料夾結構
- `20260302/` - 舊版投影片 (abstract1-6)
- `20260309/` - 新版投影片 (abstract7)
- 未來新增使用 `YYYYMMDD/` 命名

## GitHub Repository
- **Repo URL**: https://github.com/chang4chihkai/CandE2026
- **Platform**: GitHub Pages

## GitHub Pages 設定
1. 進入 Repo Settings → Pages
2. Source 選擇 "Deploy from a branch"
3. Branch: `main`，Folder: `/ (root)`
4. 儲存後等待1-2分鐘

## 預覽網址
- **Pattern**: `https://chang4chihkai.github.io/CandE2026/[folder]/[filename].html`

| 資料夾 | 檔案 | 主題 |
|--------|------|------|
| 20260302 | abstract1.html | Generative AI & Creative Thinking Learning |
| 20260302 | abstract2.html | Multimodal Learning Analytics (MMLA) Systematic Review |
| 20260302 | abstract3.html | VR Serious Games & Environmental Education |
| 20260302 | abstract4.html | AI Knowledge Scale Development & Validation |
| 20260302 | abstract5.html | Critical Thinking Intervention & GenAI Collaborative Learning |
| 20260302 | abstract6.html | AGI & Discourse Analysis (CGT-LLM Framework) |
| 20260309 | abstract7.html | Expressions of learner agency in virtual inquiry |

## Commands
- Preview locally: Open HTML files in browser (requires internet for CDN)
- Update slides: Edit HTML files, then `git add . && git commit -m "update" && git push`
