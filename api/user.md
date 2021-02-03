# User

| Name | Type | Description |
| :--- | :--- | :--- |
| **id** | int | Die ID eines User |
| **username** | String |  |
| **vorname** | String |  |
| **nachname** | String |  |
| rolle | Rolle |  |
| email | email |  |
| klasse | String | _optional_ |

{% api-method method="get" host="/" path="users/{user.id}" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
Die ID des Users
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentifizierung um die Berechtigungen des Benutzers abzufragen
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1234567890,
    "username": "MaxMusterman",
    "vorname": "Max",
    "nachname": "Musterman",
    "email": "max@example.com",
    "klasse": "0c"
    "rolle": {
        "id": 1234567890,
        "permissions": []
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "error": 404,
    "message": "User existiert nicht"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



