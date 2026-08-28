### Gitlab-CI

Три стейджа в правильном порядке: test, build, deploy
Джоба для тестов (имя: run_tests) - Использует образ node:18-alpine - Устанавливает зависимости: npm ci - Запускает тесты: npm test
Джоба для сборки (имя: build_app) - Собирает проект: npm run build - Сохраняет папку dist/ как артефакт
Джоба для деплоя (имя: deploy_staging) - Выводит сообщение "Deploying to staging..." - Требует ручного запуска. Только для ветки develop.