# CONTEXT RESTORE — Восстановление контекста

> **🔥 ЧИТАЙ ЭТОТ ФАЙЛ ПЕРВЫМ В КАЖДОМ НОВОМ ЧАТЕ!**

Последнее обновление: **2026-05-28 10:00 +06**  
Автор последней сессии: **referturnet** (Perplexity Comet browser)

---

## 🎯 Цель проекта

**Perplexity Scenario Factory** — систематизированный knowledge base из 200 сценариев использования Perplexity/Comet browser automation + система deep research (50+ параллельных запросов) + проектная память (Karpathy LLM-Wiki pattern) + инструкции для IDE-агентов (Claude Code, Codex, Cursor, Windsurf).

**Репо:** https://github.com/referturnet/perplexity-scenario-factory

---

## ✅ Что УЖЕ СДЕЛАНО (Session 1: 2026-05-28)

### Созданы файлы

| Файл | Статус | Описание |
|------|--------|------------|
| `README.md` | ✅ Готов | Полная архитектура проекта, ссылки на open source stack |
| `CLAUDE.md` | ✅ Готов | Project instructions для Claude Code: workflow, правила, формат INDEX.md |
| `CONTEXT_RESTORE.md` | ⏳ Создаётся | Этот файл |
| `LICENSE` | ✅ Готов | MIT License |

### Deep Research (проведён)

Сделано **50+ запросов** по темам:
- Open-source AI scenario generators, use case libraries
- Deep research systems: GPT-Researcher, STORM (Stanford)
- Project memory: Graphiti (temporal KG), Mem0, Zep, Karpathy LLM-Wiki
- Perplexity API/MCP интеграции
- n8n workflow templates, MCP servers
- Repo packing tools: Repomix, context tools
- Backlog/task management: Backlog.md (MCP-compatible)

Все ссылки зафиксированы в README.md.

### Синтез архитектуры

Создана **полная структура проекта** (см. README.md):
- `memory/` — Karpathy LLM-Wiki pattern (raw/, wiki/, INDEX.md)
- `catalog/` — 200 use cases (по категориям: research, shopping, admin-ops, learning, dev, marketing, finance, productivity)
- `guides/` — 200 подробных гайдов
- `deep-research/` — система deep research (RESEARCH_SCHEMA.md, runners/, queries/, results/)
- `synthesis/` — синтез новых сценариев
- `backlog/` — TODO.md, BACKLOG.md
- `agent-instructions/` — CLAUDE.md, AGENTS.md, CURSOR_RULES.md, WINDSURF.md, AIDER.md
- `skills/` — повторяемые agent skills
- `scripts/` — Python/bash/n8n/userscripts
- `patterns/` — prompt-grammar, workflow templates, evaluation rubric
- `examples/` — golden examples

---

## ⏳ ЧТО НАДО СДЕЛАТЬ ДАЛЬШЕ (Next Session)

### Приоритет 1: Ключевые файлы для контекста

- [ ] `INDEX.md` — живой индекс всех файлов (ОБНОВЛЯТЬ ПОСЛЕ КАЖДОГО файла!)
- [ ] `STATUS.md` — текущий статус проекта
- [ ] `ROADMAP.md` — фазы и milestones
- [ ] `CONTEXT_MAP.md` — карта связей компонентов
- [ ] `backlog/TODO.md` — активные задачи
- [ ] `backlog/BACKLOG.md` — полный backlog

### Приоритет 2: Agent instructions

- [ ] `AGENTS.md` — universal agent instructions (Codex, Gemini CLI)
- [ ] `agent-instructions/CURSOR_RULES.md`
- [ ] `agent-instructions/WINDSURF.md`
- [ ] `agent-instructions/AIDER.md`

### Приоритет 3: Catalog (начало)

- [ ] `catalog/000-master-table.md` — таблица 200 сценариев (начать с 25 UC chunk 1)
- [ ] `catalog/000-taxonomy.md` — классификация и теги

### Приоритет 4: Memory layer

- [ ] `memory/INDEX.md`
- [ ] `memory/wiki/concepts/` — первые концепт-страницы
- [ ] `memory/raw/` — исходники deep research

---

## 📚 Как работать с этим проектом

### Для новой сессии (Claude Code / Perplexity Comet)

1. **Читай CONTEXT_RESTORE.md** (этот файл) — узнай что сделано
2. **Читай INDEX.md** — узнай какие файлы существуют
3. **Читай CLAUDE.md** — узнай правила работы
4. **Читай backlog/TODO.md** — узнай активные задачи
5. **Читай STATUS.md** — узнай текущий этап

### При создании нового файла

1. **Создай файл**
2. **ОБНОВИ INDEX.md** — добавь запись с путём, описанием, датой
3. **Обнови STATUS.md** (если это важный milestone)

### Перед завершением сессии

1. **Обнови backlog/TODO.md** — отметь completed задачи
2. **Обнови STATUS.md** — запиши что готово
3. **ОБНОВИ CONTEXT_RESTORE.md** — запиши контекст для следующей сессии

---

## 🛠 Важные правила

### ✅ Делай ВСЕГДА
- Обновляй **INDEX.md** после каждого нового файла
- Обновляй **CONTEXT_RESTORE.md** перед завершением сессии
- Следуй структуре из README.md
- Используй markdown для всех документов
- Добавляй ссылки в полном виде (https://...)

### ❌ Не делай НИКОГДА
- Не создавай файлы без обновления INDEX.md
- Не пропускай приоритетные файлы
- Не забывай обновить CONTEXT_RESTORE.md

---

## 🔗 Полезные ссылки

- **Репо:** https://github.com/referturnet/perplexity-scenario-factory
- **README:** https://github.com/referturnet/perplexity-scenario-factory/blob/main/README.md
- **CLAUDE.md:** https://github.com/referturnet/perplexity-scenario-factory/blob/main/CLAUDE.md

### Связанные репо @homgorn
- https://github.com/homgorn/prodsynth-monorepo — ProdSynth (BMAD, Graphiti, 12 agents)
- https://github.com/homgorn/AI-Scraping-Stack — Multi-agent web intelligence

### Open Source Stack
- GPT-Researcher: https://github.com/assafelovic/gpt-researcher
- STORM (Stanford): https://github.com/stanford-oval/storm
- Graphiti: https://github.com/getzep/graphiti
- Mem0: https://github.com/mem0ai/mem0
- Karpathy LLM-Wiki: https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- Backlog.md: https://github.com/MrLesk/Backlog.md
- Repomix: https://github.com/yamadashy/repomix
- Perplexity MCP: https://github.com/perplexityai/modelcontextprotocol

---

**Версия:** 1.0 | **Последнее обновление:** 2026-05-28 10:00 +06
