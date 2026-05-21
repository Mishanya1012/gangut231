# Los Santos Dating

SPA-прототип игровой социальной сети знакомств для GTA 5 RP сервера.

## Что работает

- Первый экран: регистрация или вход через Discord.
- Регистрация привязывает Discord локально, принимает имя UCP аккаунта без проверки и просит ник для социальной сети.
- После входа доступны вкладки: поиск, профиль, матчи, чат, гости, уведомления, VIP, админ-панель.
- Поиск показывает анкеты игровых персонажей и соигроков вне самой игры.
- Лайк и пропуск переключают анкеты через Zustand-store.
- Интерфейс адаптирован под desktop, tablet и mobile.

## Стек

- Next.js
- TypeScript
- Tailwind CSS
- Framer Motion
- Zustand
- Axios

## Запуск

```bash
npm install
npm run dev
```

Фронтенд ожидает API на `http://localhost:4000`. Адрес можно поменять через `NEXT_PUBLIC_API_URL`.

## Быстрое превью без npm

В проекте есть автономный `index.html`, который можно открыть напрямую в браузере.

Также можно поднять простой static preview:

```bash
node preview-server.js
```

После запуска страница будет доступна на `http://localhost:4173`.

## План backend API

- `POST /auth/login`
- `POST /auth/register`
- `POST /auth/logout`
- `GET /profile`
- `PUT /profile`
- `POST /likes`
- `GET /likes`
- `GET /matches`
- `GET /messages`
- `POST /messages`

## Интеграция GTA сервера

- `GET /api/player/:id`
- `POST /api/auth/game`
- `GET /api/player/status`
