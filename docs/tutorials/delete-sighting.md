---
layout: default
title: Delete a sighting
parent: Tutorials
nav_order: 10
---

**On this page:**

- TOC
{:toc}

# Delete a sighting: a tutorial

This tutorial should take you about 10 minutes to complete.

## Before you begin

1. Make sure you've [set up your environment](./set-up-dev-env.md).
2. [Start the Orca Sightings service](./start-service.md) with `json-server`.

## How to delete a sighting

In this section, you'll delete the sighting with an `id` of `4`.

{: .note }
To list all sightings and pick a different sighting to delete, refer to [Get started by listing orca sightings: a tutorial](./quickstart.md)

**To use cURL:**

1. Open a new terminal window.
2. Run the following command:

```shell
curl -X DELETE http://localhost:3000/sightings/4
```

{: .tip }
The `4` at the end of the URL specifies the sighting ID.

**To use Postman:**

1. In Postman's main panel on the right, toward the top, select **DELETE**.
2. Add the following content to the URL text box next to GET: `http://localhost:3000/sightings/4`.
3. Click **Send**.

{: .note }
If you don't specify a sighting ID, the service won't delete all the sightings. Instead, it returns a **404 Not Found** error message.

## View the response

The response body should show an empty record:

```json
{}
```

In Postman, you should also see a green 200 OK message at the top of the pane. Hover over that text to see the full confirmation message.

That's it. Next, view the reference topic [`DELETE /sightings`](../reference/sightings/sightings-delete.md).

Also, you can try other [tutorials](./tutorials.md) or view other topics in the [API reference](../reference/api-reference.md).
