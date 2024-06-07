# Reviewing a Pull Request Using CI artefact

Our CI (Continuous Integration) process, which runs automatically for all PRs (Pull Requests), compiles a packaged .zip
file of the mod with the updates associated with the PR.

This means you don't need to manually build the mod .zip file, you can just link to it.

The format of the link is:

```
https://ci.appveyor.com/api/projects/krzychu124/tmpe/artifacts/TMPE.zip?branch=branch_name
```

Where `branch_name` should be replaced by whatever branch is associated with the PR.

For example, if your branch is `some-new-feature`, the URL to the .zip would be:

```
https://ci.appveyor.com/api/projects/krzychu124/tmpe/artifacts/TMPE.zip?branch=some-new-feature
```

When creating your own PRs it's super helpful to beta testers (including those who just want to playtest a new feature)
if you can include the link in the OP of the PR. It allows more people to test the mod in-game without having to set up
a build environment.