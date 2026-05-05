# Agents Week 2026

Репозиторий с материалами интенсива по AI-агентам: лекциями, семинарами, конспектами, ноутбуками и финальным заданием. Курс последовательно проходит путь от базовой идеи LLM-агента до tool calling, памяти, guardrails, multi-agent systems, eval и production engineering.

## Структура репозитория

```text
Agents Week/
├── 01_01_intro_to_ai_agents_llm/                         # Intro to AI Agents & LLM
├── 01_02_tools_and_mcp/                                  # Tools & MCP
├── 02_memory_and_guardrails/                             # Memory and Guardrails
├── 03_agent_workflows_multi_agent_systems_multimodality/ # Workflows, MAS, Multimodality
├── 04_agent_evaluation/                                  # Agent Evaluation
├── 05_production_engineering_for_llm_agents/             # Production Engineering
├── Final_Task/                                           # Финальное задание
└── QA-Session/                                           # Итоговая QA-сессия
```

## Навигация по материалам

| Блок | Тема | Спикер | Материалы | Видео |
|---|---|---|---|---|
| 1.1 | [Intro to AI Agents & LLM](01_01_intro_to_ai_agents_llm/README.md) | Zaytseva Alena, AI Lead @ Yandex Lavka | конспект, презентация, 2 ноутбука | [YouTube](https://www.youtube.com/live/C1OCgbONSAw?si=KRjmoE3Coqq1F-j0), [VK Video](https://vkvideo.ru/video-84793390_456240032?list=ln-GUOayt6zxDB6MbQNVZ) |
| 1.2 | [Tools & MCP](01_02_tools_and_mcp/README.md) | Zaytseva Alena, AI Lead @ Yandex Lavka | конспект, презентация, ноутбук | [YouTube](https://www.youtube.com/live/VctYHtCap3o?si=q6PwW9T3BU1Tk7j9), [VK Video](https://vkvideo.ru/video-84793390_456240033?list=ln-9Z1JBhDTw12ZpFjQqq) |
| 2 | [Memory and Guardrails](02_memory_and_guardrails/README.md) | Kirill Mishchenko, ML Team Lead @ Yandex Browser  | конспект, презентация, семинар, схема архитектуры | Лекция: [YouTube](https://www.youtube.com/live/iJGh5cBSReo?si=gkvAfm82tlNloSs8), [VK Video](https://vkvideo.ru/video-84793390_456240034?list=ln-p3nTstxNqJsFP4Cuth)<br>Семинар: [YouTube](https://www.youtube.com/live/JEFiiM9C_po?si=HHXPBUxPgeIQd77N), [VK Video](https://vkvideo.ru/video-84793390_456240035?list=ln-ocaDFVbgcew2tDQnyt) |
| 3 | [AI Agent Workflow & Multi-Agent Systems](03_agent_workflows_multi_agent_systems_multimodality/README.md) | Sofya Proskurina, AI Agents Platform @ Yandex Lavka | конспект, презентация, семинар | Лекция: [YouTube](https://www.youtube.com/live/_gdXItwkhUE), [VK Video](https://vkvideo.ru/video-84793390_456240036?list=ln-IYzZ1qlFb6T1mxUxcM)<br>Семинар: [YouTube](https://www.youtube.com/live/s4BfSnWwAQE?si=NPOz028B9g6tJ8HY), [VK Video](https://vkvideo.ru/video-84793390_456240037?list=ln-XlND5RpJQu8Kz1IzzZ) |
| 4 | [Agent Evaluation](04_agent_evaluation/Agent.Evaluation_Quality.md) | Sergey Kuptsov, Agent Solutions in Alice & Smart Devices | конспект, презентация, семинар | Лекция: [YouTube](https://www.youtube.com/live/RqM3G3STkGE?si=k7ugiPjZtiFiVzuu), [VK Video](https://vkvideo.ru/video-84793390_456240038?list=ln-h8sMoZ05rvUany06as)<br>Семинар: [YouTube](https://www.youtube.com/live/VYEX17iibkQ?si=JUO4-zYBVS3FGqlD), [VK Video](https://vkvideo.ru/video-84793390_456240039?list=ln-C0ZIvShdj8WF6w0A9y) |
| 5 | [Production Engineering for LLM Agents](05_production_engineering_for_llm_agents/README.md) | Daniil Artamonov, Head of AI Platform; Kirill Vlasov, PM, AI Studio Yandex Cloud | конспект, 2 презентации | Лекция 5.1: [YouTube](https://www.youtube.com/live/sNemTIFlz08?si=Q2KdL2kYwg-ZpWHN), [VK Video](https://vkvideo.ru/video-84793390_456240040?list=ln-Tp7HdGUZFszu0lwh7F)<br>Лекция 5.2: [YouTube](https://www.youtube.com/live/UxgjgvI_wKY?si=HzQLhKnIS5PJ5bRf), [VK Video](https://vkvideo.ru/video-84793390_456240041?list=ln-v7UzBvkPgEvumWc03d) |
| Final | [Финальное задание](Final_Task/README.md) | - | постановка, ноутбук с решением, демо-профили | - |
| QA | [QA Session](QA-Session/README.md) | - | итоговая сессия с вопросами и ответами | [Запись](https://disk.yandex.ru/d/qtQgTekJnBYTnQ/QA-session%20%E2%80%94%20Agents%20Week.mp4) |

## Краткое содержание курса

### 1.1. Intro to AI Agents & LLM

Вводная лекция про применение AI-агентов, эволюцию взаимодействия с LLM и базовую формулу агента:

```text
Agent = runtime(AI model + prompts + tools + memory + guardrails + planning skills)
```

Также разобраны основы LLM: токенизация, авторегрессия, стратегии выбора следующего токена, pre-training, instruction tuning и RLHF.

### 1.2. Tools & MCP

Блок про инструменты как контракт между LLM и внешним миром: описание функций, аргументы, структурированный вывод, обработка ошибок и идемпотентность. Отдельно разобран Model Context Protocol: зачем он нужен, какие роли есть в архитектуре Host / Client / Server и какие проблемы масштабирования инструментов он решает.

### 2. Memory and Guardrails

Раздел про память и безопасность агентных систем. В части Memory разобраны short-term, long-term, entity и context memory, RAG, query rewriting, decomposition, HyDE и two-stage retrieval. В части Guardrails разобраны prompt injection, jailbreaking, hallucinations, content filters, action limiters, sandboxing, human confirmation и мониторинг.

### 3. Agent Workflows, MAS, Multimodality

Лекция и семинар про TAO-loop, ReAct, structured output для планирования, single-agent и multi-agent architectures. Основной акцент на том, как декомпозировать задачу между специализированными агентами, когда MAS оправдана, какие архитектуры бывают и почему tracing нужен с самого начала. Также затронуты мультимодальные агенты: vision, voice и комбинированные pipeline.

### 4. Agent Evaluation

Блок про eval как инженерную дисциплину. Ключевая идея: агент нужно оценивать не только по финальному тексту, а по всей траектории `Reasoning -> Action -> Outcome`. В конспекте разобраны evaluation suite, eval harness, критерии качества, code-based graders, LLM-as-a-Judge, human review, Iron User, Pass@k / Pass^k и культура качества в production.

### 5. Production Engineering for LLM Agents

Практический разбор того, почему Jupyter-прототип агента не готов к production. Темы: latency, стоимость, silent failures, невоспроизводимость, observability, structured logging, trace hierarchy, LangFuse / LangSmith, offline и online eval, DSPy, model router, кеширование, лимиты, безопасность инструментов, canary deployment и shared platform для нескольких агентов.

### QA Session

Итоговая сессия с ответами на вопросы по курсу и практическим уточнениям: как выбирать архитектуру агента, где оправдана multi-agent система, как подходить к eval, memory, guardrails и production-эксплуатации LLM-агентов.

## Финальное задание

Финальное задание находится в [`Final_Task`](Final_Task/README.md). Оно посвящено shopping-сценарию для небольшого магазина электроники.

Реализованы три части:

1. **Tool-Calling ReAct Agent** - агент ищет товары через `search_products` и при явном запросе добавляет их в корзину через `add_to_cart`.
2. **Memory Agent** - агент сохраняет пользовательские предпочтения в JSON-профиль и использует историю диалога для follow-up запросов.
3. **Multi-Agent System** - система из `RetrieverAgent`, `ProsAgent`, `ConsAgent`, `RankerAgent` и `CoordinatorAgent`, где поиск, анализ плюсов/минусов, ранжирование и добавление в корзину разделены между компонентами.

Подробнее: [Final_Task/README.md](Final_Task/README.md).

## Технологии и подходы

- **LLM agents**: ReAct, TAO-loop, tool calling, planning, structured output.
- **Memory**: short-term history, long-term JSON profile, RAG-подходы.
- **Multi-agent systems**: coordinator, specialized agents, handoff, shared context.
- **Evaluation**: eval suite, trajectory evaluation, LLM-as-a-Judge, code-based graders.
- **Production**: tracing, observability, canary deployment, cost optimization, model routing.
- **Инструменты**: Python, Jupyter Notebook, LangChain, MCP, Pydantic, LangFuse / LangSmith.

## Полезные материалы

- [Claw-Code](https://github.com/ultraworkers/claw-code)
- [Browser-Use](https://github.com/browser-use/browser-use)
- [GPT-Researcher](https://github.com/assafelovic/gpt-researcher)
- [OpenHands](https://github.com/OpenHands/OpenHands)
- [OpenAI Agents SDK Presentation](https://www.youtube.com/watch?v=joHR2pmxDQE)
- [Lilian Weng - LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)
- [Andrej Karpathy - Intro to Large Language Models](https://www.youtube.com/watch?v=zjkBMFhNj_g)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Anthropic - Model Context Protocol Announcement](https://www.anthropic.com/news/model-context-protocol)
- [LangChain Tools](https://docs.langchain.com/oss/python/integrations/tools)
- [Awesome MCP Servers](https://github.com/punkpeye/awesome-mcp-servers)
- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)
- [Anthropic - Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
- [DSPy](https://dspy.ai)
- [LangFuse](https://langfuse.com)
