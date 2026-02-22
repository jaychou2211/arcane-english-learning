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
