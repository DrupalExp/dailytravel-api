# Get Activities

{% api-method method="get" host="https://APIURL" path="/v1/activities" %}
{% api-method-summary %}
Get all Activit
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get all .
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token to track down who is emptying our stocks
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="fields" type="string" required=false %}
all or comma separated list of fields:  
id, name, slug, summary, content, images, cat\_id, log\_id, information, guide, address, open\_time, intro\_video, status
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
        "id": 1,
        "name": "du lich ba na",
        "slug": "/activity/du-lich-ba-na",
        "summary": "test summary"
        "content": "test content",
        "images": "[image path1, image path2]",
        "cat_id": 1,
        "log_id": 1,
        "information": "test information",
        "guide": "test guide",
        "address": "da nang, viet nam",
        "open_time": "08am-22pm",
        "intro_video": "video path",
        "status": 1,
    },
    {
        "id": 2,
        "name": "vinpearl da nang",
        "slug": "/activity/vinpearl-da-nang",
        "summary": "test summary"
        "content": "test content",
        "images": "[image path1, image path2]",
        "cat_id": 1,
        "log_id": 1,
        "information": "test information",
        "guide": "test guide",
        "address": "da nang, viet nam",
        "open_time": "08am-22pm",
        "intro_video": "video path",
        "status": 1,
    },
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
    "message": "There is no activity found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



