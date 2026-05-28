# CLAUDE.md — Project Instructions for Claude Code

> **Это root-level project instructions для Claude Code. Читается автоматически.**

## Цель проекта

**Perplexity Scenario Factory** — систематизированная библиотека из 200 сценариев использования Perplexity/Comet browser automation + система deep research + проектная память (LLM-Wiki pattern).

## Структура проекта.

```
perplexity-scenario-factory/
├── README.md              # Entry point
├── CONTEXT_RESTORE.md     # 🔥 КАК ВОССТАНОВИТЬ КОНТЕКСТ (для новых чатов)
├── INDEX.md               # 🔥 ЖИВОЙ индекс всех файлов (обновляй ВСЕГДА)
├── STATUS.md              # Текущий статус проекта
├── ROADMAP.md             # Фазы и план
├── CONTEXT_MAP.md         # Карта связей компонентов
├── CLAUDE.md              # Этот файл
├── AGENTS.md              # Universal agent instructions
│
├── memory/                # Karpathy LLM-Wiki pattern
│   ├── INDEX.md
│   ├── wiki/              # LLM-compiled knowledge
│   └── raw/               # Source materials (immutable)
│
├── catalog/               # 200 use cases
│   ├── 000-master-table.md
│   ├── 000-taxonomy.md
│   └── [categories]/
│
├── guides/                # 200 detailed guides
├── deep-research/         # Research system
├── synthesis/             # Scenario synthesis
├── backlog/
│   ├── TODO.md            # 🔥 АКТИВНЫЕ ЗАДАЧИ
│   └── BACKLOG.md
│
├── agent-instructions/    # IDE agent configs
├── skills/                # Reusable agent skills
├── scripts/               # Automation scripts
├── patterns/              # Templates
└── examples/              # Golden examples
```

## Workflow для агента

### 1. При старте сессии
1. Прочитай **CONTEXT_RESTORE.md** — узнай что уже сделано
2. Прочитай **INDEX.md** — узнай какие файлы существуют
3. Прочитай **TODO.md** — узнай активные задачи
4. Прочитай **STATUS.md** — узнай текущий этап

### 2. При создании/изменении файлов
1. **ВСЕГДА обновляй INDEX.md** после создания нового файла
2. Добавляй запись: путь, краткое описание, дата создания
3. Группируй по категориям (root, memory, catalog, guides...)

### 3. При завершении задачи
1. Обнови **TODO.md** — отметь задачу completed
2. Обнови **STATUS.md** — укажи что готово
3. Обнови **CONTEXT_RESTORE.md** — запиши контекст для следующей сессии

## Правила и ограничения

### ✅ Делай
- Создавай файлы последовательно (по layers)
- Обновляй INDEX.md после КАЖДОГО нового файла
- Пиши подробные CONTEXT_RESTORE.md записи
- Следуй структуре из README.md
- Используй markdown для всех документов
- Добавляй ссылки в полном виде: https://github.com/...

### ❌ Не делай
- Не создавай файлы без обновления INDEX.md
- Не меняй структуру папок без согласования
- Не удаляй существующие файлы без причины
- Не пропускай этапы из ROADMAP.md

## Приоритетные файлы (создавать первыми)

1. ✅ README.md (готов)
2. ⏳ CLAUDE.md (этот файл)
3. ⏳ CONTEXT_RESTORE.md
4. ⏳ INDEX.md
5. ⏳ STATUS.md
6. ⏳ ROADMAP.md
7. ⏳ TODO.md
8. ⏳ CONTEXT_MAP.md
9. ⏳ AGENTS.md

## Karpathy LLM-Wiki Pattern

Проект использует паттерн из https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f:

- **memory/raw/** — исходники (immutable, только чтение для LLM)
- **memory/wiki/** — LLM-compiled wiki (агент пишет, человек читает)
- **memory/INDEX.md** — каталог всех страниц wiki
- **CLAUDE.md** / **AGENTS.md** — schema (как работать с wiki)

При добавлении нового источника:
1. Положи в `memory/raw/`
2. Обнови `memory/wiki/` страницы
3. Обнови `memory/INDEX.md`

## Формат INDEX.md

```markdown
# INDEX — Master File Index

Последнее обновление: 2026-05-28 10:00 +06

## Root Files
- `README.md` — Entry point, архитектура (создан 2026-05-28)
- `CLAUDE.md` — Claude Code instructions (создан 2026-05-28)
- ...

## memory/
- `memory/INDEX.md` — Wiki catalog
- `memory/wiki/concepts/automation.md` — ...
...
```

## Самокритика

- Перед каждым действием: проверь что файл нужен по ROADMAP
- После каждого действия: обновил ли INDEX.md?
- Перед завершением: записал ли контекст в CONTEXT_RESTORE.md?

---

**Версия:** 1.0 | **Дата:** 2026-05-28 | **Автор:** referturnet
