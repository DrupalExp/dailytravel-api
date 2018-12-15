# users

{% api-method method="get" host="https://domain.com" path="/api/v1/users?\_format=json" %}
{% api-method-summary %}
List all users
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all users.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
    "name":"simon",
    "mail":"tusinh.information@gmail.com",
    "roles":"administrator",
    "status":"1"
  },
  {
    "name":"username2",
    "mail":"username2@test.com",
    "roles":"",
    "status":"1"
  }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": ""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Example:

```javascript
axios.get('https://apiurl.com/api/v1/users?_format=json', {
  headers: {
    Authorization: 'Bearer token_string'
  }
}).then(response => {
  console.log(response.data);
}).catch(error => {
  console.log(error.response.data.message);
})
```



