# Information architecture for orca-sightings-api docs

*Draft 3*

## `/docs`

Root of doc set deliverable. Docs appear at https://juliebro.github.io/orca-sightings-api/.

### `index.md`

Overview topic.

### `/tutorials`

Contains "index" file  `tutorials.md`.  Also includes:

- `quickstart.md` → a tutorial abut how to list all orca sightings (GET sightings)
- `add-user.md` → how to add a new user using the POST method
- `update-user.md` → how to update all or part of a user (PUT/PATCH)
- `delete-user.md` → how to delete a user
- `add-sighting.md` → how to add a new sighting using the POST method
- `update-sighting` → how to update all or part of a sighting (PUT/PATCH)
- `delete-sighting` → how to delete a sighting

Supporting topics that are reused across other topics:

- `set-up-dev-env.md` → how to set up the environment for using tutorials
- `start-service.md` → how to start the Orca Sightings service

### `/reference`

Contains reference topics and related information.

- `api-reference.md` → "index" file for API reference
- `/users` → directory for topics about the `/users` resource
  - `users-resource.md` → "index" file for topics about the `/users` resource
  - `users-*.md` → reference topics; one each for get, post, put, patch, and delete
  
- `/sightings` → directory for topics about the `/sightings` resource
  - `sightings-resource.md` → contains information about the `/sightings` resource
  - `sightings-*.md` → reference topics; one each for get, post, put, patch, and delete

Supporting topics:

- `base-url.md` → topic describing what `{base_url}` in an endpoint URL means
- `iso-8601-format.md` → topic describing what ISO 8601 format is; linked from `sightings-resource.md`
