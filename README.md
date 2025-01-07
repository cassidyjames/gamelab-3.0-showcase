# gamelab-3.0-showcase

A little proof-of-concept showcase of some games. It works by:
- submoduling the public games' repos
- assuming each Godot project is at the root of its repo (some are not, and so fail)
- using a GitHub Actions workflow to
  - download and cache Godot Engine
  - copy the export preset into the project
  - export the game for web
  - upload to GitHub Pages

Ideally we could still file some PRs against the actual games to get that upstreamed, but this was a quick proof of concept to throw together.

## Adding a game

To add a game, use `git submodule` from the root of ths repo, e.g.:

```sh
git submodule add https://github.com/USER/REPO.git
```

This will create a submodule folder for the given repo in this project's root, which will then be picked up automatically by the GitHub Action workflow when pushed.
