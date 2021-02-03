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

{% api-method method="get" host="/" path="users/:id" %}
{% api-method-summary %}
Get User
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Die ID des Users
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentifizierung um die Berechtigungen des Benutzers zu überprüfen
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
    "code": 404,
    "message": "User existiert nicht"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="/" path="users" %}
{% api-method-summary %}
Create User
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentifizierung um die Berechtigungen des Benutzers zu überprüfen
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="klasse" type="string" required=false %}
Die Klasses eines Benutzers
{% endapi-method-parameter %}

{% api-method-parameter name="rolle" type="integer" required=false %}
Die ID der Rolle des Benutzers, wenn nicht angegeben, wird die default Rolle verwended
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Die Email des Benutzers
{% endapi-method-parameter %}

{% api-method-parameter name="nachname" type="string" required=true %}
Der Nachname des Benutzers
{% endapi-method-parameter %}

{% api-method-parameter name="vorname" type="string" required=true %}
Der Vorname des Benutzers
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" required=true %}
Der Benutzername
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "id": 1234567890,
    "username": "MaxMusterman",
    "vorname": "Max",
    "nachname": "Musterman",
    "email": "mac@example.com",
    "rolle": 123
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "code": 401,
    "message": "Benutzer nicht authorisiert"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="/" path="users/:id" %}
{% api-method-summary %}
Delete User
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
Die ID des Benutzers der gelöscht werden soll
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentifizierung, um die Berectigungen des Benutzers zu überprüfen
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "code": 200,
    "message": "Benutzer gelöscht"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



