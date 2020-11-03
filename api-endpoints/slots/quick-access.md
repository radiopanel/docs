# Get multiple slots

{% api-method method="get" host="https://api.radiopanel.co" path="/api/v1/slots" %}
{% api-method-summary %}
List slots
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-tenant" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="authorization" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="beforeDate" type="number" required=false %}
UNIX timestamp
{% endapi-method-parameter %}

{% api-method-parameter name="afterDate" type="number" required=false %}
UNIX timestamp
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "_embedded": [
        {
            "uuid": "7a751c6b-7b77-40e9-b8a1-979fa625d330",
            "title": "New slot",
            "tenantUuid": "141bc871-f1e5-44b9-98f7-59fd1e31faea",
            "userUuid": "d7facb17-6012-48d3-b560-d039b5f043c7",
            "slotTypeUuid": "90731312-6a6e-4e75-8856-42a67f65b2f2",
            "start": 1604415600,
            "end": 1604419200,
            "recurring": false,
            "updatedAt": "2020-11-03T15:25:55.903Z",
            "createdAt": "2020-11-03T15:25:55.903Z",
            "slotType": {
                "uuid": "90731312-6a6e-4e75-8856-42a67f65b2f2",
                "name": "Podcast",
                "tenantUuid": "141bc871-f1e5-44b9-98f7-59fd1e31faea",
                "description": "Podcast show",
                "color": "#b80000",
                "updatedAt": "2020-06-25T18:08:44.779Z",
                "createdAt": "2020-06-25T18:08:44.779Z"
            },
            "user": {
                "uuid": "d7facb17-6012-48d3-b560-d039b5f043c7",
                "firstName": "Felikx",
                "lastName": "",
                "avatar": "https://radiopanel.s3.nl-ams.scw.cloud/c9a65443-eed1-41ed-b9d2-743223b5ee75/bcab441c-88a4-4198-8d5d-cee0d6852a6c.png",
                "bio": "Radiopanel Developer",
                "email": "hidden",
                "password": "hidden",
                "updatedAt": "2020-05-16T13:42:38.142Z",
                "admin": true,
                "createdAt": "2020-05-16T13:42:38.142Z",
                "socials": {
                    "twitch": "",
                    "discord": "",
                    "twitter": "https://twitter.com/FelikxVanSaet",
                    "youtube": "",
                    "facebook": "",
                    "instagram": ""
                }
            }
        }
    ],
    "_page": {
        "totalEntities": 0
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



