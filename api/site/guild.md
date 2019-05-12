# Guild

{% hint style="info" %}
Если не добавлять ID к запросу, то вернутся данные о сервере, на котором был сгенерирован ключ!
{% endhint %}

{% api-method method="get" host="https://api.server-discord.com" path="/guild/:id" %}
{% api-method-summary %}
Get guild
{% endapi-method-summary %}

{% api-method-description %}
Информация о сервере
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
ID сервера
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
  "avatar":"https://cdn.discordapp.com/icons/464270024518008863/ad570812a5408afac56ec58ffbf553d8.jpg",
  "lang":"ru",
  "rating":100,
  "name":"SD.Community",
  "des":"Описание сервера",
  "invite":"https://discord.gg/GWTcywt",
  "owner":"MegaVasiliy007#3301",
  "online":250,
  "members":500,
  "bot":1,
  "boost":3,
  "status":8,
  "color":"#53cca8",
  "upCount":299,
  "tags":"communication,programming,community"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.server-discord.com" path="/guild/:id/place" %}
{% api-method-summary %}
Get place
{% endapi-method-summary %}

{% api-method-description %}
Получить место сервера в списке
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
ID сервера
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
    "place": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.server-discord.com" path="/guild/:id/rated" %}
{% api-method-summary %}
Get rated
{% endapi-method-summary %}

{% api-method-description %}
Получить всех проголосовавших пользователей и их оценки
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=false %}
ID сервера
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
    "000000000000000000":1,
    "111111111111111111":1,
    "222222222222222222":1,
    "333333333333333333":1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

