A simple major mode to edit YAML file for emacs

This is a fork [of the original Yaml Mode](https://github.com/yoshiki/yaml-mode/pull/114). The reason it was forked are various disagreements with maintainers of the original mode, and my interest in contributing there is not enough to put any more resources into that.

# REQUIREMENTS

Emacs 24.1

# SYNOPSIS

To install, just drop this file into a directory in your
`load-path' and (optionally) byte-compile it.  To automatically
handle files ending in '.yml', add something like:

```lisp
(require 'yaml-mode)
(add-to-list 'auto-mode-alist '("\\.yml\\'" . yaml-mode))
```

to your `.emacs` file.

Unlike python-mode, this mode follows the Emacs convention of not
binding the ENTER key to `newline-and-indent`.  To get this
behavior, add the key definition to `yaml-mode-hook`:

```lisp
(add-hook 'yaml-mode-hook
  '(lambda ()
    (define-key yaml-mode-map "\C-m" 'newline-and-indent)))
```

# DESCRIPTION

yaml-mode is major mode for emacs.

# INSTALL

You can install yaml-mode typing below.

    $ make
    $ make install

or

    $ make PREFIX=/your/home/dir
    $ make install PREFIX=/your/home/dir

# AUTHOR

Yoshiki Kurihara <kurihara@cpan.org> Copyright (C) 2010 by Free Software
Foundation, Inc.

This file is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This file is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with GNU Emacs.  If not, see <https://www.gnu.org/licenses/>.
