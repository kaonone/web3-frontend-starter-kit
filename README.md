# Frontend starter kit for Ethereum DApps (active development)

## npm scripts

- ```npm i``` install frontend and contracts dependencies
- ```npm run dev``` start locally in watch mode
- ```npm run codegen``` generate type definitions and React hooks by graphql schema and local queries (see `src/generated` folder)
- ```npm run build``` build production (see `build` folder)
- ```npm lint``` start code style linting and type checking
- ```npm test``` or ```npm t``` start test
- ```npm run deploy``` build production and deploy to gh-pages

## About starter kit

This starter kit is intended for frontend development based on Ethereum smart-contracts and subgraphs of [TheGraph](https://thegraph.com/).

Starter kit features:
- Interface build library [React](https://github.com/facebook/react)
- Project build with [Webpack](https://webpack.js.org/)
- Boilerplate code generation with [graphql-codegen](https://github.com/dotansimha/graphql-code-generator) and [typechain](https://github.com/ethereum-ts/TypeChain)
- Deploy in gh-pages
- Several basic features implemented
  - Connection to the wallets
  - Sent transaction notification show up
  - Multilingual
  - Form building components

## Structure

### src/core

Contains root component, which initializes right dependencies and connects right context-providers

### src/app

Contains app pages, basic routing and navigation

### src/features

Contains features not related to routing, can be used on app pages

### src/services

App basic services. Can be used in any place of app.

#### api

Service interacted with external environment. Contracts reading, transactions sending, wallet connection are going through it

#### apollo

Apollo setup service

#### i18n

Internationalization service

### utils

Contains helpers, decorators, formaters, validators, React-hooks, etc.
