---
description: Get all locations
---

# GetLocations

{% api-method method="get" host="https://APIURL" path="/v1/locations" %}
{% api-method-summary %}
Get all locations
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all locations.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="fields" type="string" required=false %}
**all** or comma separated list of **fields**:  
id, name, slug, location, images, summary, content, timezone, currency, status, parent\_id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "parent_id": 1,
    "name": "Location name",
    "slug": "location path",
    "image": "image path"
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



