# Примеры мини-агентов (Уровень 2)

Данный документ содержит детальные профили мини-агентов с их знаниями, возможностями и сценариями использования.

## Категория: Domain Expert Agents

### MA-001: Team Communication Expert

**Область ответственности:**
- Кластер: L3-001 (SMB Team Chat)
- Кластер: L3-002 (Enterprise Team Communication)

**Экспертные знания приложений:**

| Приложение | Уровень знания | Специализация |
|-----------|----------------|---------------|
| Slack | 98% | Setup, integrations, workflows |
| Microsoft Teams | 95% | Office 365 integration |
| Discord | 90% | Community building |
| Mattermost | 85% | Self-hosted setup |
| Rocket.Chat | 80% | Open source deployment |

**Типичные задачи:**

1. **Первичная настройка команды**
   ```yaml
   Запрос: "Настрой team chat для 15 человек"

   Шаги:
   1. Анализ потребностей:
      - Размер команды: 15
      - Бюджет: Уточнить
      - Интеграции: Уточнить существующие tools

   2. Рекомендация:
      IF budget < $50/мес:
        → Recommend: Slack Free или Discord
      ELSE IF budget < $150/мес:
        → Recommend: Slack Standard
      ELSE:
        → Recommend: Slack Plus или MS Teams

   3. Setup:
      - Создать workspace
      - Настроить channels (#general, #random, #important)
      - Invite team members
      - Setup integrations (Calendar, Drive, etc)
      - Configure notifications
      - Create guidelines document

   4. Training:
      - Provide quick start guide
      - Best practices document
      - Video tutorial links
   ```

2. **Интеграция с другими системами**
   ```yaml
   Запрос: "Подключи Trello к Slack, чтобы видеть обновления"

   Действия:
   - Проверить доступность Trello integration
   - Установить Trello app в Slack
   - Configure webhook/notifications
   - Set up which boards to track
   - Choose notification channels
   - Test integration
   - Document for team
   ```

3. **Оптимизация существующей setup**
   ```yaml
   Запрос: "У нас хаос в Slack, помоги организовать"

   Анализ:
   - Audit current channels (сколько, какие используются)
   - Check notification settings
   - Review integrations
   - Analyze usage patterns

   Рекомендации:
   - Archive inactive channels
   - Rename channels по convention (#proj-, #team-, #fun-)
   - Create channel guidelines
   - Setup Slack workflows для routine tasks
   - Configure do-not-disturb schedules
   - Train team on search and threads
   ```

**Знание паттернов:**

```python
class TeamCommunicationPatterns:
    """
    Паттерны, которые знает агент
    """

    CHANNEL_NAMING_CONVENTIONS = {
        'project': '#proj-project-name',
        'team': '#team-department',
        'topic': '#topic-subject',
        'fun': '#fun-watercooler',
        'temp': '#temp-event-date'
    }

    NOTIFICATION_BEST_PRACTICES = {
        'work_hours': {
            'mentions': 'allow',
            'all_messages': 'notify',
            'keywords': ['urgent', 'asap', '@here']
        },
        'after_hours': {
            'mentions': 'allow',
            'all_messages': 'mute',
            'keywords': ['critical', 'emergency']
        }
    }

    INTEGRATION_RECOMMENDATIONS = {
        'must_have': ['Google Calendar', 'Google Drive/Dropbox'],
        'nice_to_have': ['GitHub', 'Trello/Asana', 'Zoom'],
        'by_role': {
            'developers': ['GitHub', 'Jira', 'monitoring'],
            'marketing': ['Social media', 'Analytics'],
            'sales': ['CRM', 'Calendar']
        }
    }
```

**Метрики успеха:**
- Setup time: <2 часа
- User adoption: >90% в течение недели
- Satisfaction: >4.5/5

---

### MA-015: SMB CRM Setup Expert

**Область ответственности:**
- Кластер: L3-030 (SMB Sales CRM)
- Частично: L3-040 (Customer Support)

**Экспертные знания приложений:**

| Приложение | Уровень знания | Специализация |
|-----------|----------------|---------------|
| HubSpot CRM | 98% | All aspects, от free до Pro |
| Pipedrive | 95% | Visual pipeline, sales focus |
| Zoho CRM | 90% | Configuration, customization |
| Freshsales | 90% | AI features, phone integration |
| Salesforce Essentials | 85% | Migration from bigger Salesforce |

