# Выбор решения класса API-Gateway

## Status (Статус)
DONE

## Context (Условия)
Альтернативы:
* Kong (https://konghq.com/products/kong-gateway)
* Gravitee (https://www.gravitee.io/)
* Tyk (https://tyk.io/)
* KrakenD (https://www.krakend.io/)
* Apache APISIX (https://apisix.apache.org/)

| Критерий / Решение                     | Kong    | Gravitee | Tyk     | APISIX  | KrakenD |
|:---------------------------------------|:--------|:---------|:--------|:--------|:--------|
| Трудоемкость внедрения и использования | Низкая  | Средняя  | Средняя | Низкая  | Низкая  |
| Cloud-ready                            | Да      | Да       | Да      | Да      | Да      |
| OpenSource                             | Да      | Да       | Да      | Да      | Да      |
| Поддержка сообщества                   | Сильная | Слабая   | Сильная | Сильная | Сильная |
| Наличие GUI администратора             | Нет     | Да       | Да      | Да      | Да      |
| Поддержка GraphQL                      | Плагин  | Да       | Да      | Частич. | Да      |

- Kong controls layer 4 and 7 traffic and is extended through Plugins, which provide extra functionality and services beyond the core platform. В квадранте лидеров по Gartner. 
- KrakenD benefits: simplicity, statelessness, immutability, and performance. Большое кол-во интеграций.
- APISIX тоже производительный и удобный, и не имеет дополнительных костов для enterprise.

## Decision (Решение)
Будем использовать KrakenD из-за производительности и statelessness. Не требует БД. Синхронизируется через etcd. 

## Consequences (Последствия)
Для развертывания потребуется etcd. 
https://www.krakend.io/docs/deploying/
https://www.krakend.io/docs/overview/

## Metainformation (Заметки)
*[Comparison Chart](https://sourceforge.net/software/compare/Gravitee.io-vs-Kong-Konnect-vs-Tyk-vs-WSO2-API-Manager/)
*[Comparison Chart](https://sourceforge.net/software/compare/Apache-APISIX-vs-Gravitee.io-vs-KrakenD-vs-Tyk/)
*[](https://dev.to/apisix/how-to-choose-the-right-api-gateway-3f9i)
*[](https://habr.com/ru/articles/765944/)
*[](https://api7.ai/tyk-vs-kong)

## Measurements (Измерения)
N/A
