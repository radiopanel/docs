---
description: >-
  This page contains some small code snippets to interact with the Radiopanel
  api through Python
---

# Python

## Get the live DJ

```python
import requests
headers = {
    "Authorization": "YOUR_AUTHORIZATION_HEADER",
    "X-Tenant": "YOUR_TENANT_UUID"
}

j = requests.get("https://api.radiopanel.co/api/v1/slots/live", headers=headers)

if j.text == "":
    # This function gets triggered when someone is live.
    t = "Auto DJ"
else:
    # This function gets triggered when no one is live.
    json = j.json()
    t = str(json["user"]["firstName"])
```