**Специализированные знания:**

1. **Sales Process Design**
   ```yaml
   Понимает типичные sales процессы:

   B2B Services (long cycle):
   Lead → Qualification → Discovery Call →
   Proposal → Negotiation → Closed Won/Lost
   Duration: 30-90 дней

   B2B SaaS (medium cycle):
   Lead → Demo Request → Demo → Trial →
   Proposal → Decision → Closed Won/Lost
   Duration: 14-45 дней

   B2B Products (short cycle):
   Lead → Quote Request → Quote →
   Purchase Order → Closed Won/Lost
   Duration: 7-21 день

   B2C (very short):
   Lead → Interest → Offer → Purchase
   Duration: 0-7 дней
   ```

2. **CRM Configuration**
   ```yaml
   Запрос: "Настрой HubSpot для SaaS стартапа"

   Discovery Questions:
   - Размер sales team?
   - Monthly Recurring Revenue target?
   - Average deal size?
   - Sales cycle length?
   - Current tools for sales?
   - Need marketing features?

   Based on answers, configures:

   Deal Stages:
   - Lead (new contact)
   - Qualified (MQL → SQL)
   - Demo Scheduled
   - Demo Completed
   - Trial Started
   - Proposal Sent
   - Negotiation
   - Closed Won / Closed Lost

   Properties to track:
   - Company size (employees)
   - Industry
   - Budget range
   - Decision maker
   - Timeline
   - Lead source
   - Pain points

   Automation:
   - Auto-assign leads (round robin)
   - Task creation (follow-up reminders)
   - Email sequences for each stage
   - Deal probability by stage
   - Notifications for stage changes

   Reports:
   - Sales pipeline overview
   - Conversion rates by stage
   - Average deal size
   - Sales cycle length
   - Win/loss analysis
   - Rep performance
   ```

3. **Data Migration**
   ```yaml
   Запрос: "Перенеси данные из Excel в Pipedrive"

   Process:
   1. Data Audit:
      - Review Excel structure
      - Identify: Contacts, Companies, Deals
      - Check data quality (duplicates, formatting)
      - Determine required cleanup

   2. Data Preparation:
      - Clean duplicates
      - Standardize formats (phone, email)
      - Map Excel columns → CRM fields
      - Create custom fields if needed

   3. Import:
      - Start with Companies
      - Then Contacts (link to companies)
      - Then Deals (link to contacts)
      - Import notes/history if available

   4. Validation:
      - Check record counts
      - Verify relationships
      - Test data integrity
      - Sample check 10% of records

   5. Training:
      - Show team where data is
      - Explain new structure
      - Provide import summary
   ```

**Типичные сценарии:**

**Сценарий 1: Компания переходит с Google Sheets на CRM**

```
Пользователь: "Мы сейчас ведем продажи в Google Sheets, хотим CRM"

Агент:
1. Discovery:
   - "Сколько сейчас лидов обрабатываете в месяц?"
   - "Сколько людей в sales team?"
   - "Какая средняя стоимость сделки?"
   - "Используете email для коммуникации? Какой?"

2. Answers example:
   - 50-100 лидов/месяц
   - 3 sales people
   - $2000 average deal
   - Gmail

3. Recommendation:
   "Рекомендую HubSpot CRM Free tier потому что:
   - Бесплатный до 1M contacts
   - Отличная интеграция с Gmail
   - Достаточно функционала для начала
   - Легко масштабируется когда вырастете"

4. Implementation Plan:
   Week 1:
   - Setup HubSpot account
   - Import existing data from Sheets
   - Configure pipeline stages
   - Connect Gmail

   Week 2:
   - Train sales team (2-hour session)
   - Parallel running (Sheets + HubSpot)

   Week 3:
   - Full migration to HubSpot
   - Disable Sheets for sales

   Week 4:
   - Review and optimize
   - Setup reports
   - Adjust based on feedback

5. Execution:
   - Does the technical setup
   - Provides training materials
   - Monitors adoption
   - Tweaks based on usage
```

**Сценарий 2: CRM работает плохо, нужна оптимизация**

