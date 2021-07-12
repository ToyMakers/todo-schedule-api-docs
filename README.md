
---
description: api for todo
---

# Todo

{% api-method method="get" host="https://api.cakes.com" path="/api/todo" %}
{% api-method-summary %}
All Todo
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer \[access token\]
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "result" : [
        {
            "todoId" : 1,
            "createdAt" : 1626046618378,
            "items" :[
                {
                    "todoItemId" : 1,
                    "addedAt" : 1626046618491,
                    "contents" : "입실체크하기",
                    "status" : true
                },
                {
                    "todoItemId" : 2,
                    "addedAt" : 1626046625491,
                    "contents" : "엄마 안부전화",
                    "status" : true
                },
            ]
        },
        {
            "todoId" : 2,
            "createdAt" : 1626058918378,
            "items" :[
                {
                    "todoItemId" : 3,
                    "addedAt" : 1626047618491,
                    "contents" : "vue 과제하",
                    "status" : false
                },
                {
                    "todoItemId" : 4,
                    "addedAt" : 1626047725491,
                    "contents" : "spring 과제하기",
                    "status" : false
                },
            ]
        }
    ]

}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.cakes.com" path="/api/todo" %}
{% api-method-summary %}
Create Todo list
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer \[access token\]
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "todoId" : 1
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.cakes.com" path="/api/todo/:todoId" %}
{% api-method-summary %}
Add Todo Item
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer \[access token\]
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="contents" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="status" type="boolean" required=true %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "todoId" : 1,
    "todoItemId" : 4,
    "contents" : "docker 실습 정리해서 글쓰기",
    "status" : false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.cakes.com" path="/api/todo/:todoId" %}
{% api-method-summary %}
Update Todo Item
{% endapi-method-summary %}

{% api-method-description %}
!! should include contents or status in body
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="todoId" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer \[access token\]
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="contents" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="status" type="boolean" required=false %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "todoId" : 1,
    "todoItemId" : 4,
    "contents" : "jenkins 실습 정리해서 글쓰기",
    "status" : false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.cakes.com" path="/api/todo/:todoId" %}
{% api-method-summary %}
Remove Todo Item
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Bearer \[access token\]
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "todoId" : 1,
    "todoItemId" : 4
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}


