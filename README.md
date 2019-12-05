# Frontend starter kit for Ethereum DApps (active development)

## npm scripts

- ```npm i``` install frontend and contracts dependencies
- ```npm run dev``` start locally in watch mode
- ```npm run codegen``` generate type definitions and React hooks by graphql schema and local queries (see `src/generated` folder)
- ```npm run build``` build production (see `build` folder)
- ```npm lint``` start code style linting and type checking
- ```npm test``` or ```npm t``` start test
- ```npm run deploy``` build production and deploy to gh-pages

## О стартерките

Данный стартеркит предназначен для разработки фронтенда на базе эфировских смарт-контрактов и сабграфов TheGraph.

Особенности стартер кита:

- библиотека для построения интерфейсов `React`
- сборка проекта с помощью `webpack`
- кодогенерация бойлерплейта с помощью `graphql-codegen` и `typechain`
- деплой в gh-pages
- реализованы некоторые базовые фичи
  - подключение к кошелькам
  - отображение нотификаций по отправленным транзакциям
  - мультиязычность
  - компоненты для построения форм

## Структура

### src/core

Содержит корневой компонент, который инициализирует нужные зависимости и подключает нужные контекст провайдеры

### src/app

Содержит страницы приложения, базовый раутинг и навигацию

### src/features

Содержит фичи не привязанные к раутингу, могут быть использованы на страницах приложения

### src/services

Базовые сервисы приложения. Могут быть использованы в любом месте приложения

#### api

Сервис отвечающий за коммуникацию с внешним миром, через него происходит чтение контрактов, отправка транзакций, коннект с кошельком

#### apollo

Сервис отвечающий за настройку Apollo

#### i18n

Сервис отвечающий за интернационализацию

### utils

Содержит хелперы, декораторы, форматеры, валидаторы, реакт-хуки и т.д.
