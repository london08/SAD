# Выбор решения класса API-Gateway

## Status (Статус)
IN PROGRESS

## Context (Условия)
Альтернативы:
* Kong (https://konghq.com/products/kong-gateway)
* Gravitee (https://tyk.io/)
* Tyk (https://tyk.io/)
* KrakenD (https://www.krakend.io/)


| Критерий / Решение                     | Kong    | Gravitee | Tyk     | APISIX   | KrakenD |
|:---------------------------------------|:--------|:---------|:--------|:---------|:--------|
| Трудоемкость внедрения и использования |         |          |         |          |         |
| Cloud-ready                            | Да      |          |         |          |         |
| OpenSource                             | Да      | Нет      | Да      |          |         |
| Поддержка сообщества                   | Сильная | Слабая   | Сильная | Сильная  |         |
|                                        |         |          |         |          |         |
|                                        |         |          |         |          |         |
|                                        |         |          |         |          |         |
|                                        |         |          |         |          |         |



## Decision (Решение)
Будем использовать...

## Consequences (Последствия)
 Kong controls layer 4 and 7 traffic and is extended through Plugins, which provide extra functionality and services beyond the core platform.
 KrakenD because of its simplicity, statelessness, immutability, and performance.
APISIX тоже производительный и удобный, и не имеет дополнительных костов для enterprise

## Metainformation (Заметки)
*[Comparison Chart](https://sourceforge.net/software/compare/Gravitee.io-vs-Kong-Konnect-vs-Tyk-vs-WSO2-API-Manager/)
*[](https://dev.to/apisix/how-to-choose-the-right-api-gateway-3f9i)
*[](https://habr.com/ru/articles/765944/)
*[](https://api7.ai/tyk-vs-kong)

## Measurements (Измерения)
N/A
