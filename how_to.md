# How to edit and deploy

## Editing content

Authoring content: https://getdoks.org/docs/basics/authoring-content/

- Home Page: Edit `content/_index.md` to see this page change. See `layouts/index.html` for its design.
- Top menus: Edit `config/_default/menus/menus.en.toml`
- Add Markdown files to `content` folder to create new pages. Doks will automatically generate a sidebar based on the filesystem structure of your documentation, using each file’s title property as the sidebar entry. For details see [Navigation documentation](https://getdoks.org/docs/basics/navigation/)
- Site config: Edit your config in `config/_default/params.toml`

## Deploy

1- Edit and commit your changes
2- Open GitHub actions tab: https://github.com/Cellular-Semantics/Cellular-Semantics.github.io/actions
3- Select `Deploy Thulite site to Pages` action from the left pane
4-On the `Run workflow` dropdown, select `main` branch and click `Run workflow`
5- Refresh the page and select the top item (with yellow spinner) to view its progress.
6- After successful completion of the action, site should be updated


## Source

This repo is sourced from https://github.com/thuliteio/doks-gh-pages

For details see https://getdoks.org
