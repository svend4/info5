# FAQ - Frequently Asked Questions

Ответы на часто задаваемые вопросы о проекте INFO5.

## Общие вопросы

### Что такое INFO5?

**INFO5** - это методология и архитектура для автоматизации рутинной офисной работы через четырехуровневую пирамиду, которая соединяет искусственный интеллект с тысячами бизнес-приложений через специализированных мини-агентов и организованные кластеры.

Подробнее: [Quick Start](/docs/QUICK_START.md)

### Почему называется INFO5?

**INFO** = Information (работа с информацией)
**5** = 5 компонентов системы:
1. Пользователь
2. AI (Уровень 1)
3. Мини-агенты (Уровень 2)
4. Кластеры (Уровень 3)
5. Приложения (Уровень 4)

### Кто создал INFO5?

Методология разработана в январе 2026 года для решения проблемы разрыва между мощными AI-системами и тысячами разрозненных бизнес-приложений.

### Это уже работает?

**Статус (Январь 2026):**
- ✅ Методология: Завершена
- ✅ Документация: Готова
- 🔄 Прототипы агентов: В разработке
- 📅 Pilot: Q2 2026
- 📅 Beta: Q4 2026
- 📅 Public Launch: Q1 2027

См. [Roadmap](/docs/ROADMAP.md)

---

## Для пользователей

### Кому это нужно?

**Идеально для:**
- 🎯 Стартапы (нужна быстрая настройка инфраструктуры)
- 🎯 SMB (ограничены временем и ресурсами)
- 🎯 Фрилансеры (нужна автоматизация без команды)
- 🎯 Агентства (много повторяющихся операций)
- 🎯 Корпоративные команды (хотят масштабироваться)

**Не подходит для:**
- ❌ Крупные enterprise с legacy системами (пока)
- ❌ Высоко regulated отрасли (пока нет compliance)
- ❌ Те кто предпочитает ручной контроль всего

### Сколько времени я сэкономлю?

**Типичная экономия:**
- Стартап setup: **2 недели → 3 часа** (97% экономия)
- Еженедельная рутина: **20-30 часов → 5-10 часов** (60-75% экономия)
- Настройка нового tool: **2-4 часа → 10 минут** (95% экономия)

**В среднем: 60-80% времени на рутинных задачах**

### Сколько это будет стоить?

**Планируемые цены (Q1 2027):**

| Tier | Цена | Что включено |
|------|------|--------------|
| **Free** | $0 | 3 мини-агента, 50 tasks/месяц |
| **Starter** | $49/мес | 10 агентов, 500 tasks/месяц |
| **Professional** | $199/мес | Unlimited агенты, 5K tasks/месяц |
| **Enterprise** | Custom | Все + dedicated support |

**Pilot & Beta: Бесплатно для участников**

### Безопасны ли мои данные?

**Безопасность:**
- 🔒 Данные зашифрованы (in transit & at rest)
- 🔒 OAuth 2.0 для подключений
- 🔒 Никогда не храним пароли
- 🔒 GDPR compliant (будет)
- 🔒 SOC2 certification (в планах для Enterprise)

**Что мы видим:**
- Metadata (какие apps используете)
- Anonymous usage analytics
- Performance metrics

**Что НЕ видим:**
- Ваши клиентские данные
- Контент ваших emails
- Финансовые транзакции

### Могу ли я контролировать что делает AI?

**Да! Несколько уровней контроля:**

1. **Preview mode:** Видите план до выполнения
2. **Approval gates:** Критичные действия требуют подтверждения
3. **Audit log:** Полная история всех действий
4. **Rollback:** Можно откатить изменения
5. **Manual override:** Всегда можете взять управление

**Философия: AI помогает, вы контролируете**

### Что если AI ошибется?

**Защита от ошибок:**

1. **Human-in-the-loop:** Критичные операции требуют одобрения
   - Финансовые транзакции
   - Удаление данных
   - Изменение security settings

2. **Sandbox mode:** Тестирование без последствий

3. **Automatic backups:** Данные сохраняются перед изменениями

4. **Fallback options:** Всегда есть manual way

5. **Support team:** Помощь в решении проблем

**Success rate: >90% (цель)**

### Заменит ли это мою работу?

**Нет! INFO5 заменяет рутину, не работу.**

