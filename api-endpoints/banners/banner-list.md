---
description: Get banners for your radio's website.
---

# Banner List

{% api-method method="get" host="https://api.radiopanel.co" path="/api/v1/banners" %}
{% api-method-summary %}
Get the banner list
{% endapi-method-summary %}

{% api-method-description %}
Get the list of banners
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="X-Tenant" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="Authentication" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Banner found and returned
{% endapi-method-response-example-description %}

```text
{
  "_embedded": [
    {
      "uuid": "1437e326-90d0-4172-a31c-65fe74cad3b3",
      "name": "radiopaneldiscord",
      "slug": "rpdisc",
      "link": "https://discord.gg/Mr9yZbxEZW",
      "tag": "sitebanners",
      "image": "https://radiopanel.s3.nl-ams.scw.cloud/141bc871-f1e5-44b9-98f7-59fd1e31faea/1437e326-90d0-4172-a31c-65fe74cad3b3.png",
      "tenantUuid": "141bc871-f1e5-44b9-98f7-59fd1e31faea",
      "updatedAt": "2020-12-08T10:24:22.488Z",
      "createdAt": "2020-12-08T10:24:22.488Z"
    }
  ],
  "_page": {
    "totalEntities": 1,
    "currentPage": 1,
    "itemsPerPage": 20
  }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
No banners found
{% endapi-method-response-example-description %}

```text
{
  "_embedded": [

  ],
  "_page": {
    "totalEntities": 0,
    "currentPage": 1,
    "itemsPerPage": 20
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

