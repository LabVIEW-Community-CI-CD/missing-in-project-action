# Missing In Project (pinned)

This action wraps [LabVIEW-Community-CI-CD/missing-in-project](https://github.com/LabVIEW-Community-CI-CD/missing-in-project)
and pins it to a specific commit to ensure stable builds. When the upstream action updates and is verified, this repository will
update the pinned commit and communicate the change through release notes.

Before invoking the upstream action, this wrapper validates the inputs and
fails early if the specified project file does not exist.

## Release Notes

- `missing-files` output now returns a newline-separated list instead of a comma-separated list. Update parsing logic accordingly.