**Освобождает время для:**
- ✅ Стратегическое мышление
- ✅ Креативная работа
- ✅ Общение с клиентами
- ✅ Развитие бизнеса
- ✅ Обучение и рост

**Автоматизирует:**
- 🤖 Настройка инструментов
- 🤖 Data entry
- 🤖 Рутинные интеграции
- 🤖 Repetitive tasks
- 🤖 Мониторинг и отчеты

**Аналогия:** Excel не заменил бухгалтеров, но сделал их работу эффективнее и интереснее.

---

## Технические вопросы

### Какие технологии используются?

**Stack:**
- **Level 1 (AI):** GPT-4, Claude 3.5 Sonnet
- **Level 2 (Agents):** LangChain, CrewAI, Python
- **Level 3 (Clusters):** PostgreSQL, Elasticsearch
- **Level 4 (Apps):** Make.com SDK, REST APIs, OAuth
- **Infrastructure:** AWS/GCP, Kubernetes

### С какими приложениями работает?

**На запуске (Q1 2027):**
- Top 100 популярных apps (direct integration)
- 2000+ apps через Make.com
- 7000+ apps через Zapier (fallback)

**Категории:**
- CRM (HubSpot, Salesforce, Pipedrive...)
- Email marketing (Mailchimp, Klaviyo...)
- Project management (Asana, Trello, Monday...)
- Accounting (QuickBooks, Xero...)
- E-commerce (Shopify, WooCommerce...)
- И многие другие

**К 2028: 10,000+ приложений**

### Нужны ли технические знания?

**Нет!** Это основная идея.

**Что НЕ нужно знать:**
- ❌ Программирование
- ❌ API и webhooks
- ❌ Database design
- ❌ Complex workflows

**Что нужно:**
- ✅ Сформулировать что хотите ("Setup CRM")
- ✅ Ответить на уточняющие вопросы
- ✅ Проверить результат

**Target audience: Non-technical business users**

### Можно ли кастомизировать?

**Да, несколько уровней:**

**Level 1: Basic (No-code)**
- Выбор из рекомендованных apps
- Настройка базовых параметров
- Включение/выключение автоматизаций

**Level 2: Advanced (Low-code)**
- Кастомизация workflows
- Создание custom rules
- Настройка triggers и actions

**Level 3: Expert (Code)**
- Custom agents
- API access
- Webhooks
- Advanced integrations

**Professional tier и выше: Полная кастомизация**

### Как обрабатываются API limits?

**Стратегии:**

1. **Rate limiting:** Автоматическое соблюдение limits
2. **Batching:** Группировка запросов когда возможно
3. **Caching:** Переиспользование данных
4. **Queueing:** Отложенное выполнение при превышении
5. **Notifications:** Предупреждение при приближении к limit

**В большинстве случаев вы не заметите ограничений**

### Работает ли offline?

**Нет, требуется интернет:**
- AI models в облаке
- Приложения в облаке
- Интеграции требуют connectivity

**Но:**
- Dashboard кэшируется (читать offline)
- Mobile app sync когда доступен интернет
- Offline mode planned для некоторых функций

---

## Бизнес вопросы

### Какой ROI ожидать?

**Типичный ROI в первые 3 месяца:**

**Экономия времени:**
- 50-100 часов/месяц на команду
- × средняя ставка ($50-100/час)
- = $2,500-10,000/месяц value

**Увеличение revenue:**
- Лучшая конверсия (CRM automation)
- Больше повторных покупек (email automation)
- Faster sales cycle (automation)
- Типично: +10-30% revenue impact

**Стоимость:**
- INFO5: $49-199/месяц
- **ROI: 20-50x в первые 3 месяца**

### Как долго до результатов?

**Timeline:**

| Milestone | Time | Value |
|-----------|------|-------|
| First automation | Day 1 | Quick win |
| Core processes automated | Week 1 | Noticeable relief |
| Full stack running | Week 2-3 | Dramatic change |
| Team adopted | Month 1 | Full value |
| Optimized & scaled | Month 2-3 | Maximum ROI |

**First value: Within hours**
**Full value: Within 1-2 months**

### Нужно ли менять существующие tools?

**Нет! INFO5 работает с вашим стеком.**

**Сценарии:**

