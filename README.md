# Aidoku Sources for Russians

[![Добавить в Aidoku](https://img.shields.io/badge/%D0%94%D0%BE%D0%B1%D0%B0%D0%B2%D0%B8%D1%82%D1%8C%20%D0%B2-Aidoku-ff2d55?style=for-the-badge)](https://redcatpet.github.io/aidoku-sources-for-russians/)

Русскоязычные источники для [Aidoku](https://aidoku.app) на iPhone и iPad.

## Установка

Нажмите кнопку выше или добавьте список вручную: `Настройки` → `Список источников` → `+`.

```text
https://redcatpet.github.io/aidoku-sources-for-russians/index.min.json
```

После установки списка выберите и установите нужные источники в Aidoku. Новые версии публикуются по тому же адресу автоматически.

## Источники

| Источник | Сайт | Версия | Статус | Содержимое |
| --- | --- | :---: | --- | --- |
| [AllHentai](sources/ru.allhentai/) | [allhen.online](https://allhen.online) | v6 | beta, вход через WebView | манга 18+ |
| [Senkuro](sources/ru.senkuro/) | [senkuro.com](https://senkuro.com) | v13 | работает | манга, манхва, маньхуа, комиксы |
| [Senkognito](sources/ru.senkognito/) | [senkognito.com](https://senkognito.com) | v12 | работает | каталог 18+ Senkuro |
| [ReadManga](sources/ru.readmanga/) | [readmanga.live](https://readmanga.live) | v7 | beta, вход через WebView | манга |
| [InkStory](sources/ru.inkstory/) | [inkstory.net](https://inkstory.net) | v2 | beta, вход через WebView | манга, манхва, маньхуа |
| [MangaBuff](sources/ru.mangabuff/) | [mangabuff.ru](https://mangabuff.ru) | v4 | beta | манга, манхва, маньхуа |
| [Ranobes](sources/ru.ranobes/) | [ranobes.com](https://ranobes.com) | v7 | beta | ранобэ |
| [RanobeHub](sources/ru.ranobehub/) | [ranobehub.org](https://ranobehub.org) | v2 | beta | ранобэ |
| [Ранобэ.рф](sources/ru.ranoberf/) | [ранобэ.рф](https://ранобэ.рф) | v4 | beta | ранобэ |

Некоторые сайты ограничивают доступ по региону, VPN или возрасту. Доступные домены и авторизация находятся в настройках соответствующего источника.

## Разработка

Исходники находятся в `sources/<id>`, общий код — в `templates/`. Пакеты собираются через [aidoku-rs](https://github.com/Aidoku/aidoku-rs).

```bash
rustup target add wasm32-unknown-unknown
cargo install --git https://github.com/Aidoku/aidoku-rs aidoku-cli
cd sources/ru.senkuro
aidoku package
```

Пуш в `main` запускает GitHub Actions, обновляет `.aix`, индекс источников и GitHub Pages.

## Лицензия

MIT. Репозиторий не связан с владельцами сайтов или разработчиками Aidoku.
