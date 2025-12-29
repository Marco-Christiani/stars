---
repo: firebase/firebase-functions-python
url: 'https://github.com/firebase/firebase-functions-python'
homepage: null
starredAt: '2023-06-04T04:14:41Z'
createdAt: '2022-08-25T23:03:16Z'
updatedAt: '2025-12-20T18:52:18Z'
language: Python
license: Apache-2.0
branch: main
stars: 162
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:58.625Z'
description: null
tags: []
---

# Cloud Functions for Firebase Python SDK

The [`firebase-functions`](https://pypi.org/project/firebase-functions/) package provides an SDK for defining Cloud Functions for Firebase in Python.

Cloud Functions provides hosted, private, and scalable environment where you can run server code. The Firebase SDK for Cloud Functions integrates the Firebase platform by letting you write code that responds to events and invokes functionality exposed by other Firebase features.

## Learn more

Learn more about the Firebase SDK for Cloud Functions in the [Firebase documentation](https://firebase.google.com/docs/functions/) or [check out our samples](https://github.com/firebase/functions-samples).

Here are some resources to get help:

- Start with the quickstart: <https://firebase.google.com/docs/functions/get-started>
- Go through the guide: <https://firebase.google.com/docs/functions/>
- Read the full API reference: <https://firebase.google.com/docs/reference/functions/2nd-gen/python>
- Browse some examples: <https://github.com/firebase/functions-samples>

If the official documentation doesn't help, try asking through our official support channels: <https://firebase.google.com/support/>

## Usage

```python
# functions/main.py
from firebase_functions import db_fn
from notify_users import api

@db_fn.on_value_created(reference="/posts/{post_id}")
def new_post(event):
    print(f"Received new post with ID: {event.params.get('post_id')}")
    return notifyUsers(event.data)
```

## Contributing

To contribute a change, [check out the contributing guide](.github/CONTRIBUTING.md).

## License

© Google, 2025. Licensed under [Apache License](LICENSE).

