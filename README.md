# Слова из слова — Telegram Mini App

Игра: из букв длинного слова собрать слова поменьше. 222 уровня, подсказки со значениями слов (Викисловарь, CC BY-SA), прогресс в Telegram CloudStorage.

## Файлы
- `index.html` — приложение
- `levels.json` — уровни и списки слов
- `defs.json` — значения слов для подсказок

Все три файла должны лежать рядом.

## Публикация на GitHub Pages
1. Создайте репозиторий и загрузите в корень эти файлы.
2. Settings → Pages → Source: `Deploy from a branch`, Branch: `main` / `(root)` → Save.
3. Через минуту сайт будет доступен по адресу `https://<логин>.github.io/<репозиторий>/`.

## Подключение к Telegram
1. @BotFather → `/newbot` → создайте бота.
2. `/newapp` → выберите бота → укажите URL из шага выше → задайте короткое имя (например `slova`).
3. Игра откроется по ссылке `t.me/<ваш_бот>/slova`.
4. Опционально: `/mybots` → бот → Bot Settings → Menu Button → тот же URL.

## Прогресс
Каждый уровень хранится отдельным ключом в CloudStorage (привязан к аккаунту Telegram, синхронизируется между устройствами). Копия дублируется в localStorage.

## Источники данных
- Существительные: Harrix/Russian-Nouns (MIT)
- Частотность для отбора слов: hermitdave/FrequencyWords (MIT, на основе OpenSubtitles)
- Значения слов: ru.wiktionary.org (CC BY-SA 3.0)
