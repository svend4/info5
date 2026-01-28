# Contributing to INFO5

Спасибо за интерес к проекту INFO5! Мы приветствуем вклад от сообщества.

## Текущий статус проекта

**Phase 0 - Foundation (Q1 2026)**

Проект находится в стадии разработки методологии и документации. Код появится в Q2 2026.

## Как можно помочь

### 1. 💡 Обратная связь и идеи

**Методология**
- Комментарии к методологиям [Уровня 2](/docs/methodology/level-2-mini-agents.md) и [Уровня 3](/docs/methodology/level-3-clustering.md)
- Предложения по улучшению
- Выявление gaps или противоречий

**Кластеризация**
- Предложения дополнительных кластеров
- Коррекция существующих кластеров
- Добавление приложений в кластеры

**Use Cases**
- Описание ваших сценариев использования
- Практические задачи из реальной работы
- Специфичные для отрасли потребности

**Как предложить:**
- Откройте [GitHub Issue](https://github.com/svend4/info5/issues)
- Template: `[FEEDBACK] Ваша тема`

### 2. 📝 Документация

**Что нужно:**
- Исправление опечаток и грамматики
- Улучшение ясности объяснений
- Добавление примеров
- Перевод на другие языки (планируется)

**Процесс:**
1. Fork репозитория
2. Создайте branch: `docs/your-improvement`
3. Внесите изменения
4. Создайте Pull Request

**Guidelines:**
- Используйте четкий, понятный язык
- Добавляйте примеры где возможно
- Следуйте существующему стилю форматирования
- Проверьте ссылки

### 3. 🔍 Исследование

**Темы для исследования:**
- Анализ дополнительных существующих решений
- Сравнение с новыми конкурентами
- Изучение специфичных для отрасли инструментов
- Технические подходы к реализации

**Формат:**
- Markdown документ в `/docs/research/`
- Структура: Проблема → Исследование → Выводы → Рекомендации

### 4. 🎯 Use Cases и примеры

**Что нужно:**
- Реальные истории использования
- Детальные workflow descriptions
- ROI расчеты
- Before/After сравнения

**Формат:**
```markdown
# Use Case: [Название]

## Контекст
- Компания/роль
- Размер команды
- Текущие проблемы

## Решение через INFO5
- Какие агенты использованы
- Какие кластеры задействованы
- Workflow

## Результаты
- Экономия времени
- ROI
- Другие benefits
```

### 5. 🧪 Pilot Testing (Q2 2026)

**Как стать pilot user:**
1. Откройте issue: `[PILOT] Ваша компания`
2. Опишите:
   - Ваш бизнес (размер, отрасль)
   - Основные проблемы с автоматизацией
   - Готовность давать feedback (1-2 часа/неделю)
   - Желаемые use cases

**Что получите:**
- Бесплатный доступ к pilot версии
- Прямая связь с командой
- Влияние на направление продукта
- Упоминание как early adopter

**Критерии отбора:**
- SMB или startup
- Активное использование SaaS tools
- Готовность к детальному feedback
- 5-50 человек в команде (ideal)

### 6. 💻 Код (Q2 2026+)

**Когда:**
- Code base появится в Q2 2026
- Сначала: Agent SDK (open source)
- Потом: Community contributed agents

**Технологии:**
- Python (agents)
- TypeScript (API)
- React (UI)
- PostgreSQL (data)
- LangChain / CrewAI (frameworks)

**Contribution types:**
- Bug fixes
- New agent implementations
- Integration connectors
- Tests
- Performance improvements

**Process (будет детализирован позже):**
1. Check [issues](https://github.com/svend4/info5/issues) for "good first issue"
2. Comment на issue что берете
3. Fork, branch, code, test
4. PR with description
5. Code review
6. Merge!

## Code of Conduct

### Наши ценности

**Respect (Уважение)**
- Уважайте различные мнения и опыт
- Конструктивная критика welcome
- Личные нападки недопустимы

**Collaboration (Сотрудничество)**
- Работаем вместе к общей цели
- Помогаем друг другу
- Делимся знаниями

**Excellence (Качество)**
- Стремимся к высокому качеству
- Тестируем перед submit
- Документируем наши изменения

**Openness (Открытость)**
- Прозрачность в процессах
- Открытое обсуждение идей
- Feedback приветствуется

### Неприемлемое поведение

❌ Harassment или discrimination
❌ Trolling или оскорбительные комментарии
❌ Personal или political attacks
❌ Публикация private информации других
❌ Spam или irrelevant content

**Последствия:**
1. Предупреждение
2. Временный ban
3. Permanent ban

**Сообщить о нарушении:**
- Email: conduct@info5.ai (future)
- GitHub: Private message to maintainers

## Development Setup (Q2 2026)

*Будет добавлено когда появится code base*

## Pull Request Process

### Перед созданием PR

- [ ] Прочитали CONTRIBUTING.md
- [ ] Issue существует для этого изменения
- [ ] Branch создан из latest main
- [ ] Commits логичные и атомарные
- [ ] Commit messages описательные

### PR Template

```markdown
## Описание
Четкое описание что меняет этот PR

## Мотивация и контекст
Почему это изменение необходимо? Какую проблему решает?

Fixes #(issue_number)

## Тип изменения
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Как тестировалось?
Опишите тесты

## Checklist
- [ ] Мой код следует style guidelines
- [ ] Self-review выполнен
- [ ] Комментарии добавлены где нужно
- [ ] Документация обновлена
- [ ] Нет новых warnings
- [ ] Тесты добавлены/обновлены
- [ ] Все тесты проходят
```

### Review Process

1. **Automated checks:**
   - Linting
   - Tests
   - Build

2. **Code review:**
   - Минимум 1 approver
   - Обсуждение и итерации
   - Changes requested → Update → Re-review

3. **Merge:**
   - Squash merge (обычно)
   - Descriptive merge commit message
   - Delete branch after merge

## Issue Guidelines

### Creating Issues

**Bug Report:**
```markdown
**Describe the bug**
Clear description

**To Reproduce**
Steps to reproduce

**Expected behavior**
What should happen

**Screenshots**
If applicable

**Environment**
- OS:
- Browser:
- Version:

**Additional context**
Any other info
```

**Feature Request:**
```markdown
**Is your feature request related to a problem?**
Description of problem

**Describe the solution you'd like**
Clear description of desired feature

**Describe alternatives considered**
Other solutions you've thought about

**Additional context**
Mockups, examples, etc.
```

**Use Case Submission:**
```markdown
**Use Case Title**

**Context:**
- Company/Role:
- Team size:
- Current problems:

**Desired Solution:**
What you want to automate

**Expected Benefits:**
Time saved, ROI, etc.
```

### Issue Labels

- `good first issue` - Good for newcomers
- `help wanted` - Extra attention needed
- `bug` - Something isn't working
- `enhancement` - New feature or request
- `documentation` - Documentation improvements
- `question` - Further information requested
- `feedback` - Feedback on methodology/approach
- `use-case` - Use case submission
- `pilot` - Pilot program related

## Recognition

### Contributors

Все contributors будут упомянуты в:
- CONTRIBUTORS.md
- Release notes
- Website (when launched)

### Types of Contributions

- 📝 **Documentation** - Improving docs
- 💡 **Ideas** - Valuable feedback and suggestions
- 🐛 **Bug Reports** - Finding issues
- ✨ **Code** - Pull requests
- 🧪 **Testing** - Pilot testing, QA
- 🌍 **Translation** - Localization
- 🎨 **Design** - UI/UX, diagrams
- 📢 **Advocacy** - Spreading the word

## Communication Channels

### GitHub
- **Issues**: Bug reports, features, discussions
- **Pull Requests**: Code contributions
- **Discussions**: General questions (coming)

### Future Channels (Q2 2026+)
- Discord: Real-time chat
- Forum: Long-form discussions
- Newsletter: Updates
- Blog: Deep dives

## Timeline for Contributions

### Q1 2026 (Current)
- ✅ Documentation feedback
- ✅ Use case submissions
- ✅ Methodology suggestions
- ✅ Pilot program sign-up

### Q2 2026
- Code contributions (Agent SDK)
- Pilot testing
- Bug reports
- Feature requests

### Q3-Q4 2026
- Community agents
- Integration connectors
- Translations
- Advanced features

### 2027+
- Full ecosystem contributions
- Marketplace submissions
- Plugin development

## Questions?

- 📧 Check [FAQ](/docs/FAQ.md)
- 💬 Open a [GitHub Issue](https://github.com/svend4/info5/issues)
- 📖 Read [Documentation](/docs/README.md)

## Thank You!

Каждый вклад, большой или маленький, ценится. Вместе мы создаем будущее intelligent automation! 🚀

---

*Версия: 1.0*
*Последнее обновление: 2026-01-28*
