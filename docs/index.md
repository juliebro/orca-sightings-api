---
layout: default
title: Overview
nav_order: 1
has_toc: false
---

# San Juan Islands Orca Sightings service

This cloud-based service tracks the movements of orca pods around the San Juan Islands in the Salish Sea. Orcas are also known as killer whales.

Using this service, orca enthusiasts can report the location and time of their sightings off the coast of any of the San Juan Islands, making it easy for others to sight these whales from land so they don't have to charter a boat. As a developer, you can include this service in your app.

To get started, learn how to [set up your environment](./tutorials/set-up-dev-env.md) and [list all sightings](./tutorials/quickstart.md) in the service, or jump down to learn more about the [user community](#user-community) and [features](#features).

![ Photo of orca whales](./images/orca-photo.png)

## User community

The orca whale watching community is niche but active. It includes a variety of enthusiasts from around the world, and many seek the orcas that frequent the San Juan Islands. Whale watchers can see orca pods swim near the land there year-round. The orca whale's distinctive, large dorsal fin makes it easier to spot from far away than other whales or dolphins.

## Features

{: .comment }
I need to make sure the following links work after I've created the files.

The Orca Sightings service is a RESTful API designed to support this community. It offers two main resources: `/users` and `/sightings`. Each resource supports standard HTTP methods, including GET, POST, PUT, PATCH, and DELETE, so your app can perform the following actions:

- [Create new user profiles](./tutorials/add-user.md) and [log new orca sightings](./tutorials/add-sighting.md).
- [Retrieve all or specific user](./tutorials/list-users.md) and [sighting records](./tutorials/list-sightings.md).
- [Update existing user information](./tutorials/update-user.md) and [sighting details](./tutorials/update-sighting.md).
- [Delete user accounts](./tutorials/delete-user.md) and [sighting entries](./tutorials/delete-sighting.md).

{: .warning }
This is a simulated REST interface only for the demonstration of API documentation.
