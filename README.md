# AppCenter Reviews

This repository is used for deploying apps to the [elementary AppCenter Flatpak
repository][1]. You can view your or any other app's review status by checking
[open pull requests][2].

>⚠️ **Note:** The new AppCenter Dashboard is unfinished and under rapid
development. If you have issues using it, please [report them][3].

To submit an app, please use [AppCenter Dashboard][4], as it will speed up the
review process and ensure all the needed data is entered correctly. If you want
to publish an app that is not hosted on GitHub, your app has an RDNN that does
not match where the code is hosted, or are having an issue submitting with
AppCenter Dashboard: first make sure your app adheres to the [publishing
requirements][5], then submit a pull request against this repository following
the structure below.

## Review Process

All apps and updates in the review queue are listed as [open pull requests][2].
Once a pull request is approved and merged by a reviewer, that app will be
published to the [AppCenter Flatpak repository][1]. If any questions or
requested changes come up during the review process, the reviewer will tag the
app developer in the conversation on the pull request if possible.

Once your app is approved and merged into this repository, future releases and
tagged commits will be automatically submitted for review and approval.

## Repository Structure

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

[1]: https://flatpak.elementary.io
[2]: https://github.com/elementary/appcenter-reviews/pulls?q=is%3Apr+is%3Aopen+sort%3Acreated-desc
[3]: https://github.com/elementary/appcenter-dashboard/issues
[4]: https://beta.developer.elementary.io
[5]: https://docs.elementary.io/develop/appcenter/publishing-requirements
