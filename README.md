# Infrastructure: учебный DevOps-проект

О проекте
Учебный репозиторий девопс инфраструктуры : 
Terraform, Ansible, Kubernetes, Docker, мониторинг и Github Actions.

Структура проекта
- `terraform/` — описание инфраструктуры
- `ansible/` — настройка серверов
- `kubernetes/` — манифесты Kubernetes
- `docker/` — Dockerfile и калькулятор
- `monitoring/` — конфигурация Prometheus
- `.github/workflows/` — CI/CD pipeline
Запуск через Docker
docker build -t calculator-app docker/
docker run -d -p 5000:5000 calculator-app

Open 'http://localhost:5000'
CI/CD
Workflow `.github/workflows/ci.yml` запускается на push и pull request в main.
Deployment 
Автоматический деплой пока не настроен. Для локального запуска надо использовать раздел Запуск через Docker
Работа с ветками
Прямые изменения в `main` не делаем: каждая фича идёт через отдельную ветку `feature/*` и Pull Request.
cat >> README.md <<'EOF'
Работа с ветками
Прямые изменения в `main` не делаем: каждая фича идёт через отдельную ветку `feature/*` и Pull Request.
