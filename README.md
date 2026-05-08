# Aidoku Sources for Russians

[![Добавить в Aidoku](https://img.shields.io/badge/%D0%94%D0%BE%D0%B1%D0%B0%D0%B2%D0%B8%D1%82%D1%8C%20%D0%B2-Aidoku-ff2d55?style=for-the-badge)](https://redcatpet.github.io/aidoku-sources-for-russians/)

Русскоязычные источники для [Aidoku](https://aidoku.app) на iOS/iPadOS.

## Установка

Нажмите кнопку выше или откройте на iPhone/iPad:

```text
https://redcatpet.github.io/aidoku-sources-for-russians/
```

и нажмите `Добавить в Aidoku`.

Для ручной установки в Aidoku откройте `Настройки` → `Список источников` → `+` и вставьте URL:

```text
https://redcatpet.github.io/aidoku-sources-for-russians/index.min.json
```

Если GitHub Pages ещё не обновился, можно временно добавить raw-индекс:

```text
https://raw.githubusercontent.com/redcatpet/aidoku-sources-for-russians/gh-pages/index.min.json
```

После добавления списка источники появятся в разделе установки. Если Aidoku показывает старые данные, удалите этот список источников, полностью закройте приложение и добавьте URL заново.

## Источники

| Источник | Сайт | Версия | Статус | Содержимое |
| --- | --- | :---: | --- | --- |
| [Senkuro](sources/ru.senkuro/) | https://senkuro.com | v8 | работает | манга, манхва, маньхуа, комиксы |
| [Senkognito](sources/ru.senkognito/) | https://senkognito.com | v7 | работает | 18+ каталог Senkuro |
| [ReadManga](sources/ru.readmanga/) | https://readmanga.live | v5 | beta, web-login | манга |
| [MangaBuff](sources/ru.mangabuff/) | https://mangabuff.ru | v1 | beta | манга, манхва |
| [Ranobes](sources/ru.ranobes/) | https://ranobes.com | v5 | beta | ранобэ |
| [RanobeHub](sources/ru.ranobehub/) | https://ranobehub.org | v2 | beta | ранобэ |
| [Ранобэ.рф](sources/ru.ranoberf/) | https://ранобэ.рф | v2 | beta | ранобэ |

## Что исправлено в этом форке

- Senkuro снова использует актуальный GraphQL-запрос `mangaTachiyomiSearch` и типы фильтров `MangaTachiyomiSearch*Filter`.
- Фильтры типа, формата, статуса, статуса перевода, жанров и возрастного рейтинга снова передаются в API.
- Версии Senkuro и Senkognito увеличены, чтобы Aidoku предложил обновление после публикации списка.
- README и ссылки на список источников обновлены под репозиторий `redcatpet/aidoku-sources-for-russians`.

## Разработка

Каждый источник находится в `sources/<id>` и собирается через [aidoku-rs](https://github.com/Aidoku/aidoku-rs).

Локальная сборка отдельного источника:

```bash
rustup target add wasm32-unknown-unknown
cargo install --git https://github.com/Aidoku/aidoku-rs aidoku-cli
cd sources/ru.senkuro
aidoku package
```

Публикация автоматическая: при пуше в `main` GitHub Actions собирает `.aix` пакеты, создаёт `index.min.json` и выкладывает результат в ветку `gh-pages`.

## Лицензия

MIT. См. [LICENSE](LICENSE).

Этот репозиторий не связан с владельцами сайтов-источников или приложением Aidoku.