1. **Сохранить все:**
   - INFO5 интегрируется с текущими apps
   - Добавляет intelligence layer сверху

2. **Optimize стек:**
   - INFO5 может рекомендовать better alternatives
   - Но решение всегда за вами

3. **Start fresh:**
   - INFO5 помогает выбрать optimal стек с нуля

**Философия: Работать с вами, не против вас**

### Можно ли использовать для клиентов?

**Да! Особенно для:**

**Agencies:**
- Автоматизация client onboarding
- Faster project setup
- Consistent delivery
- Scale без найма

**Consultants:**
- Быстрые implementations
- Better client outcomes
- More clients capacity

**Resellers:**
- White-label option (Enterprise tier)
- Partner program planned

**Rev share или partnership: Contact us**

---

## Сравнения

### Чем отличается от Zapier?

**Короткий ответ:**
- Zapier = Инструменты
- INFO5 = Мастер с инструментами

**Детально:**
- Zapier: Вы решаете что соединять → INFO5: AI рекомендует
- Zapier: Ручная настройка → INFO5: Авто-настройка
- Zapier: Integration tool → INFO5: Intelligence + Integration
- INFO5 использует Zapier как один из инструментов!

См. [Полное сравнение](/docs/COMPARISON.md)

### Чем отличается от ChatGPT?

**Короткий ответ:**
- ChatGPT = Советчик
- INFO5 = Советчик + Исполнитель

**Детально:**
- ChatGPT: Дает советы → INFO5: Выполняет
- ChatGPT: General knowledge → INFO5: Specialized expertise
- ChatGPT: Forget between sessions → INFO5: Remembers your setup
- INFO5 использует GPT-4 как "мозг"!

### Чем отличается от AutoGPT?

**Короткий ответ:**
- AutoGPT = Research project
- INFO5 = Production system

**Детально:**
- AutoGPT: Пытается все подряд → INFO5: Знает что работает
- AutoGPT: 30-50% success → INFO5: >90% success
- AutoGPT: Expensive → INFO5: Cost-effective
- AutoGPT: General → INFO5: Specialized per domain

---

## Участие в проекте

### Можно ли попробовать сейчас?

**Pilot Program (Q2 2026):**
- 🎯 Looking for 5-10 pilot users
- ✅ Free access
- ✅ Direct feedback channel
- ✅ Shape the product

**Criteria:**
- SMB or startup
- Willing to provide feedback
- 1-2 hours/week for testing

**Sign up: [Contact via GitHub]**

### Как внести вклад?

**Non-technical:**
- 💡 Suggest use cases
- 💡 Feedback on methodology
- 💡 Spread the word
- 💡 Join pilot program

**Technical:**
- 🔧 Contribute to documentation
- 🔧 Code (when open-sourced)
- 🔧 Build custom agents
- 🔧 Create integrations

**Business:**
- 💼 Partner opportunities
- 💼 Reseller program
- 💼 Investment inquiries

**See: CONTRIBUTING.md (coming soon)**

### Когда будет open source?

**Roadmap:**

- **Core platform:** Proprietary (SaaS)
- **Agent SDK:** Open source (Q3 2026)
- **Templates:** Open source (Q4 2026)
- **Community agents:** Marketplace (2027)

**Philosophy:**
- Platform = closed (reliable service)
- Extensions = open (community innovation)

### Ищете инвестиции?

**Funding status:**
- Phase 0-1: Bootstrap + Angels (~$100K)
- Phase 2-3: Seed round (Q2 2026, $400K target)
- Phase 5: Series A (Q1 2027, $5M target)

**Interested investors: Contact via GitHub**

---

## Troubleshooting

### AI не понимает мой запрос

**Solutions:**

1. **Be more specific:**
   - ❌ "Set up email"
   - ✅ "Set up email marketing for my Shopify store"

2. **Provide context:**
   - Team size
   - Industry
   - Budget
   - Existing tools

3. **Use examples:**
   - "Like how Shopify does X"
   - "Similar to what I saw at company Y"

4. **Break down:**
   - Complex task → Multiple simple tasks

### Automation не работает

**Debugging steps:**

1. **Check connections:**
   - Are apps still connected?
   - Expired OAuth tokens?

2. **Check permissions:**
   - Does INFO5 have necessary scopes?

3. **Check triggers:**
   - Is trigger condition met?
   - Data format correct?

