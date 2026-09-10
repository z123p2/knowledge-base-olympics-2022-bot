[English](README.md) | Русский

# Knowledge Base Olympics 2022 Bot

![Python](https://img.shields.io/badge/python-3.x-blue)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/z123p2/knowledge-base-olympics-2022-bot/blob/main/knowledge_base_olympics_2022_bot.ipynb)
[![Telegram Bot](https://img.shields.io/badge/Telegram-Bot-blue?logo=telegram)](https://t.me/knowledge_base_olympics_2022_bot)
![OpenAI](https://img.shields.io/badge/LLM-GPT--4o--mini-green)
![License](https://img.shields.io/badge/license-MIT-green)

Telegram-бот, который отвечает на вопросы о зимних Олимпийских играх 2022
года, используя метод Search-Ask с эмбеддингами и GPT.

Доступен в Telegram: [@knowledge_base_olympics_2022_bot](https://t.me/knowledge_base_olympics_2022_bot)

## Как это работает

1. База знаний скачивается из репозитория (ZIP с текстами статей и
   эмбеддингами)
2. Вопрос пользователя преобразуется в эмбеддинг через
   `text-embedding-3-small`
3. Находятся наиболее релевантные секции статей по косинусному расстоянию
4. Релевантные секции добавляются как контекст в промпт GPT-4o-mini
5. Ответ возвращается пользователю

## Бизнес-ценность

Пример бота-справочной службы: отвечает клиентам или сотрудникам по
документам компании вместо оператора. Тот же пайплайн работает с любой
базой документов (FAQ, регламенты, документация продукта).

## Настройка

1. Получите API-ключ OpenAI: https://platform.openai.com/api-keys
2. Создайте бота через [@BotFather](https://t.me/BotFather) и получите токен
3. В Google Colab добавьте секреты (значок ключа в левой панели):
   - `M_TOKEN` - API-ключ OpenAI
   - `B_TOKEN` - токен Telegram-бота
   - `BASE_URL` - `https://api.openai.com/v1`

## Запуск

1. Откройте `knowledge_base_olympics_2022_bot.ipynb` в Google Colab
2. Запустите все ячейки
3. Напишите боту в Telegram команду `/start` или задайте любой вопрос по
   Олимпиаде-2022

База знаний скачивается автоматически из репозитория при запуске блокнота.

## Структура проекта

- `knowledge_base_olympics_2022_bot.ipynb` - основной блокнот с ботом
- `data/winter_olympics_2022_v3_small.zip` - база знаний (архив)
- `requirements.txt` - зависимости Python
- `img/` - скриншоты работы бота
- `README.md` - этот файл

## Команды бота

- `/start` - приветственное сообщение
- `/help` - информация о базе знаний (тематика, количество записей, пример
  запроса)
- Любой текстовый запрос - бот ищет ответ в базе знаний и возвращает
  результат

## Скриншоты

![Команды /start и /help](img/knowledge_base_start_help.jpg)

![Вопрос и ответ бота](img/knowledge_base_question_answer.jpg)
