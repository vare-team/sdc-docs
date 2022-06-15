---
description: Отправка данных о количестве серверов и шардов.
---

# SDC Bots

{% api baseUrl="https://api.server-discord.com/v2" method="post" path="/bots/:id/stats" summary="Send bot data" %}

{% api-parameter in="path" name="id" type="string" required="true" %}
Bot ID
{% endapi-parameter %}

{% api-parameter in="header" name="Authorization" type="string" required="true" %}
SDC Token
{% endapi-parameter %}

{% api-parameter in="body" name="shards" type="number" required="true" %}
Количество шардов, не менее 1
{% endapi-parameter %}

{% api-parameter in="body" name="servers" type="number" required="true" %}
Количество серверов, не менее 1
{% endapi-parameter %}

{% api-response status="200" description="Данные успешно установлены" %}
```javascript
{
  "status": true
}
```
{% endapi-response %}

{% api-response status="404" description="Формат ошибок" %}
```javascript
{
  "error": {
    "msg": "Page not found",
    "type": "NOT FOUND",
    "code", 404
  }
}
```
{% endapi-response %}

{% endapi %}

### Ограничения

{% hint style="danger" %}
Вы не можете делать больше 2 запросов за 1 минуту.
{% endhint %}
