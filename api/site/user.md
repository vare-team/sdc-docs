# User

{% api-method method="get" host="https://api.server-discord.com/v2" path="/user/:id/rated" %}
{% api-method-summary %}
Get rated servers
{% endapi-method-summary %}

{% api-method-description %}
Получение списка id серверов и статуса голосования на них
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID пользователя
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
    //1: Положительная оценка.
    //-1: отрицательная оценка.
    "000000000000000000": 1,
    "111111111111111111": 1,
    "222222222222222222": 1,
    "333333333333333333": 1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



