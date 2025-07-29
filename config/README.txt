Инструкция по добавлению USB dongle в Sofle:

1. Поместите файлы Kconfig.shield, Kconfig.defconfig, sofle_dongle.overlay в каталог shields/sofle вашего zmk-config.
2. Для сборки прошивки dongle используйте:
   west build -s app -b nice_nano_v2 -- -DSHIELD=sofle_dongle
3. Для split-половинок собирайте как раньше (sofle_left / sofle_right).
4. Перед первой загрузкой новой конфигурации используйте settings_reset на всех устройствах.

---
Файлы overlay для dongle не содержат физических пинов, только mock_kscan и layout Sofle.
