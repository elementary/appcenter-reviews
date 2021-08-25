# AppCenter Reviews

This repository is used for reviewing apps and deploying them to the [elementary
AppCenter Flatpak repository][1]. You can view your or any other app's review
status by checking the [open pull requests].

>⚠️ **Note:** The new [AppCenter Dashboard] is unfinished and under development.
>For now, apps can be submitted as pull requests against this repository.

## Submitting an app

First, **make sure your app adheres to the [publishing requirements][2]**, then
submit a pull request against this repository following the structure below.

## Review process

All apps and updates in the review queue are listed as [open pull requests].
Once a pull request is approved and merged by a reviewer, that app will be
published to the [AppCenter Flatpak repository][1]. If any questions or
requested changes come up during the review process, the reviewer will tag the
app developer in the conversation on the pull request if possible.

## Repository structure

All app releases in this repository are found under the `applications/` folder
and follow this schema `<rdnn>.json`. The JSON file looks like
this:

```json
{
  "source": "https://github.com/danrabbit/harvey.git",
  "commit": "45dd52660c0069207fa4b0c1fcf7ac6d7157d34b",
  "version": "1.0.1"
}
```

The `source` field needs to be a publicly accessible Git repository. The
`commit` field is the full Git sha for the release we are building. And the
`version` needs to be a SemVer tag.

>⚠️ **Note:** Until the new [AppCenter Dashboard] is finished, updates must also
>be submitted for review and approval; submit a pull request modifying your
>app's existing JSON file with the new commit and version tag.

[AppCenter Dashboard]: https://beta.developer.elementary.io
[open pull requests]: https://github.com/elementary/appcenter-reviews/pulls?q=is%3Apr+is%3Aopen+sort%3Acreated-desc
[1]: https://flatpak.elementary.io
[2]: https://docs.elementary.io/develop/appcenter/publishing-requirements
