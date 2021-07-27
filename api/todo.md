---
description: 'description: api for todo'
---

# Todo

{% api-method method="get" host="https://api.todo-scheduler.com" path="/api/todo?date=yyyy-mm-dd" %}
{% api-method-summary %}
Todos by date 
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

{% api-method-query-parameters %}
{% api-method-parameter name="date" type="string" required=true %}
format 'yyyy-mm-dd'
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "todos " : [
        {
                    "todoId" : 1,
                    "todoDate" : "2021-07-21 14:11:09",
                    "todoContents" : "입실체크하기",
                    "todoStatus" : false
        },
        {
                    "todoId" : 2,
                    "todoDate" : "2021-07-25 15:26:09",
                    "todoContents" : "엄마 안부전화",
                    "todoStatus" : true
        }
    ]

}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.todo-scheduler.com" path="/api/todo" %}
{% api-method-summary %}
Create Todo
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
{% api-method-parameter name="todoContents" type="string" required=true %}
must be from 2 to 80 bytes
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
    "todoId" : 1,
    "todoDate" : "2021-07-21 14:11:09",
    "todoContents" : "입실체크하기",
    "todoStatus" : false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="patch" host="https://api.todo-scheduler.com" path="/api/todo/:todoId" %}
{% api-method-summary %}
Update Todo
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
{% api-method-parameter name="todoContents" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="todoStatus" type="boolean" required=false %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
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

{% api-method method="delete" host="https://api.todo-scheduler.com" path="/api/todo/:todoId" %}
{% api-method-summary %}
Remove Todo
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

