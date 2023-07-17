Проверка коммитов на соответствие формату conventional commits производится локально у разработчика, вносящего изменения.

## Workflows

### [`pr-checks.yml`](https://github.com/NikolayMagarin/ci-homework/blob/master/.github/workflows/pr-checks.yml)

- Запускает тесты на pull request
- Выполняет установку пакетов `npm ci`
- Прогоняет unit тесты `npm run test-ci` и сохранят результат (html) в артефакты
- Прогоняет e2e тесты `npm run e2e` и сохранят результат (html) в артефакты

### [`release.yml`](https://github.com/NikolayMagarin/ci-homework/blob/master/.github/workflows/release.yml)

- Запускается на push с тегом `v<число>` (например, `v12`)
- Выполняет установку пакетов `npm ci`
- Прогоняет unit тесты `npm run test-ci` и сохранят результат (html) в артефакты
- Прогоняет e2e тесты `npm run e2e` и сохранят результат (html) в артефакты
- Выполняет сборку приложения `npm run build`
- Выполняет деплой приложения на github pages
- Создаёт issue с автором и датой релиза, номером версии и changelog

---

telegram: [@NikolayMagarin](https://t.me/NikolayMagarin)
