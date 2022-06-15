---
description: Отправка данных о количестве серверов и шардов.
---

# SDC Bots

{% botsapi baseUrl="https://api.server-discord.com/v2" method="post" path="/bots/:id/stats" summary="Send bot data" %}

{% botsapi-parameter in="path" name="id" type="string" required="true" %}
Bot ID
{% endbotsapi-parameter %}

{% botsapi-parameter in="header" name="Authorization" type="string" required="true" %}
SDC Token
{% endbotsapi-parameter %}

{% botsapi-parameter in="body" name="shards" type="number" required="true" %}
Количество шардов, не менее 1
{% endbotsapi-parameter %}

{% botsapi-parameter in="body" name="servers" type="number" required="true" %}
Количество серверов, не менее 1
{% endbotsapi-parameter %}

{% botsapi-response status="200" description="Данные успешно установлены" %}
```javascript
{
  "status": true
}
```
{% endbotsapi-response %}

{% botsapi-response status="404" description="Формат ошибок" %}
```javascript
{
  "error": {
    "msg": "Page not found",
    "type": "NOT FOUND",
    "code", 404
  }
}
```
{% endbotsapi-response %}

{% endbotsapi %}

### Ограничения

{% hint style="danger" %}
Вы не можете делать больше 2 запросов за 1 минуту.
{% endhint %}
