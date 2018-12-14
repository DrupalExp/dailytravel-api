# List users

{% api-method method="get" host="https://apiurl.com" path="/api/v1/users?\_format=json" %}
{% api-method-summary %}
List all users
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="status" type="number" %}
Filter by user's status.  
0: blocked, 1 active. Default is 1
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
The access token start with "Bearer "
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="role" type="string" %}
Filter users by their role.  
Available roles: **administrator**, **partner**..
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="number" %}
Filter users by user's status.  
0: blocked.  
1: active  
default: 1
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
[
    {
        "uid":[{"value":7}],
        "uuid":[{"value":"f764b60e-22f6-49fb-adce-2a5193221e90"}],
        "langcode":[{"value":"en"}],
        "preferred_langcode":[{"value":"en"}],
        "preferred_admin_langcode":[{"value":"en"}],
        "name":[{"value":"simon"}],
        "mail":[{"value":"test@test.com"}],
        "timezone":[{"value":"Asia\/Krasnoyarsk"}],
        "status":[{"value":true}],
        "created":[{"value":"2018-12-13T07:45:06+00:00","format":"Y-m-d\\TH:i:sP"}],
        "changed":[{"value":"2018-12-13T09:16:38+00:00","format":"Y-m-d\\TH:i:sP"}],
        "access":[{"value":"2018-12-13T10:04:46+00:00","format":"Y-m-d\\TH:i:sP"}],
        "login":[{"value":"2018-12-13T08:15:58+00:00","format":"Y-m-d\\TH:i:sP"}],
        "init":[{"value":"tusinh.information@gmail.com"}],
        "roles":[{"target_id":"administrator","target_type":"user_role","target_uuid":"2bd96fbc-303c-4ad2-8f5b-c6d136046780"}],
        "default_langcode":[{"value":true}],
        "path":[{"alias":null,"pid":null,"langcode":"en"}],
        "user_picture":[]
    }
    ...
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "Ain't no cake like that."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



