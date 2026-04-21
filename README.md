# Shadowrocket: Маршрутизация


## Конфигурации (конфиги)

| Конфиг             | Краткое описание                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| [sr_ru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_basic.conf)  | Базовый конфиг: весь трафик идет напрямую через оператора, кроме доменов из списка, для которых используется прокси. Включает списки сообщества «Про Shadowrocket на русском» и порты голосового трафика.        |
| [sr_ru_geo.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_geo.conf)  | Все в прокси кроме доменов ru/рф, они мимо туннеля. Лучший вариант для звонков Telegram, Whatsapp и Facetime. Подключите дополительно ГЕО базы, ссылки на них есть в 94 строке. Обратите внимание, что может увеличиться время загрузки из Апстора и возможны другими минусы, которые автор пока не обнаружил.|
| [sr_ru_whitelist.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_whitelist.conf)  | БС через провайдера, а остальное в прокси|
| [sr_ru_mini.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_mini.conf)   | Минимальный конфиг с ограниченным числом популярных проксированных доменов для быстрой и легкой настройки.    |
| [sr_ru_extended.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_ru_extended.conf) | Расширенный конфиг с возможностью добавлять собственные правила маршрутизации. Можно не скачивать, а создать в приложении.                              |
| [sr_nonru_basic.conf](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/main/conf/sr_nonru_basic.conf) | Конфиг для тех, кто зарубежом, проксирующий все российские домены и домены на кириллице.

## Модули
Для YouTube доступен модуль [YT-Premium-V1-RU.module](https://raw.githubusercontent.com/misha-tgshv/shadowrocket-configuration-file/refs/heads/release/modules/YT-Premium-V1-RU.module) с отключенными китайскими субтитрами и необходимыми правилами. Требует выпуск HTTPS-сертификата на устройства. Хорошо работает на iOS, плохо на macOS и не работает на Apple TV.

## Актуальные списки
- `domains_community.list` — домены сообщества «Про Shadowrocket на русском», включающие универсальные правила для популярных доменов;
- `voice_ports.list` — порты для работы аудиозвонков в Whatsapp и Telegram;
- `Telegram.list` — универсальный список, включающий в себя правила по доменам и диапазону IP-адресов от [@blackmatrix7](https://github.com/blackmatrix7/ios_rule_script/refs/heads/master/rule/Shadowrocket/Telegram/Telegram.list);
