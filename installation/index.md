---
title: Installation
layout: default
---

# Installation

To automatically install Cask, run this command:

    curl -fsSkL https://raw.github.com/rejeep/cask.el/master/go | sh

You can also clone the repository.

    $ git clone https://github.com/cask/cask.git

Don't forget to add Cask's bin to your `PATH`.

    $ export PATH="/path/to/code/cask/bin:$PATH"

To upgrade Cask itself and its dependencies, run:

    $ cask upgrade