```
Пользователь: "CRM есть, но никто не пользуется"

Агент:
1. Diagnosis:
   - Login to CRM, analyze:
     * Pipeline health (deals moving?)
     * Activity levels (emails, calls logged?)
     * User logins (daily active users?)
     * Data quality (empty fields, old data?)

   - Interview team:
     * "Почему не используете?"
     * "Что мешает?"
     * "Что бы помогло?"

2. Common Issues Found:
   - Too complicated (90 custom fields!)
   - Slow/laggy
   - Duplicate data entry (CRM + Sheets)
   - No training
   - No enforcement from leadership

3. Action Plan:
   - Simplify: Remove 70 unnecessary fields
   - Integration: Connect email (auto-log)
   - Automation: Auto-populate data where possible
   - Training: Quick 15-min sessions
   - Accountability: Weekly pipeline reviews

4. Implementation:
   - Execute technical fixes
   - Create "CRM Quick Start" video
   - Set up success metrics dashboard
   - Weekly check-ins for 4 weeks
```

**Best Practices агента:**

```yaml
CRM_BEST_PRACTICES:
  data_quality:
    - "Clean data > More data"
    - "Require minimum fields only"
    - "Auto-populate whenever possible"
    - "Regular deduplication"

  adoption:
    - "Make it easier than old way"
    - "Show value quickly (reports)"
    - "Train in small chunks"
    - "Leadership must use it"
    - "Celebrate wins from CRM data"

  pipeline:
    - "5-7 stages maximum"
    - "Clear definition per stage"
    - "Required actions per stage"
    - "Probability % per stage"
    - "Regular pipeline review meetings"

  automation:
    - "Start simple"
    - "Automate the annoying stuff first"
    - "Don't over-automate (keep human touch)"
    - "Document all automations"
```

**Метрики успеха:**
- CRM setup: <1 день
- Data migration: <3 дня (зависит от объема)
- User adoption: >80% в течение 2 недель
- Data quality: >90% complete key fields

---

### MA-025: SMB Email Marketing Expert

**Область ответственности:**
- Кластер: L3-050 (SMB Email Marketing)
- Кластер: L3-055 (E-commerce Email Marketing)

**Экспертные знания приложений:**

| Приложение | Уровень знания | Специализация |
|-----------|----------------|---------------|
| Mailchimp | 98% | All features, automation |
| ConvertKit | 95% | Creator economy, sequences |
| ActiveCampaign | 95% | Complex automations |
| Klaviyo | 92% | E-commerce, segmentation |
| Sendinblue | 90% | Multi-channel |

**Специальные знания:**

1. **Email Deliverability**
   ```yaml
   Понимает:
   - SPF, DKIM, DMARC records
   - IP warming strategies
   - Spam trigger words/patterns
   - List hygiene best practices
   - ISP reputation factors

   Can diagnose and fix:
   - Low open rates (<15%)
   - Spam folder delivery
   - Blacklist issues
   - Domain reputation problems
   ```

2. **Automation Workflows**
   ```yaml
   Знает 20+ готовых workflows:

   Welcome Series:
   - Email 1 (Day 0): Welcome, set expectations
   - Email 2 (Day 2): Value proposition, story
   - Email 3 (Day 5): Social proof, testimonials
   - Email 4 (Day 7): First offer/CTA

   Abandoned Cart (E-commerce):
   - Email 1 (1 hour): "Forgot something?"
   - Email 2 (24 hours): Add urgency, testimonial
   - Email 3 (48 hours): Discount offer

   Re-engagement:
   - Trigger: No open in 60 days
   - Email 1: "We miss you" + value reminder
   - Email 2 (7 days): Special offer
   - Action: If no open → Unsubscribe or tag

   Post-Purchase:
   - Email 1 (Day 1): Thank you, what's next
   - Email 2 (Day 7): How-to, tips
   - Email 3 (Day 30): Review request, upsell
   ```

3. **Segmentation Strategies**
   ```yaml
   Demographic:
   - Location
   - Age/gender (if available)
   - Company size (B2B)
   - Industry (B2B)

   Behavioral:
   - Engagement level (opens, clicks)
   - Purchase history
   - Website behavior
   - Product interests
   - Lifecycle stage (lead/customer/churned)

   Psychographic:
   - Interests
   - Pain points
   - Goals
   ```

**Типичные задачи:**

**Задача 1: Первая email кампания**

