---
description: Отправка данных о количестве серверов и шардов.
---

# SDC Bots

{% api-method method="post" host="https://api.server-discord.com/v2" path="/bots/:id/stats" %}
{% api-method-summary %}
Send bot data
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Bot ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
SDC Token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="shards" type="number" required=false %}
Количество шардов
{% endapi-method-parameter %}

{% api-method-parameter name="servers" type="number" required=false %}
Количество серверов
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Данные успешно установлены
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