4. **View logs:**
   - Dashboard → Automation → Logs
   - See exact error

5. **Contact support:**
   - In-app chat
   - help@info5.ai (future)

### Интеграция перестала работать

**Common causes:**

1. **API changes:** App updated their API
   - Solution: INFO5 auto-updates usually
   - If not: Report via in-app

2. **Rate limits:** Too many requests
   - Solution: Automatic throttling
   - Upgrade plan if needed

3. **App downtime:** Third-party service down
   - Solution: Automatic retry
   - Notification sent

4. **Credentials expired:** OAuth token expired
   - Solution: Re-authenticate (click notification)

### Хочу отменить действие

**Options:**

1. **Undo button:** Сразу после действия
2. **Rollback:** В dashboard → History
3. **Manual fix:** В самом приложении
4. **Support:** Если не получается

**Prevention: Preview mode (включить в настройках)**

---

## Roadmap Questions

### Когда добавите [feature]?

**Check roadmap:** [ROADMAP.md](/docs/ROADMAP.md)

**Priority определяется:**
1. User votes (feature requests)
2. Business impact
3. Technical feasibility
4. Strategic fit

**Request feature:**
- GitHub Issues
- In-app voting (beta+)
- User interviews

### Какие приложения добавите?

**Priority:**
1. Most requested apps
2. Popular in target segments
3. Good API quality
4. Strategic partnerships

**Request app integration:**
- Vote in dashboard
- Explain use case
- Contribute connector (open source SDK)

### Будет ли поддержка [language]?

**Language support roadmap:**

- **Phase 4 (Q1 2027):** English
- **Phase 5 (Q2-Q4 2027):**
  - Spanish
  - Russian
  - German
  - French
- **2028+:**
  - 10+ languages
  - Community translations

**UI translation:** Earlier
**Agent knowledge:** Takes time per language

---

## Contact & Support

### Как связаться?

**Current (Development):**
- GitHub: [svend4/info5](https://github.com/svend4/info5)
- GitHub Issues: Questions & bug reports

**Future (Launch):**
- Email: help@info5.ai
- Chat: In-app support
- Community: Discord/Forum
- Social: Twitter, LinkedIn

### Где получить помощь?

**Self-service:**
- 📚 [Documentation](/docs/README.md)
- 💡 [Quick Start](/docs/QUICK_START.md)
- 🎯 [Use Cases](/examples/use-cases.md)
- ❓ This FAQ

**Community:**
- GitHub Discussions (coming)
- Discord (coming)
- Forum (coming)

**Direct support:**
- Free tier: Community
- Paid tiers: Email support
- Enterprise: Dedicated success manager

### Нашли bug?

**Report via:**
1. GitHub Issues (preferred)
2. In-app (when available)
3. Email

**Include:**
- What you tried to do
- What happened
- Expected behavior
- Screenshots if possible
- Browser/device info

**Bug bounty program: Coming in beta**

---

## Updates & News

### Как следить за развитием?

**Stay updated:**
- ⭐ Star on GitHub
- 👁️ Watch repository
- 📧 Newsletter (coming)
- 🐦 Twitter (coming)
- 💼 LinkedIn (coming)

### Как часто обновления?

**Development phase (2026):**
- Major updates: Monthly
- Documentation: Weekly
- Blog posts: Bi-weekly

**Post-launch (2027+):**
- Product updates: Weekly
- New agents: Monthly
- Major features: Quarterly

---

## Miscellaneous

### Почему стоит доверять INFO5?

**Transparency:**
- Open methodology
- Public roadmap
- Clear documentation
- Honest about limitations

**Track record:**
- Will be proven through pilot & beta
- Public case studies
- User testimonials

**Philosophy:**
- User-first
- Privacy-conscious
- Ethical AI use
- Long-term thinking

### Что если проект закроется?

**Data ownership:**
- Ваши данные = ваши данные
- Export в любой момент
- Standard formats

**Exit strategy:**
- Advance notice (90 days minimum)
- Data export tools
- Migration assistance
- Possibly open-source code

**Но план: Build for long-term success! 🚀**

---

*Версия: 1.0*
*Последнее обновление: 2026-01-28*
*Не нашли ответа? [Open an issue on GitHub](https://github.com/svend4/info5/issues)*
