# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A personal English vocabulary learning project built around the animated series **Arcane** (League of Legends). Each episode has a subtitle file (SRT) and a corresponding vocabulary notes file with definitions, examples, and Traditional Chinese (繁體中文) translations.

## Repository Structure

```
arcane/
├── 01.srt              # Episode 1 subtitle file
├── vocab/
│   └── ep01.md          # Episode 1 vocabulary notes
└── expressions/
    └── ep01.md          # Episode 1 colloquial expressions & sentence patterns
```

- **SRT files** — Full subtitles for each episode (named `NN.srt`)
- **vocab/** — New words and their definitions per episode (named `epNN.md`)
- **expressions/** — Useful colloquial expressions, idioms, and sentence patterns per episode (named `epNN.md`)

## Entry Format

Each entry in `vocab/epNN.md` and `expressions/epNN.md` follows this structure:

```markdown
## word or phrase
- **part of speech** definition in English
  - 例：English example sentence（中文翻譯）
- **lyrics/dialogue:** original line from the episode
  - 中文解釋，含劇情脈絡
```

Key conventions:
- Part of speech labels: `adj.`, `n.`, `v.`, `phrasal v.`, `idiom`, `informal`, `sentence pattern`, `adv.`
- Use `lyrics:` for song lyrics, `dialogue:` for spoken lines
- Include character context and scene notes in Chinese explanations
- List common collocations with `常見搭配：`
- Multiple definitions for the same word get separate bullet points under the same heading

## Line-by-line Teaching Format

When the user selects lines from an SRT file and asks for explanation/analysis, respond **line-by-line** with each dialogue line as a self-contained block. Do NOT produce a summary-style bullet list of vocab/expressions detached from the original lines — the teaching points must stay attached to the line they come from.

Format template (per dialogue line):

```markdown
### <SRT line number>｜<Speaker>: <original English line>

「<繁體中文翻譯>」<必要時補一句語氣/情境說明>
- **<詞彙或片語>**：<詞性> <簡短定義，中英並陳>
- 例：<English example>（<中文翻譯>）
- 常見搭配：<collocations>（可選）
- <句型/語氣/補充說明>（可選）
```

Rules:
- One `###` block per dialogue line. Skip pure sound-effect lines like `[knocks on door]` unless they carry meaning.
- Start each block with the Chinese translation of the line, then drill into the learning points **inline** under that same line.
- Cover vocabulary, idioms, phrasal verbs, sentence patterns, and tone/register as they appear — bold the target term with `**...**`.
- Include short English example sentences with Chinese translations when useful.
- Use `---` separators between dialogue blocks for readability.
- After all lines are covered, end with a short suggestion block proposing which items to add to `vocab/epNN.md` vs `expressions/epNN.md`, and **wait for the user to confirm** before editing files.
