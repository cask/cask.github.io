---
title: DSL
layout: default
---

# DSL

* [source](#source)
* [package](#package)
* [package-file](#package-file)
* [depends-on](#depends-on)
* [development](#development)

---

## <a id="source"></a>source

Add a package mirror.

```
(source ALIAS)
(source NAME URL)
```

Example:

```
(source melpa)
(source "melpa" "http://melpa.milkbox.net/packages/")
```

Available aliases:

 * `gnu` (<http://elpa.gnu.org/packages/>)
 * `melpa` (<http://melpa.milkbox.net/packages/>)
 * `marmalade` (<http://marmalade-repo.org/packages/>)
 * `SC` (<http://joseito.republika.pl/sunrise-commander/>)
 * `org` (<http://orgmode.org/elpa/>)

## <a id="package"></a>package

Define this package (used only for package development).

    (package NAME VERSION DESCRIPTION)

Example:

    (package "ecukes" "0.2.1" "Cucumber for Emacs.")

## <a id="package-file"></a>package-file

Define this package and its runtime dependencies from the package
headers of a file (used only for package development). The name of the
file is relative to the directory containing the `Cask` file.

    (package-file FILENAME)

Example:

    (package-file "foo.el")

## <a id="depends-on"></a>depends-on

Add a dependency.

    (depends-on NAME [VERSION])

Example:

    (depends-on "ecukes")
    (depends-on "magit" "0.8.1")

## <a id="development"></a>development

Set scope to development.

    (development [DEPENDENCIES])

Example:

    (development
     (depends-on "ecukes")
     (depends-on "ert-runner"))
