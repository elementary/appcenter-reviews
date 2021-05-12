# AppCenter Reviews

This repository is used for deploying applications to the [elementary flatpak
repository][1]. You can view your review status by [looking at the open PRs][2].

To submit an application, please use the [AppCenter dashboard][3], as it will
speed up the review process and ensure all the needed data is entered correctly.
If you want to publish a git repository that is not on GitHub, make sure you
adhere to the [publishing requirements][4], then you can make a PR here.

## Review Process

All applications currently in the review queue can be viewed in the
[pending PRs][2]. Once the PR is approved and merged by one of our reviewers, it
will be published to our [flatpak repository][1]. If any questions or changes
come up during the review process, our reviewer will tag the application author
in the conversation (if possible).

## Repo Structure

All application releases in this repository are found under the `application/`
folder and follow this schema `<rdnn>/<release tag>.json`. The JSON file looks
like this:

```json
{
  "source": "https://github.com/danrabbit/harvey.git",
  "commit": "45dd52660c0069207fa4b0c1fcf7ac6d7157d34b"
}
```

The `source` field needs to be a publicly accessible git repository. The
`commit` field is the full git sha for the release we are building.

[1]: https://flatpak.elementary.io
[2]: https://github.com/elementary/appcenter-reviews/pulls?q=is%3Apr+is%3Aopen+sort%3Acreated-desc
[3]: https://beta.developer.elementary.io
[4]: https://docs.elementary.io/develop/appcenter/publishing-requirements
