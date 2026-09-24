# Astro + Netlify starter

Static Astro site in plain JavaScript, managed with Yarn 4 (`node_modules` linker), hosted on Netlify.

## Start a new site

```sh
yarn create astro my-site --template benomatis/astro-netlify-starter --no-install --no-git
cd my-site
yarn install
netlify sites:create --name my-site   # or: netlify link
```

Or use GitHub's "Use this template" button.

Then set `name` in `package.json`.

## Commands

| Command | Action |
| --- | --- |
| `yarn dev` | Local dev server at `localhost:4321` |
| `yarn build` | Build to `./dist/` |
| `yarn preview` | Preview the build locally |
| `yarn deploy` | Build and deploy to production on Netlify |
| `yarn deploy:preview` | Build and create a draft deploy (preview URL) |

## Notes

- Yarn skips package versions published less than 24 hours ago. If an install fails with "quarantined", pin the previous version.
- Netlify adds a "Built with Netlify" badge by default. Turn it off per site:
  `netlify api updateSite --data '{"site_id":"<id>","body":{"built_with_badge_enabled":false}}'`
