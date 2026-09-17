Emoji Finder — React + TypeScript + Node.js API
Приложение создано в рамках практической работы по интеграции фронтенда (React + TypeScript) с backend‑сервисом (Node.js + Express).
Проект позволяет искать эмодзи по названию и ключевым словам, отображать результаты и обрабатывать состояния загрузки и ошибок.

Функционал
Поиск эмодзи по параметру q (название или ключевые слова)

Отображение списка эмодзи (символ, название, ключевые слова)

Состояния:

загрузка

ошибка (если сервер выключен)

пустой результат

Стилизация карточек + hover‑эффект

Полная типизация данных (TypeScript)

Разделение логики API и компонентов

Технологии
Frontend
React

TypeScript

Axios

Create React App

Backend
Node.js

Express

CORS

dotenv

Структура проекта
Код
emoji server/
│ app.js                — backend API
│ assets/emojis.json    — база эмодзи
│ start.bat             — запуск сервера (Windows)
│ client/               — React + TypeScript приложение
│   src/
│   public/
│   package.json
│   tsconfig.json
Запуск проекта
1. Запуск backend
Перейдите в корень проекта:

Код
cd emoji server
node app.js
Сервер запустится на:

Код
http://localhost:3000
Проверка:

Код
http://localhost:3000/api/emojis
2. Запуск frontend
Перейдите в папку клиента:

Код
cd client
npm install
npm start
Фронтенд работает на:

Код
http://localhost:3001
🔍 Примеры запросов API
Все эмодзи:
http://localhost:3000/api/emojis

Поиск по слову:
http://localhost:3000/api/emojis?q=fire

Поиск по названию:
http://localhost:3000/api/emojis?q=smile

Выполненные требования практической работы
Типизация данных (интерфейсы без any)

Логика запросов вынесена в src/api/emojiApi.ts

Обработка состояний: загрузка, ошибка, пустой результат

Поиск по мере ввода текста

Стилизация карточек + hover‑эффект

Разделение backend и frontend

Полностью рабочая интеграция