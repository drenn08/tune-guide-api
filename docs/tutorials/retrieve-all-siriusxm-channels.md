---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
parent: Tutorials
# tags used by AI files
description: Find `channel` resources by genre
tags:
    - api
categories: 
    - tutorial
ai_relevance: high
importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/channels
related_pages: []
examples: []
api_endpoints:
    - GET /channels
version: "v1.0"
last_updated: "2025-09-03"
# vale  on
# markdownlint-enable
---

# Tutorial: Get a complete list of all available SiriusXM channels

In this tutorial, you'll learn how to use the GEt /channels endpoint to retrieve a list of all SiriusXM channels.

**Time to complete**: 10-15 minutes

## What you'll achieve

- Find all channels in SiriusXM in the Channels resource.
- Get more information about the request format and required fields
- Verify that your task was successfully created
- Learn how to handle common errors

## Before you start

Make sure you've completed the [Before you start a tutorial](../before-you-start-a-tutorial.md)
topic on the development system you'll use for this tutorial.

### Prerequisites

- Local service is accessible at your configured `base_url`
- Postman app installed

### Using Postman

1. Start the local service if it's not already running:

    ```shell
    cd <your-github-workspace>/tune-guide-api/api
    json-server -w tune-guide-db.json
    ```

2. Open the Postman app on your desktop.
3. Create a new request with these values:
    - **METHOD**: `GET`
    - **URL**: `http://localhost:3000/channels
    - **Headers**:
      - `Content-Type: application/json`
4. In the Postman app, choose **Send** to make the request.
5. The API returns a JSON array of user objects. Your response should look like this:

    ```json
    {
        "channel_number": 8,
        "name": "80s on 8",
        "genre": "1980s",
        "description": "Pop hits from the 1980s MTV era",
        "target_audience": "Baby boomers, Gen X, Millennials",
        "id": 1
    },
    {
        "channel_number": 34,
        "name": "Lithium",
        "genre": "Grunge rock, 90s alternative",
        "description": "Grunge and 90s alternative rock",
        "target_audience": "Grunge fans, 90s rock fans, Gen X, Millennials",
        "id": 2
    },
    {
        "channel_number": 26,
        "name": "Classic Vinyl",
        "genre": "1960s, 1970s",
        "description": "60s/70s classic rock",
        "target_audience": "Baby boomers, Gen X, Millennials",
        "id": 3
    },
    {
        "channel_number": 2,
        "name": "Hits 1",
        "genre": "Pop",
        "description": "Pop hits, now to next",
        "target_audience": "Gen X, Millennials, Gen Z, Gen alpha",
        "id": 4
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language.
To do this, adapt the values from the tutorial to the properties
and arguments that the language uses to make REST API calls.

## Completion and validation

If you received a JSON array of users, you have successfully used the
GET /users endpoint in the To-Do Service API.

## Troubleshooting common errors

|Status Code|Error|Solution|
|---------------------------|------------------------|------------------------------|
|`400 Bad Request`|Missing required field|Ensure request includes all required fields|
|`404 Not Found`|Invalid `id`| Verify channel exists, call `GET /channels`|
|`500 Internal Server Error`|Service connection issue|Check json-server is running|
|`Connection refused`|Service not running|Start local service using step 1|

## Next steps

- Review the [channels api reference](../api/channels.md) for more details.

## Related topics

- [Get all channels](../api/channels-get-all-channels.md) in the system.
- [Get a channel by id](../api/channels-get-channel-by-id.md) in the system.
