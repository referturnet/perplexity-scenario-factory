# Pattern: Spec-Driven Development for Scenario Factory

**Категория:** patterns  
**Теги:** spec-kit, workflow, governance, scenario-factory  
**Обновлено:** 2026-05-29

## Контекст

GitHub Spec Kit описывает spec-driven development как подход, где спецификации становятся центром AI-assisted workflows.

## Паттерн

Формула работы: `constitution → specification → plan → tasks → implementation → memory update`.

### Mapping to repository

| Stage | Repository artifact | Purpose |
|-------|---------------------|----------|
| Constitution | `CONSTITUTION.md`, `agent-instructions/` | Governing rules |
| Specification | `catalog/guides/UC-*.md`, `catalog/000-master-table.md` | What to build |
| Plan | `skills/`, `patterns/` | How to build |
| Tasks | `PROGRESS.md`, `backlog/TODO.md` | What to do next |
| Implementation | final markdown/scripts/examples | Actual deliverables |
| Memory update | `memory/wiki/`, `CHANGELOG.md` | Compounding context |

## Когда использовать

- Когда каталог растёт сериями, а не единичными файлами.
- Когда несколько агентов или сессий должны продолжать одну систему.
- Когда важно сохранять контекст в markdown и снижать хаос между сессиями.

## Связанные файлы

- `CONSTITUTION.md`
- `agent-instructions/perplexity-space.md`
- `PROGRESS.md`
