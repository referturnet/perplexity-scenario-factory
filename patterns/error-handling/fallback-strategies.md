# Pattern: Fallback Strategies

## Описание

Паттерн для graceful degradation при неудаче основных операций. Позволяет системе продолжить работу с альтернативным функционалом.

## Проблема

Когда основная операция недоступна:
- API недоступен
- Элемент не найден
- Данные не загрузились
- Сервис временно не работает

Нужно предоставить пользователю альтернативный путь вместо полного отказа.

## Решение

Реализовать цепочку fallback-опций с приоритетом от наиболее предпочтительного к минимально приемлемому.

---

## Реализация

### Базовая структура

```markdown
Функция operation_with_fallback:
    primary_options = [option1, option2, option3]
    fallback_options = [fallback1, fallback2, default]
    
    Попробовать primary_options:
        Если успешно -> вернуть результат
        
    Если все primary failed:
        Попробовать fallback_options по очереди:
            Если успешно -> вернуть результат
            Логировать использование fallback
    
    Если все failed:
        Вернуть graceful default или error
```

### Пример для навигации

```markdown
## Навигация с fallback

Цель: Открыть страницу продукта

Приоритет 1: Прямая ссылка
    Navigate к /product/12345
    Проверить наличие заголовка продукта
    
Приоритет 2: Поиск через навигацию
    Navigate к /products
    Найти продукт через фильтр/поиск
    Click на результат
    
Приоритет 3: Поиск через search
    Navigate к /search
    Ввести название продукта
    Click на первый результат
    
Fallback: Категория + фильтр
    Navigate к категории продукта
    Применить фильтры
    Найти вручную
    
Default: Вернуть ошибку с контекстом
    Логировать все попытки
    Вернуть error с деталями
```

---

## Типы Fallback стратегий

### 1. Alternative Method

```markdown
Использование альтернативного метода достижения цели

Пример:
- Основной: API call
- Fallback: Screen scraping
- Default: Cached data

✅ Разные пути к одной цели
❌ Может быть медленнее
```

### 2. Degraded Functionality

```markdown
Упрощенная версия функционала

Пример:
- Основной: Полные данные с изображениями
- Fallback: Только текстовые данные
- Default: Список названий

✅ Частичный функционал лучше нуля
❌ Пользователь получает меньше
```

### 3. Cached/Static Data

```markdown
Использование сохраненных данных

Пример:
- Основной: Live API data
- Fallback: Cached data (5 min old)
- Default: Static snapshot

✅ Быстро и надежно
❌ Данные могут быть устаревшими
```

### 4. Manual Override

```markdown
Переключение на ручное выполнение

Пример:
- Основной: Auto-fill форма
- Fallback: Частичное заполнение
- Default: Пустая форма + инструкции

✅ Всегда работает
❌ Требует больше времени
```

---

## Best Practices

1. **Приоритизация**: Упорядочить опции от лучшего к худшему
2. **Логирование**: Записывать когда используется fallback
3. **Мониторинг**: Отслеживать частоту использования fallback
4. **Документирование**: Описать каждый уровень fallback
5. **Тестирование**: Проверить все пути включая worst-case

---

## Когда использовать

### ✅ Подходит для:
- Критичных операций, которые должны завершиться
- Систем с нестабильными зависимостями
- Когда есть несколько способов достичь цели
- Production environments

### ❌ Не подходит для:
- Операций где важна точность метода
- Когда fallback создает больше проблем
- Временных/одноразовых скриптов

---

## Граничные случаи

- **Все fallback failed**: Иметь graceful default
- **Fallback медленнее**: Добавить таймауты
- **Inconsistent state**: Проверять состояние после каждого fallback
- **Infinite loops**: Ограничить количество попыток

---

## Связанные паттерны

- `retry-logic.md` - Retry перед fallback
- `wait-strategies.md` - Wait между попытками
- `circuit-breaker.md` - Предотвращение избыточных попыток
- `graceful-degradation.md` - Общая концепция

---

## Примеры использования

### Authentication Fallback

```markdown
1. Try OAuth login
2. Fallback: Username/password
3. Fallback: Email magic link
4. Default: Guest mode
```

### Data Retrieval Fallback

```markdown
1. Try primary database
2. Fallback: Replica database
3. Fallback: Cache
4. Default: Static content
```

### UI Element Fallback

```markdown
1. Try CSS selector (specific)
2. Fallback: XPath
3. Fallback: Text search
4. Default: OCR or manual
```

---

## История изменений

- **2026-05-28**: Создан pattern fallback-strategies.md
