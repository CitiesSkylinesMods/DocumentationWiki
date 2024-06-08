# Code Style and Naming Guide

We are using spaces, not tabs. Tab width is 8. Indent is 4.

If an inconsistent naming is found, prefer project style, not file style.

## Type and Namespace Naming

* Use `CamelCase` for enums, classes and structs.
* Use `CamelCase` namespaces.
    * Prefer full namespace paths where you refer to a type. It helps to read the code. For example `UI.Button` is
      better than just `Button` because a similarly named type might exist elsewhere.

## Class Fields and Functions

* Private fields `camelCase_` (lowercase camel with underscore)
* All other fields `CamelCase`
* Const values `UPPER_CASE`
* Functions and get properties to start with `Get`, `Is`, or another verb.
* Other functions to start with a verb, indicating the action they do.

## Function Args and Variables

* Prefer explicit types over `var`, unless its obvious `LongClassName c = new LongClassName()` is silly, in such case
  just use var.
* Arguments and local variables are `camelCase`