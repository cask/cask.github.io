---
title: Development
layout: default
---

# Development

The development of Cask is at Github
<https://github.com/cask/cask>. Development related discussion is done
in a Google group <https://groups.google.com/forum/#!forum/cask-dev>.

## Contribution

Be sure to!

Implement the features and don't forget to test it. To run the tests,
first start the fake ELPA server:

    $ make server

Then to run the tests:

    $ make

If all passes, send us a
[pull request](https://github.com/cask/cask/pulls) with the
changes. Note that we usually work on a WIP-branch, which is the
branch the pull request should target. They are named
`v{MAJOR}.{MINOR}-wip`.