```
Запрос: "Никогда не делали email маркетинг, с чего начать?"

Агент действия:

1. Assess Current State:
   - "У вас есть список email адресов?"
   - "Если да, как собирали? (важно для compliance)"
   - "Какая цель кампании?"
   - "Какой продукт/сервис?"

2. Setup (assuming starting from scratch):

   Step 1: Choose Platform
   - Recommend: Mailchimp Free (до 500 contacts)
   - Reason: Простота, хороший free tier

   Step 2: Technical Setup
   - Create account
   - Authenticate domain (SPF, DKIM)
   - Create signup form
   - Add form to website
   - Setup double opt-in (best practice)

   Step 3: First Campaign
   - Create first email template
   - Write compelling subject line
   - Include clear CTA
   - Mobile-optimized
   - Plain text version

   Step 4: List Building
   - Add signup form to website
   - Create lead magnet (ebook, checklist)
   - Social media promotion
   - Goal: 100+ subscribers before first send

3. First Send Guidelines:
   - Segment: Start with engaged users
   - Time: Tuesday-Thursday, 10am-2pm
   - Test: A/B test subject lines
   - Monitor: Open rate, click rate, unsubscribes

4. Provide Training:
   - Email marketing 101 document
   - Compliance guide (CAN-SPAM, GDPR)
   - Subject line formulas
   - Content templates
```

**Задача 2: Низкие open rates - диагностика**

```
Запрос: "Open rate упал с 25% до 10%, что делать?"

Агент диагностика:

1. Data Analysis:
   - Timeline: Когда началось падение?
   - Segments: Все segments или конкретные?
   - Device: Desktop vs mobile?
   - Email client: Gmail, Outlook, etc?

2. Common Causes Check:

   a) List Quality:
      - Купили список? (плохо!)
      - Много неактивных emails?
      - Bounces увеличились?
      → Solution: List cleaning

   b) Subject Lines:
      - Стали слишком "salesy"?
      - Spam trigger words?
      - Emoji overload?
      → Solution: A/B test different approach

   c) Sending Frequency:
      - Отправляете слишком часто?
      - Или наоборот, редко?
      → Solution: Optimize frequency

   d) Sender Reputation:
      - Check: MXToolbox blacklist
      - Check: Gmail Postmaster Tools
      - Check: Complaint rate
      → Solution: Warm up, clean list

   e) Content Relevance:
      - То же самое всем?
      - Релевантно ли audience?
      → Solution: Better segmentation

3. Action Plan:
   Priority 1 (Do now):
   - Clean list (remove hard bounces)
   - Check blacklists
   - Implement re-engagement campaign

   Priority 2 (This week):
   - A/B test subject lines
   - Segment by engagement
   - Review send frequency

   Priority 3 (This month):
   - Improve signup quality
   - Better onboarding flow
   - Content refresh

4. Monitoring:
   - Daily: Open rates, bounces
   - Weekly: Segment performance
   - Monthly: List growth quality
```

**Задача 3: E-commerce abandoned cart setup**

```
Запрос: "У нас Shopify магазин, настрой abandoned cart emails"

Агент:

1. Platform Choice:
   - Shopify → Recommend Klaviyo
   - Reason: Best Shopify integration, powerful

2. Technical Setup:
   - Install Klaviyo app
   - Connect Shopify store
   - Sync historical data
   - Test data flow

3. Abandoned Cart Flow:

   Email 1 (1 hour after abandonment):
   ---
   Subject: "Still interested in [Product]?"

   Content:
   - Friendly reminder
   - Product image
   - "Complete your order" CTA
   - No discount yet

   Email 2 (24 hours):
   ---
   Subject: "[Name], your cart expires soon!"

   Content:
   - Urgency ("expires in 24h")
   - Product benefits
   - Customer testimonials
   - "Buy now" CTA

   Email 3 (48 hours):
   ---
   Subject: "10% off your cart - expires tonight!"

   Content:
   - Discount code: CART10
   - Scarcity ("last chance")
   - FAQ (shipping, returns)
   - "Claim discount" CTA

4. Optimization:
   - A/B test: Discount timing
   - A/B test: Subject lines
   - Monitor: Recovery rate (target: 10-15%)
   - Adjust: Based on cart value (bigger discount for bigger carts?)

5. Expected Results:
   - Recovery rate: 10-15% of abandoned carts
   - ROI: 10-40x (very high ROI for this flow)
   - Revenue: If 100 carts/week at $50 average
     → Recover 10-15 = $500-750/week extra revenue
```

