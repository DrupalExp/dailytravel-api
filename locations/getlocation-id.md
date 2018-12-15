# GetLocation:id

{% api-method method="get" host="https://APIURL" path="/v1/location/:id" %}
{% api-method-summary %}
Get location by 
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get location by id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
ID of the location
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="fields" type="string" %}
**all** or comma separated list of **fields:**  
id, name, slug, location, images, summary, content, timezone, currency, status, parent\_id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Location successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "name": "Viet Nam",
    "slug": "/location/viet-nam",
    "location": "5.6283253,96.8623023"
    "images": "[path1, path2]",
    "summary": "test summary",
    "content": "tets content",
    "timezone": "GMT+7",
    "currentcy": "vn",
    "status": 1,
    "parent_id": 1,
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "message": "There is no location found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



