# Song History

{% api-method method="get" host="https://api.radiopanel.co" path="/api/v1/song-history" %}
{% api-method-summary %}
Song history
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
{% api-method-parameter name="pagesize" type="number" required=false %}
Size of the page
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="number" required=false %}
Page nr
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
            "uuid": "a9b05827-ea84-4785-8529-5e297cf4572f",
            "songUuid": "e1097dd8-5af9-4cf3-8921-a4d3b083e21f",
            "tenantUuid": "ba7a7cb1-0a0d-49be-bb95-186f3346fea5",
            "slotUuid": null,
            "createdAt": "2020-11-03T15:21:36.903Z",
            "song": {
                "uuid": "e1097dd8-5af9-4cf3-8921-a4d3b083e21f",
                "externalId": "84005735a41c58041c979221c20ae704",
                "title": "Dear Future Husband",
                "artist": "Meghan Trainor",
                "album": "Title (Deluxe)",
                "originalTitle": "Meghan Trainor - Dear Future Husband",
                "previewUrl": "https://p.scdn.co/mp3-preview/c6b59581df7d714784e538eeb198934990934c3b?cid=8cc80ab9c4f846b699befef45cf9dd02",
                "durationMs": 184226,
                "releaseDate": "2015-01-09T00:00:00.000Z",
                "graphic": {
                    "large": "https://i.scdn.co/image/ab67616d0000b2733b11178cccd78ec77fc12dbc",
                    "small": "https://i.scdn.co/image/ab67616d000048513b11178cccd78ec77fc12dbc",
                    "medium": "https://i.scdn.co/image/ab67616d00001e023b11178cccd78ec77fc12dbc"
                },
                "extraInfo": {
                    "album": {
                        "id": "5W98Ab4VvQEuFEE4TIe5fE",
                        "uri": "spotify:album:5W98Ab4VvQEuFEE4TIe5fE",
                        "href": "https://api.spotify.com/v1/albums/5W98Ab4VvQEuFEE4TIe5fE",
                        "album_type": "album",
                        "release_date": "2015-01-09",
                        "total_tracks": 15,
                        "external_urls": {
                            "spotify": "https://open.spotify.com/album/5W98Ab4VvQEuFEE4TIe5fE"
                        },
                        "release_date_precision": "day"
                    },
                    "track": {
                        "id": "3cU2wBxuV6nFiuf6PJZNlC",
                        "uri": "spotify:track:3cU2wBxuV6nFiuf6PJZNlC",
                        "href": "https://api.spotify.com/v1/tracks/3cU2wBxuV6nFiuf6PJZNlC",
                        "explicit": false,
                        "external_urls": {
                            "spotify": "https://open.spotify.com/track/3cU2wBxuV6nFiuf6PJZNlC"
                        }
                    },
                    "artist": {
                        "id": "6JL8zeS1NmiOftqZTRgdTz",
                        "uri": "spotify:artist:6JL8zeS1NmiOftqZTRgdTz",
                        "href": "https://api.spotify.com/v1/artists/6JL8zeS1NmiOftqZTRgdTz",
                        "name": "Meghan Trainor"
                    }
                },
                "tenantUuid": "ba7a7cb1-0a0d-49be-bb95-186f3346fea5",
                "updatedAt": "2020-09-19T22:25:11.431Z",
                "createdAt": "2020-09-19T22:25:11.431Z"
            },
            "slot": null
        },
        {
            "uuid": "2c9d6549-d400-4116-90ca-89eec0ae59e7",
            "songUuid": "70698488-a53f-4721-ab83-f29f05172e7d",
            "tenantUuid": "ba7a7cb1-0a0d-49be-bb95-186f3346fea5",
            "slotUuid": null,
            "createdAt": "2020-11-03T15:17:26.475Z",
            "song": {
                "uuid": "70698488-a53f-4721-ab83-f29f05172e7d",
                "externalId": "e16b678474fb52b6a159a91258f05f10",
                "title": "Love Again (Horse Meat Disco Remix)",
                "artist": "Dua Lipa",
                "album": "Love Again (Horse Meat Disco Remix)",
                "originalTitle": "Dua Lipa - Love Again",
                "previewUrl": "https://p.scdn.co/mp3-preview/35f37922b7219fcecedf42129554111c9442a38a?cid=8cc80ab9c4f846b699befef45cf9dd02",
                "durationMs": 331813,
                "releaseDate": "2020-09-11T00:00:00.000Z",
                "graphic": {
                    "large": "https://i.scdn.co/image/ab67616d0000b273e17ae8a7e12a286de2ae3c32",
                    "small": "https://i.scdn.co/image/ab67616d00004851e17ae8a7e12a286de2ae3c32",
                    "medium": "https://i.scdn.co/image/ab67616d00001e02e17ae8a7e12a286de2ae3c32"
                },
                "extraInfo": {
                    "album": {
                        "id": "1y2LqeaZgsAghX8GJge48N",
                        "uri": "spotify:album:1y2LqeaZgsAghX8GJge48N",
                        "href": "https://api.spotify.com/v1/albums/1y2LqeaZgsAghX8GJge48N",
                        "album_type": "single",
                        "release_date": "2020-09-11",
                        "total_tracks": 1,
                        "external_urls": {
                            "spotify": "https://open.spotify.com/album/1y2LqeaZgsAghX8GJge48N"
                        },
                        "release_date_precision": "day"
                    },
                    "track": {
                        "id": "79b6pe9ecV33Pxi4yAQAIc",
                        "uri": "spotify:track:79b6pe9ecV33Pxi4yAQAIc",
                        "href": "https://api.spotify.com/v1/tracks/79b6pe9ecV33Pxi4yAQAIc",
                        "explicit": false,
                        "external_urls": {
                            "spotify": "https://open.spotify.com/track/79b6pe9ecV33Pxi4yAQAIc"
                        }
                    },
                    "artist": {
                        "id": "6M2wZ9GZgrQXHCFfjv46we",
                        "uri": "spotify:artist:6M2wZ9GZgrQXHCFfjv46we",
                        "href": "https://api.spotify.com/v1/artists/6M2wZ9GZgrQXHCFfjv46we",
                        "name": "Dua Lipa"
                    }
                },
                "tenantUuid": "ba7a7cb1-0a0d-49be-bb95-186f3346fea5",
                "updatedAt": "2020-09-18T22:47:10.193Z",
                "createdAt": "2020-09-18T22:47:10.193Z"
            },
            "slot": null
        }
    ],
    "_page": {
        "totalEntities": 23744,
        "currentPage": 1,
        "itemsPerPage": 20
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



