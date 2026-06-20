# Bootstreep Profile — Architecture

## Overview

This repository is **Samuel's GitHub profile README source**. It is the
landing page shown at https://github.com/braeuningsamuel-cmyk and exists to
introduce the person behind the Bootstreep homelab projects.

Unlike the other Bootstreep repos, this one has **no application code** —
it's pure markdown describing who Samuel is, what he builds, and where to
find the projects.

## Contents

```
braeuningsamuel-cmyk/
|-- README.md          Profile README (rendered on the GitHub profile page)
|-- ARCHITECTURE.md    This file — explains the repo's purpose
|-- Makefile           Standard Bootstreep Quality Bar targets
|-- .env.example       Empty by design — profile has no env vars
`-- .gitignore         Standard ignores for OS / IDE / editor cruft
```

## Components

There are no runtime components. The only artefact is `README.md`, which
GitHub renders at the profile URL.

## Data Flow

```
edit README.md
      |
      v
git commit -m "..."
      |
      v
git push origin main
      |
      v
GitHub renders README.md at:
https://github.com/braeuningsamuel-cmyk
```

## Deployment

There is no deployment step — GitHub serves the README directly from the
`main` branch. Push to `main` and the profile updates within ~1 minute.

## How this fits into Bootstreep

This profile README is also mirrored in the `Homelab-Base` monorepo under
`profile/`, so the same content stays in sync across both views.

See:

- https://github.com/braeuningsamuel-cmyk/Homelab-Base/tree/main/profile
- https://github.com/braeuningsamuel-cmyk

## Maintenance

- **Edit the README**: make changes, commit, push.
- **Sync to monorepo**: copy `README.md` to `Homelab-Base/profile/README.md`
  and push there too.
- **Verify links**: every link in the README should point to a live repo or
  gist. Run `make secrets` to confirm no credentials leaked into the file.