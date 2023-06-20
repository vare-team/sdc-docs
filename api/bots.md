---
description: Отправка данных о количестве серверов и шардов.
---

# SDC Bots

{% swagger method="post" path="/bots/:id/stats" baseUrl="https://api.server-discord.com/v2" summary="Send bot data" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" required="true" name="id" type="String" %}
Айди бота
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" required="true" type="String" %}
SDC Token
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="servers" type="Number" %}
Количество серверов, не менее 1
{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="shards" type="Number" %}
Количество шардов, не менее 1
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Данные успешно установлены" %}
```javascript
{
  "status": true
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Формат ошибок" %}
```javascript
{
  "error": {
    "msg": "Page not found",
    "type": "NOT FOUND",
    "code": 404
  }
}
```
{% endswagger-response %}
{% endswagger %}

### Ограничения

{% hint style="danger" %}
Вы не можете делать больше 2 запросов за 1 минуту.
{% endhint %}
