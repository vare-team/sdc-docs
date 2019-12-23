---
description: Публичный чёрный список ID спамеров и их гнёзд (серверов).
---

# SDC Blacklist

{% api-method method="get" host="https://api.server-discord.com/v2" path="/warns/:id" %}
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

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
SDC Token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "id": "000000000000000000",
    "type": "user",
    "warns": 1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

