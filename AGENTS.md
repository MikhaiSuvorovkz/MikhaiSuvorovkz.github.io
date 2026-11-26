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
- Cyberbeat: `https://mikhaisuvorovkz.github.io/cyberbeat/`
- Cyberbeat Privacy Policy: `https://mikhaisuvorovkz.github.io/cyberbeat/privacy-policy/`
- Skymane: Horse & Pegasus Sim (бывший Forest Horse Simulator) Privacy Policy: `https://mikhaisuvorovkz.github.io/skymane/privacy-policy/`
- app-ads.txt: `https://mikhaisuvorovkz.github.io/app-ads.txt`
- Google Play: `https://play.google.com/store/apps/details?id=magic.horse.simulator.free.sim.games.kids`

## Публикация на haenphi.com

- Сайт публикуется на `https://haenphi.com/` workflow-ом `.github/workflows/deploy-haenphi.yml`
  на каждый push в `main`: Jekyll 4 собирает `_site/`, rsync заливает его на VPS в
  `/opt/haenphi-site/public`, Caddy отдаёт эту папку как статику.
- Деплой включается переменной репозитория `ENABLE_HAENPHI_DEPLOY=true`. Нужны переменные
  `HAENPHI_SERVER_HOST`, `HAENPHI_SERVER_PORT`, `HAENPHI_SERVER_USER`, `HAENPHI_SSH_KNOWN_HOSTS`
  и секрет `HAENPHI_SITE_DEPLOY_SSH_KEY` (ключ на сервере ограничен `rrsync` только этой папкой).
- Сборка идёт с `--strict_front_matter`: значения во front matter с двоеточием брать в кавычки,
  иначе деплой упадёт.
- `AGENTS.md`, `README.md` и `docs/` в сборку не попадают (`exclude` в `_config.yml`).
- Пути на сайте только абсолютные от корня (`/assets/...`), без `site.url`/`baseurl`.

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
- Страницу `cyberbeat/privacy-policy/index.html` руками не править: это побайтовая копия
  файла, который генерируется в Unity-проекте `Cyberbeat` из игровой локализации
  (`python3 -I tools/privacy/build_privacy_page.py`, результат в
  `Documentation/Privacy/privacy-policy.html`). Обновление политики - перегенерировать там
  и скопировать файл сюда, чтобы текст в игре и на сайте совпадал.
- Не делать лишний рефакторинг без задачи.

## Рабочий порядок

1. Править содержимое в минимальном scope.
2. Проверять локально или через GitHub Pages, что ссылки открываются.
3. Если меняются публичные URL, обновлять документацию вместе с сайтом.
4. При добавлении новой игры фиксировать ее package name, Play URL, privacy URL и рекламные требования.
5. Если пользователь просит что-либо добавить на сайт, после завершения правок сразу закоммитить и запушить изменения, дождаться завершения GitHub Actions и проверить опубликованный сайт. Для работы с GitHub Actions можно использовать GitHub CLI (`gh`).
