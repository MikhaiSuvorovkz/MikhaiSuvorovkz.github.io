# AGENTS.md

Рабочие правила для этого репозитория.

## Назначение

Этот репозиторий содержит GitHub Pages сайт для игры `Wild Horse Simulator Family 3D`
(`magic.horse.simulator.free.sim.games.kids`).

Сайт используется для:

- главной страницы игры;
- `app-ads.txt`;
- политики конфиденциальности.

## Канонические URL

- Сайт: `https://mikhaisuvorovkz.github.io/`
- Privacy Policy: `https://mikhaisuvorovkz.github.io/privacy-policy/`
- app-ads.txt: `https://mikhaisuvorovkz.github.io/app-ads.txt`
- Google Play: `https://play.google.com/store/apps/details?id=magic.horse.simulator.free.sim.games.kids`

## Что уже сделано

- Репозиторий создан и опубликован как `MikhaiSuvorovkz/MikhaiSuvorovkz.github.io`.
- Главная страница собрана в `index.html`.
- Политика конфиденциальности собрана в `privacy-policy.md` через Jekyll layout.
- `app-ads.txt` лежит в корне сайта и содержит строку AdMob:
  `google.com, pub-5851292782907536, DIRECT, f08c47fec0942fa0`
- Hero-изображение лежит в `assets/horse-family-hero.png`.

## Структура

- `index.html` - главная страница.
- `privacy-policy.md` - политика конфиденциальности.
- `_layouts/default.html` - layout для Markdown-страниц.
- `_config.yml` - настройки Jekyll/GitHub Pages.
- `app-ads.txt` - файл для проверки рекламных seller-ов.
- `assets/` - стили и изображения.
- `docs/` - проектная документация.

## Правила изменений

- `app-ads.txt` держать в корне репозитория.
- Формат строк в `app-ads.txt` не ломать.
- Если меняется набор рекламных сетей, обновлять файл по исходному шаблону и отдельно сохранять AdMob строку.
- Если добавляется новая игра, заводить для нее отдельную страницу и отдельную политику, если у игры свой package name или отдельный лендинг.
- После любых правок проверять, что корень сайта, `privacy-policy/` и `app-ads.txt` отдают `200`.
- Не делать лишний рефакторинг без задачи.

## Рабочий порядок

1. Править содержимое в минимальном scope.
2. Проверять локально или через GitHub Pages, что ссылки открываются.
3. Если меняются публичные URL, обновлять документацию вместе с сайтом.
4. При добавлении новой игры фиксировать ее package name, Play URL, privacy URL и рекламные требования.