**Email Marketing Formulas агента:**

```yaml
SUBJECT_LINE_FORMULAS:
  curiosity:
    - "You won't believe what happened..."
    - "The secret to [desired outcome]"
    - "Why [surprising fact]"

  benefit:
    - "[Benefit] in [timeframe]"
    - "Get [result] without [pain point]"
    - "How to [achieve goal]"

  urgency:
    - "Last chance: [offer] expires [time]"
    - "Only [number] left!"
    - "[Time]-hour flash sale"

  personalization:
    - "[Name], special offer inside"
    - "[Name], you left something behind"
    - "Recommended for you, [Name]"

CONTENT_STRUCTURES:
  problem_agitate_solve:
    - Identify problem
    - Agitate pain
    - Present solution (your product)
    - CTA

  story_based:
    - Personal story/anecdote
    - Lesson learned
    - How it applies to reader
    - CTA

  value_first:
    - Useful tip/insight
    - More value
    - "Want more? Click here"
    - CTA

BEST_SEND_TIMES:
  b2b:
    - Tuesday-Thursday
    - 10am-11am or 2pm-3pm
    - Avoid: Monday morning, Friday afternoon

  b2c:
    - Weekend mornings (8-10am)
    - Tuesday-Wednesday evenings
    - Varies by industry

FREQUENCY_GUIDELINES:
  newsletter: "1x/week"
  promotional: "2-3x/week max"
  transactional: "as needed"
  abandoned_cart: "3 emails over 72 hours"
  welcome_series: "4-5 emails over 7-14 days"
```

**Метрики успеха:**
- Setup time: <4 hours для базовой кампании
- Open rate: >20% (industry average)
- Click rate: >2.5%
- Unsubscribe rate: <0.5%
- ROI: >$30 per $1 spent (email marketing average)

---

## Категория: Process Automation Agents

### MA-100: Invoice Processing Agent

**Область ответственности:**
- Автоматизация процесса выставления счетов
- Кластеры: L3-070 (Accounting), L3-075 (Payments)

**Что автоматизирует:**

```yaml
Manual Process (Before):
1. Client asks for invoice
2. Find template
3. Fill in details (manually)
4. Calculate totals
5. Send email
6. Track payment status
7. Send reminders
8. Mark as paid
Time: 15-20 минут per invoice

Automated Process (After):
1. Trigger: Project marked complete OR end of month
2. Auto-generate invoice from project data
3. Auto-send to client
4. Auto-track payment
5. Auto-send reminders (if unpaid)
6. Auto-mark as paid when payment received
Time: 0 минут (fully automated)
```

**Integration Setup:**

```
Project Management Tool (Asana/Trello)
    ↓ when project = complete
Accounting Software (QuickBooks/Xero)
    ↓ generate invoice
Email (Gmail)
    ↓ send to client
Payment Processor (Stripe/PayPal)
    ↓ payment link
Webhook back to Accounting
    ↓ mark as paid
Notification to team (Slack)
```

**Typical Setup:**

```
Client: "Автоматизируй создание счетов"

Agent:
1. Current Process Audit:
   - How many invoices/month?
   - What info needed on invoice?
   - How track projects? (Asana, Excel, etc)
   - Current accounting software?
   - How clients pay? (bank transfer, card, etc)

2. Example Setup (Asana + QuickBooks + Stripe):

   Trigger 1: Project completed in Asana
   ↓
   Action: Create draft invoice in QuickBooks
   - Pull project name, hours, rate
   - Calculate total
   - Add standard terms

   Trigger 2: Invoice approved (or auto-approve if <$X)
   ↓
   Action: Send invoice email
   - Professional email template
   - PDF invoice attached
   - Stripe payment link
   - Due date reminder

   Trigger 3: Payment received in Stripe
   ↓
   Action: Mark invoice paid in QuickBooks
   - Reconcile transaction
   - Send thank you email
   - Notify team in Slack

   Trigger 4: Invoice overdue (due date + 3 days)
   ↓
   Action: Send reminder email
   - Polite reminder
   - Copy of invoice
   - Payment link
   - Repeat every 7 days

3. Testing:
   - Run test invoice through entire flow
   - Verify all data correctly populated
   - Check emails look professional
   - Confirm payment process works

4. Documentation:
   - Process flow diagram
   - How to handle exceptions
   - How to customize templates
   - Monthly report of invoices sent/paid

Results:
- Time saved: 15 mins × invoices/month
- If 50 invoices/month = 12.5 hours saved
- Faster payment (payment link in email)
- Fewer missed invoices
- Better cash flow tracking
```

