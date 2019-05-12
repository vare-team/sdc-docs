---
description: Публичный чёрный список IDшников спамеров и их гнёзд(серверов).
---

# SDC Blacklist

{% hint style="info" %}
Если не добавлять ID к запросу, то вернутся данные о сервере, на котором был сгенерирован ключ!
{% endhint %}

{% api-method method="get" host="https://api.server-discord.com" path="/warns/:id" %}
{% api-method-summary %}
Get warns
{% endapi-method-summary %}

{% api-method-description %}
Получить варны человека или сервера
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="dKey" type="string" required=true %}
Ключ разработчика
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "id":"000000000000000000",
    "type":"user",
    "warns":1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



