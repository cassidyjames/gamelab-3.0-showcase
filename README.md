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
