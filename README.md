DevOps infrastructure repository

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
