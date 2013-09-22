---
title: Usage
layout: default
---

# Usage

Create a file called `Cask` in your project root and specify
dependencies:

```
$ cask init [--dev]
```

_(Use `--dev` if the project is for package development)_

If you are using Cask for your Emacs configuration, add this to your
`.emacs` file:

```
(require 'cask "~/.cask/cask.el")
(cask-initialize)
```

To install all dependencies, run:

```
$ cask [install]
```

This will create a directory called `.cask`, containing all dependencies.

## Commands

Below all Cask commands are described.

### <a id="exec"></a>exec

Execute command with correct `PATH` (see [path](#path)) and
`EMACSLOADPATH` (see [load-path](#load-path)) set up.

```
$ cask exec echo foo
$ cask exec ecukes --script --reporter gangsta
$ cask exec ert-runner --pattern performance
```

### <a id="help"></a>help

Show Cask usage information.

```
$ cask help
$ cask -h
$ cask --help
```

### <a id="info"></a>info

Show info about this project, such as name, description and version.

```
$ cask info
```

### <a id="init"></a>init

Create new `Cask`-file. If the project is for package development, use
the `--dev` option.

```
$ cask init       # For Emacs configuration
$ cask init --dev # For package development
```

### <a id="install"></a>install *(default)*

Install all runtime and development dependencies specified in the
`Cask`-file.

```
$ cask
$ cask install
```

### <a id="list"></a>list

List all runtime and development dependencies.

```
$ cask list
```

### <a id="load-path"></a>load-path

Print `EMACSLOADPATH`-friendly string with path to all dependencies to
this project.

The [exec](#exec) command includes the output of this command
automatically. This means that if the command executed is an Emacs
process, there's no hassle with the `load-path`, just require the
dependencies.

```
$ cask load-path
```

### <a id="outdated"></a>outdated

Show list of all outdated dependencies. That is dependencies that have
a more recent version available.

```
$ cask outdated
```

### <a id="package"></a>package

Create a `-pkg.el` file (see
<http://www.gnu.org/software/emacs/manual/html_node/elisp/Multi_002dfile-Packages.html#Multi_002dfile-Packages>).

```
$ cask package
```

### <a id="package-directory"></a>package-directory

Print path to package directory, that is the path to the directory
where all dependencies are installed (`.cask/EMACS-VERSION/elpa`).

```
$ cask package-directory
```

### <a id="path"></a>path

Print `PATH` and prepend path to all directories called `bin` in this
projects dependencies.

For example if this project depends on `ecukes`, this command will
include `.cask/EMACS-VERSION/elpa/ecukes-VERSION/bin`.

```
$ cask path
```

### <a id="update"></a>update

Update all project dependencies.

```
$ cask update
```

### <a id="upgrade"></a>upgrade

Upgrade Cask and all its dependencies.

```
$ cask upgrade
```

### <a id="version"></a>version

Print version of this package.

```
$ cask version
```
