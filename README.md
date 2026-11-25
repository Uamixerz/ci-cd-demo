# ci-cd-demo (fork)

[![CI](https://github.com/Uamixerz/ci-cd-demo/actions/workflows/ci.yml/badge.svg)](https://github.com/Uamixerz/ci-cd-demo/actions/workflows/ci.yml)

Fork навчального репозиторію [vivalafit/ci-cd-demo](https://github.com/vivalafit/ci-cd-demo) для практичної 7.

## Локальний запуск

Потрібен Node.js 18 або новіший.

```bash
git clone https://github.com/Uamixerz/ci-cd-demo.git
cd ci-cd-demo
npm ci
npm test
```

Очікується: 2 тести пройдено.

## CI

`.github/workflows/ci.yml` запускається на `push` і `pull_request`: checkout, Node 18 з кешем npm, `npm ci`, тести з покриттям. Покриття зберігається як артефакт `coverage`.

`.github/workflows/docker.yml` на `main` збирає образ і публікує його в GHCR з тегом `sha-<commit>`.

Зміни щодо оригіналу: артефакт покриття, `timeout-minutes`, ім'я образу в нижньому регістрі для GHCR, цей README.
