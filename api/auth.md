---
description: 'api for Auth'
---

# Auth

{% api-method method="post" host="https://api.todo-scheduler.com" path="/api/auth/signup" %}
{% api-method-summary %}
Sign up 
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
The plain password is encrypted by bycrypt
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
automatically sign in, after completely sign up.
{% endapi-method-response-example-description %}

```text
{
  "grantType": "bearer",
  "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJhdXRoIjoiUk9MRV9VU0VSIiwibmFtZSI6ImpveWxpc2giLCJleHAiOjE2MjYwNDM2ODU1MDZ9.PRMXi5ICATcvOA0oqzVVAG9AjVJh1JJprTHlx8-hVsq7oEk-Zo3BBo-icqAr_TFWiO3rv8Om14LqW1wc1LfkOg",
  "refreshToken": "eyJhbGciOiJIUzUxMiJ9.eyJleHAiOjE2MTU3MTczNjV9.tZytWyCWkWIYitvT3pa8FSnxilBDMtSevUzKRFK21TGLITf2eLXEwNNS_Q7rylD9uUe3Rx9ZR2NVqE_ZNWxTqg",
  "expiredAt": 1615114365284
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{    
    "message": "Check value of properties"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.todo-scheduler.com" path="/api/auth/signin" %}
{% api-method-summary %}
Sign in
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
The plain password is encrypted by bycrypt
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "grantType": "bearer",
  "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJhdXRoIjoiUk9MRV9VU0VSIiwibmFtZSI6ImpveWxpc2giLCJleHAiOjE2MjYwNDM2ODU1MDZ9.PRMXi5ICATcvOA0oqzVVAG9AjVJh1JJprTHlx8-hVsq7oEk-Zo3BBo-icqAr_TFWiO3rv8Om14LqW1wc1LfkOg",
  "refreshToken": "eyJhbGciOiJIUzUxMiJ9.eyJleHAiOjE2MTU3MTczNjV9.tZytWyCWkWIYitvT3pa8FSnxilBDMtSevUzKRFK21TGLITf2eLXEwNNS_Q7rylD9uUe3Rx9ZR2NVqE_ZNWxTqg",
  "expiredAt": 1615114365284
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.todo-scheduler.com" path="/api/auth/reissue" %}
{% api-method-summary %}
Reissue access token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Content-Type" type="string" required=true %}
application/json
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="accessToken" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="refreshToken" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "grantType": "bearer",
  "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJhdXRoIjoiUk9MRV9VU0VSIiwibmFtZSI6ImpveWxpc2giLCJleHAiOjE2MjYwNDM2ODU1MDZ9.PRMXi5ICATcvOA0oqzVVAG9AjVJh1JJprTHlx8-hVsq7oEk-Zo3BBo-icqAr_TFWiO3rv8Om14LqW1wc1LfkOg",
  "refreshToken": "eyJhbGciOiJIUzUxMiJ9.eyJleHAiOjE2MTU3MTczNjV9.tZytWyCWkWIYitvT3pa8FSnxilBDMtSevUzKRFK21TGLITf2eLXEwNNS_Q7rylD9uUe3Rx9ZR2NVqE_ZNWxTqg",
  "expiredAt": 1615114365284
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="" %}
{% api-method-summary %}
Sign out \(none\)
{% endapi-method-summary %}

{% api-method-description %}
!! Browser just delete tokens, not request to server
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

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