---

### MA-105: Onboarding Automation Agent

**Область ответственности:**
- Автоматизация employee или customer onboarding
- Кластеры: L3-090 (Project Management), L3-001 (Communication)

**Employee Onboarding автоматизация:**

```yaml
Manual Process:
Day -7: Send offer letter
Day -1: IT setup (accounts, laptop)
Day 1: Welcome, paperwork, tour
Week 1: Training sessions, meet team
Week 2: First projects
Month 1: Check-in, feedback
Time investment: 20-30 hours HR time

Automated Process:
Day -7: Auto-send offer letter (DocuSign)
Day -3: Auto-create accounts (Google, Slack, etc via Okta)
Day -1: Auto-send welcome packet, agenda
Day 1: Auto-assign onboarding tasks (in Asana)
Week 1: Auto-schedule meetings, send training materials
Week 2: Auto-assign first project, introduce to team (Slack)
Month 1: Auto-schedule check-in, survey
Time investment: 2-3 hours HR time (monitoring)
```

**Customer Onboarding (SaaS) автоматизация:**

```yaml
Trigger: New customer signed up

Day 0 (Immediate):
- Send welcome email
- Account setup guide
- Schedule onboarding call (Calendly link)
- Assign customer success manager

Day 1:
- Check: Did they log in?
  YES → Send "Getting started" email
  NO → Send "Need help?" email

Day 3:
- Check: Did they complete key action?
  YES → Send "Advanced features" email
  NO → Send tips + offer help call

Day 7:
- Trigger check-in email from CSM
- Usage report (what they've done)
- Ask: "Any questions?"

Day 14:
- Check engagement level:
  High → Send case study, encourage expansion
  Medium → Send tips, webinar invite
  Low → CSM outreach (at-risk)

Day 30:
- Satisfaction survey
- Feature request form
- Based on feedback → segment for future communications

Throughout:
- In-app messages based on behavior
- Email tips series
- Auto-assign tasks to CSM based on signals
```

---

## Координация между агентами

### Example: Full Marketing Campaign Setup

```
User Request: "Запусти маркетинговую кампанию для нового продукта"

Level 1 (AI) - Orchestrator:
Декомпозирует на задачи:
1. Landing page
2. Email marketing
3. Paid ads
4. Social media
5. Analytics
6. CRM для лидов

Assigns to agents:

MA-080 (Landing Page Expert):
- Create landing page in Webflow
- Setup form capture
- Optimize for conversion
- Connect to email tool

MA-025 (Email Marketing Expert):
- Setup welcome series
- Configure segmentation
- Create nurture campaign
- Connect to CRM

MA-090 (Paid Ads Expert):
- Setup Google Ads campaign
- Setup Facebook Ads
- Connect to landing page
- Setup conversion tracking

MA-095 (Social Media Expert):
- Create content calendar
- Schedule posts
- Setup monitoring
- Engage with audience

MA-110 (Analytics Expert):
- Setup Google Analytics
- Create dashboard
- Setup conversion goals
- Connect all sources

MA-015 (CRM Expert):
- Setup lead pipeline in HubSpot
- Connect form submissions
- Configure lead scoring
- Setup follow-up workflows

Coordination:
All agents report back to Level 1
Level 1 synthesizes into:
"Campaign is live! Here's your dashboard: [link]"
```

---

## Статистика

**Domain Expert Agents:** 100-150
- Communication: 5-8
- CRM: 8-12
- Marketing: 15-20
- Finance: 8-10
- Project Management: 10-12
- Development: 15-20
- HR: 8-10
- Sales: 10-12
- Analytics: 5-8
- E-commerce: 10-15

**Process Automation Agents:** 50-80
**Integration Specialists:** 30-50
**Troubleshooting Agents:** 20-30

**Total: ~200-310 мини-агентов**

---

*Версия: 1.0*
*Дата: 2026-01-28*
*Статус: Примеры созданы, требуется расширение*
