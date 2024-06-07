# Milestone

## Overview

Each release should have a
related [Milestone](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/milestones) that
tracks _all_ changes associated with the release.

## Creating a Milestone

If it doesn't already
exist, [Create New Milestone](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/milestones/new)
for the release:

* **Title** = version number, eg. `10.21`
* **Due Date** = when a release is being published, set the date to when the files were uploaded to workshop
* **Description** = changelog for the release, covering all notable changes
    * This is usually updated multiple times during the development/test/release cycle.

## Milestone descriptions

Keep on top of the description text, because during release it gets copied to lots of other places:

* [](Readme-and-Changelog.md)
* [](Release-Binaries.md) (description field)
* [](Steam-Workshop.md) (mod Description page, and also the Change Notes tab)

You can look at [Closed Milestones] to see examples of formatting of the **Description** field (note: you have to edit
the milestone to see the markdown). In general, each entry should stat with a word that indicates the nature of the
change, as applicable:

```
* Added: _summarise new feature_ (_refs_)
* Improved: _summarise improvement (a partial fix or enhancement)_ (_refs_)
* Fixed: _summarise a bug fix_ (_refs_)
* Updated: _summarise update to existing feature_ (_refs_)
* Removed: _summarise what was removed_ (_refs_)
* Meta: _summarise some other change, eg. build process or GitHub stuff_ (_refs_)
```

If any change was contributed by someone not on the core TM:PE team, thank them in the release notes, for example:

> * Updated: Whatever translation (thanks whoever) (#whatever)

## Tracking changes

Every change should have an
associated [Issue](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/issues)
and/or [Pull Request](https://github.com/krzychu124/Cities-Skylines-Traffic-Manager-President-Edition/pulls), and those
should be assigned to the relevant Milestone (via link in sidebar of the issue or PR).

## Closing a Milestone

When a release has been published, the Milestone should be closed, but make sure the **Due Date** has been set to the
release date first.