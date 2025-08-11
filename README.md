# Missing In Project (pinned)

This action wraps the
[`missing-in-project`][upstream-action]
action from [`ni/labview-icon-editor`][repo] and pins it to a
specific commit to ensure stable builds. When the upstream action updates and is
verified, this repository will update the pinned commit and communicate the
change through release notes.

Before invoking the upstream action, this wrapper validates the inputs and
fails early if the specified project file does not exist.

## Outputs

- `passed` – True if the missing-file check reported success.
- `missing-files` – Newline-separated list of files that could not be found.
- `missing-files-count` – Number of entries in `missing-files`.

## Release Notes

- Pinned upstream action to commit [`204c218`][pinned-action] from
  `ni/labview-icon-editor/.github/actions/missing-in-project`.
- `missing-files` output now returns a newline-separated list instead of a
  comma-separated list. Update parsing logic accordingly.
- Added default `arch` input, enforced `.lvproj` project-file extension, and
  switched to CSV-based output parsing to preserve spaces and commas.

[upstream-action]: https://github.com/ni/labview-icon-editor/tree/develop/.github/actions/missing-in-project
[repo]: https://github.com/ni/labview-icon-editor
[pinned-action]: https://github.com/ni/labview-icon-editor/tree/204c21874646c6571fceb3adf69e35cc939d61f7/.github/actions/missing-in-project
