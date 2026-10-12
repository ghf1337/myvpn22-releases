# Сторонние компоненты MyVPN22 для Android

Приложение MyVPN22 использует следующие компоненты с открытым исходным кодом.
Этот файл публикуется вместе со сборками в `ghf1337/myvpn22-releases`.

| Компонент | Версия | Лицензия | Исходники |
|---|---|---|---|
| Xray-core | v26.9.30 (внутри AndroidLibXrayLite) | MPL-2.0 | https://github.com/XTLS/Xray-core |
| AndroidLibXrayLite (`libv2ray.aar`) | v26.9.30 | LGPL-3.0 | https://github.com/2dust/AndroidLibXrayLite/tree/v26.9.30 |
| mihomo | v1.19.32 | GPL-3.0 | https://github.com/MetaCubeX/mihomo/tree/v1.19.32 |
| hev-socks5-tunnel | 2.18.0 | MIT | https://github.com/heiher/hev-socks5-tunnel/tree/2.18.0 |
| libXray (iOS-сборка: Xray-core для Apple) | v26.9.30 | MIT | https://github.com/XTLS/libXray/tree/v26.9.30 |
| OkHttp | 5.5.0 | Apache-2.0 | https://github.com/square/okhttp |
| Kotlin, kotlinx.coroutines, kotlinx.serialization | см. сборку | Apache-2.0 | https://github.com/JetBrains/kotlin |
| AndroidX, Jetpack Compose, Material 3 | см. сборку | Apache-2.0 | https://android.googlesource.com/platform/frameworks/support |
| Google Tink | 1.23.0 | Apache-2.0 | https://github.com/tink-crypto/tink-java |
| SnakeYAML Engine | 2.10 | Apache-2.0 | https://github.com/snakeyaml/snakeyaml-engine |

## Как используются компоненты с copyleft-лицензиями

- **mihomo (GPL-3.0)** — неизменённый исполняемый файл из официального релиза, запускается **отдельным
  процессом** и общается с приложением только через локальный SOCKS-порт; в код приложения не линкуется.
  Точные исходники этой версии — по ссылке на тег выше.
- **AndroidLibXrayLite (LGPL-3.0)** — неизменённая библиотека из официального релиза, загружается
  динамически (`libgojni.so`). Исходники — по ссылке на тег выше.
- **Xray-core (MPL-2.0)** — файлы Xray-core не изменялись.
- **iOS-версия** использует Xray-core через libXray (MIT) и hev-socks5-tunnel (MIT); mihomo в iOS-версии нет.

Полные тексты лицензий — по ссылкам на исходники каждого компонента.
