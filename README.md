# LEVIKOUABLAN.NET

[![Netlify Status](https://api.netlify.com/api/v1/badges/4ed8d336-d020-48e7-ac32-5dfb438c94da/deploy-status)](https://app.netlify.com/sites/levikouablan/deploys)

Personal website, built with [Hugo](https://gohugo.io/) and the [hugo-coder](https://github.com/luizdepra/hugo-coder) theme, deployed on Netlify.

## Requirements

- Hugo **extended 0.167.0**, the version pinned in `netlify.toml` (`HUGO_VERSION`) and in `.devcontainer/Dockerfile`. Bump both together.
- The theme is a git submodule. After cloning, run:

  ```sh
  git submodule update --init
  ```

## Usage

```sh
hugo server -D                          # local preview, drafts included
hugo new content projects/<slug>        # new case study from archetypes/projects/
hugo --gc --minify                      # production build into public/
```

Netlify deploy previews build with drafts included, so draft pages can be reviewed on a pull request before merging.
