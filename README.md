# VAIT Static Sites monorepo

This repo contains VAIT static sites apart from the [homepage project](https://github.com/viet-aus-it/homepage).
Each folder in the `sites` directory represents a site that links to the same subdomain (e.g., `chat` links to `chat.vait.au`).

## Sites

| Dir      | Site                                                 | Type   |
| -------- | ---------------------------------------------------- | ------ |
| chat     | [https://chat.vait.au](https://chat.vait.au)         | SPA    |
| fb       | [https://fb.vait.au](https://fb.vait.au)             | SPA    |
| linkedin | [https://linkedin.vait.au](https://linkedin.vait.au) | SPA    |
| yt       | [https://yt.vait.au](https://yt.vait.au)             | SPA    |
| cert     | [https://cert.vait.au](https://cert.vait.au)         | Static |
| links    | [https://links.vait.au](https://links.vait.au)       | Static |

## Configuration

All sites are configured separately in CloudFlare and point to their respective worker project.

### SPA Sites

`chat`, `fb`, `linkedin`, and `yt` are configured as single-page applications. Each site only needs an `index.html` at the bucket root.

### Static Sites

`cert` and `links` are purely static sites. Files placed in the bucket are served directly under the corresponding URL. For example, adding a file `dist/2026/certificate.pdf` to the `cert` bucket makes it available at `https://cert.vait.au/2026/certificate.pdf`.
