---
description: >-
  This page contains some small code snippets to interact with the Radiopanel
  api through JS
---

# JavaScript

## Get the live DJ

```javascript
fetch('https://api.radiopanel.co/api/v1/slots/live', {
    headers: {
        "x-tenant": "YOUR_TENANT_UUID",
        "authorization": "YOUR_AUTHORIZATION_HEADER"
    }
})
    .then((result) => result.json())
    .then((slot) => {
        // This function gets triggered when someone is live
        document.querySelector('.dj-name').innerHTML = slot.user.firstName;
        document.querySelector('.dj-avatar').src = slot.user.avatar || "LINK_TO_DEFAULT_AVATAR";
    })
    .catch(() => {
        // This function gets triggered when no one is live
        document.querySelector('.dj-name').innerHTML = "AutoDJ";
        document.querySelector('.dj-avatar').src = "LINK_TO_DEFAULT_AVATAR";
    });
```

