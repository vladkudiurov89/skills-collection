# Claude Skills Collection

Личная коллекция скиллов для Claude Code, отложенных на будущее — сюда
складываются интересные находки, чтобы не потерять и не устанавливать сразу
всё подряд.

## Что внутри

### [ui-ux-pro-max-skill](ui-ux-pro-max-skill/)

AI-скилл с "дизайнерским интеллектом" для UI/UX. Не просто просит модель
угадать цвета/шрифты — прогоняет запрос через движок правил:

- 192 категории продуктов (включая **Finance: Fintech/Crypto, Banking,
  Personal Finance Tracker** — подходит для дашбордов трейдинг-приложений)
- 79 стилей UI, 192 цветовые палитры, 74 сочетания шрифтов, 34 паттерна
  лендингов
- 25 рекомендаций по типам графиков для дашбордов/аналитики
- Чек-лист перед сдачей: контраст текста, `prefers-reduced-motion`,
  адаптивность на 375/768/1024/1440px

Источник: https://github.com/nextlevelbuilder/ui-ux-pro-max-skill

**Когда пригодится:** вёрстка UI для trading_app (есть отдельная категория
Fintech + рекомендации по дашбордам/графикам), любые лендинги/интерфейсы.
Для печатных PDF/Excel-отчётов не подходит — там лучше встроенный skill
`dataviz`.

### [aeo-geo-skill](aeo-geo-skill/)

AEO/GEO (Answer Engine Optimization / Generative Engine Optimization) —
оптимизация контента, чтобы его цитировали ИИ-поисковики (ChatGPT,
Perplexity, Google AI Overviews, Gemini) с указанием бренда, а не просто
вытаскивали факт без атрибуции ("Ghost Citation").

Инструменты внутри (чистый Python stdlib, без внешних зависимостей):

- `scripts/aeo_audit.py` — аудит markdown-статьи на готовность к цитированию
- `scripts/aeo_optimizer.py` — переписывает статью: заголовок, Schema.org
  JSON-LD, цитаты, alt-тексты, привязка фактов к бренду
- `scripts/llms_txt_generator.py` — генерация/валидация `llms.txt`
- `scripts/query_researcher.py` — поиск реальных формулировок запросов,
  вызывающих цитирование
- `scripts/citation_tracker.py` — учёт цитирований по 4 состояниям
  (both/ghost/mention/neither)
- `scripts/report_generator.py` — матрица Keep/Fix/Remove/Add для рефреша
  контента

Источник: https://github.com/Asmadey/aeo-geo-skill

**Когда пригодится:** если появится публичный контент/блог/маркетинговые
страницы, важные для видимости в ИИ-поисковиках. Для текущих
инфраструктурных/бэкенд-проектов прямого применения нет.

---

## Установленные скиллы (уже стоят в Claude Code на этой машине)

Эти пять реально подключены и работают у меня в Claude Code. Здесь лежат
для бэкапа/справки — если понадобится переустановить на другой машине.

### [agent-skills-mcp](agent-skills-mcp/)

MCP-сервер — официальный каталог скиллов Tech Leads Club (включая
`pr-review`: ревью PR с привязкой к Jira/Linear-тикетам по номеру в ветке,
поддержка GitLab/Bitbucket). Progressive disclosure: сначала ищет по
каталогу, потом подгружает только нужный `SKILL.md` и валидированные
referenced-файлы — не грузит контекст всем каталогом сразу.

Установка: `claude plugin marketplace add tech-leads-club/agent-skills` →
`claude plugin install agent-skills-mcp@tech-leads-club`
Источник: https://github.com/tech-leads-club/agent-skills

### [kanban](kanban/)

Плагин с несколькими скиллами: `kanban-jira-agent` (канбан-задачи,
локальный `kanban.json` или Jira Cloud как бэкенд — заменяет голый
`mcp-atlassian`/`jira-mcp`), плюс `notify` (push через Pushover) и `memory`
(RAG-память между сессиями, помечено как stub на момент установки).

Установка: `claude plugin marketplace add kirinchen/claude-workbench` →
`claude plugin install kanban@claude-workbench`
Источник: https://github.com/kirinchen/claude-workbench

### [planning-with-files](planning-with-files/)

Персистентное файловое планирование для долгих задач: план переживает
`/clear`, компакцию контекста и краш сессии — автоматическое
восстановление читает только локальные файлы проекта, без сети.

Установка: `claude plugin marketplace add OthmanAdi/planning-with-files` →
`claude plugin install planning-with-files@planning-with-files`
Источник: https://github.com/OthmanAdi/planning-with-files

### [graphify](graphify/)

Превращает кодовую базу (код + доки + SQL-схемы + конфиги) в queryable
knowledge graph через детерминированный AST-парсинг (без векторной БД).
Вызывается командой `/graphify .` внутри Claude Code.

Установка: `uv tool install graphifyy` → `graphify install --platform claude`
Источник: https://github.com/Graphify-Labs/graphify

### skillspector (не вендорится — это CLI-инструмент, не папка со SKILL.md)

Сканер безопасности для AI-скиллов/MCP: ищет уязвимости, вредоносные
паттерны, prompt injection и supply-chain риски **до** установки стороннего
скилла/сервера.

Установка: `uv tool install --force 'skillspector[mcp] @ git+https://github.com/NVIDIA/skillspector.git'`
Использование: `skillspector scan ./путь-к-скиллу --no-llm`
Источник: https://github.com/NVIDIA/SkillSpector

## Как установить скилл из этой коллекции в Claude Code

Скопировать нужную папку в `~/.claude/skills/<name>/` (глобально) или
`.claude/skills/<name>/` (для конкретного проекта) — Claude Code
автоматически обнаружит `SKILL.md` внутри. Либо смотри инструкцию по
установке в README самого скилла (`ui-ux-pro-max-skill/README.md`,
`aeo-geo-skill/README.md` — там есть npm/pip-пакеты).
