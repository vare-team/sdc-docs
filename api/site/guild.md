# Guild

{% hint style="info" %}
Если не добавлять ID к запросу, то вернутся данные о сервере, на котором был сгенерирован ключ!
{% endhint %}

{% api-method method="get" host="https://api.server-discord.com/v1" path="/guild/:id" %}
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
  "avatar": "a_8f05534e4f750cf535988ae8a91fe9ad",
  "lang": "ru",
  "name": "SD.Community",
  "des": "Описание сервера",
  "invite": "https://discord.gg/GWTcywt",
  "owner": "MegaVasiliy007#3301",
  "online": 250,
  "members": 500,
  "bot": 1,
  "boost": 3,
  "status": 8,
  "upCount": 299,
  "tags": "communication,programming,community"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Если вы хотите проверить, есть ли значок **Разработчик Сайта**, всё что нужно сделать - это использовать побитовый оператор.
{% endhint %}

```javascript
const status = 40;
status & 8   //True (Разработчик сайта)
status & 10  //False (Фаворитка)
status & 20  //True (Баг хантер)
```

{% code-tabs %}
{% code-tabs-item title="Информация о статусах" %}
```javascript
botdev: 0x1
partner: 0x2
verefied: 0x4
sitedev: 0x8
favorite: 0x10
bughunter: 0x20
easteregg: 0x40
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% api-method method="get" host="https://api.server-discord.com/v1" path="/guild/:id/place" %}
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

{% api-method method="get" host="https://api.server-discord.com/v1" path="/guild/:id/rated" %}
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

