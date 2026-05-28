# Perplexity Scenario Factory

> **Фабрика сценариев автоматизации Perplexity браузера** — 200 use cases, система deep research, память проекта (LLM-Wiki pattern), инструкции для IDE-агентов.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status: Active](https://img.shields.io/badge/Status-Active-green.svg)](STATUS.md)
[![Scenarios: 200](https://img.shields.io/badge/Scenarios-200-blue.svg)](catalog/000-master-table.md)

---

## Что это

Системный knowledge base + automation framework для:
- **200 сценариев** использования Perplexity/Comet в браузере
- **Deep Research** машины (50+ параллельных запросов, STORM + GPT-Researcher паттерн)
- **Памяти проекта** (Karpathy LLM-Wiki: incremental markdown wiki, auto-index)
- **Синтеза новых сценариев** из существующих (комбинирование, эскалация, gap analysis)
- **Инструкций для IDE-агентов**: Claude Code, Codex, Cursor, Windsurf, Aider
- **Скриптов и паттернов** автоматизации: Python, n8n, userscript, MCP

---

## Архитектура (самокритика применена)

```
perplexity-scenario-factory/
├── README.md                    # Этот файл — точка входа
├── INDEX.md                     # ЖИВОЙ индекс всех файлов (auto-updated)
├── STATUS.md                    # Текущий статус проекта
├── ROADMAP.md                   # Фазы и milestones
├── CONTEXT_MAP.md               # Карта связей всех компонентов
├── CLAUDE.md                    # Project rules для Claude Code (root)
├── AGENTS.md                    # Universal agent instructions
│
├── memory/                      # PROJECT MEMORY (Karpathy LLM-Wiki)
│   ├── INDEX.md                 # Каталог всего в wiki
│   ├── wiki/                    # LLM-compiled wiki
│   │   ├── concepts/            # Концепты: automation, research, browser
│   │   ├── entities/            # Инструменты, API, паттерны
│   │   └── synthesis/           # Кросс-референсные синтезы
│   └── raw/                     # Исходники (immutable)
│
├── catalog/                     # КАТАЛОГ 200 СЦЕНАРИЕВ
│   ├── 000-master-table.md      # Все 200 UC в одной таблице
│   ├── 000-taxonomy.md          # Классификация + теги
│   ├── research/                # UC-001..UC-040
│   ├── shopping/                # UC-041..UC-060
│   ├── admin-ops/               # UC-061..UC-090
│   ├── learning/                # UC-091..UC-110
│   ├── dev/                     # UC-111..UC-140
│   ├── marketing/               # UC-141..UC-165
│   ├── finance/                 # UC-166..UC-180
│   └── productivity/            # UC-181..UC-200
│
├── guides/                      # 200 ПОДРОБНЫХ ГАЙДОВ
│   └── UC-001.md .. UC-200.md
│
├── deep-research/               # СИСТЕМА DEEP RESEARCH
│   ├── RESEARCH_SCHEMA.md       # Как запускать 50+ запросов
│   ├── runners/                 # Python/CLI runners
│   ├── queries/                 # Архив запросов
│   └── results/                 # Результаты (MD)
│
├── synthesis/                   # СИНТЕЗ НОВЫХ СЦЕНАРИЕВ
│   ├── SYNTHESIS_SCHEMA.md      # Правила создания новых UC
│   ├── patterns/                # combination, escalation, gap-analysis
│   └── proposals/               # Черновики новых UC
│
├── backlog/                     # BACKLOG + TODO
│   ├── TODO.md                  # Активные задачи
│   └── BACKLOG.md               # Все задачи + приоритеты
│
├── agent-instructions/          # IDE AGENT MD FILES
│   ├── CLAUDE.md                # Claude Code
│   ├── AGENTS.md                # Codex, Gemini CLI
│   ├── CURSOR_RULES.md          # Cursor rules
│   ├── WINDSURF.md              # Windsurf
│   └── AIDER.md                 # Aider
│
├── skills/                      # AGENT SKILLS (skill.md format)
│   ├── scenario-search/
│   ├── scenario-synthesis/
│   ├── deep-research-runner/
│   ├── index-updater/
│   └── backlog-manager/
│
├── scripts/                     # AUTOMATION SCRIPTS
│   ├── perplexity-sonar-deep-research.py
│   ├── scenario-generator.py
│   ├── index-builder.py
│   ├── wiki-compiler.py
│   ├── scenario-gap-finder.py
│   ├── n8n-workflows/
│   └── userscripts/
│
├── patterns/                    # REUSABLE PATTERNS
│   ├── prompt-grammar.md
│   ├── workflow-template.md
│   ├── guide-template.md
│   ├── automation-patterns.md
│   ├── risk-framework.md
│   └── evaluation-rubric.md
│
└── examples/                    # GOLDEN EXAMPLES
    ├── UC-001-full-example.md
    └── research-flow-example.md
```

---

## Как использовать

### Для людей
1. Открой [catalog/000-master-table.md](catalog/000-master-table.md) — найди нужный сценарий
2. Перейди в [guides/UC-XXX.md](guides/) — получи подробный гайд
3. Смотри [patterns/prompt-grammar.md](patterns/prompt-grammar.md) — используй готовые промпты

### Для IDE-агентов (Claude Code, Codex, Cursor)
1. Читай [CLAUDE.md](CLAUDE.md) или [agent-instructions/AGENTS.md](agent-instructions/AGENTS.md)
2. Используй [skills/](skills/) для повторяемых действий
3. Управляй задачами через [backlog/TODO.md](backlog/TODO.md)

### Для deep research
1. Читай [deep-research/RESEARCH_SCHEMA.md](deep-research/RESEARCH_SCHEMA.md)
2. Запускай [scripts/perplexity-sonar-deep-research.py](scripts/perplexity-sonar-deep-research.py)
3. Результаты сохраняются в [deep-research/results/](deep-research/results/) и компилируются в [memory/wiki/](memory/wiki/)

---

## Open Source стек (синтез deep research)

| Компонент | Решение | Ссылка |
|---|---|---|
| Deep Research | GPT-Researcher | https://github.com/assafelovic/gpt-researcher |
| Research Wiki | STORM (Stanford) | https://github.com/stanford-oval/storm |
| Project Memory | Graphiti (temporal KG) | https://github.com/getzep/graphiti |
| Agent Memory | Mem0 | https://github.com/mem0ai/mem0 |
| LLM Wiki Pattern | Karpathy gist | https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f |
| Backlog/Tasks | Backlog.md | https://github.com/MrLesk/Backlog.md |
| Repo Packing | Repomix | https://github.com/yamadashy/repomix |
| Perplexity MCP | Official | https://github.com/perplexityai/modelcontextprotocol |
| n8n Templates | awesome-n8n | https://github.com/enescingoz/awesome-n8n-templates |
| MCP Servers | awesome-mcp | https://github.com/punkpeye/awesome-mcp-servers |

---

## Связанные репозитории @homgorn

- https://github.com/homgorn/prodsynth-monorepo — ProdSynth (BMAD, Graphiti memory, 12 agents)
- https://github.com/homgorn/AI-Scraping-Stack — Multi-agent web intelligence
- https://github.com/homgorn/perplexity_search_real — Perplexity API Python tool
- https://github.com/homgorn/repomix-AI-friendly-file — Repo packing

---

## Статус

См. [STATUS.md](STATUS.md) и [backlog/TODO.md](backlog/TODO.md)

**Версия:** 1.0.0-alpha | **Дата:** 2026-05-28 | **Аккаунт:** referturnet
