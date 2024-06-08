# Boost Filesystem Path Error

> Verified: February 2020 - TM:PE 11.1.0

## Symptom

You get an error mentioning `boost::filesystem`, such as:

* `boost::filesystem::path codecvt to wstring: error`

## Cause

[Boost](https://www.boost.org/) is a C++ library, so this error is very deep - probably in Unity game engine, or the
Mono environment in which it runs, and possibly even your operating system or virtual machine.

It can sometimes be caused by strange characters in a file path, but often it will be due to having very old versions of
libraries installed.

## Solution

Completely uninstall and then reinstall the game, and Steam, and then reinstall from scratch.

## Was it Fixed?

If not, you'll have to hunt the internet for answers. One extreme option would be a complete re-installation of your
operating system.

Other issues? See: [](Troubleshooting.md)