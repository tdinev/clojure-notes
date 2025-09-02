# Installation and setup

## Clojure CLI & Emacs

Add the following packages to your NixOS configuration file (residing usually in `/etc/nixos/configuration.nix`):

```nix
clojure
emacs
git
```

## Prelude

Check if you have an Emacs configuration file or directory and, if so, rename it (as we will use the Prelude configuration):

```bash
mv ~/.emacs ~/.emacs-backup
mv ~/.emacs.d ~/.emacs.d-backup
```

Clone the Prelude configuration as your Emacs configuration directory (this is why we installed `git` in the previous section):

```bash
git clone https://github.com/bbatsov/prelude.git ~/.emacs.d
```

Copy the modules sample:

```bash
cp ~/.emacs.d/sample/prelude-modules ~/.emacs.d/
```

Activate the Clojure module by removing the `;;` from the line containing `(require 'prelude-clojure)`:

```elisp

```

Open Emacs to 