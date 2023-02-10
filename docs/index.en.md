# Quick Start

Необходимо установить Python (рекомендуется `3.8`), Pipenv, Docker и cookiecutter. Подробнее смотрите в разделе [Установка зависимостей](install_deps.md).

Далее создаем [новый проект](install_new_project.md) или [запускаем существующий](install_start_project.md). Перейдите по ссылкам для подробной документации.

Если подробная документация не требуется, то можете использовать команды ниже.

## Новый проект

```bash
cookiecutter https://github.com/garpixcms/garpixcms-empty-template
cd website
cp example.env .env
pipenv install
pipenv shell
docker-compose up -d
python3 backend/manage.py makemigrations
python3 backend/manage.py migrate
python3 backend/manage.py createsuperuser
python3 backend/manage.py runserver
```

# Запускаем существующий проект

```bash
git clone <repo_url>
cd <directory>
cp example.env .env
pipenv install
pipenv shell
docker-compose up -d
python3 backend/manage.py migrate
python3 backend/manage.py createsuperuser
python3 backend/manage.py runserver
```
