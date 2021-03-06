---
layout: index
title: "NPM Publish Scripts"
navigation_weight: 0
---

# Why

There are a few reasons why this project exists:

1. To give a common way to release versions of projects on NPM.
1. To offer a consistent look and feel for GitHub pages.
1. Encourage a more structured way of documenting projects.

If your project suffers from human errors when releasing, has build files
in the master branch or you simply want reference docs, then this
module may be useful.

# Install

This module contains shell scripts and themes for Jekyll and JSDoc.
Simple install via NPM like so:

    npm install npm-publish-scripts --save-dev

# Usage

There are three pieces to this project:

1. Publishing a Release

    The `publish-release.sh` script will run the following steps
    when releasing a new version of a project to NPM:

      1. Perform any build steps.
      1. Run any tests the project has.
      1. Bundle any assets to include in the final release.
      1. Bump the version number and publish to NPM.
      1. (If supported) Publish docs to Github pages.

    Setting this up means releases are more consistent and anyone
    on the team can perform a release without needing to know
    or perform any manual steps.

    <a href="./publish-release">How to Publish a Release</a>

1. Build a Github Pages Site

    If you want to have stylised docs with versioning for reference
    documentation you can use `publish-docs.sh` to help.

    This script will set up a Jekyll theme and keep it up to date
    and if you have a `reference-docs` directory, it will generate
    a sorted version list for the theme to use.

    <a href="./build-github-pages">Build a Github Pages Site</a>

1. Use the JSDoc Theme

    To match the Jekyll theme, this project has a JSDoc theme. This
    is solely to give the Github Pages a bit more consistency and
    to give control over the look and feel of the reference
    documentation.

    <a href="./use-jsdoc-theme">Use the JSDoc Theme</a>
