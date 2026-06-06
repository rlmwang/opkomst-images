# opkomst-images

Hosted hero images for [opkomst.nu](https://opkomst.nu) events.

The app PUTs uploads here via the GitHub Contents API; files land at `events/{event_id}/{timestamp}.jpg` and are served from `raw.githubusercontent.com`. Old files are not pruned by design — replacing an event image overwrites the URL stored in the database; the prior commit is the audit log.

This repo is **public** because `raw.githubusercontent.com` 404s on private repos for anonymous fetches. The PAT the app uses is fine-grained, scoped to this repo, and only carries `contents: write`.
