# Information architecture for orca-sightings-api docs

*Draft 1*

## `/docs`

Root of doc set deliverable. Docs are published to https://juliebro.github.io/orca-sightings-api/ 

### `index.md`

Overview topic.

### `/how-tos`

Contains how-to topics (procedures) and related information.

### `/reference`

Contains reference topics and related information.

* `index.md` --> lists all reference files; currently populated with a placeholder file
* `users-resource.md` --> contains information about the `/users` resource. Iincludes a list of links to all related reference topics.
* `sightings-resource.md` --> contains information about the `/sightings` resource. Links to a topic about ISO 8601format and includes a list of links to all related sightings topics.

### `/templates` 

Contains templates for writing docs. Not part of the deliverable doc set.

### `/tutorials`

Contains `quickstart.md` and `tutorial.md` Could include an `index.md` file if there were more tutorials. Quickstart is linked from `/docs/index.md`.

