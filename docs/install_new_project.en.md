# Start new project

Зависимости должны быть установлены.

#### Шаг 1. Создаем новый сайт из шаблона

Будет создана директория с проектом в интерактивном режиме.

```bash
cookiecutter https://github.com/garpixcms/garpixcms-empty-template
cd website
```

#### Шаг 2. Применяем переменные окружения

Загляните в файл `.env`. Вполне возможно, что вы захотите отредактировать содержимое.

```bash
cp example.env .env
```

#### Шаг 3. Устанавливаем зависимые пакеты

Перейдите в директорию с проектом и установите зависимости.

```bash
pipenv install
pipenv shell
```

#### Шаг 4. Поднимаем docker

Поднимаем базу данных и другие сервисы через docker-compose.

```bash
docker-compose up -d
```

#### Шаг 5. Создаем миграции

```bash
python3 backend/manage.py makemigrations
```
