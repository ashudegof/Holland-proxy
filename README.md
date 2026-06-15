# Holland-proxy

**SOCKS5-прокси на базе Dante** — готовый к использованию прокси-сервер в Docker.

[![Docker Hub](https://img.shields.io/docker/pulls/banfen321/dante-proxy)](https://hub.docker.com/r/banfen321/dante-proxy)
[![Build](https://github.com/ashudegof/Holland-proxy/actions/workflows/docker.yml/badge.svg)](https://github.com/ashudegof/Holland-proxy/actions/workflows/docker.yml)

## 🚀 Возможности

- **Zero config** — не требует настройки
- **Автоопределение сети** — сам находит сетевой интерфейс
- **Безопасная генерация пароля** — надёжный пароль создаётся автоматически
- **Работает без root** — все процессы от пользователя `nobody`
- **Основан на Dante** — самый надёжный open-source SOCKS5-сервер

## 📦 Быстрый старт

### 1. Откройте порт

```bash
sudo ufw allow 1080/tcp

### 2. Запуск

git clone https://github.com/ashudegof/Holland-proxy.git
cd Holland-proxy
docker compose up -d

### 3. Получение пароля

docker compose logs | grep -i password

_______________________

 Подключение
Параметр	Значение
Тип прокси	SOCKS5
IP-адрес	IP вашего сервера
Порт	1080
Логин	proxy
Пароль	из логов
🛠 Управление
Действие	Команда
Запустить	docker compose up -d
Остановить	docker compose down
Логи	docker compose logs
Сменить пароль	docker compose down && docker compose up -d

📄 Лицензия
MIT

🙏 Благодарности
banfen321/dante-proxy

adegtyarev/docker-dante

