# CONSTITUTION — Spec-Driven + LLM Wiki

**Последнее обновление:** 2026-05-29 18:59 +06  
**Подход:** GitHub Spec-Kit + Karpathy LLM Wiki

## Purpose

Этот репозиторий развивает каталог сценариев использования Perplexity AI по принципу spec-driven development: сначала спецификация, потом план, потом задачи, потом реализация.

Для этого проекта подход особенно полезен, потому что каталог из 200 UC требует предсказуемого процесса, а не ad-hoc создания файлов.

## Core Principles

### Artifacts over chat
Главный результат работы агента — обновлённые файлы в репозитории, а не длинные сообщения в чате.

### Spec before implementation
Для каждой крупной единицы работы нужен минимум: specification, plan, tasks, implementation artifact.

### Atomic knowledge
Одна идея = один файл или одна чёткая секция.

### Compounding memory
Каждая сессия должна усиливать следующую через progress, changelog, wiki, guide, skill и pattern.

### Cross-linking by default
Ключевые файлы должны ссылаться друг на друга.

## Repository Model

### Spec Layer
- `catalog/` — use cases и гайды.
- `agent-instructions/` — schema для агентов и Spaces.
- `CONSTITUTION.md` — governing rules.

### Planning Layer
- `ROADMAP.md` — фазы и milestones.
- `PROGRESS.md` — текущий прогресс.
- `backlog/` — текущие задачи.

### Knowledge Layer
- `skills/` — переиспользуемые навыки.
- `patterns/` — паттерны работы.
- `memory/wiki/` — атомарная wiki-память.
- `memory/raw/` — сырые материалы.

### Operational Layer
- `scripts/` — автоматизация.
- `examples/` — эталонные примеры.

## Mandatory Session Workflow

### Step 1 — Restore context
Всегда начинать с чтения `PROGRESS.md`, `ROADMAP.md`, `CHANGELOG.md`, `INDEX.md`, `CONTEXT_RESTORE.md`.

### Step 2 — Determine active work unit
Каждая сессия должна иметь один явный work unit.

### Step 3 — Split into sub-tasks
Большая задача разбивается на 3–7 подзадач.

### Step 4 — Update memory
После содержательных изменений обновляется хотя бы один memory-файл.

## Spec-Kit Mapping

### Specify
Что строим и зачем: UC guides в `catalog/guides/` и taxonomy/master table в `catalog/`.

### Plan
Как строим: `skills/`, `patterns/` и agent instructions.

### Tasks
Какие конкретно шаги делаем: `PROGRESS.md` и `backlog/TODO.md`.

### Implement
Что создано фактически: markdown files, scripts, examples и linked wiki pages.

## Quality Rules

- Использовать H2-H4 для LLM readability.
- Предпочитать таблицы для сравнений.
- Каждый UC должен иметь цель, вход, шаги, выход, пример промпта и критерии качества.
- Каждый skill/pattern должен быть переиспользуемым и связанным с UC.
- Каждый существенный инсайт должен попадать в `memory/wiki/` или связанный markdown-файл.

## Refertur.net Priority Layer

Если выбор между абстрактным UC и practically useful UC неочевиден, приоритет получают сценарии, полезные для Refertur.net: research, SEO/content, traffic and conversion, competitor analysis, tourism/regional opportunity research и developer productivity.

## Anti-Patterns

Не делать большие неделимые файлы, не дублировать логику, не создавать файлы без обновления progress/context и не переходить к следующей фазе без фиксации текущей.

## Evolution Rule

`CONSTITUTION.md` — живой документ; лучшие правила работы должны фиксироваться здесь.
