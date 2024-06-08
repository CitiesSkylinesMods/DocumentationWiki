# Interface Style Guide
> This page is in early stages of development and is likely to change a lot

We want to provide users with a great toolset for managing their traffic. These are some emergent guidelines for achieving that.

## General

The user needs to know:

* that the feature exists
* what it does
* how to enable and/or apply it
* that their change was applied
* how to revert mistakes

### Discoverability

How does the user know the feature exists?

* On-screen UI
* Adviser text, tooltips
* Screenshots/videos on workshop pages

We should always provide change notes, which should mention new features, but most users won't read them.

### Comprehension

How does the user comprehend what the feature does?

?

### Application

How does the user activate and/or apply the feature?

* Do they need to enable it or configure it in mod options?
* Do they need to click a button?
* Do they need to use a modifier key?
* Something else?

For all those things, how do they know what to do?

### Feedback & Awareness

How does the user know their changes have been applied?

* There should be direct visual feedback while using the feature
* Where applicable, provide persistent overlays

If the user action will alter an existing state (whether global default or context specific), how do we make them aware of that?

### Reverting

How does user revert changes, for example to recover from mistakes?

* UI should make it easy to rapidly change a customization and reapply the correct action that will make the user happy
* Undo tool _might_ be useful in some cases
* Bulk delete (eg. delete key can remove lane connections from an entire node)

### Coherence & Consistency

> todo

## Styling

### Colors

> todo

### Selectors

Show what will be selected / changed when editing networks on the map.

> todo: images + more detail

* Node circle
* Segment sausage
* Half-segment sausage
* Lane sausage
* Half-lane sausage (does not exist yet)

> Do we have a centralized class for this stuff?
 