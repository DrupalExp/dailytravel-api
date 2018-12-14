---
description: qweqweqw
---

# User

```javascript
{ 
   handleEnter: { 
     key: 13, 
     handler: function (range, context) { 
       if (range.length > 0) { this.quill.scroll.deleteAt(range.index, range.length); // So we do not trigger text-change } let lineFormats = Object.keys(context.format).reduce(function(lineFormats, format) { if (Parchment.query(format, Parchment.Scope.BLOCK) && !Array.isArray(context.format[format])) { lineFormats[format] = context.format[format]; } return lineFormats; }, {}); var previousChar = this.quill.getText(range.index - 1, 1); // Earlier scroll.deleteAt might have messed up our selection, // so insertText's built in selection preservation is not reliable this.quill.insertText(range.index, '\n', lineFormats, Quill.sources.USER); if (previousChar == '' || previousChar == '\n') { this.quill.setSelection(range.index + 2, Quill.sources.SILENT); } else { this.quill.setSelection(range.index + 1, Quill.sources.SILENT); } this.quill.selection.scrollIntoView(); Object.keys(context.format).forEach((name) => { if (lineFormats[name] != null) return; if (Array.isArray(context.format[name])) return; if (name === 'link') return; this.quill.format(name, context.format[name], Quill.sources.USER); }); } } }

```

{% api-method method="get" host="https://dailytravel.app" path="/v1/cakes/:id?\_format=json" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" %}
ID of the cake to get, for free of course.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer jwt\_token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="recipe" type="string" %}
The API will do its best to find a cake matching the provided recipe.
{% endapi-method-parameter %}

{% api-method-parameter name="gluten" type="boolean" %}
Whether the cake should be gluten-free or not.
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
    "name": "Cake's name",
    "recipe": "Cake's recipe name",
    "cake": "Binary cake"
}
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

* [ ] Task 1
* [x] Task 2

{% hint style="info" %}
**Token** is not require for this action
{% endhint %}

| Params | Type | Description |
| :--- | :--- | :--- |
| \_format | string |  |





## Hello



