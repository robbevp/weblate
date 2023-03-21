In the upstream repo:

```
git diff weblate-${old}..weblate-${new} requirements*
```

Transmit all differences to `pyprojects.toml`, as long as they are not optional.

Update `version` in `pyproject.toml`.

Then:

```
poetry update --lock
```

Update weblate version in flake.nix input.

