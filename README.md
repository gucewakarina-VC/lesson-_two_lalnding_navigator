# AI-бюро «Навигатор» — лендинг

Современный одностраничный сайт для AI-бюро, которое помогает малому бизнесу внедрять нейросети, чат-ботов и автоматизацию.

## Возможности

- **Приветственный баннер** — показывается при первом визите, можно закрыть или перейти к квизу
- **Быстрый AI-маршрут** — интерактивный квиз из 3 вопросов с рекомендацией услуги
- **Форма заявки** — валидация, сохранение в `localStorage`, открытие Telegram с готовым текстом
- **Анимации при скролле**, адаптивная вёрстка, активная навигация, кнопка «Наверх»

## Структура проекта

```
navigator-landing/
├── index.html          # Разметка лендинга
├── styles.css          # Стили
├── js/
│   ├── config.js       # Контакты и настройки сайта
│   ├── main.js         # Меню, скролл, навигация
│   ├── welcome.js      # Приветственный баннер
│   ├── quiz.js         # AI-квиз
│   └── form.js         # Форма заявки
├── assets/
│   └── favicon.svg     # Иконка сайта
├── package.json
├── vite.config.js
└── README.md
```

## Быстрый старт

### Вариант A — без установки (сразу посмотреть)

Откройте `index.html` в браузере или запустите простой сервер:

```bash
cd ~/Projects/navigator-landing
python3 -m http.server 8080
```

Затем откройте [http://localhost:8080](http://localhost:8080).

### Вариант B — через Vite (рекомендуется для разработки)

#### 1. Установить зависимости

```bash
cd ~/Projects/navigator-landing
npm install
```

### 2. Запустить локальный сервер

```bash
npm run dev
```

Сайт откроется на [http://localhost:5173](http://localhost:5173).

### 3. Сборка для публикации

```bash
npm run build
npm run preview
```

Готовые файлы появятся в папке `dist/`.

## Настройка контактов

Отредактируйте `js/config.js`:

```javascript
window.SITE_CONFIG = {
  telegram: 'https://t.me/your_username',
  telegramUsername: 'your_username',
  email: 'hello@your-domain.ru',
  // ...
};
```

## Деплой

Подойдёт любой хостинг статики:

- **GitHub Pages** — загрузите содержимое `dist/` после `npm run build`
- **Netlify / Vercel** — укажите команду сборки `npm run build` и папку `dist`
- **Обычный хостинг** — загрузите файлы проекта или результат сборки

## Технологии

- HTML5, CSS3, JavaScript (без фреймворков)
- [Vite](https://vitejs.dev/) — dev-сервер и сборка
- Google Fonts (Manrope)

## Лицензия

MIT
