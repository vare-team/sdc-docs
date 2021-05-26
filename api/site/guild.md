# Guild

{% hint style="info" %}
Если не добавлять ID к запросу, то вернутся данные о сервере, на котором был сгенерирован ключ!
{% endhint %}

{% api-method method="get" host="https://api.server-discord.com/v2" path="/guild/:id" %}
{% api-method-summary %}
Get guild
{% endapi-method-summary %}

{% api-method-description %}
Информация о сервере
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID сервера
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
Если вы хотите проверить, есть ли значок **Пасхантер**, всё что нужно сделать - это использовать побитовый оператор.
{% endhint %}

```javascript
const status = 40;
status & 8   //True (Фаротика)
status & 10  //False (Баг хантер)
status & 20  //True (Пасхантер)
```

{% tabs %}
{% tab title="Информация о статусах" %}
```javascript
sitedev: 1
verefied: 2
partner: 4
favorite 8
bughunter: 16
easteregg: 32
botdev: 64
youtube: 128
twitch: 256
spamhunt: 512
```
{% endtab %}
{% endtabs %}

{% api-method method="get" host="https://api.server-discord.com/v2" path="/guild/:id/place" %}
{% api-method-summary %}
Get place
{% endapi-method-summary %}

{% api-method-description %}
Получить место сервера в списке
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID сервера
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
    "place": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.server-discord.com/v2" path="/guild/:id/rated" %}
{% api-method-summary %}
Get rated
{% endapi-method-summary %}

{% api-method-description %}
Получить всех проголосовавших пользователей и их оценки
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
ID сервера
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



