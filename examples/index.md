---
title: Examples
layout: default
---

# Examples

Here are a few examples of how a `Cask`-file might look like.

## Emacs configuration

```
(source melpa)

(depends-on "auto-complete")
(depends-on "dash")
(depends-on "f")
(depends-on "flycheck")
(depends-on "helm")
(depends-on "magit")
(depends-on "popup")
(depends-on "projectile")
(depends-on "s")
(depends-on "smartparens")
(depends-on "yasnippet")
```

## Package development

```
(source melpa)

(package "super" "0.7.6" "Super project.")

(depends-on "commander")
(depends-on "f")
(depends-on "s")
(depends-on "dash")

(development
 (depends-on "el-mock")
 (depends-on "ecukes")
 (depends-on "ert-runner"))
```

## I still don't get it, give me some real examples

These are some projects and configurations using Cask:

* [rejeep/emacs](https://github.com/rejeep/emacs)
* [drag-stuff](https://github.com/rejeep/drag-stuff)
* [emacs-jedi](https://github.com/tkf/emacs-jedi)
* [flycheck](https://github.com/lunaryorn/flycheck)
* [projectile](https://github.com/bbatsov/projectile)
* [smartparens](https://github.com/Fuco1/smartparens)
* [ecukes](https://github.com/ecukes/ecukes)
* [expand-region](https://github.com/magnars/expand-region.el)
* [and more...](https://github.com/search?l=Emacs+Lisp&q=cask&ref=opensearch&type=Code)
