# Модуль Magento 1.7 - 1.9 для Украины

## Установка:

* Распаковать архив в корень сайта.

* В админ панеле Magento открыть System->Configuration->Payment Methods и выбрать Platon.

* В настройках указать ключ и пароль. Также можете изменить название платежного метода.

* Установить значение платежного метода в статус Enabled.

* Примечание: взаимодействие CMS и gateway пишется в лог по адресу: /{MAGENTO_PATH}/var/log/platon_callback.log. Убедитесь, что эта директория доступна для записи веб-серверу.

## Ссылка для коллбеков:
https://ВАШ_САЙТ/platon/connector/process/

## Тестирование:
В целях тестирования используйте наши тестовые реквизиты.

| Номер карты  | Месяц / Год | CVV2 | Описание результата |
| :---:  | :---:  | :---:  | --- |
| 4111  1111  1111  1111 | 02 / 2022 | Любые три цифры | Не успешная оплата без 3DS проверки |
| 4111  1111  1111  1111 | 06 / 2022 | Любые три цифры | Не успешная оплата с 3DS проверкой |
| 4111  1111  1111  1111 | 01 / 2022 | Любые три цифры | Успешная оплата без 3DS проверки |
| 4111  1111  1111  1111 | 05 / 2022 | Любые три цифры | Успешная оплата с 3DS проверкой |
