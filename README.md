<img src="logo.svg" width="96" align="right">

# Metro Map

Карта в стиле Metro (плоские цветные плитки). Kotlin + Jetpack Compose + OpenStreetMap (osmdroid).

- Поиск места (Nominatim)
- Моё местоположение
- Зум плитками, живые плитки
- Переключение схема / рельеф
- Темы, акцентный цвет, RU/EN

## Две версии в одном репозитории

| Версия | Сборка | Устройство |
| ------ | ------ | ---------- |
| `phone` | `MetroMap-phone-*.apk` | телефон / планшет (касания) |
| `tv` | `MetroMap-tv-*.apk` (`com.example.metromap.tv`) | Android TV (пульт) |

Код общий, различия только во flavor-ах (`app/build.gradle.kts`, `app/src/tv/`).

### Управление на ТВ

- **Режим карты:** `← ↑ ↓ →` — двигать карту, `CH+/CH−` (или `PgUp/PgDn`, `+/−`) — масштаб, `OK` — открыть меню.
- **Режим меню:** стрелки — выбор кнопки, `OK` — нажать, `Назад` — вернуться к карте.

## Сборка

APK собирается автоматически: **Actions → Build APK → Artifacts**.
Релизы: создайте тег `v2.1` — в **Releases** появятся оба APK.

Локально: `gradle assemblePhoneDebug assembleTvDebug`
